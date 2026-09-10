# Multi-Site Enterprise Network with VLANs and OSPF

## Objective

The Multi-Site Enterprise Network project aims to design, implement, and
validate a simulated enterprise network connecting a Headquarters (HQ)
and a Branch Office using GNS3.

The objective is to reproduce a realistic enterprise network architecture
with logical network segmentation, inter-VLAN routing, dynamic routing
between sites, and structured IP addressing.

The project is developed progressively through multiple phases, starting
with the network foundation and routing infrastructure, followed by
enterprise services, network security, hardening, and troubleshooting.

The current implementation includes:

- Headquarters (HQ) network
- Branch Office network
- VLAN-based departmental segmentation
- 802.1Q trunking
- Router-on-a-Stick for inter-VLAN routing
- WAN connectivity between HQ and Branch
- OSPF dynamic routing
- IPv4 addressing and subnetting
- Connectivity testing and troubleshooting

---

## Network Architecture

The simulated enterprise network consists of two sites:

### Headquarters (HQ)

- HR VLAN 10
- Finance VLAN 20
- IT VLAN 30

### Branch Office

- HR VLAN 10
- Finance VLAN 20
- IT VLAN 30

The two sites are interconnected through a routed WAN link using OSPF.

---

## IP Addressing Plan

| Site | VLAN | Department | Network | Default Gateway |
|------|------|------------|---------|-----------------|
| HQ | 10 | HR | 192.168.10.0/24 | 192.168.10.1 |
| HQ | 20 | Finance | 192.168.20.0/24 | 192.168.20.1 |
| HQ | 30 | IT | 192.168.30.0/24 | 192.168.30.1 |
| Branch | 10 | HR | 192.168.110.0/24 | 192.168.110.1 |
| Branch | 20 | Finance | 192.168.120.0/24 | 192.168.120.1 |
| Branch | 30 | IT | 192.168.130.0/24 | 192.168.130.1 |

### WAN Link

| Device | Interface | IP Address |
|--------|-----------|------------|
| R-HQ | GigabitEthernet0/0 | 10.255.0.1/30 |
| R-BRANCH | GigabitEthernet0/0 | 10.255.0.2/30 |

---

## Technologies Used

- **GNS3**
  - Network simulation platform
- **Cisco IOS**
  - Router configuration
- **vIOS-L2**
  - Layer 2 switching
- **OSPF**
  - Dynamic routing protocol
- **802.1Q**
  - VLAN trunking
- **VPCS**
  - End-host simulation

---

## Skills Learned

- Enterprise network design and topology planning.
- IPv4 addressing and subnetting.
- VLAN creation and management.
- Access port configuration.
- 802.1Q trunk configuration.
- Inter-VLAN routing using Router-on-a-Stick.
- WAN connectivity between multiple sites.
- OSPF configuration and verification.
- Routing table analysis.
- Network connectivity testing.
- Network troubleshooting using Cisco IOS commands.
- Verification of VLAN and trunk configurations.
- Basic enterprise network documentation.

---

## Project Phases

### Phase 1 — Network Foundation & Routing

**Status: Completed ✅**

The first phase focused on establishing the basic enterprise network
infrastructure.

Implemented:

- HQ and Branch topology
- VLAN 10 — HR
- VLAN 20 — Finance
- VLAN 30 — IT
- Access port configuration
- 802.1Q trunking
- Router-on-a-Stick
- IPv4 addressing
- WAN connectivity
- OSPF Area 0
- Inter-VLAN routing
- Inter-Site routing
- Connectivity testing
- Troubleshooting

### Phase 2 — Enterprise Services

**Status: Planned 🔄**

Planned components:

- DHCP
- Automatic IP address assignment
- DHCP pools per VLAN
- DNS services
- Service verification and troubleshooting

### Phase 3 — Network Security & Segmentation

**Status: Planned 🔒**

Planned components:

- Extended ACLs
- Department-based traffic restrictions
- Inter-VLAN access control
- Network segmentation policies
- Management access restrictions

### Phase 4 — Network Hardening

**Status: Planned 🔒**

Planned components:

- SSH configuration
- Secure device management
- Port security
- PortFast
- BPDU Guard
- Management VLAN
- Unused interface shutdown
- Native VLAN hardening

### Phase 5 — Monitoring & Troubleshooting

**Status: Planned 🔍**

Planned scenarios:

- VLAN configuration errors
- Trunk failures
- Gateway misconfiguration
- Interface failures
- OSPF adjacency issues
- Routing problems
- ACL-related connectivity issues

### Phase 6 — Final Enterprise Scenario

**Status: Planned 🚀**

The final phase will combine the implemented technologies into a
complete multi-site enterprise network scenario.

The final architecture will include:

- VLAN segmentation
- Inter-VLAN routing
- OSPF
- DHCP
- ACL-based security
- Secure device management
- Network hardening
- Troubleshooting scenarios


