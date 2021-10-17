This template creates an SNS topic for publishing the messages(MySNSTopic) with type as SQS.
SQS queue (MyQueue) is created as an consumer for the messages published by the SNS topic by creating QueuePolicy.
Whenver the messages are received by SQS an lambda execution(LambdaFunction) will be triggered.
These lambda executions will then push these messages to the S3 bucket (MyS3Bucket).
S3 bucket is created with version and lifecycle policies enabled.
Appropriate permissions(logs , S3-bucket) is created for the lambda execution.
