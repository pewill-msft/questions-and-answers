# WebJobs Monitoring

## How can I monitor the status of my WebJobs?
Two approaches to monitor continous webjobs are available:

1. [Enable Application Insights Logging](https://learn.microsoft.com/en-us/azure/app-service/webjobs-sdk-get-started#enable-application-insights-logging) in the WebJobs code to track exceptions and other telemetry. If the code is expected to perform tasks at a certain cadence a custom metric can be logged and monitored. For example, if a WebJob is expected to run every 5 minutes, a custom metric can be logged every time the WebJob runs. This metric can be monitored to ensure the WebJob is running as expected. 


2. Use the [Web Jobs API](https://github.com/projectkudu/kudu/wiki/WebJobs-API) to check status of continous jobs. This is helpful for high level monitoring of WebJobs status and can be used as a health check for the WebJobs. 

