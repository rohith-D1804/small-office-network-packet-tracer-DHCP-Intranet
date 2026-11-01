# Small Office Network with DHCP, DNS, and Intranet

A small-office network simulation built in **Cisco Packet Tracer**. The network separates Admin and IT devices into two subnets, assigns IP settings automatically through DHCP, and provides an internal website accessible by DNS name.

## Project Overview

The simulated office includes:

- 1 router
- 2 switches
- 4 PCs (2 Admin, 2 IT)
- 1 server providing DNS and HTTP services

## Network Addressing

| Department / Device | Network / IP | Default Gateway |
|---|---|---|
| Admin network | `192.168.10.0/24` | `192.168.10.1` |
| IT network | `192.168.20.0/24` | `192.168.20.1` |
| Server | `192.168.10.2` | `192.168.10.1` |

The router provides DHCP for both subnets. The server provides DNS and hosts the internal website.

## Services

- **DHCP:** Automatically assigns IP addresses, subnet masks, gateways, and DNS settings to the PCs.
- **DNS:** Resolves `intranet.office` to `192.168.10.2`.
- **HTTP:** Hosts an internal website accessible at `http://intranet.office`.

## Validation

The following tests were completed:

- All four PCs received network settings through DHCP.
- Admin and IT devices communicated across the two subnets.
- `intranet.office` resolved to `192.168.10.2`.
- The internal website loaded from both departments.

## Troubleshooting

The initial server-based DHCP configuration did not provide the expected gateway and DNS settings. DHCP was moved to the router and configured with separate pools for Admin and IT. After the change, all four PCs received the correct settings and connectivity tests succeeded.

## Files

- `Small_Office_Network_Project2.pkt` — Cisco Packet Tracer simulation
- Project documentation — network design, configuration, tests, and screenshots

## Tools

- Cisco Packet Tracer

## Note

This project is a **network simulation for learning and portfolio purposes**, not a live office deployment.