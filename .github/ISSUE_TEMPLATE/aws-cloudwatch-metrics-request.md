---
name: AWS CloudWatch metrics request
about: Request enabling metrics export to AWS CloudWatch
title: "[METRICS REQUEST]"
labels: ''
assignees: ''

---

**Please provide your Momento customer-id (usually your email address)**
e.g. foo@bar.com

**Please provide your AWS account id**
123456789

We have the capability to export metrics to our customer's AWS accounts via CloudWatch. Specifically, we can emit metrics for Requests, Hits, Misses, Errors, Latency, Bytes for our APIs. Customers can then create dashboards to get insights into how their requests are performing with Momento. For example, some customers may monitor bytes to get an idea of how much data is being sent to Momento etc.

- You need to log into your AWS account to create a `MomentoMetricsExporterRole` with `PutMetricDataPermissions` for Cloudwatch namespace `Momento/Metrics`. You can do this by clicking [this stack creation link](https://console.aws.amazon.com/cloudformation/home?region=us-west-2#/stacks/create/review?stackName=momento-metrics-exporter-role&templateURL=https://momento-public-resources-us-west-2.s3.us-west-2.amazonaws.com/momento_metrics_exporter_stack.template.json).
