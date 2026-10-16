# linux-infra-lab
# 🐧 Linux Infra Lab

### Enterprise Network Infrastructure · Linux System Administration · DevOps

<p align="center">
  <img src="https://img.shields.io/badge/Linux-Infrastructure-1793D1?style=for-the-badge&logo=linux&logoColor=white" alt="Linux Infrastructure" />
  <img src="https://img.shields.io/badge/VirtualBox-Virtualization-183A61?style=for-the-badge&logo=virtualbox&logoColor=white" alt="VirtualBox" />
  <img src="https://img.shields.io/badge/Networking-TCP%2FIP-1677C8?style=for-the-badge&logo=cisco&logoColor=white" alt="Networking" />
  <img src="https://img.shields.io/badge/Focus-Systems%20%26%20DevOps-2563EB?style=for-the-badge&logo=linuxcontainers&logoColor=white" alt="Systems and DevOps" />
</p>

<p align="center">
  <i>A practical laboratory for building, configuring, documenting, and understanding Linux-based enterprise infrastructure.</i>
</p>

---

## 🌐 About the Project

**Linux Infra Lab** is a hands-on infrastructure project developed as part of the *Fundamentals of Computer Networks* course at Universidad del Valle, Pacific Campus, Buenaventura, Colombia.

The project focuses on the design, implementation, and administration of a decentralized enterprise network using Linux virtual machines and a collection of network and infrastructure services.

The laboratory is designed to explore how different services work together to provide connectivity, communication, centralized authentication, data management, storage, and printing capabilities within an enterprise environment.

Beyond service installation, this project emphasizes technical documentation, network architecture, troubleshooting, service availability, and reproducible configuration procedures.

## 🎯 Project Objectives

- Design and document a Linux-based enterprise network architecture.
- Configure and administer network services in a virtualized environment.
- Understand communication between client and server systems.
- Explore centralized authentication and shared infrastructure resources.
- Validate service functionality through connectivity and operational tests.
- Document configuration procedures and troubleshooting steps.
- Establish a foundation for future infrastructure automation and containerization.

## 🏗️ Infrastructure Architecture

The original laboratory is based on two Linux virtual machines managed through Oracle VirtualBox.

```text
                  ENTERPRISE NETWORK LAB
                            |
                   +------------------+
                   |  Virtual Network |
                   +------------------+
                            |
                 +----------+----------+
                 |                     |
        +----------------+    +----------------+
        |  Linux Client  |    |  Linux Server  |
        |                |    |                |
        | Service access |    | Network and    |
        | Connectivity   |    | infrastructure  |
        | Validation     |    | services       |
        +----------------+    +----------------+
                                      |
                          +-----------+-----------+
                          |           |           |
                        Web/DNS    Identity    Data and
                        Services   Services   Resources
```

*Conceptual diagram. The final architecture will reflect the actual network topology, service distribution, and dependencies implemented in the laboratory.*

### Infrastructure Components

| Component | Purpose |
|---|---|
| Linux Client | Accessing services and validating connectivity |
| Linux Server | Hosting and administering infrastructure services |
| VirtualBox | Virtual machine management |
| Virtual Network | Communication between virtualized systems |
| Service Configuration | Defining service behavior and dependencies |
| Testing and Documentation | Verifying and recording operational results |

## 🧩 Enterprise Services

The project requirements cover ten infrastructure services or service areas.

| # | Service | Purpose |
|---|---|---|
| 01 | Firewall | Network traffic filtering and access control |
| 02 | Web Server / HTTPS | Hosting web resources and enabling encrypted communication |
| 03 | DNS Server | Resolving hostnames to IP addresses |
| 04 | Proxy Server | Managing and controlling supported client web traffic |
| 05 | DHCP Server | Providing automatic network configuration to clients |
| 06 | Network Storage — TrueNAS | Centralized storage and shared resources |
| 07 | Mail Server | Supporting email communication |
| 08 | Centralized Authentication — LDAP | Managing centralized directory-based authentication |
| 09 | MySQL Database — Docker | Providing a database service in a containerized environment |
| 10 | Print Server — CUPS | Managing network printing resources |

