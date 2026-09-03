AWS Jenkins SonarQube Nexus Infrastructure using Terraform
This project provisions DevOps infrastructure on AWS using Terraform.

The infrastructure includes separate EC2 servers for:

Jenkins - CI/CD automation
SonarQube - Code quality and security analysis
Nexus Repository - Artifact repository
Terraform is used to create and manage the required AWS infrastructure, including networking, IAM, security groups, EC2 instances, and server configuration.

Architecture
The infrastructure follows this workflow:

Developer | v GitHub | v Jenkins | +----> SonarQube | +----> OWASP Dependency-Check | v Maven Build | v Nexus Repository | v Docker | v Docker Hub | v Kubernetes

Infrastructure Components
AWS
VPC
Public Subnet
Internet Gateway
Route Table
Security Groups
IAM
EC2
DevOps Tools
Jenkins
SonarQube
Nexus Repository
OWASP Dependency-Check
Maven
Docker
Docker Hub
Kubernetes
Project Structure
aws-jenkins-sonarqube-nexus-terraform/
│
├── data.tf
├── iam.tf
├── main.tf
├── provider.tf
├── variable.tf
├── output.tf
│
├── jenkins-server.tf
├── sonar-server.tf
├── nexus-server.tf
│
├── jenkins-server.sh
├── sonar-server.sh
├── nexus-server.sh
│
├── README.md
├── .gitignore
└── .terraform.lock.hcl
