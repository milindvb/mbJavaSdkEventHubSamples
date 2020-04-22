# Azure Event Hubs Java samples

Azure Event Hubs is a highly scalable data streaming platform and event ingestion service, capable of receiving and processing millions of events per second. The samples present here enables Java developers to easily ingest and process events from your event hub.

## Prerequisites

1.	The samples depend on the Java JDK 1.8 and are built using Maven. You can [download Maven](https://maven.apache.org/download.cgi). [Install and configure Maven](https://maven.apache.org/install.html). The sample require Maven version > 3.3.9. 
2.	You need an Azure Subscription, if you do not have one - create a [free account](https://azure.microsoft.com/free/?ref=microsoft.com&utm_source=microsoft.com&utm_medium=docs&utm_campaign=visualstudio) before you begin
3.	[An Event Hubs namespace and an event hub where you ingest the data](https://docs.microsoft.com/azure/event-hubs/event-hubs-create)
4.	[A SAS key to access the event hub](https://docs.microsoft.com/azure/event-hubs/event-hubs-create#SAS)

### Sending events

* **SimpleSend** - The [SimpleSend](./Basic/SimpleSend) sample illustrates how to ingest events into your event hub.
 
### Processing events

* **EventProcessorSample** - The [EventProcessorSample](./Basic/EventProcessorSample) sample illustrates how to receive events from an event hub using the event processor host, which provides automatic partition selection and fail-over across multiple concurrent receivers.

## Build and run

All samples can be built at once with

```bash
mvn clean package
```

The samples are dropped into the respective sample's ./target subfolder. The build packages all dependencies into a single assembly so that you can execute them with:

```bash
java -jar ./target/{project}-1.0.0-jar-with-dependencies.jar
```
