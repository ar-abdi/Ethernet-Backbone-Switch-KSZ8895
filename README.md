# 4-Port Fast Ethernet Switch Board (KSZ8895)

## Overview

This project documents the design of a standalone 4-port 10/100 Mbps Ethernet switch board based on the KSZ8895 Ethernet switch IC from Microchip Technology.

The board was developed to serve as a centralized Ethernet communication backbone for distributed robotic subsystems.

Firmware configuration and network management are handled by the software team. This repository focuses exclusively on hardware architecture and PCB implementation.

---

## Why This Board Was Needed

As the robotic system evolved, multiple independent control boards required Ethernet connectivity for data exchange and coordination.

Initially, subsystem-to-subsystem communication relied on direct point-to-point connections, which introduced:

- Limited scalability
- Increased wiring complexity
- Reduced modularity
- Difficulty expanding the system

To support a structured and scalable architecture, a dedicated Ethernet backbone was required.

This switch board enables:

- Centralized network topology
- Simplified subsystem integration
- Cleaner physical wiring organization
- Modular hardware expansion
- Reliable multi-node communication

The board separates communication infrastructure from individual control boards, improving system maintainability and scalability.

---

## Hardware Architecture

Key components:

- KSZ8895 4-Port Fast Ethernet Switch
- Magnetics-based isolation per port
- 3.3V regulated power domain
- SPI hardware interface for management configuration

The KSZ8895 integrates switching logic and PHY functionality, enabling standalone Ethernet switching without requiring an external MAC controller.

---

## PCB Design Considerations

The design emphasized signal integrity and EMI control:

- Differential pair routing for TX/RX signals
- Length matching between paired traces
- Continuous reference planes for high-speed routing
- Controlled trace spacing
- Reduced via usage in critical paths
- Clean separation between high-speed and power domains

---

## Tools Used

- Altium Designer
- Multi-layer PCB layout
- Datasheet-driven hardware implementation
