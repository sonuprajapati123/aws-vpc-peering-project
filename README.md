# AWS VPC Peering Project

## Project Overview
This project demonstrates connectivity between two Amazon VPCs using AWS VPC Peering.

## Architecture

### VPC A
- Name: sonu-vpc-a
- CIDR: 10.10.0.0/16
- Public subnet: 10.10.1.0/24
- Private subnet: 10.10.2.0/24
- Bastion Host: 10.10.1.65
- App-A: 10.10.2.238

### VPC B
- Name: sonu-vpc-b
- CIDR: 10.20.0.0/16
- Private subnet: 10.20.1.0/24
- App-B: 10.20.1.22

## AWS Services Used
- Amazon VPC
- Public and private subnets
- VPC Peering
- Route Tables
- Internet Gateway
- EC2 Instances
- Security Groups
- SSH and ICMP connectivity testing

## Implementation Steps
1. Created two VPCs with non-overlapping CIDR blocks.
2. Created public and private subnets.
3. Created and activated a VPC Peering connection.
4. Added routes between the two VPCs.
5. Configured security groups for SSH and ICMP traffic.
6. Launched a Bastion host and private EC2 instances.
7. Tested connectivity using ping and SSH.

## Validation Results
- Bastion to App-A: Ping successful.
- Bastion to App-B: Ping successful.
- App-B to App-A: Ping successful.
- SSH connection from Bastion to App-B: Successful.

## Security Notes
- Private application instances do not require public IP addresses.
- SSH access should be restricted to trusted sources.
- Never upload private keys, passwords, or AWS credentials to GitHub.

## Cleanup
Delete or stop lab resources when they are no longer needed to avoid unnecessary AWS charges.
