# Active-Directory-Lab

## Objective

The Active Directory Lab project aimed to establish a controlled virtual environment to simulate and analyse Windows domain-based networks. The primary focus was to implement Active Directory Domain Services (AD DS), monitor event logs within a Security Information and Event Management (SIEM) system (Splunk), and generate test telemetry mimicking real-world attack scenarios using tools like Atomic Red Team. This hands-on project deepened understanding of enterprise-level authentication systems, attack detection, and defensive strategies.

### Skills Learned

- Configuring and managing Active Directory environments  
- Deploying and utilising SIEM for log collection and analysis  
- Simulating adversarial techniques in a controlled lab  
- Critical thinking and troubleshooting in cybersecurity scenarios  

### Tools Used

- **Splunk** – for ingesting and analysing Windows event logs  
- **Atomic Red Team** – for simulating attack techniques (MITRE ATT&CK)  
- **VirtualBox** – as the hypervisor to host all virtual machines  
- **Windows Server 2022, Windows 10, Ubuntu Server, Kali Linux** – for simulating enterprise and attack infrastructure  

---

## Steps

### 1. Overview

This lab consists of four virtual machines configured within a VirtualBox NAT network:

| Machine              | Tools               |
|----------------------|---------------------|
| Ubuntu Server        | Splunk (SIEM)       |
| Windows Server 2022  | AD DS               |
| Windows 10           | Splunk Forwarder    |
| Kali Linux           | Atomic Red Team     |

*Ref: A table displaying all four virtual machines and their associated tooling*

**Network Configuration:**

| Machine              | IP Address | Subnet           | Default Gateway  |
|----------------------|------------|------------------|------------------|
| Ubuntu Server        | 192.168.x.x| 192.168.10.0/24  | 192.168.10.1     |
| Windows Server 2022  | 192.168.x.x| 192.168.10.0/24  | 192.168.10.1     |
| Windows 10           | 192.168.x.x| 192.168.10.0/24  | 192.168.10.1     |
| Kali Linux           | 192.168.x.x| 192.168.10.0/24  | 192.168.10.1     |

*Ref: A table displaying all four virtual machines’ network assignments*

> Add a network diagram here
> *Ref A: Network diagram showing VM connections and NAT configuration*

---

### 2. Installing & Configuring Virtual Machines

Each machine was installed and configured as follows:

- **Ubuntu Server** – Installed Splunk for log ingestion and dashboard setup  
- **Windows Server 2022** – Installed Active Directory Domain Services (AD DS) and promoted to Domain Controller  
- **Windows 10** – Joined the domain and had Splunk Universal Forwarder installed for log shipping  
- **Kali Linux** – Used to run Atomic Red Team scripts to simulate attack scenarios  

Assumes VirtualBox is already installed on the host (Windows 11).
