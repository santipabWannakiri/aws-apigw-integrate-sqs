# aws-apigw-integrate-sqs
aws-apigw-integrate-sqs

[Set up REST API and an Amazon SQS integration](https://repost.aws/knowledge-center/api-gateway-rest-api-sqs-errors)

[AWS API Gateway with FIFO SQS](https://www.youtube.com/watch?v=dXa9KA-G9Dg)


[AWS SQS (Standard VS FIFO)](https://www.youtube.com/watch?v=DQLtW9_9HpA)

 ```
#set($dedupId = $context.requestId)
#set($groupId = $input.json('$.data.jobNumber'))
Action=SendMessage&MessageBody=$input.body&MessageGroupId=$groupId&MessageDeduplicationId=$dedupId
```
