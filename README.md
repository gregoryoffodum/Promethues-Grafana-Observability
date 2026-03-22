# Web Application Monitoring Dashboard

This repository contains a complete, containerized observability stack for monitoring a FastAPI web application. It uses Prometheus to scrape application metrics and Grafana to visualize them in real-time.

## Architecture Stack

* **App:** FastAPI (Python)
* **Metrics & Time-Series DB:** Prometheus
* **Visualization:** Grafana
* **Orchestration:** Docker Compose

## Repository Structure

* `docker-compose.yaml`: The infrastructure configuration to spin up the FastAPI app, Prometheus, and Grafana containers.
* `prometheus.yml`: Configuration file for Prometheus, defining the scrape intervals and the FastAPI target endpoint.
* `fastapi-collection.json`: An API collection (e.g., Postman/Insomnia) to easily hit the FastAPI endpoints and generate traffic/metrics.
* `Web Application Monitoring Dashboard...`: final dashboard exported

## Getting Started

### Prerequisites

* Docker
* Docker Compose

### 1. Start the Stack

Navigate to the root directory of this repository and run the following command to start all services in the background:

```bash
docker-compose up -d

### 2. Access the Services
Once the containers are running, you can access the services at the following local ports (adjust if your docker-compose.yaml uses different mappings):

*FastAPI Application: http://localhost:8000

*Prometheus: http://localhost:9090

*Grafana: http://localhost:3000

### 3. Cleanup

```bash
docker-compose down
