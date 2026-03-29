# AWS Auto Scaling Web Application

### ðŸŒ Highly Available â€¢ Scalable â€¢ Production-Ready Cloud Architecture

This project showcases the design and deployment of a **fault-tolerant and auto-scalable web application** on AWS using industry-standard cloud architecture patterns.

It simulates a **real-world production environment** capable of handling variable traffic loads while ensuring **high availability, performance, and security**.

---

## ðŸ“Œ ðŸ“– Project Overview

Modern applications must handle unpredictable traffic while maintaining uptime.
This project solves that by implementing:

* ðŸ”„ **Auto Scaling Infrastructure**
* âš–ï¸ **Load Balancing Across Instances**
* ðŸŒ **Multi-AZ High Availability**
* ðŸ” **Secure Networking via VPC**

---

## ðŸ—ï¸ Architecture Components

### ðŸ”¹ VPC (Virtual Private Cloud)

* Custom CIDR block for isolation
* Public subnets for ALB
* Private subnets for EC2 instances
* Route tables and Internet Gateway configured

### ðŸ”¹ Application Load Balancer (ALB)

* Layer 7 load balancing (HTTP/HTTPS)
* Intelligent request routing
* Health checks to ensure only healthy instances serve traffic

### ðŸ”¹ Auto Scaling Group (ASG)

* Dynamic scaling based on demand
* Maintains minimum, desired, and maximum capacity
* Automatic instance replacement (self-healing)

### ðŸ”¹ EC2 Instances

* Deployed using Launch Template
* Pre-configured web server (e.g., Nginx/Node.js)

---

## ðŸ“Š Architecture Diagram

```
            Internet
                â”‚
         â”Œâ”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”
         â”‚     ALB     â”‚
         â””â”€â”€â”€â”€â”€â”¬â”€â”€â”€â”€â”€â”€â”€â”˜
               â”‚
     â”Œâ”€â”€â”€â”€â”€â”€â”€â”€â”€â”´â”€â”€â”€â”€â”€â”€â”€â”€â”€â”
     â”‚                   â”‚
 â”Œâ”€â”€â”€â”€â”€â”€â”€â”          â”Œâ”€â”€â”€â”€â”€â”€â”€â”
 â”‚ EC2   â”‚          â”‚ EC2   â”‚
 â”‚ (AZ1) â”‚          â”‚ (AZ2) â”‚
 â””â”€â”€â”€â”€â”€â”€â”€â”˜          â””â”€â”€â”€â”€â”€â”€â”€â”˜
     â”‚                   â”‚
     â””â”€â”€â”€â”€â”€â”€ Auto Scaling â”€â”€â”€â”€â”€â”€â”˜
```

---

## âš™ï¸ Key Features

âœ… High Availability across multiple AZs
âœ… Elastic scaling based on traffic
âœ… Zero downtime deployment capability
âœ… Health monitoring & auto recovery
âœ… Secure VPC-based network architecture

---

## ðŸ“ˆ Performance & Scalability

* ðŸš€ Automatically scales out during high traffic
* ðŸ’¸ Scales in during low usage to reduce cost
* âš¡ Improves response time with load balancing
* ðŸ“Š Ensures consistent performance under load

---

## ðŸ›¡ï¸ Security Best Practices

* ðŸ” Security Groups for controlled access
* ðŸŒ Private subnets for backend instances
* ðŸš« No direct public access to EC2
* ðŸ”‘ IAM roles for secure AWS service interaction

---

## ðŸ“Š Monitoring & Logging

* ðŸ“ˆ AWS CloudWatch for metrics & alarms
* ðŸ“œ Logs for debugging and performance tracking
* ðŸš¨ Alerts for unusual activity or failures

---

## ðŸ› ï¸ Tech Stack

* â˜ï¸ AWS EC2
* âš–ï¸ AWS Application Load Balancer
* ðŸ“ˆ AWS Auto Scaling
* ðŸŒ AWS VPC
* ðŸ” IAM & Security Groups
* ðŸ“Š AWS CloudWatch

---

## ðŸš€ Deployment Steps

1. Create a custom VPC with subnets
2. Configure Internet Gateway & routing
3. Launch EC2 instances / create Launch Template
4. Set up Application Load Balancer
5. Configure Target Group & Health Checks
6. Create Auto Scaling Group
7. Attach ALB to ASG
8. Test scaling with simulated traffic

---

## ??? Frontend Overview

The `frontend/index.html` file now delivers the dashboard that powers the user experience in this repo. It reads from `/instance` and renders thematic cards for hostname, scaling status, CPU utilization, RPS, latency, and desired capacity, plus:

* A Live Timeline of autoscaling signals that rotates every few seconds.
* AWS-focused highlight tiles covering Auto Scaling Group, ALB, VPC/networking, and monitoring.
* A control panel with a slider, notification banner, and theme picker (Night Mode, Sunset Glow, Light/Paper, and Simple Light).

## ?? Running Locally

1. `cd backend && npm install` (once) to install dependencies.
2. Run `npm start` so Express serves the `/instance`, `/health`, and the static frontend from `http://localhost:3000`.
3. Open the browser, click “Check Instance,” tweak the slider if desired, and switch themes to see the palettes.## ðŸ“· Demo / Screenshots

> Add screenshots of:

* ALB dashboard
* EC2 instances
* Auto Scaling activity
* CloudWatch metrics

---

## ðŸ“ˆ Real-World Use Cases

* ðŸŒ High-traffic web applications
* ðŸ›’ E-commerce platforms
* ðŸ“± SaaS products
* ðŸš€ Startup production systems

---

## ðŸ’¡ Future Enhancements

* ðŸ” Add HTTPS using AWS ACM
* ðŸ—„ï¸ Integrate RDS (MySQL/PostgreSQL)
* âš¡ Add caching with Redis / ElastiCache
* ðŸ”„ CI/CD pipeline using GitHub Actions / AWS CodePipeline
* ðŸŒ Deploy using Infrastructure as Code (Terraform / CloudFormation)

---

## ðŸ¤ Contributing

Contributions are welcome!

If you'd like to improve this project:

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Open a Pull Request

---

## ðŸ’¬ Support

If you have any questions, suggestions, or issues:

* ðŸ“© Open an issue in this repository
* ðŸ’¡ Reach out via GitHub

If you found this project helpful:

ðŸ‘‰ Give it a â­ on GitHub â€” it really helps!

---

## ðŸ‘¨â€ðŸ’» Author

**Tanay Sasane**
ðŸ’¼ Aspiring Cloud & DevOps Engineer
ðŸ”— GitHub: https://github.com/TanaySasane

---

## ðŸ§¾ Conclusion

This project demonstrates how to design a **scalable, resilient, and production-ready cloud architecture** using AWS.

By leveraging services like **Auto Scaling and Application Load Balancer**, the system can:

* Handle real-world traffic efficiently
* Maintain high uptime
* Optimize cost through dynamic scaling

It reflects key **Cloud & DevOps engineering principles**, making it a strong foundation for deploying modern applications in the cloud.

---

â­ *Built with a focus on scalability, reliability, and real-world cloud practices.*

