# 🚀 Automatic EC2 Shutdown using AWS Lambda

A serverless AWS automation project that automatically stops Amazon EC2 instances on a schedule using AWS Lambda and Amazon EventBridge to reduce unnecessary cloud costs.

---

# 📌 Problem Statement

In cloud environments, EC2 instances are often left running even when they are not being actively used. This leads to unnecessary AWS billing and inefficient resource utilization.

Manually stopping instances every day is repetitive and error-prone.

The goal of this project is to automate the shutdown process of EC2 instances using a serverless approach so that unused resources can be stopped automatically at scheduled times.

---

# 🎯 Objective

Build a serverless automation solution that:

- Automatically stops EC2 instances
- Runs on a scheduled time
- Requires no manual intervention
- Helps optimize AWS cloud costs
- Uses AWS managed services

---

# 🏗️ Architecture

+----------------------+
|  Amazon EventBridge  |
|   (Scheduled Rule)   |
+----------+-----------+
           |
           v
+----------------------+
|    AWS Lambda        |
|  (Python Function)   |
+----------+-----------+
           |
           v
+----------------------+
|    Amazon EC2        |
|   Stop Instance API  |
+----------------------+



🛠️ AWS Services Used


AWS Service	Purpose
Amazon EC2	Virtual machine instance
AWS Lambda	Executes automation logic
Amazon EventBridge	Triggers Lambda on schedule
IAM	Grants required permissions
CloudWatch Logs	Stores execution logs



⚙️ How the Project Works
Amazon EventBridge triggers the Lambda function based on a schedule.
Lambda executes Python code using Boto3.
The function calls the EC2 StopInstances API.
The EC2 instance changes from running to stopped.
Execution logs are stored in CloudWatch Logs.



🧪 Testing Steps
Launch an EC2 instance
Deploy the Lambda function
Attach IAM role with EC2 permissions
Create EventBridge scheduled rule
Trigger Lambda manually for testing
Verify EC2 state changes from:
running
to stopped
Check logs in CloudWatch


📚 Learning Outcomes

This project helped in understanding:

AWS Lambda automation
Serverless architecture
Amazon EC2 management
IAM roles and policies
EventBridge scheduling
CloudWatch monitoring
Boto3 AWS SDK usage



🌟 Key Benefits
Reduces AWS costs
Eliminates manual effort
Fully serverless solution
Easy to scale
Simple and lightweight architecture


👨‍💻 Author

DIVESH TAYADE
