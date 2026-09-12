
# Cybersecurity Lab Environment

### WEEK 01 | LAB BUILD & NETWORK VALIDATION

**Kali Linux · Oracle VirtualBox · Virtual Networking · Linux Networking**

## Lab Purpose

This lab establishes a **controlled, isolated, and reproducible cybersecurity environment** using Oracle VirtualBox and Kali Linux.

The environment is designed to provide a safe foundation for hands-on experimentation, network analysis, security testing, and future cybersecurity projects without exposing production systems or unauthorized networks to laboratory activities.

### Practical Focus

* Computer & Network Security
* Linux Administration
* Cisco & Network Configuration
* Ethical Hacking
* Vulnerability Assessment & Penetration Testing (VAPT)
* Security Tools & Laboratory Exercises
* Python for Cybersecurity
* Security Automation

## Lab Environment

The laboratory is implemented as a **virtualized cybersecurity workspace** on a Windows 11 host, with **Oracle VirtualBox 7.2.14** providing the virtualization layer and **Kali Linux 2026.2** serving as the primary security workstation.

The virtual environment is connected through a dedicated **NAT Network** using the `10.0.0.0/24` IPv4 address space. Kali Linux operates at `10.0.0.2/24`, with `10.0.0.1` as the default gateway and `8.8.8.8` as the configured DNS resolver.

This setup establishes a **controlled and repeatable network boundary** for laboratory activities. Network configuration, connectivity, and routing are validated from within the virtual environment, while a VirtualBox snapshot preserves the known-good baseline for subsequent experimentation and recovery.

### Environment Specification

| Layer                    | Configuration                                                     |
| ------------------------ | ----------------------------------------------------------------- |
| **Host Layer**           | Windows 11 · Intel Core i3/i5 · 8–16 GB RAM · 512 GB–1 TB Storage |
| **Virtualization Layer** | Oracle VirtualBox 7.2.14                                          |
| **Security Layer**       | Kali Linux 2026.2                                                 |
| **Network Layer**        | NAT Network · IPv4                                                |
| **Address Space**        | `10.0.0.0/24`                                                     |
| **Kali Linux**           | `10.0.0.2/24`                                                     |
| **Default Gateway**      | `10.0.0.1`                                                        |
| **DNS Resolver**         | `8.8.8.8`                                                         |
| **Recovery Baseline**    | VirtualBox Snapshot                                               |

> **Configuration Note:** Hardware and network parameters should reflect the actual laboratory environment used during implementation.

## Tools & Resources

The lab environment was built using the following tools and official resources:

| Tool / Resource       | Purpose                                                    |
| --------------------- | ---------------------------------------------------------- |
| **7-Zip**             | Extracting and preparing virtual machine files             |
| **Oracle VirtualBox** | Creating and managing the virtualized lab environment      |
| **Kali Linux**        | Primary operating system for cybersecurity laboratory work |

### Official Resources

