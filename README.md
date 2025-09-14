# UFW Firewall Configuration — README

## Overview
This repository contains the results and documentation for **Task 2: Basic Firewall Configuration with UFW**.  
The objective was to configure a basic firewall on a Linux VM using UFW (Uncomplicated Firewall).  

---

## Contents
- `ufw_config_results.txt` — Raw UFW status output (if saved).  
- `ufw_task_report.pdf` — Generated PDF report with details and screenshot.  
- `screenshots/` — Directory containing screenshots of the UFW output.  
- `README.md` — This file.  

---

## Environment
- Host OS: Kali Linux (VirtualBox VM)  
- Firewall tool: **UFW (Uncomplicated Firewall)**  

---

## Steps Performed
1. Install UFW (if not installed):  
   ```bash
   sudo apt install ufw -y
   ```

2. Allow SSH traffic (22/tcp):  
   ```bash
   sudo ufw allow ssh
   sudo ufw allow 22/tcp
   ```

3. Deny HTTP traffic (80/tcp):  
   ```bash
   sudo ufw deny http
   sudo ufw deny 80/tcp
   ```

4. Enable UFW:  
   ```bash
   sudo ufw enable
   ```

5. Check UFW status with verbose details:  
   ```bash
   sudo ufw status verbose
   ```

---

## Findings
- **Allow Rule:** SSH (22/tcp) is allowed to ensure remote access.  
- **Deny Rule:** HTTP (80/tcp) is denied to block unwanted web traffic.  
- **Status:** Firewall is active and enabled at system startup.  
- **IPv4 & IPv6:** Rules apply to both address families.  

### Significance
- Allowing SSH ensures administrators can log in remotely.  
- Denying HTTP demonstrates how to block unnecessary services.  
- UFW simplifies firewall management with easy commands.  

---

## Deliverables for GitHub
1. `ufw_config_results.txt` — Output of firewall status (optional).  
2. `README.md` — This documentation file.  
3. `screenshots/` — Screenshot folder with UFW status evidence.  
4. `ufw_task_report.pdf` — Formal PDF report with details.  
5. Optionally: `demo_video.mp4` — Screencast demonstrating the configuration.  

---

## Reproducing the Setup (Quick Guide)
1. Boot Kali Linux VM and open a terminal.  
2. Run `sudo apt install ufw -y` (if needed).  
3. Allow SSH: `sudo ufw allow 22/tcp`  
4. Deny HTTP: `sudo ufw deny 80/tcp`  
5. Enable firewall: `sudo ufw enable`  
6. Verify: `sudo ufw status verbose`  

---

## Notes & Recommendations
- Always double-check firewall rules to avoid locking yourself out (especially SSH).  
- Use UFW profiles for specific applications (`sudo ufw app list`).  
- Regularly review and update firewall policies as per security requirements.  




