
**Identity and Access Management (IAM)**

1. Which of the following IAM policies grants least privilege for a user accessing an S3 bucket?
    - a) Allow full access to S3 bucket * (Incorrect - Grants too much access)
    - b) Allow read-only access to the S3 bucket and all objects (Correct)
    - c) Allow S3:ListBuckets and S3:GetObject for the specific bucket (More granular but may not be the least privilege)
    - d) Grant IAM user access to the IAM console (Incorrect - Doesn't grant access to S3 bucket)

2. What is the BEST practice for managing IAM user credentials?
    - a) Store them in plain text (Incorrect - Highly insecure)
    - b) Share them among developers (Incorrect - Increases risk)
    - c) Use temporary credentials with IAM roles (Correct)
    - d) Rotate passwords every year (While good practice, temporary credentials offer more granular control)

**Encryption**

3. Which service provides server-side encryption for data at rest by default?
    - a) Amazon S3 (Correct)
    - b) Amazon EC2 (Encryption needs to be manually configured)
    - c) Amazon DynamoDB (Encryption needs to be manually configured)
    - d) Amazon RDS (Encryption needs to be manually configured)

4. What is the benefit of using AWS Key Management Service (KMS) for encryption keys?
    - a) Automatic key rotation (Correct)
    - b) Increased storage capacity (Incorrect)
    - c) Reduced data transfer costs (Incorrect)
    - d) Improved data encryption algorithm (KMS supports various algorithms but doesn't dictate which one to use)

**Logging and Monitoring**

5. Which service continuously monitors your AWS resources for suspicious activity?
    - a) Amazon CloudWatch (Correct)
    - b) Amazon CloudTrail (Logs API calls but doesn't analyze for suspicious activity)
    - c) Amazon S3 (Storage service, not for monitoring)
    - d) Amazon IAM (For identity and access management, not continuous monitoring)

6. What is the purpose of a CloudWatch log group?
    - a) Define data retention policies (Correct)
    - b) Specify IAM permissions (Incorrect - Done through IAM policies)
    - c) Configure alarms for specific metrics (Done through CloudWatch alarms)
    - d) Encrypt log data (Encryption can be configured but not the primary purpose)

**Infrastructure Security**

7. Which security group rule allows all inbound traffic on port 22?
    - a) Allows all traffic from 0.0.0.0/0 on port 22 (Incorrect - Too permissive)
    - b) Allows SSH access from a specific IP address on port 22 (Correct)
    - c) Denies all inbound traffic on port 22 (Too restrictive)
    - d) Allows inbound traffic from the internet on port 22 (Less secure than a specific IP)

8. What is the benefit of using Amazon VPC endpoints for S3 access?
    - a) Reduced data transfer costs (Incorrect)
    - b) Improved data encryption (Encryption can be used but not the primary benefit of VPC endpoints)
    - c) Increased data throughput (Incorrect)
    - d) Prevents data exfiltration to the public internet (Correct)

**Data Protection**

9. Which service helps classify and protect sensitive data in S3 buckets?
    - a) Amazon S3 Object Lock (Protects against accidental deletion)
    - b) Amazon Macie (Correct)
    - c) AWS CloudTrail (Logs API calls, not for data classification)
    - d) Amazon Kinesis (Data streaming service, not for data protection)

10. How can AWS WAF be used to protect against SQL injection attacks?
    - a) By blocking specific IP addresses (Limited effectiveness) 
    - b) By using a web application firewall rule that matches malicious SQL patterns (Correct)
    - c) By encrypting data at rest (Encryption is important but doesn't address SQL injection)
    - d) By using strong IAM policies (IAM controls access, not specific attack vectors)

**Security best practices**

11. Which of the following principles is the foundation of the AWS shared responsibility model?
    - a) AWS manages security of the customer's application data. (Incorrect - Customer responsibility)
    - b) Customer manages security of the physical infrastructure. (Incorrect - AWS responsibility)
    - c) AWS manages security of the underlying cloud infrastructure. (AWS responsibility)
    - d) Customer is responsible for security of their applications and data in the cloud. (Correct)

12. What is the MOST SECURE way to store an IAM user's access key?
    - a) In a browser extension (Highly insecure)
    - b) In a text file on the user's desktop (Insecure)
    - c) In an environment variable (Less secure than secrets manager)
    - d) In AWS Secrets Manager (Correct)

**IAM Roles and Policies**

13. Which of the following is NOT a valid IAM permission boundary?
    - a) A managed IAM policy (Correct)
    - b) An AWS Organizations policy (Can be used as a boundary)
    - c) A customer-managed IAM policy (Can be used as a boundary)
    - d) An IAM role (Roles can be used as boundaries)  

14. What happens when you attach an IAM policy with read-only access to an S3 bucket and another policy with full access?
    - a) The most permissive policy takes effect (Correct - Principle of least privilege not enforced)
    - b) An error occurs due to conflicting permissions (Not necessarily)
    - c) IAM merges the permissions from both policies (Policies are evaluated in order attached)
    - d) Only the read-only policy applies (Least privilege not enforced)

**Encryption**

15. Which AWS service encrypts data in transit by default?
    - a) Amazon S3 (Encryption needs to be configured)
    - b) Amazon EC2 (Data in transit encryption needs to be configured)
    - c) Amazon SQS (Messages are encrypted at rest by default)
    - d) Amazon Kinesis (Encryption needs to be configured)

