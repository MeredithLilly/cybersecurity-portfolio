# Lab 01: Kali Linux Home Lab Setup

> **Security Notice:**  
> This lab is performed in a controlled, isolated environment that I own.  
> No real-world systems, sensitive data, or unauthorized targets are used.  
> All examples, tools, and configurations are for educational purposes only.

---

## Objective
Set up a personal cybersecurity home lab using **Kali Linux** in a virtual environment.  
This lab demonstrates installing and configuring Kali Linux safely, preparing for hands-on security exercises, and creating a snapshot for rollback and safe experimentation.

---

## Tools Required
- Virtualization software: **VirtualBox** or **VMware**  
- Kali Linux ISO or VM image (latest version)  
- Host OS: Windows, macOS, or Linux  
- Optional tools for later labs: Wireshark, Metasploit, Nmap  

---

## Steps

### 1. Download Kali Linux
- Official website: [https://www.kali.org/get-kali/](https://www.kali.org/get-kali/)  
- Download either the **VM image** or **ISO installer** depending on your preference.

---

### 2. Create a Virtual Machine
- Open VirtualBox or VMware  
- Create a new VM with:
  - OS type: Linux → Debian (64-bit)  
  - RAM: 2–4 GB (or more if available)  
  - Disk: 20 GB dynamically allocated  

*Figure 1: Creating a Kali Linux virtual machine in VirtualBox.* (see cybersecurity-portfolio/labs/Screenshots/Lab-01 for screenshots)

---

### 3. Install Kali Linux
- If using ISO, attach it to the VM and start the installer  
- Follow the guided installation steps  
- Create a user account and password  
- Use default partitioning unless customization is required  


*Figure 2: Completing the Kali Linux installation.* (see cybersecurity-portfolio/labs/Screenshots/Lab-01 for screenshots)

---

### 4. Configure Networking
- Configure the VM network adapter using **NAT** or **Host-Only Adapter**  
- Verify network connectivity:

```bash
ping 192.168.56.1
```

Note: This address is a private IP used by a host-only virtual network.

### 5. Take a Snapshot
- Before making major changes, create a **VM snapshot**:  
  - VirtualBox: Machine → Take Snapshot  
  - Name: `Kali_Base_Install`  
  - Description: Fresh install of Kali Linux with networking configured and essential tools installed

### 6. Update and Install Basic Tools
bash sudo apt update && sudo apt upgrade -y sudo apt install nmap net-tools wireshark -y
