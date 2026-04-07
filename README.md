🚀 Automated CI/CD Pipeline for Node.js on AWS
📌 Project Overview
This project demonstrates a complete End-to-End DevOps Pipeline for a Node.js web application. It automates the process of fetching code from GitHub, building a Docker image, and deploying it to an AWS EC2 instance using Jenkins.

Key Features:
Continuous Integration: Automated build and image creation upon code push.

Continuous Deployment: Seamless deployment to AWS EC2 using Docker containers.

Infrastructure: AWS EC2 instance configured with Security Groups for HTTP/SSH access.

Containerization: Environment-agnostic deployment using optimized Dockerfiles.

🏗 Architecture
Developer pushes code to the GitHub repository.

Jenkins (running on EC2) detects the change (via Webhook or Polling).

Jenkins executes the Jenkinsfile (or Freestyle steps):

Clones the repository.

Builds a Docker Image from the source code.

Stops/Removes existing containers to avoid conflicts.

Runs the new Docker Container on the EC2 instance.

The application becomes accessible via the EC2 Public IP.

🛠 Tech Stack
Source Control: Git & GitHub

CI/CD Tool: Jenkins

Containerization: Docker

Cloud Provider: Amazon Web Services (AWS EC2)

Runtime: Node.js

OS: Linux (Ubuntu/Amazon Linux 2)

🚀 Getting Started
1. Prerequisites
An AWS Account with an EC2 instance running.

Security Groups configured to allow ports: 8080 (Jenkins), 22 (SSH), and your app port (e.g., 3000).

Jenkins and Docker installed on the EC2 instance.

2. Installation & Setup
Clone the repository:

Bash

git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
Configure Jenkins:

Create a new Freestyle project or Pipeline.

Link your GitHub repository URL.

Add the build steps (or use the provided Jenkinsfile).
