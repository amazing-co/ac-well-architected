# well-architected

Architecture framewwork based on [AWS Well-Architected](https://aws.amazon.com/architecture/well-architected/)

---

## 1. Operational Excellence
The operational excellence pillar focuses on running and monitoring systems to deliver business value, and continually improving processes and procedures. Key topics include managing and automating changes, responding to events, and defining standards to successfully manage daily operations.

* Infrastructure as code - CloudFormation, Terraform, Ansible
* Perform operations as code - Bash files
* Monitoring - CloudWatch, CloudTrail
* CI/CD - Packer, Jenkins, Buildkite, CircleCI, Ansible, Bamboo, Octopus
* Disaster Recovery
* Playbooks/RunBooks
* Game days - ChaosMonkey

## 2. Security
The security pillar focuses on protecting information & systems. Key topics include confidentiality and integrity of data, identifying and managing who can do what with privilege management, protecting systems, and establishing controls to detect security events. 

* Create account programatically
* IAM
* ConfigFiles & System Manager/Parameter Store
* Alerts - CloudWatch, CloudTrail, GuardDuty
* Apply security at all layers - VPC, CloudFront, AWS Shield(DDos), WAF, Security groups
    - Everything in VPC
    - Public Subnet: ELB
    - Private Subnet 1: ECS/Services
    - Private Subnet 2: Databases
* Data classification - High/Low
* Protect data at rest - KMS
* Protect data in transit - TLS, encoded/encryption/tokenisation
* Keep people away from data
* Separate AWS instances

## 3. Reliability
The reliability pillar focuses on the ability to prevent, and quickly recover from failures to meet business and customer demand. Key topics include foundational elements around setup, cross project requirements, recovery planning, and how we handle change.

* Automatically recover from failures - SQS/Lambda retries
* Scale horizontally to increase aggregate system availability - Small instances, Auto-scalling group
* Multi Avilability Zones
* Self healing

## 4. Performance Efficiency
The performance efficiency pillar focuses on using IT and computing resources efficiently. Key topics include selecting the right resource types and sizes based on workload requirements, monitoring performance, and making informed decisions to maintain efficiency as business needs evolve.

* Right tool for the right project
* Democratize advanced technologies - NoSQL, Media transcoding, Machine learning
* Go global in minutes
* Instances(SSDs and GPUs): ECS/EKS for services(Flexibility/Portability) and Serverless for simpler services
* Experiment more often
* Consult with experts
* Storage - CAP, Latency, Durability, Scalability and Query Capability
* Caching - ElasticCache
* CDN - CloudFront
* Route53 - Latency based routing


## 5. Cost Optimisation
Cost Optimisation focuses on avoiding un-needed costs. Key topics include understanding and controlling where money is being spent, selecting the most appropriate and right number of resource types, analysing spend over time, and scaling to meet business needs without overspending.

* CAPEX vs OPEX
* Machine instances
* On Demand + Spot instances
* Metrics based scaling: CloudWatch Alarm/Alarm, AutoScaling group 
