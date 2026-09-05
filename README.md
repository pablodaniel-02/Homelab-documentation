# Homelab-documentation
## Overview

### Homelab Infrastructure

- **Host Machine**: HP ProDesk 400 G4 Mini running **Proxmox VE**
- **Hardware**:
  - **CPU**: Intel Core i5-8500 (6 cores @ 3.00 GHz)
  - **Memory**: 16 GB DDR4
  - **Storage**: 238 GB NVMe SSD
  - **External Storage**: Seagate external drive 2TB (mounted for Nextcloud)

All services run as LXC containers or VMs on this single host.


### Services

The lab is split into infrastructure services (LXC containers) and virtual machines used for security testing.

#### LXC Containers

- **WireGuard**: A modern, lightweight VPN providing secure remote access to the lab without exposing internal services directly to the internet.
- **Nextcloud**: A self-hosted file storage and sync platform, backed by an external drive mounted to the host.

#### Virtual Machines

- **Kali Linux**: An offensive-security distribution used as the attack box, equipped with tools such as Metasploit and Nmap.
- **Metasploitable 2**: A deliberately vulnerable Linux target used to practice and document attacks in an isolated environment.
