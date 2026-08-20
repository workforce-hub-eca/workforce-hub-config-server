# Config Server ⚙️

Centralized configuration management for the entire WorkForceHub polyrepo.

## 🛠️ Tech Stack
- **Java**: 25
- **Spring Boot**: 4.1.0
- **Spring Cloud Config**

## ✨ Architecture Highlights
- Serves YAML configurations directly from `src/main/resources/configs/`.
- Microservices connect to this server during initialization to fetch properties (e.g., MongoDB URIs, Eureka settings).
- **Clean Configuration**: We strictly removed legacy WebFlux `globalcors` properties from `api-gateway.yml` to prevent lifecycle conflicts in our WebMVC environment.

## 🚀 Running Locally
- Port: `8888`
- Must be the **first** service started in the backend ecosystem.
