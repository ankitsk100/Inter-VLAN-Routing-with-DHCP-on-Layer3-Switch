# Inter-VLAN Routing with DHCP on Layer 3 Switch

## Project Overview

This project demonstrates Inter-VLAN Routing using a Layer 3 Switch (3560) 
with DHCP service configured on the multilayer switch.

The network is divided into three departments:

- VLAN 10 – IT Department
- VLAN 20 – Sales Department
- VLAN 30 – HR Department

The Layer 3 Switch performs:
- Inter-VLAN Routing
- DHCP Server functionality
- Default Gateway services for all VLANs

---

## What is Inter-VLAN Routing?

VLANs are isolated broadcast domains. Devices in different VLANs cannot 
communicate unless a Layer 3 device routes traffic between them.

In this project, the Layer 3 switch performs routing using:
- SVIs (Switch Virtual Interfaces)
- `ip routing` command

---

## What is DHCP?

Dynamic Host Configuration Protocol (DHCP) automatically assigns:

- IP Address
- Subnet Mask
- Default Gateway
- DNS Server

The Layer 3 switch acts as the DHCP server for all VLANs.

---

## Topology

See full topology inside:

`docs/topology.png`

---

## Network Design

| VLAN | Department | Network | Gateway |
|------|------------|----------|----------|
| 10 | IT | 192.168.1.0/24 | 192.168.1.1 |
| 20 | SALES | 192.168.2.0/24 | 192.168.2.1 |
| 30 | HR | 192.168.3.0/24 | 192.168.3.1 |

---

## Features Implemented

- VLAN creation and port assignment
- Trunk links between switches and L3 switch
- Inter-VLAN routing via SVIs
- DHCP configuration per VLAN
- DHCP IP exclusion ranges
- Layer 3 switching with `ip routing`

---

## Verification Commands

show vlan brief
show ip interface brief
show ip route
show ip dhcp binding

