# AWS Cloud Architecture Project

> **Note:** This is an intentionally high-level overview to maintain the integrity of my university assignment.  
> Detailed configurations, code, and implementation steps have been omitted.

---

## Project Overview

This project delivers a **secure, scalable, and highly available** AWS cloud infrastructure — designed with fault tolerance, hybrid connectivity, and layered security in mind. The goal is to model a **production-ready architecture** that can handle real-world workloads while staying resilient to failures and attacks.

---

## Key Features

### **Networking & Connectivity**
- **Global DNS Routing:** Amazon Route 53 for low-latency traffic steering.
- **Hybrid Access:** Site-to-Site VPN + Client VPN for secure on-premises integration.
- **Multi-AZ VPC:** Public and private subnets split across Availability Zones.
- **Controlled Egress:** NAT Gateways + Internet Gateway with traffic segmentation.

### **Compute & Scalability**
- **Load-Balanced Workloads:** EC2 instances in private subnets behind an ALB.
- **On-Demand Scaling:** Auto Scaling Groups to meet demand without overprovisioning.

### **Security & Compliance**
- **Defense in Depth:** AWS WAF, Shield, and Network Firewall for multi-layer protection.
- **Governance & Threat Detection:** IAM, Security Hub, GuardDuty, and AWS Artifact.
- **Data Protection:** KMS encryption with fine-grained IAM access control.

### **Data & Storage**
- **Highly Available Databases:** Amazon RDS with primary-standby replication + RDS Proxy.
- **Secure Object Storage:** Amazon S3 with encryption and policy controls.
- **Secret Management:** AWS Secrets Manager for credential lifecycle control.

### **Monitoring & Logging**
- **Performance & Health:** Amazon CloudWatch metrics, dashboards, and alarms.
- **Audit & Compliance:** AWS CloudTrail for complete API activity history.

---

## Architecture Diagram

<p align="center">
  <img src="https://i.imgur.com/CggZaoE.png" alt="AWS Architecture Diagram" width="750px">
</p>

---

## Future Recommendations

To align more closely with **enterprise-grade** environments, future iterations could include:

- **Automated Deployments:** Integrate CI/CD pipelines (AWS CodePipeline, GitHub Actions).  
- **Federated Access:** Use AWS SSO or Okta/Azure AD for unified identity management.  
- **Microservices Migration:** Adopt ECS, EKS, or Lambda for containerized workloads.  
- **Resilience at Scale:** Add cross-region backup & disaster recovery configurations.  
- **Infrastructure as Code:** Implement Terraform or AWS CDK for repeatable deployments.  
- **Advanced Networking:** Introduce Transit Gateway & dynamic routing for complex VPCs.  
- **Analytics Layer:** Build a data lake/warehouse (Athena, Redshift) for business insights.  

---
