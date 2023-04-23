# AWS Compliance Check for S3 Buckets
This code is an AWS Lambda function that checks the compliance of S3 buckets against a specific set of requirements. It checks each S3 bucket in the account against the following requirements:

## The bucket has a website configuration
Default encryption is enabled
Versioning is enabled
Public access is blocked
Logging is enabled
For each bucket that does not meet these requirements, the function outputs a message to the Lambda logs with the bucket name and the specific compliance issue.

## Getting Started
To use this function, you'll need an AWS account and the AWS CLI installed on your local machine. Here are the steps to get started:

Clone or download the code from this repository.
Open a command prompt or terminal window and navigate to the directory where the code is saved.
Run the following command to create a new AWS Lambda function:


Make sure to replace 123456789012 with your AWS account number and lambda-role with the name of an IAM role that has permissions to list and read S3 buckets.

Create a CloudWatch Events rule to schedule the function to run on a regular basis (e.g., daily or weekly). You can do this using the AWS Management Console or the AWS CLI. Here's an example CLI command to create a new rule:


This will create a new CloudWatch Events rule that runs the function every day at 9:00 AM UTC.

Finally, add a target to the rule that invokes the Lambda function. You can do this using the AWS Management Console or the AWS CLI. Here's an example CLI command to add a target:

Make sure to replace 123456789012 with your AWS account number and s3-compliance-check with the name of the Lambda function you created in step 3.

That's it! The function will now run on a regular basis and check the compliance of your S3 buckets.

## Viewing Results
To view the results of the compliance check, you can view the Lambda logs in the AWS Management Console or using the AWS CLI. Here's an example CLI command to view the logs:

## Conclusion
This AWS compliance check function helps ensure that your S3 buckets meet a specific set of requirements for security and compliance. By running this function on a regular basis, you can stay on top of any compliance issues and take action to address them.