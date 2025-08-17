# Spring Projects

This repository contains a collection of Spring Boot and Spring Cloud projects, demonstrating various microservices patterns and concepts.

## Modules

The repository is organized into the following modules:

*   **GradleSpace**: A Gradle-based project that includes:
    *   A Spring Boot application with Spring Cloud's Eureka client.
    *   A simple REST controller.
    *   A collection of Java lambda expression examples.
    *   A Selenium test for web automation.

*   **springboot**: A Maven-based Spring Boot web application that showcases:
    *   WebSocket and STOMP messaging configurations.
    *   Server-Sent Events (SSE) implementation.
    *   Basic web controllers.

*   **SpringCloud**: A Gradle-based project demonstrating various Spring Cloud features, including:
    *   A Eureka server for service registration and discovery.
    *   A Feign client for declarative REST API calls.
    *   Hystrix for circuit breaking and fault tolerance.
    *   A consumer that interacts with other services.

*   **SpringCloudZuul**: A Gradle-based project that sets up a Zuul API Gateway. It includes:
    *   Pre, Post, Route, and Error filters for request lifecycle management.
    *   Integration with Eureka for dynamic routing.

*   **SpringConfigServer**: A Gradle-based project that provides centralized configuration management using Spring Cloud Config. It includes:
    *   A native configuration repository.
    *   Configuration files for different services and profiles.

## How to Run

Each module is a standalone project and can be run independently.

### Prerequisites

*   Java 8 or higher
*   Maven (for the `springboot` project)
*   Gradle (for the other projects)

### Running the Applications

1.  **SpringConfigServer**: Start this application first, as it provides the configuration for the other services.
2.  **SpringCloud (Eureka Server)**: Start the `AdminApplication` to enable service discovery.
3.  **GradleSpace (Client Server)**: Run the `CloudApplication`. This is a client that registers with Eureka.
4.  **SpringCloudZuul**: Start the `ZuulApplication` to enable the API Gateway.
5.  **springboot**: Run the `Application` class to start the web application.

You can then access the services through the Zuul API Gateway.
