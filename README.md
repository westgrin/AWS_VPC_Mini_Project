# # AWS VPC - Virtual Private Cloud Mini Project

## Project Overview
This 2-hour mini-project explores AWS VPC for GatoGrowFast.com, covering VPC creation, subnets, internet gateways, NAT gateways, route tables, and VPC peering, executed on Ubuntu (WSL) with VS Code via Ubuntu.

## Setup
- Initiated on Jul 01, 2025, 08:12 PM WAT.
- Used Ubuntu terminal (WSL) with VS Code, documented in ~/Documents/Workspace/AWS_VPC_Mini_Project.

## Project Execution

### 1. Set Up a Virtual Private Cloud (VPC)
- Created `gato-vpc` with CIDR `10.0.0.0/16`.

### 2. Configure Subnets within the VPC
- Created `gato-public-subnet` (CIDR `10.0.1.0/24`) and `gato-private-subnet` (CIDR `10.0.2.0/24`).

### 3. Create Internet Gateway and Attach to VPC
- Created `gato-igw` and attached it to `gato-vpc`.

### 4. Enable Internet Connectivity with Route Tables
- Created `gato-public-rt`, associated `gato-public-subnet`, and added route `0.0.0.0/0` to `gato-igw`.

### 5. Enable Outbound Internet Access through NAT Gateway
- Created `GatoNAT` in `my-private-subnet-1`, updated route table with `0.0.0.0/0` to `GatoNAT`, and associated `my-private-subnet-1`.

### 6. Establish VPC Peering Connections
- Created `GatoVPC2` with CIDR `172.16.0.0/16`, set up peering between `GatoVPC1` and `GatoVPC2`, and updated route tables with respective CIDRs.

### Project Reflection
- **Completed Tasks**: Successfully set up VPC infrastructure and configured network components.
- **Hands-On Experience**: Navigated AWS console to create and manage VPC resources.
- **Challenges**: Resolved CIDR block size errors by adjusting ranges; troubleshooted peering by verifying route tables.
- **Network Architecture**: Gained insights into subnets, gateways, and routing for secure cloud networking.
- **Security Measures**: Recognized NAT gateway and VPC peering’s role in secure communication.
- **Overall Learning**: Acquired practical skills in cloud networking fundamentals applicable to real-world scenarios.

## Tools Used
- **Ubuntu Terminal (WSL)**: For documentation.
- **VS Code**: For editing `README.md`.
- **Git Bash**: For version control and GitHub push.
- **AWS Management Console**: For VPC configuration.

## Project Deliverables
- **Documentation**: This `README.md` details the process and reflection.
- **Script Link**: [GitHub Repository](https://github.com/westgrin/AWS_VPC_Mini_Project)

## Conclusion
This project effectively implemented a secure VPC network for GatoGrowFast.com, enhancing connectivity and security with practical cloud networking skills.