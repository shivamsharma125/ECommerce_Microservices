# 🛒 E-Commerce Microservices Project

Welcome to the **E-Commerce Microservices Project** – a robust, scalable, and modular system built using **Spring Boot** and following modern **microservices principles**. This repository serves as the central entry point for all microservices that make up the project.

Each microservice is maintained in a separate repository and is independently deployable and testable. This architecture enables high scalability, maintainability, and clear separation of concerns.

---

## 🧹 Microservices Overview

| Service                                                                | Description                                                                                        | Link                                                            |
|------------------------------------------------------------------------| -------------------------------------------------------------------------------------------------- | --------------------------------------------------------------- |
| 🛍️ Product Service                                                    | Handles product catalog, search, and caching logic with Redis and advanced filtering capabilities. | [View Repo](https://github.com/shivamsharma125/ProductService)   |
| 👤 User Service                                                        | Manages user registration, JWT-based and OAuth2 (Google) authentication, and profile updates.      | [View Repo](https://github.com/shivamsharma125/UserService)      |
| 📧 Email Service                                                       | Listens to Kafka events and sends transactional emails using JavaMail API.                         | [View Repo](https://github.com/shivamsharma125/EmailService)     |
| 💳 Payment Service                                                     | Integrates with Razorpay and Stripe to generate dynamic payment links.                             | [View Repo](https://github.com/shivamsharma125/PaymentService)   |
| 🔍 Service Discovery                                                   | Eureka-based service registry to enable dynamic discovery between microservices.                   | [View Repo](https://github.com/shivamsharma125/ServiceDiscovery) |

---

## ⚙️ Architecture Diagram

```
                              +-----------------------+
                              |    Eureka Server      |
                              |   (Service Discovery) |
                              +-----------+-----------+
                                          |
                       +--------------------------+----------------
                       |            |              |              |
                +------+---+   +----+----+   +-----+----+   +------+---+
                | Product   |   |  User   |   | Payment  |   | Email   |
                | Service   |   | Service |   | Service  |   | Service |
                |           |   |         |   |          |   |         |
                +-----------+   +---------+   +----------+   +---------+
```

---

## 🚀 Key Highlights

✅ Built with **Java 17** and **Spring Boot 3** <br>
✅ Service-to-service communication using **RestTemplate** and **Eureka Discovery** <br>
✅ Stateless JWT & OAuth2 Authentication (Google Login) <br>
✅ Event-driven email service using **Kafka** <br>
✅ Redis caching and MySQL-based persistence <br>
✅ Integration with **Razorpay** and **Stripe** <br>
✅ Fully covered with **JUnit 5**, **Mockito**, and **MockMvc** test cases <br>
✅ API-first design with REST principles

---

## 🧪 Testing Strategy

* All services are covered with **unit tests** and **MockMvc-based tests**
* Testing includes:

    * Valid and invalid inputs
    * Exception handling
    * Token generation & validation
    * Kafka message consumption
    * Payment gateway fallback handling

---

## 🔐 Security

* **JWT-based Authentication**: Used in User Service for all protected endpoints
* **OAuth2 Login with Google**: Seamless integration using Spring Security
* **Stateless Services**: Token passed on each secured request, allowing easy scaling

---

## 🌍 External Integrations

| Service   | Provider                      |
| --------- | ----------------------------- |
| Email     | JavaMail (SMTP with Gmail)    |
| Payment   | Razorpay (INR) & Stripe (USD) |
| Caching   | Redis                         |
| Messaging | Apache Kafka                  |
| Discovery | Netflix Eureka                |

---

## 🧱 Tech Stack

* Java 17, Spring Boot 3
* Spring Security, Spring Data JPA
* Redis, Kafka, MySQL
* Maven
* JUnit 5, Mockito, MockMvc
* RESTful APIs
* Eureka Server

---

## 📊 Future Enhancements

* 🛒 Cart Service
* 📦 Order Management Service
* 📊 Product & User Analytics
* 📝 Email templating with HTML
* 🔁 Retry mechanism for failed email/payment operations
* 🌐 Centralized API Gateway (Spring Cloud Gateway)
* 📃 Swagger/OpenAPI documentation for all microservices

---

## 📌 How to Navigate This Project

This is the root repository. Each microservice has its own GitHub repo with:

* Detailed README
* Architecture & tech details
* REST API documentation
* Test coverage info

Feel free to explore each microservice by clicking on the links above! 🎯

---

> 💼 Engineered with clean architecture, optimized for growth, and crafted with production-readiness in mind.
