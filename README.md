# DevOps 
Docker and Route 53

Objective : Deploy a Multi-Region Application with Docker and AWS Route 53
Procedure:
  1. Create Docker images for the application and push them to ECR.
  2. Set up EC2 instances in multiple AWS regions.
  3. Deploy the Docker containers in each region.
  4. Configure Route 53 for DNS failover and latency-based routing.
  5. Test the multi-region setup and handle failover scenarios.

1. Create Docker Images and Push to ECR
  -Build Docker Images:
  -Create a Dockerfile for your application.

2. Docker build tool to create the image.
   -Tag the image with a repository name and tag, e.g., your-image:latest.
   -Authenticate to ECR.
   -Push the tagged image to your ECR repository.

2. Setting Up EC2 Instances in Multiple AWS Regions
  -Create EC2 Instances. (in different regions)

3. Deploy Docker Containers in Each Region
  -Install Docker on the EC2 instances.
  -Pull the Docker image from your ECR repository to each instance.
   -Use docker run or Docker Compose to start the containers.

4. Configure Route 53 for DNS Failover and Latency-Based Routing
  -Create a hosted zone for your domain in Route 53.
  -Create A records for each region's EC2 instance public IP address.
  -Use Route 53's failover and latency-based routing policies.

TOOLS USED-
Docker: For packaging your application and running it in containers.
AWS ECR: For storing your Docker images.
AWS EC2: For hosting your application in multiple regions.
AWS Route 53: For managing your domain name and routing traffic.

OVERALL GOAL-
The end result is a distributed application that can handle failures and provide low latency to users around the world.

![image](https://github.com/user-attachments/assets/dea89f2d-63b7-42e1-9c3c-19a6bf2640ae)

