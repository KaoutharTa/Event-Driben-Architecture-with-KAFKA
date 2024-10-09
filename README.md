# Report on Real-Time Data Processing with Kafka and Spring Cloud Streams

## Introduction
This report details the implementation of a real-time data processing application utilizing Apache Kafka, Spring Cloud Streams, and Docker. The objective of the project was to create a robust system comprising producer, consumer, supplier services, and a data analytics service. Additionally, a web application was developed to display real-time analytics results.

## Project Overview

### 1. Kafka Setup
The first phase of the project involved setting up Apache Kafka on a local machine. The following steps were undertaken:

- **Download and Install Kafka**: The latest version of Apache Kafka was obtained and installed.
- **Start Zookeeper**: The Zookeeper service, essential for managing Kafka brokers, was initialized.
- **Start Kafka Server**: The Kafka broker was launched, enabling the production and consumption of messages.
- **Testing**: Kafka's console producer and consumer tools were utilized to verify that messages could be sent and received successfully.

### 2. Docker Setup
To enhance portability and ease of deployment, Docker was used to containerize the Kafka and Zookeeper services. The process included:

- **Docker Integration**: Docker was utilized to manage the Kafka and Zookeeper services.
- **Docker Compose**: A `docker-compose.yml` file was created to define the necessary services and their configurations.
- **Start Containers**: The Zookeeper and Kafka broker containers were launched using Docker.
- **Testing**: The functionality was verified again using Kafka's console producer and consumer.

### 3. Spring Cloud Streams Implementation
The core functionality of the application was developed using Spring Cloud Streams, comprising the following services:

- **Kafka Producer Service**: A REST controller was created, allowing users to publish `PageEvent` messages to specified Kafka topics. An endpoint was defined for message publication.
- **Kafka Consumer Service**: This service was implemented to consume messages from Kafka topics and process them in real time using Kafka Streams.
- **Kafka Supplier Service**: An interface was developed to facilitate sending events to Kafka topics.
- **Data Analytics Service**: This service enabled real-time stream processing with Kafka Streams, allowing for the aggregation and analysis of `PageEvent` data.
- **Web Application**: A front-end application was built to display real-time analytics results from the stream processing service. Server-Sent Events (SSE) were utilized to provide live updates of analytics data.

## Technologies Used
The project employed a variety of technologies, including:
- **Apache Kafka**
- **Spring Cloud Streams**
- **Docker**
- **Java**
- **Maven**
- **HTML/CSS** (for the web application)


## Testing the Application
To test the application, Kafka console tools can be used to produce and consume messages.

## Docker Commands
The following commands can be used to manage the Docker containers:

- **Start the Services**: Launch the services defined in the `docker-compose.yml`.
- **Stop the Services**: Shut down the running services.

## Conclusion
This project successfully demonstrates the capabilities of Apache Kafka and Spring Cloud Streams for real-time data processing. Through the integration of Docker, the application achieves portability and ease of deployment. The implementation provides a solid foundation for further enhancements and scalability in real-time analytics.
