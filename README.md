# Prometheus + Grafana Monitoring Stack 📊

A complete system monitoring stack using Prometheus, Grafana, Node Exporter, cAdvisor and Alertmanager — deployed with Docker Compose.

## 🛠 Tech Stack

| Tool | Purpose |
|---|---|
| Prometheus | Metrics collection and storage |
| Grafana | Visualization and dashboards |
| Node Exporter | Host system metrics (CPU, Memory, Disk) |
| cAdvisor | Container metrics |
| Alertmanager | Alert routing and notifications |
| Docker Compose | Container orchestration |

## 📊 What Gets Monitored

- CPU usage and load average
- Memory usage and swap
- Disk I/O and space
- Network traffic
- Container metrics
- System uptime

## 🚀 How to Run

1. Clone the repo

git clone https://github.com/Lekha15-cse/prometheus-grafana-monitoring.git
cd prometheus-grafana-monitoring

2. Start the stack

docker compose up -d

3. Access the services

| Service | URL |
|---|---|
| Grafana | http://localhost:3000 |
| Prometheus | http://localhost:9090 |
| Alertmanager | http://localhost:9093 |
| cAdvisor | http://localhost:8081 |
| Node Exporter | http://localhost:9100 |

Grafana login — Username: admin / Password: foobar

## 📈 Import Dashboard

1. Login to Grafana at http://localhost:3000
2. Go to Dashboards → New → Import
3. Enter dashboard ID: 1860
4. Select Prometheus as datasource
5. Click Import

You will see live CPU, Memory, Disk and Network metrics.

## 🏗 Architecture

Node Exporter → Prometheus (scrapes every 15s) → Grafana (visualizes)
cAdvisor     → Prometheus (scrapes every 15s) → Grafana (visualizes)
Prometheus   → Alertmanager (fires alerts on threshold breach)

## 🧹 Cleanup

docker compose down

## 💡 Key Concepts Demonstrated

- Metrics collection with Prometheus scraping
- Time series data visualization with Grafana
- Container monitoring with cAdvisor
- Host monitoring with Node Exporter
- Alert routing with Alertmanager
- Multi-container setup with Docker Compose

## 👤 Author

Lekha P 
GitHub: https://github.com/Lekha15-cse
