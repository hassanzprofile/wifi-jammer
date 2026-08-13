<p align="center">
  <img src="assets/banner.jpeg" alt="WiFi-Jammer-Automation Banner" width="100%"/>
</p>

<h1 align="center">WiFi-Jammer-Automation</h1>
<p align="center">
  <b>Automate Monitor Mode & 802.11 Deauthentication Testing</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Language-Bash-blue" alt="Bash">
  <img src="https://img.shields.io/badge/Tool-aircrack--ng-red" alt="aircrack-ng">
  <img src="https://img.shields.io/badge/License-MIT-green" alt="MIT">
</p>

A lightweight Bash utility to automate wireless interface management and 802.11 deauthentication testing using the aircrack-ng suite.

Built for security researchers and pentesters who need a fast, repeatable workflow without manual steps.

## Overview

Manually putting a wireless card into monitor mode, killing conflicting services, and handling channel hopping is repetitive and breaks easily. 
This script handles the entire lifecycle for you:

1.  **Auto Interface Detection** Detects your active wireless interface automatically
2.  **Daemon Management** Stops conflicting services like iwd, NetworkManager, wpa_supplicant
3.  **Monitor Mode** Safely switches your NIC to monitor mode
4.  **Attack Workflow** Streamlines the jump from scanning to targeted deauth
5.  **Graceful Cleanup** On exit or Ctrl+C, it restores managed mode and restarts network services

## Features
- Auto detects the primary wireless interface
- Handles errors and hardware race conditions
- Restores system network state on exit using trap
- Works with any NIC that supports Monitor Mode and Packet Injection

## Prerequisites

**Software**
- Linux OS with root access
- `aircrack-ng` suite installed

Install on Debian/Ubuntu:
``bash
sudo apt update && sudo apt install aircrack-ng

Installation
git clone https://github.com/hassanzprofile/wifi-jammer
cd wifi-jammer

Give execution permission:
chmod +x jamm.sh

Usage
Run with root privileges:
sudo ./jamm.sh

The script will:
Detect your wireless interfaceKill interfering processesEnable monitor modeLaunch aircrack-ng tools for you to continue testingTo stop: Press Ctrl+C. The script will automatically restore your interface to managed mode.

To stop: Press Ctrl+C. The script will automatically restore your interface to managed mode. 

# Disclaimer:
This tool is for educational purposes and authorized security testing only. 
Do not use it on networks you do not own or do not have explicit permission to test. 
The author is not responsible for any misuse.

LICENCE:
MIT License

Author:
Hassan
Security Researcher and Automation Specialist
