AWS three-tier web architecture 


 Prerequisites

Before getting started, ensure you have the following:

1. AWS Account: If you don’t have one, [create an AWS account](https://aws.amazon.com/console/).

2. IDE/Text Editor: Use any text editor or IDE of your choice, such as Visual Studio Code or IntelliJ IDEA.

3. Basic AWS Knowledge: Familiarity with AWS services like VPC, EC2, RDS, S3, and ELB is recommended to get the most out of this project.

 Overview

In this project, we implement a three-tier web architecture on AWS that is robust and scalable. The architecture is designed to efficiently manage traffic, secure data, and ensure high availability across all tiers. A scalable web application can be run in a production environment by configuring the network, security, application, and database layers manually.

Architecture Breakdown

The architecture is composed of three main layers:

- Web Tier: This layer handles incoming client traffic through a public-facing Application Load Balancer (ALB). Requests go to EC2 instances with Nginx servers, which show the React.js frontend. API requests are sent to an internal load balancer, which then sends them to the application tier.

- Application Tier: The application tier is powered by Node.js, handling business logic and processing API requests. Data is returned to the web tier after being processed by this tier, which interacts with the database layer. EC2 instances are distributed across multiple internal load balancers to ensure redundancy and scalability.





- Database Tier: Database Tier: This layer is made up of a multi-AZ-deployed Amazon Aurora MySQL database. High availability and data integrity are ensured by the database tier's ability to manage data storage, retrieval, and manipulation.Database Tier: This layer is made up of a multi-AZ-deployed Amazon Aurora MySQL database.The database setup keeps your data available and secure, handling storage and access smoothly.


Auto-scaling groups, load balancing, and health checks are built into every layer to ensure the architecture's availability and performance.


 Key Features

- Scalability: Auto Scaling is set up at every tier to manage different loads, making sure the system can adjust to sudden increases in traffic.

- Security:To isolate and safeguard all of the application levels, the architecture makes use of security groups, subnets, and VPCs.


- High Availability: The application is kept up to date even in the event of failures thanks to the utilization of load balancers and multi-AZ deployments.


 Architecture Diagram

![fdd](https://github.com/user-attachments/assets/ef932648-d66a-4f77-b366-2754b7017375)

Project Walkthrough

This section provides a step-by-step guide on how to set up the three-tier architecture:

1. VPC and Subnet Configuration: Set up a Virtual Private Cloud (VPC) with public and private subnets across multiple Availability Zones.

2. Security Groups: Configure security groups to control traffic between the web, application, and database tiers.

3. EC2 Instances: Launch EC2 instances in the web and application tiers, with the necessary configurations for Nginx and Node.js.

4. Load Balancers: Set up both the public ALB for the web tier and the internal ALB for the application tier.

5. Database Setup: Create an Aurora MySQL database with multi-AZ deployment in the private subnets.

6. Auto Scaling: Configure Auto Scaling groups to automatically adjust the number of EC2 instances based on traffic.

Key Learnings and Insights

I developed a greater awareness of the design and implementation of scalable, secure, and high-availability architectures in AWS during this assignment. My understanding of fundamental AWS services and best practices for cloud architecture design have been strengthened by my practical experience with manual configuration.



The AWS Three-Tier Web Architecture project showcases the fundamental elements and setups needed to implement a dependable and expandable web application. The project highlights the value of scalability, security, and high availability in present-day cloud infrastructures through meticulous design and implementation.