**Implementation status:** These are the project's required service areas. Individual configurations, dependencies, and validation results will be documented as they are verified.

## 🔐 Networking and Security

Network services must operate within a coherent architecture. Their configuration requires attention to connectivity, access control, name resolution, and service dependencies.

The laboratory provides an environment for studying:

- TCP/IP networking and IP addressing.
- Client-server communication.
- Firewall rules and traffic filtering.
- DNS resolution and DHCP address assignment.
- HTTPS and encrypted communication.
- LDAP-based centralized authentication.
- Service ports and network reachability.
- Troubleshooting and operational verification.

Security configurations and test results will be documented without exposing passwords, private keys, authentication tokens, or sensitive network information.

## 🐳 Containerization and DevOps Roadmap

A future development goal is to explore how selected services can be deployed using Docker and Docker Compose.

The containerized version will be evaluated separately from the original VirtualBox environment.

Planned areas of exploration include:

- Containerizing suitable services.
- Defining services through `compose.yaml`.
- Managing configuration and environment variables.
- Using persistent volumes for service data.
- Creating appropriate container networks.
- Implementing health checks and connectivity tests.
- Documenting deployment and recovery procedures.

Not every infrastructure service is suitable for direct containerization. Services requiring specialized networking, operating-system integration, or hardware access will be evaluated individually.

## 📁 Repository Structure

```text
linux-infra-lab/
├── README.md
├── .gitignore
├── docs/
│   ├── architecture.md
│   ├── network.md
│   ├── services.md
│   └── troubleshooting.md
├── client/
│   └── scripts/
├── server/
│   ├── config/
│   └── scripts/
├── tests/
└── evidence/
```

The directory structure will evolve according to the actual configuration files, scripts, documentation, and test evidence collected during implementation.

## 🧪 Testing and Validation

Each service should have documented verification procedures appropriate to its function.

Examples include:

- Checking service status.
- Validating listening ports.
- Testing DNS resolution.
- Verifying client-server connectivity.
- Testing web access over HTTPS.
- Validating authentication and authorization.
- Checking database connectivity.
- Confirming access to shared storage and printing resources.

Test results will distinguish successful validations, known limitations, and pending tasks.

## 📚 Documentation

The documentation will include:

- Network architecture and topology.
- IP addressing and virtual network configuration.
- Service installation and configuration procedures.
- Dependencies between services.
- Test commands and expected results.
- Selected screenshots and implementation evidence.
- Troubleshooting notes and lessons learned.

## 🛠️ Technology Stack

<p>
  <img src="https://img.shields.io/badge/Linux-1793D1?style=flat-square&logo=linux&logoColor=white" alt="Linux" />
  <img src="https://img.shields.io/badge/VirtualBox-183A61?style=flat-square&logo=virtualbox&logoColor=white" alt="VirtualBox" />
  <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" alt="Git" />
  <img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white" alt="GitHub" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/Networking-TCP%2FIP-2563EB?style=flat-square&logoColor=white" alt="Networking" />
</p>

*Docker is included as part of the project requirements and future development direction; the final description will reflect the services actually deployed and tested.*

## 🎓 Academic Context

**Institution:** Universidad del Valle — Pacific Campus  
**Course:** Fundamentals of Computer Networks  
**Project:** Implementation and Administration of an Enterprise Network  
**Location:** Buenaventura, Valle del Cauca, Colombia

This project combines practical system administration with network design, service configuration, technical documentation, and infrastructure troubleshooting.

## 👩‍💻 Author

**Maro Montes**

Software Development student interested in Linux infrastructure, DevOps, cybersecurity, network services, and infrastructure automation.

This laboratory is part of my ongoing technical learning journey, focused on understanding how infrastructure works, documenting what I build, and improving configurations through practical experimentation.

---

<p align="center">
  <i>Build it. Understand it. Document it. Improve it.</i>
</p>
