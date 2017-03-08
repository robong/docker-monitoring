# docker-monitoring
Monitoring the Docker Swarm with ELK stack and Prometheus

This repository will describe and publish our setup of monitoring a Docker Swarm with the help of the ELK repository and Prometheus with it's scrapers.

We were looking into getting a monitoring setup going to support us in optimizing our Docker and service deployment.
This led to the use of the following backend components:

- Prometheus
- CAdvisor
- NodeExplorer
- AlertManager
- ElasticSearch
- LogStash
- ElastAlert

As UI components we are using:

- Kibana
- Grafana

Above components are instantiated within a Docker Swarm Mode with 3 nodes on a development Environment.

On top of the above we are using a HPE storage for our persistant data storage and image/container data storage. This is not mandatory in this setup so you can use local storage volumes for testing purposes. But it is advisable to use a central storage solution in a production environment.

# The base setup

We have splitted up the monitoring stack into 2 basic parts:

1. Metric measurements:
  - Prometheus 
  - CAdvisor
  - NodeExporter
  - AlertManager
  - Grafana (UI)
2. Logging measurements:
  - ElasticSearch
  - LogStash
  - ElastAlert
  - Kibana (UI)
  
# Metric stack

The metric stack is used for raw data gathering from the services/containers. For example CPU, Memory and Network usage.



  

  




