# Monitoring
Hardware and log monitoring with grafana, prometheus, loki, etc.

## Hardware Monitoring with Grafana and Prometheus

### 1. Start the services

``` sh
docker compose up -d
```

### 2. Access Grafana and Prometheus

- Grafana: Open your web browser and go to http://localhost:3000. The default login credentials are:
  - Username: admin
  - Password: admin (or the password you set in the docker-compose.yml file)
- Prometheus: Open your web browser and go to http://localhost:9090.
  - Go to and check status in http://localhost:9090/targets 

### 3. Configure Grafana to use Prometheus as a data source

1. Log in to Grafana.
2. Navigate to `Connections` → `Data Sources`.
3. Click Add data source.
4. Choose Prometheus.
5. In the URL field, enter http://prometheus:9090.
6. Click Save & Test.

### 4. Import a Grafana Dashboard

You can import a pre-built Node Exporter dashboard into Grafana:

1. Go to `Dashboard` → `Create Dashboard` → `Import Dashboard`.
2. In the Import via grafana.com section, enter the dashboard ID 1860 (Node Exporter Full).
3. Click Load.
4. Select Prometheus as the data source.
5. Click Import.
