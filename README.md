# Firewall, IDS & Traffic Analysis Lab

This project simulates a **small company with a flat network**, where a compromised device could communicate freely with other systems and enable lateral movement.

The goal is to **segment the network and control communication between different areas**, reducing the impact of a possible compromise and applying basic network security controls.

## Tools and Security Decisions

* **Oracle VirtualBox:** used to build the virtual lab and create isolated network segments without requiring physical equipment.
* **Netplan:** used to configure static IP addresses, ensuring that each host and network segment keeps a predictable address.
* **Linux Router:** placed between the network segments so that all inter-segment traffic passes through a controlled point.
* **iptables:** used as the firewall to define which traffic can or cannot pass between the segments. Rules in the `FORWARD` chain were used to block unnecessary communication.
* **Suricata:** used as an IDS to monitor traffic between the segments and detect suspicious activity or communication attempts.
* **Wireshark:** used to capture and analyze packets, helping validate how traffic behaves before and after the security controls are applied.

## Security Approach

Instead of allowing every device to communicate freely, the network is divided into separate segments. Communication between them must pass through the router, where firewall rules can restrict access.

This approach helps reduce **lateral movement** and provides better visibility and control over network traffic.

## Current Status

* Network segmentation ✅
* Linux routing ✅
* iptables firewall ✅
* Firewall validation ✅
* Suricata IDS 🚧
* Wireshark traffic analysis 🚧
