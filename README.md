# Virtualized-IT-Infrastructure-Security-Homelab

<h2>Description</h2>


A self-built homelab simulating enterprise IT infrastructure for hands-on practice in IT support and cybersecurity. Built on a single physical machine running Proxmox VE, with network segmentation, a virtual firewall, and an isolated LAN environment.

---

## Hardware

| Component | Device |
|---|---|
| Hypervisor Host | Dell OptiPlex (repurposed desktop) |
| Switch | TP-Link TL-SG108E (managed, 8-port) |
| Access Point | TP-Link TL-WR1502X (AP mode) |

---

## Network Architecture

```
[place holder]
```

---

## Stack

| Component | Purpose |
|---|---|
| **Proxmox VE** | Hypervisor — manages all VMs |
| **pfSense** | Virtual firewall, router, VPN |
| **Windows Server** | Active Directory, DNS, DHCP |
| **Ubuntu Server** | Lab management, testing |
| **Wazuh SIEM** | Log management, threat detection |
| **WireGuard VPN** | Encrypted tunnel (via pfSense) |

---

## Network Segmentation

VLAN separation is configured on the TP-Link TL-SG108E managed switch:

| VLAN | Name | Purpose |
|---|---|---|
| VLAN 1 | Default | Home router, Proxmox management, WAN traffic |
| VLAN 2 | LAN | pfSense LAN — isolated internal lab network |

All VMs on the internal LAN (VLAN 2) route through pfSense, keeping lab traffic fully separated from the home network.

---

## Features

- **Virtual firewall** — pfSense running as a VM with dedicated WAN and LAN interfaces
- **Network segmentation** — VLAN isolation between home network and lab environment
- **Active Directory domain** — Windows Server domain controller with DNS, DHCP, and Group Policy
- **Encrypted wireless** — Dedicated access point routing through pfSense WireGuard VPN
- **Security monitoring** — Wazuh SIEM for log collection and threat detection across the lab


---

## Skills Demonstrated

- Proxmox VE hypervisor setup and VM management
- pfSense firewall configuration and network routing
- VLAN configuration on a managed switch
- Active Directory administration (users, groups, GPO, DNS, DHCP)
- WireGuard VPN setup and management
- Linux server administration (Ubuntu Server)
- Network traffic analysis and SIEM log monitoring


---

