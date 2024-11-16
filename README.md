# Spring Boot Kafka Producer

This project demonstrates a **Kafka Producer** application using **Spring Boot**. It enables sending messages to Kafka topics, showcasing an easy integration with Apache Kafka for distributed messaging.

## Features

- **Spring Boot Integration**: Uses Spring Boot for streamlined configuration and management.
- **Kafka Producer**: Sends messages to specified Kafka topics.
- **JSON Support**: Serializes messages into JSON for easy compatibility.
- **Configurable Topics**: Kafka topics are configurable via application properties.

## Prerequisites

- **Java 21** or higher
- **Apache Kafka**: A running Kafka instance
- **Maven**: For dependency management

## Configuration

The `application.yml` with Kafka details:

```yaml
spring:
  kafka:
    bootstrap-servers: localhost:9092
    producer:
      key-serializer: org.apache.kafka.common.serialization.StringSerializer
      value-serializer: org.apache.kafka.common.serialization.StringSerializer
```
## How It Works
- The producer publishes messages directly to the Kafka topic.
- Future use cases can include integrating APIs, using event triggers, or connecting to databases.
- Kafka consumers read the messages from the topic for further processing.

## Running the Application
1. Start the Kafka broker and Zookeeper.
2. Build and run the application

### Starting kafka broker and zookeeper
- Start docker cli or docker desktop to run the docker daemon
- Run following command in docker folder of the project to pull kafka and zookeeper images and run them with configuration in `docker-compose.yml`
```yml
docker-compose up -d
```

### Running Spring Boot Application
Start application by running directly from the Application class.

### Setup Offset Explorer 

- Install offset explorer to visualize the data sent from producer.
- Download offset explorer from [here](https://www.kafkatool.com/download.html).
- Setup Offset Explorer by providing the host information.
- In our case it is `localhost:29092`
- Now, we can visualize the data sent to apache kafka.


