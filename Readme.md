HEALTHCHECK-DOCKER-DEMO

A demonstration project showing how to implement health checks in Docker containers.

OVERVIEW:
This repository contains a simple demo showcasing Docker's health check feature.

PREREQUISITES:
- Docker installed
- Basic Docker knowledge

GETTING STARTED:
1. Clone repository:
   git clone https://github.com/bittush8789/HEALTHCHECK-DOCKER-DEMO.git
   cd HEALTHCHECK-DOCKER-DEMO

2. Build Docker image:
   docker build -t healthcheck-demo .

3. Run container:
   docker run -d -p 8080:8080 --name health-demo healthcheck-demo

HEALTH CHECK CONFIGURATION:
The Dockerfile includes:
HEALTHCHECK --interval=30s --timeout=3s CMD curl -f http://localhost:8080/health || exit 1

CHECKING STATUS:
View health status:
docker ps

Detailed results:
docker inspect --format='{{json .State.Health}}' health-demo

ENDPOINTS:
- / : Main endpoint
- /health : Health check endpoint

