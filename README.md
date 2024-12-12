# 🌟 AWS Cloud Cost Optimization: Identifying and Deleting Stale EBS Snapshots

🚀 Overview
This project automates the detection and cleanup of stale EBS snapshots using AWS Lambda, helping you save on storage costs and maintain an efficient cloud environment.

✨ Features
🔄 Automated Cleanup: Identifies and deletes unused EBS snapshots effortlessly.
💰 Cost Optimization: Reduces unnecessary AWS storage expenses.
🔒 Policy-Driven Access: Ensures secure and controlled execution with the right IAM policies.

🛠️ Implementation Details

🧠 Lambda Function
The Lambda function, written in Python, follows these steps:

📋 Retrieve EBS Snapshots: Fetches all snapshots owned by your AWS account ('self').
📊 Check Active Instances: Retrieves the list of active EC2 instances (running and stopped).
🔍 Identify Stale Snapshots: Determines if the snapshot's associated volume is unused.
🗑️ Delete Stale Snapshots: Cleans up snapshots not linked to active resources.

🔑 IAM Policy
To ensure the Lambda function has the required permissions, attach an IAM role with these policies:

📜 ec2:DescribeSnapshots
📜 ec2:DescribeInstances
📜 ec2:DescribeVolumes
📜 ec2:DeleteSnapshot

📂 Example Code
The Python script for the Lambda function can be found in the lambda_function.py file in this repository.

🛴 Deployment Steps
🖥️ Create a new AWS Lambda function in your account.
🔗 Attach an IAM role with the necessary permissions.
📥 Upload the lambda_function.py script to your Lambda function.
⏰ Schedule the function using a trigger (e.g., CloudWatch Event) to run at desired intervals.

🌈 Benefits
💸 Cost Savings: Eliminates charges for unused EBS snapshots.
🧹 Improved Organization: Keeps your AWS environment clean and efficient.
⚡ Quick and Customizable: Easy to deploy and tailor to your specific needs.
