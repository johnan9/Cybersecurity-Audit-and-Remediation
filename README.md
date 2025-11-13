# Cybersecurity Audit & Remediation Lab – E-MAGINE Biomedical

**Role:** Security Analyst  
**Student:** John An  
**Environment:** Windows Server 2019, Windows 10, Ubuntu Linux, pfSense Firewall (VCASTLE Lab)


## 📌 Project Overview

This project simulates a full lifecycle **cybersecurity audit and remediation** for a fictional organization, **E-MAGINE Biomedical**.

The goals of this project were to:

- Audit Windows Server, Windows 10, Linux, and pfSense systems  
- Detect misconfigurations and vulnerabilities  
- Apply remediations aligned with security best practices  
- Implement identity, access control, network segmentation, and cryptography  
- Document the workflow using a professional change-control structure (pre-execution, execution, post-execution, follow-up)

This repo demonstrates the type of security engineering and system hardening work expected from an entry-level **Security Analyst, Systems Engineer, or Network Security Engineer**.


## 🧱 Lab Architecture

**Systems included:**

- Windows Server 2019 (AD, GPO, SMB, IIS, CA)
- Windows 10 Client (domain-joined)
- Ubuntu Linux (SSH, UFW, auditd, Samba, syslog)
- pfSense Firewall (network segmentation & device management security)

**Example IP Plan:**

- `172.16.10.10` – Windows 10  
- `172.16.20.20` – Ubuntu  
- `172.16.30.30` – Windows Server  
- `172.16.100.1` – pfSense  


---

## 🧪 Week-by-Week Summary

### **Week 1 – System Auditing & Automatic Updates**
- Enabled Windows audit policy (logon events, account changes, policy changes).
- Enabled automatic updates via Group Policy.
- Configured Ubuntu unattended-upgrades.
- Installed and enabled Linux auditd with GRUB change (`audit=1`).

### **Week 2 – Access Control & File Sharing**
- Created secured Windows SMB shares for HR, IT, and COMMON.
- Applied NTFS permissions using least privilege.
- Configured Samba shares on Ubuntu with group-based access.
- Hardened pfSense GUI security (new admin account, non-standard port, restricted IP access).

### **Week 3 – Firewall Hardening & Network Segmentation**
- Configured Windows Firewall on DCs with required AD ports.
- Enabled and configured UFW on Ubuntu (SSH, syslog, NTP).
- Added pfSense rules for ICMP, AD ports, and internal segmentation.

### **Week 4 – IAM, Password Policy & RBAC**
- Removed non-IT users from Domain Admins.
- Enforced separate admin accounts (no shared privileged accounts).
- Configured password & lockout policies:
  - Min length 12  
  - Password history 24  
  - Lockout threshold 5  
- Linux: Disabled root login, enforced password aging.
- pfSense: Created read-only and read-write roles.

### **Week 5 – PKI, SSL/TLS & Secure Remote Access**
- Installed AD CS and issued an SSL certificate for the IIS server.
- Configured HTTPS and verified trusted CA chain.
- Set up SSH public-key authentication on Linux.
- Enabled pfSense SSH on a non-default port (2022) with key-based authentication only.

---

## 🔐 Key Skills Demonstrated

- **Windows Server Administration**  
  AD, GPO, NTFS permissions, audit policy, IIS, certificate services

- **Linux System Hardening**  
  UFW, auditd, SSH hardening, Samba permissions

- **Firewall & Networking**  
  pfSense firewall rules, segmentation, secure management access

- **Identity & Access Management**  
  RBAC, least privilege, password policy, account lockout, secure admin accounts

- **Cryptography & PKI**  
  Certificate Authorities, SSL/TLS, SSH key management

- **Security Engineering Concepts**  
  Defense in depth, secure configurations, change management, logging

---

## 🧩 Relevant Job Roles

This project maps well to roles such as:

- **Security Analyst / SOC Analyst (L1/L2)**
- **Systems Administrator / Systems Engineer**
- **Network Security Engineer**
- **IT Security Specialist**
- **Infrastructure Security Engineer**

---

