# Brief Guide

## Create lambda and SQS queue

* Create a new Lambda in your AWS account
* Configuring a queue to use with Lambda
* Add lambda execution role permissions
* Configuring a queue as an event source
* `mvn clean package` and deploy your lambda code
* Test from console (or use [AWS SQS message producer](https://github.com/KostyantynPanchenko/aws-sqs-message-producer)))

```json
{
    "Records": [
        {
            "messageId": "11d6ee51-4cc7-4302-9e22-7cd8afdaadf5",
            "receiptHandle": "AQEBBX8nesZEXmkhsmZeyIE8iQAMig7qw...",
            "body": "Test message.",
            "attributes": {
                "ApproximateReceiveCount": "1",
                "SentTimestamp": "1573251510774",
                "SequenceNumber": "18849496460467696128",
                "MessageGroupId": "1",
                "SenderId": "AIDAIO23YVJENQZJOL4VO",
                "MessageDeduplicationId": "1",
                "ApproximateFirstReceiveTimestamp": "1573251510774"
            },
            "messageAttributes": {},
            "md5OfBody": "e4e68fb7bd0e697a0ae8f1bb342846b3",
            "eventSource": "aws:sqs",
            "eventSourceARN": "arn:aws:sqs:us-east-2:123456789012:fifo.fifo",
            "awsRegion": "us-east-2"
        }
    ]
}
```

## Useful info
* [Using Lambda with Amazon SQS](https://docs.aws.amazon.com/lambda/latest/dg/with-sqs.html)
* [jlib AWS Lambda SLF4J/Logback Appender](https://github.com/jlib-framework/jlib-awslambda-logback)
