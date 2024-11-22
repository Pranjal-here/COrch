# COrch
Project Title: Compliance orchestrator
Description:
This project provides an automated solution for monitoring, analyzing, and notifying companies about regulatory updates relevant to their industry. It uses various AWS services to efficiently scrape regulatory websites, classify text content, match relevant updates with company profiles, and send notifications to impacted companies, ensuring they stay compliant with the latest regulations.
---
### Project Overview
Industry regulations change frequently, posing challenges for companies that must stay compliant. Our Automated Regulatory Compliance System addresses these challenges by automating the process of monitoring regulatory changes, classifying and understanding their implications, and informing the relevant companies about updates.
### Architecture
1. Data Storage:
   - Amazon RDS: Stores company data including name, industry, and relevant tags.
2. Web Scraping:
   - AWS Lambda: Periodically scrapes websites of regulatory bodies like RBI and FSSAI.
3. Document Storage:
   - Amazon S3: Stores scraped documents for further processing.
4. Text Analysis:
   - Amazon Comprehend & Bedrock: For training and deploying text classification models to analyze and tag scraped content.
5. Matching and Notification:
   - AWS Lambda: Matches updates with company tags and triggers notifications.
   - Amazon SES: Sends notifications to impacted companies.
6. Orchestration:
   - AWS StepFunctions: To orchestrate the entire flow and support retries.
### Features
- Automated Web Scraping: Collects data from specified regulatory websites without manual intervention.
- Intelligent Text Classification: Uses machine learning for processing and analyzing text data.
- Efficient Tag Matching: Identifies relevant updates for companies based on stored tags.
- Timely Notifications: Notifies companies of pertinent regulatory changes.
### AWS Services Utilized
- Amazon DocumentDB
- AWS Lambda
- Amazon S3
- Amazon Comprehend
- Amazon Bedrock
- Amazon SES
- Amazon StepFunction
- Amazon CloudWatch
### Setup Instructions
1. Prerequisites:
   - AWS Account with proper permissions to access the services mentioned above.
   - AWS CLI configured for your AWS account.
2. Deployment Steps:
   - Deploy the AWS Lambda functions for web scraping, text classification, and tag matching using AWS SAM or another IAC tool.
   - Configure Amazon DocumentDB to store company data.
   - Set up Amazon S3 buckets to store scraped documents.
   - Train and deploy machine learning models using Amazon SageMaker or incorporate pre-trained models using Amazon Bedrock.
   - Configure Amazon SNS for notifications.
3. Configuration:
   - Update configuration files with appropriate IAM roles and permissions for each AWS service.
### Usage
- Start Script: Use AWS Lambda invocations to manage the workflow from scraping to notification.
- Logging and Monitoring: Use Amazon CloudWatch for logs and metrics to monitor the system.
### Contributing
No contributions to this projects!
---