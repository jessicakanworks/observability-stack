# observability-stack

Prometheus, Alertmanager and Grafana with node and SNMP exporters — the monitoring layer for
application, database and network hosts. Runs with Docker Compose for a single node, or on
Kubernetes with the manifests in `k8s/`.

```bash
cp .env.example .env            # set GRAFANA_ADMIN_PASSWORD
docker compose up -d
# Grafana: http://localhost:3000  Prometheus: http://localhost:9090  Alertmanager: :9093
```
Add hosts to `prometheus/targets/*.yml`; Prometheus reloads them automatically.
Alert rules live in `prometheus/rules/`. Grafana datasource and dashboards are provisioned from `grafana/provisioning/`.
