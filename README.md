# NETWORKWALKS-B082-WK1-PM1-CYBERSECURITY-LAB-SETUP
Isolated virtual lab built with VirtualBox and Kali Linux for cybersecurity testing and penetration testing practice.
# 🔐 Cybersecurity Lab Environment Setup

Building an isolated virtual lab for penetration testing and ethical hacking practice.

## 📌 Project Overview

This project focuses on setting up a virtual cybersecurity and penetration-testing laboratory using VirtualBox and Kali Linux.

The purpose of the lab is to create a controlled environment where cybersecurity tools, network scanning, reconnaissance, vulnerability assessment, and other security-testing activities can be performed safely and repeatedly.

The lab is configured on a private virtual network so that additional machines can be added later and used as targets for authorized security testing.

---

## 🎯 Objectives

The main objectives of this project are to:

* Install and configure VirtualBox.
* Install/import Kali Linux as a virtual machine.
* Create a private NAT Network for the cybersecurity lab.
* Configure network connectivity for Kali Linux.
* Assign a consistent IP address to the Kali VM.
* Verify network connectivity and DNS resolution.
* Take a clean VM snapshot for recovery.
* Document the complete setup process.
* Prepare the environment for future cybersecurity projects.

---

## 🛡️ Purpose of the Lab

The lab provides an isolated and controlled environment for cybersecurity learning and authorized security testing.

It can be used for activities such as:
* Network reconnaissance
* Port scanning
* Vulnerability assessment
* Packet analysis
* Web security testing
* Exploitation practice
* Security-tool experimentation

---

## ⚙️ Lab Configuration

| 🧩 Component | ⚙️ Configuration |
| :--- | :--- |
| 🖥️ Hypervisor | VirtualBox |
| 🐉 Security OS | Kali Linux |
| 🧠 Kali RAM | 3072 MB |
| 🌐 Virtual Network | NAT Network |
| 📡 Network Address | 10.0.0.0/24 |
| 🚪 Default Gateway | 10.0.0.1 |
| 🌍 DNS Server | 8.8.8.8 |

---

## 🪜 Lab Setup Procedure

### Step 1. Install VirtualBox
VirtualBox was installed as the hypervisor.

### Step 2. Create the NAT Network
A dedicated NAT Network was created in VirtualBox.
* **Network Name:** NatNetwork
* **IPv4 Prefix:** 10.0.0.0/24
* **DHCP:** Enabled
* **IPv6:** Disabled

A NAT Network allows multiple virtual machines connected to the same NAT Network to communicate with one another while maintaining outbound internet access.

### Step 3. Import & Configure Kali Linux
The Kali Linux virtual machine was imported into VirtualBox.
* **Adapter 1:** Attached to NAT Network (`NatNetwork`)
* **RAM Allocated:** 3072 MB

### Step 4. Create a Clean VM Snapshot
A VirtualBox snapshot was created immediately after baseline configuration to preserve a clean recovery point.

---

## 🔎 Lab Verification

| test | 🧾 Command | 🎯 Expected Result |
| :--- | :--- | :--- |
| 🌐 Check IP address | `ip a` | Correct Kali IP displayed |
| 📡 Test gateway | `ping 10.0.0.1` | Successful replies |
| 🌍 Test Internet connectivity | `ping 8.8.8.8` | Successful replies |
| 🔎 Test DNS resolution | `nslookup networkwalks.com` | Domain resolves |
| 🔄 Verify snapshot | Restore snapshot and run `ip a` | Baseline configuration restored |

---

## 💡 What I Learned

1. **NAT vs. NAT Network:** Understanding how isolated subnets operate vs standard NAT.
2. **Virtual Machine Networking:** Managing hypervisor network interfaces.
3. **VM Snapshots:** Preserving baseline environments for efficient recovery.
4. **Documentation:** Properly recording step-by-step configurations.

---

## 🔐 Security & Ethical Use
This laboratory is intended strictly for educational purposes only.

---

## 👤 Author

Asanda  
Cybersecurity Student | Networkwalks B084  
🔗 

---

## 📌 Project Information
**Program Name:** Cybersecurity at Networkwalks | **Week:** 01 | **Project:** Cybersecurity & Pentesting Lab Setup