16. What is the difference between AWS Key Management Service (KMS) and AWS Secrets Manager?
    - a) KMS is for encryption keys, Secrets Manager is for general secrets (Correct)
    - b) KMS is for user credentials, Secrets Manager is for encryption keys (Incorrect)
    - c) Both services do the same thing (Incorrect)
    - d) Secrets Manager is a type of KMS key (Incorrect)

**Logging and Monitoring**

17. What type of CloudWatch logs can be used to troubleshoot issues with AWS Lambda functions?
    - a) CloudTrail logs (Logs API calls, not specific to Lambda)
    - b) Amazon S3 access logs (Not specific to Lambda)
    - c) CloudWatch Logs from Lambda functions (Correct)
    - d) Amazon VPC flow logs (Not specific to Lambda)

18. How can you configure CloudWatch alarms to trigger automated remediation actions?
    - a) By defining Lambda functions as actions for the alarms (Correct)
    - b) By integrating CloudWatch with Amazon SNS (Notifications only, not remediation)
    - c) By setting up email notifications for alarms (Notifications only, not remediation)
    - d) There is no way to automate remediation actions with CloudWatch alarms (Incorrect)

**Network Security**

19. What is the purpose of a security group in a VPC?
    - a) To define routing rules for traffic (Route tables handle routing) 
    - b) To control inbound and outbound traffic to network interfaces (Correct)
    - c) To create a private subnet within a VPC (Subnet creation is a VPC concept)
    - d) To manage IAM user permissions (IAM controls access, not network traffic)

20. How can AWS WAF be used to protect against DDoS attacks?
    - a) By blocking specific IP addresses (Limited effectiveness)
    - b) By using rate limiting rules (Effective against DDoS attacks)
    - c) By filtering malicious traffic patterns (Can be helpful)
    - d) All of the above (Correct)

**Disaster Recovery**

21. Which AWS service can be used to replicate data across Availability Zones for disaster recovery?
    - a) Amazon S3 (Versioning provides some recovery options but not true replication)
    - b) Amazon EBS (Can be used for backups but not real-time replication)
    - c) Amazon RDS with Multi-AZ deployment (Correct)
    - d) Amazon
   
  22. Which AWS service allows you to define infrastructure as code?
    - a) Amazon EC2 (Provisions EC2 instances, not for entire infrastructure)
    - b) Amazon S3 (Storage service, not for infrastructure)
    - c) AWS CloudFormation (Correct)
    - d) Amazon CloudWatch (Monitoring service, not for infrastructure)

23. What is the benefit of using AWS Config for security?
    - a) Encrypts data at rest (Encryption is a separate service)
    - b) Provides continuous security monitoring (Similar to CloudWatch, but focuses on configuration changes)
    - c) Manages IAM user credentials (IAM handles credentials)
    - d) Enables serverless computing (Not related to security)  

24. What is the AWS service that helps you perform vulnerability assessments on your workloads?
    - a) Amazon Inspector (Correct)
    - b) AWS Security Token Service (Provides temporary credentials)
    - c) Amazon CloudTrail (Logs API calls, not for vulnerability assessment)
    - d) Amazon GuardDuty (Threat detection service, not for manual assessments)

25. What is the purpose of AWS CloudTrail?
    - a) To encrypt data at rest (Encryption is a separate service)
    - b) To monitor resource utilization (CloudWatch handles this)
    - c) To record API calls made to AWS services (Correct)
    - d) To manage IAM user roles (IAM handles roles)

26. What is the difference between AWS Identity and Access Management (IAM) and AWS Organizations?
    - a) IAM manages users and roles within an account, Organizations manages accounts within an organization (Correct)
    - b) IAM defines security groups, Organizations defines VPCs (Incorrect - Both unrelated)
    - c) IAM encrypts data, Organizations manages access (Incorrect - Functions are different)
    - d) There is no difference, they do the same thing (Incorrect)

27. What is the MOST SECURE way to grant temporary access to an AWS resource?
    - a) By sharing an IAM user's credentials (Insecure)
    - b) By creating a long-lived IAM user access key (Less secure)
    - c) By using AWS STS to assume a role with temporary credentials (Correct)
    - d) By granting public access to the resource (Highly insecure)

28. Which AWS service can be used to manage secrets like database passwords securely?
    - a) Amazon S3 (Can store secrets but not manage them securely)
    - b) AWS Secrets Manager (Correct)
    - c) Amazon CloudTrail (Logs API calls, not for secrets management)
    - d) IAM user policies (Policies define permissions, not manage secrets)

29. What is the purpose of AWS Kinesis Firehose?
    - a) To store data objects in S3 (S3 stores data, Firehose delivers it)
    - b) To analyze large datasets in real-time (Kinesis Analytics is for analysis)
    - c) To deliver real-time streaming data to destinations like S3 or Elasticsearch (Correct)
    - d) To encrypt data at rest (Encryption is a separate service)

30. What is the benefit of using AWS CloudHSM for encryption keys?
    - a) Reduced storage costs (Incorrect)
    - b) Increased data transfer speeds (Incorrect)
    - c) Enhanced key management security through dedicated hardware modules (Correct)
    - d) Easier integration with IAM roles (Not the primary benefit)

Remember, these are just examples, and the actual exam may have different content and formats. Refer to official AWS resources for the most up-to-date information.
