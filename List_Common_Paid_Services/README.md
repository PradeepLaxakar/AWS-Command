# AWS Chargeable Resources Checker

## Overview
This Bash script scans all AWS regions and lists chargeable AWS resources in each region. It helps in identifying active resources that might incur costs, aiding in cost optimization and management.

## Features
- Scans all AWS regions automatically.
- Lists chargeable resources such as:
  - EC2 Instances
  - RDS Instances
  - Lambda Functions with provisioned concurrency
  - ECS Clusters
  - EKS Clusters
  - Load Balancers
  - Elastic IPs
  - CloudFormation Stacks
  - SNS Topics
  - SQS Queues
  - EBS Volumes
  - S3 Buckets (global)

## Prerequisites
- AWS CLI must be installed and configured with the necessary permissions.
- Bash shell environment.

## Usage
1. Clone the repository or copy the script to your local system.
2. Ensure AWS CLI is installed and authenticated.
3. Run the script:
   ```bash
   chmod +x aws-resource-checker.sh
   ./aws-resource-checker.sh
   ```

## Output
The script will iterate through all AWS regions and list active chargeable resources in each region. It will also display globally chargeable resources such as S3 buckets.

## Notes
- This script requires `aws configure` to be set up with valid credentials.
- Ensure your AWS IAM user has `Describe` and `List` permissions for all relevant AWS services.
- The script only lists resources and does not modify or delete any.

## License
This project is licensed under the MIT License.

## Author
Maintained by [Your Name].

