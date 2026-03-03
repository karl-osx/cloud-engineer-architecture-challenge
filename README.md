# cloud-engineer-architecture-challenge

## Deliverable

This repository contains the technical challenge deliverable for the Cloud Engineer position.

- **PDF Document:**  
  `docs/reto_tecnico_cloud_engineer`

---

## Architecture Overview

The proposed solution is a **cloud-native AWS architecture** designed with the following principles:

- High Availability (Multi-AZ)
- Security by Design
- Network Segmentation
- Managed Services
- Observability & Monitoring
- Scalability and Operational Efficiency

---

##  Architecture Components

### Edge Layer
- Amazon CloudFront (CDN)
- AWS WAF (Web Application Firewall)
- Application Load Balancer (Regional)

### Application Layer
- Amazon ECS Fargate (Auto Scaling enabled)
- Private Subnets (No Public IP)

### Data Layer
- Amazon RDS PostgreSQL (Multi-AZ Deployment)
- Encrypted at Rest (KMS)

###  Object Storage
- Amazon S3 (Encrypted Storage)
- Private Access / Signed URLs

###  Security & Monitoring
- AWS IAM (Least Privilege Roles)
- AWS Secrets Manager
- AWS KMS (Encryption)
- Amazon CloudWatch (Logs & Metrics)

---

## Architecture Diagram

The architecture diagram is included in this repository:

-  `diagrams/architecture.svg`

---

## Design Considerations

The solution prioritizes:

- Multi-AZ resilience
- Defense-in-depth security
- TLS enforcement for all external traffic
- Infrastructure ready for automation (IaC-ready design)
- Clear separation of public and private resources

Future improvements may include:

- Infrastructure as Code (Terraform / CloudFormation)
- Read replicas or caching layer (Redis)
- Formal RTO/RPO disaster recovery strategy
- CI/CD pipeline integration with security scanning

---

## Author

KARLA YOFRACIEL AQUINO MERAN
