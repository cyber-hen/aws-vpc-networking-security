📘 AWS VPC Traffic Flow & Security Project
<p align="center">
<strong>Hands-on cloud networking & security lab built on AWS</strong><br>
VPC • Subnets • Route Tables • Internet Gateway • Security Groups • NACLs
</p>

🚀 Overview
This project demonstrates how I designed and deployed a secure Amazon Virtual Private Cloud (VPC) environment.
It covers essential AWS networking components including:

VPC

Public Subnet

Internet Gateway

Route Tables

Security Groups

Network ACLs

The goal was to understand traffic flow, security boundaries, and how AWS networking works in real-world scenarios.
This project was built as part of my DevOps/DevSecOps learning journey. 

🧠 What is Amazon VPC?
Amazon VPC is an isolated virtual network inside AWS where you can run resources privately or publicly.
It allows full control over:

IP addressing

Subnets

Routing

Security layers

In this project, I used VPC to create a public subnet, attach an Internet Gateway, configure routing, and secure resources using Security Groups and Network ACLs. 

🛠️ What I Built
1. Created a Custom VPC
A dedicated virtual network to host all resources.

2. Public Subnet
Assigned a CIDR block and configured it for internet-facing resources.

3. Internet Gateway
Attached an IGW to the VPC to enable inbound/outbound internet connectivity. 

4. Route Table
Created a custom route table

Added a route:

Destination: 0.0.0.0/0

Target: Internet Gateway

Associated it with the public subnet
This made the subnet truly public. 

5. Security Groups
Security Groups act as resource-level firewalls.

Inbound rule: Allowed HTTP traffic from any IP

Outbound rule: Allowed all outbound traffic (default AWS behavior) 

6. Network ACLs (NACLs)
Subnet-level firewalls that allow or deny traffic entering/leaving the subnet.

Default NACLs allow all traffic

Custom NACLs deny all traffic until rules are added 

🔐 Security Groups vs Network ACLs
Feature	Security Group	Network ACL
Layer	Resource level	Subnet level
Stateful	Yes	No
Default behavior	Allow outbound	Allow all (default), deny all (custom)
Use case	Protect individual resources	Protect entire subnets

🌍 Route Tables & Traffic Flow
Route tables determine how traffic moves inside the VPC and to the internet.

To make a subnet public, it must have:

An Internet Gateway

A route sending 0.0.0.0/0 traffic to the IGW

Without this, even a “public” subnet cannot access the internet. 

🧩 What Surprised Me
I didn’t expect the project to be this interesting and straightforward.
It helped me understand how AWS networking pieces fit together. 


