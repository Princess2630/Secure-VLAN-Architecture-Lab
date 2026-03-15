# Secure Enterprise Branch Network - K Office

## Overview
A fully functional network simulation for a corporate branch office, designed with a focus on security and department isolation (Segmentation).

## Technical Features
- **VLAN Segmentation:** 3 Isolated networks (Management, Engineering, Guest).
- **Inter-VLAN Routing:** Implemented "Router-on-a-Stick" on a Cisco 2911.
- **Security Protocols:**
  - **SSHv2:** Encrypted remote management (RSA 1024-bit).
  - **ACLs:** Access Control Lists to prevent Guest access to internal resources.
  - **Audit Logging:** Configured Syslog timestamps and login monitoring.
- **Addressing:** Standardized 10.0.x.0/24 IP scheme.

## How to Test
1. Open the `.pkt` file in Cisco Packet Tracer.
2. Ping from **Engineering PC** to **Management PC** (Success).
3. Ping from **Guest PC** to **Management PC** (Blocked by ACL).
4. SSH from **Management PC** to `10.0.10.1` using the `admin` account.
