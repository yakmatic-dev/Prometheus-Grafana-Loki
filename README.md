<img width="1080" height="456" alt="image" src="https://github.com/user-attachments/assets/988b67c7-39de-48d8-b179-0504f1ad6e7b" /># Prometheus-Grafana-Loki
Prometheus and Grafana have become industry standards for monitoring and visualization due to their flexibility, scalability, and powerful features. These tools effectively allows you to monitor and troubleshoot complex systems.

## What is monitoring

Monitoring is collecting and visualising data about systems regurlarly so that health system can be viewed and tracked, Three main questions monitoring answered are:

- is the service on?
- is the service functioning as expected?
- is the service performing well?

## What is observability

Monitoring is part of observability, to use monitoring, we need to know what to monitor in advance with **obeservability** we can anticipate problems we havent think of yet, it tells us further where, when and why an issue occurs:

- A very deatiled of events?
### The above directories shows how to install, configure and integrate prometheus with grafana , Dashboard Design, setting alerting rules and Notification points

![Grafana](https://img-c.udemycdn.com/course/750x422/1473698_386a_11.jpg)

## Converting Grafana, Prometheus, Promtail, and Loki to system services is the best practice and gives you:

- Automatic startup on reboot
- Automatic recovery from crashes
- Unified control (start/stop/status)
- Central logging and better security

This is considered best practice for a reliable, production-grade monitoring stack. The images below shows all status of all services up and running

  ![image alt](https://github.com/yakmatic-dev/Prometheus-Grafana-Loki/blob/main/images/service%20log1.jpg?raw=true)
  ![image alt](https://github.com/yakmatic-dev/Prometheus-Grafana-Loki/blob/main/images/service%20log%202.jpg?raw=true)

## Node exporter Dashboard

Node Exporter gives infrastructure-level metrics (CPU, memory, disks, network) to help Prometheus and Grafana monitor server health example of some promql

- 100 - (avg by (instance) (rate(node_cpu_seconds_total{mode="idle"}[5m])) * 100)
- node_memory_MemTotal_bytes - node_memory_MemAvailable_bytes
- sum by (instance) (rate(node_network_receive_bytes_total{device!="lo"}[5m]))

  #### Node exporter Dashboard below

  ![image alt](https://github.com/yakmatic-dev/Prometheus-Grafana-Loki/blob/main/images/node%20exporter%20dashboard.jpg?raw=true)

  ![image alt](https://github.com/yakmatic-dev/Prometheus-Grafana-Loki/blob/9a824c0fc9bf846930850069b87bf246a4da9584/images/node%20exporter%202.jpg)

  ## Node exporter Dashboard

Node Exporter gives infrastructure-level metrics (CPU, memory, disks, network) to help Prometheus and Grafana monitor server health example of some promql

- 100 - (avg by (instance) (rate(node_cpu_seconds_total{mode="idle"}[5m])) * 100)
- node_memory_MemTotal_bytes - node_memory_MemAvailable_bytes
- sum by (instance) (rate(node_network_receive_bytes_total{device!="lo"}[5m]))

  #### BlackBox exporter Dashboard below

Blackbox Exporter = “synthetic monitoring”.
It measures whether endpoints (HTTP, HTTPS, TCP, ICMP, DNS) are reachable, responsive, and within expected performance or SSL limits, exposing those results as Prometheus metrics

  ![image alt](https://github.com/yakmatic-dev/Prometheus-Grafana-Loki/blob/main/images/Black%20Box%20exporter%20dashboard.jpg?raw=true)

  