* [7-Zip — Official Download](https://7-zip.org/download.html)
* [Oracle VirtualBox — Official Downloads](https://virtualbox.org/wiki/Downloads)
* [Kali Linux — Official Downloads](https://kali.org/get-kali)

**Documentation and software versions are referenced from official project sources to maintain a consistent and reproducible lab environment.**

## Phase 01 — Lab Setup

1. **7-Zip Setup**
2. **VirtualBox Setup**
3. **Network Configuration**
4. **Kali Linux Setup**
5. **IP Configuration**
6. **VM Snapshot**

### Step 01 — 7-Zip Installation

Install **7-Zip** to extract the downloaded virtual machine package before importing it into the virtualization environment.

**Official Download:** https://7-zip.org/download.html

### Step 02 — Oracle VirtualBox Installation

Install **Oracle VirtualBox** to create and manage the virtual machines required for the cybersecurity lab.

**Official Download:** https://virtualbox.org/wiki/Downloads
<img width="1919" height="1049" alt="Screenshot 2026-08-13 200258" src="https://github.com/user-attachments/assets/291c7f15-63d5-4173-98bc-205c7dfdf2ce" />


### Step 03 — Network Configuration

Configure a **NAT Network** in Oracle VirtualBox using the `10.0.0.0/24` IPv4 network for the lab environment.

<img width="1918" height="1022" alt="Screenshot 2026-08-13 200636" src="https://github.com/user-attachments/assets/73dbb64f-3354-48a5-8718-d9910652b72c" />


### Step 04 — Kali Linux Setup

Download and import the **Kali Linux Virtual Machine** into Oracle VirtualBox and connect it to the configured lab network.

**Official Download:** https://kali.org/get-kali

<img width="1920" height="922" alt="VirtualBox_KASL_107_10_08_2026_16_54_43" src="https://github.com/user-attachments/assets/a12ab319-b16e-4d9a-9f58-106e43c8812c" />
<img width="1914" height="1013" alt="Screenshot 2026-08-10 162755" src="https://github.com/user-attachments/assets/ff54b6f7-7ecd-44b4-bf54-79f340451245" />


### Step 05 — Kali Linux IP Configuration

Configure the Kali Linux network interface according to the lab's IPv4 addressing plan.

| Network Parameter | Configuration |
|---|---|
| **IP Address** | `10.0.0.2/24` |
| **Default Gateway** | `10.0.0.1` |
| **DNS Server** | `8.8.8.8` |

<img width="1920" height="922" alt="VirtualBox_KASL_107_13_08_2026_20_18_24" src="https://github.com/user-attachments/assets/2e41eb06-ce2e-4c6b-a671-480e9d2f740f" />

### Network Verification

The following commands were used to inspect and refresh the Kali Linux network interface:

```bash
ifconfig
sudo ifconfig eth0 down
sudo ifconfig eth0 up
```


<img width="1920" height="922" alt="VirtualBox_KASL_107_13_08_2026_20_26_48" src="https://github.com/user-attachments/assets/3777a938-e39b-4666-a5eb-4df41cbc241e" />

### Step 06 — VM Snapshot

Create a **VirtualBox snapshot** after completing the initial Kali Linux lab setup. The snapshot preserves the current VM state and provides a recovery point for future laboratory work.

**Purpose:** VM recovery and configuration rollback  
**Snapshot:** Created successfully  
**Status:** `Completed`

<img width="1919" height="1015" alt="Screenshot 2026-08-13 202858" src="https://github.com/user-attachments/assets/17de7f6d-c1a6-4dee-9310-254c66ac2fed" />


## Lab Demonstration

A short walkthrough of the completed Week 01 environment, including the virtual machine, network configuration, connectivity checks, and recovery point.

**Project Video:** 

WhatsApp Video 2026-08-13 at 9.54.02 PM.mp4
---

## Final Architecture

```text
Windows 11 Host
      │
      ▼
       │
       ▼
Oracle VirtualBox
      │
      ▼
       │
       ▼
NAT Network
10.0.0.0/24
      │
      ▼
Kali Linux
       │
       ▼
Kali Linux VM
10.0.0.2/24
```
## Key Outcomes

The Week 01 lab successfully established the core virtual cybersecurity environment and validated its initial network configuration.

- Kali Linux VM deployed and configured
- VirtualBox NAT Network established
- IPv4 addressing configured
- Network connectivity and DNS resolution verified
- VM snapshot created as a recovery point
- Environment prepared for subsequent cybersecurity exercises

## Security & Responsible Use

This laboratory is intended for authorized cybersecurity education, experimentation, and security testing.

All activities must remain within systems, networks, virtual machines, and applications that are owned or explicitly authorized for testing.


## Mentor

**Waqas Karim (CCIE)**

Technical guidance and mentorship provided throughout the cybersecurity internship.

## Phase 01 — Completion

**Status:** `COMPLETED`

Week 01 successfully established the foundational cybersecurity lab environment using **Oracle VirtualBox and Kali Linux**. The environment has been configured, network settings validated, and a recovery point created for continued laboratory work.

| Phase | Focus | Status |
|---|---|---|
| **01** | Virtualization & Network Foundations | **Completed** |

**Environment:** Kali Linux · Oracle VirtualBox · NAT Network  
**Next:** Advanced cybersecurity laboratory exercises

**Week 01 — Lab Environment Setup: Completed**
