# Overview
This is a [mu](https://github.com/stelligent/mu) extension to add the Datadog agent to all ECS services.

# Prerequisites
You need an API key from Datadog.  If you are not currently a customer, then [signup!](https://www.datadoghq.com/aws-signup/)

Once you have the key, you need to put it into an SSM parameter for CloudFormation to access:

```
aws ssm put-parameter --name DatadogApiKey --type String --value xxxxxxxx
```

# Adding to mu
To use, add the following to your mu.yml:


```
extensions:
- url: https://github.com/stelligent/mu-datadog/archive/v0.1.zip
```