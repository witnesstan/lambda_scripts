This directory holds a Lambda function written in Python that do the following:

1. Look for files with a specific file "extension" in S3.
2. Compare their modification times and determine if they're "old" (stale).
3. When old files are found, an alert is pushed through AWS SNS.
4. The list of S3 bucket, paths, and file extensions are placed in a configuration file located in an S3 bucket. It can contain multiple lines and the Lambda function will go through each one.
