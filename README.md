# Monitor System Resources Using Netdata

## Task Overview
This task demonstrates how to install and run **Netdata** using Docker to monitor system and application performance metrics. Netdata provides real-time insights into CPU, memory, disk, and Docker containers with rich visualization dashboards.

---

## Tools & Technologies
- **Netdata** (Free, open-source monitoring tool)
- **Docker**
- **Linux**

---

## Steps to Complete

### 1️ Install Docker

bash
sudo apt update -y
sudo apt install docker.io -y
sudo systemctl enable docker
sudo systemctl start docker
docker --version
----
## Run Netdata in Docker
---
docker run -d --name=netdata \
  -p 19999:19999 \
  --cap-add SYS_PTRACE \
  --security-opt apparmor=unconfined \
  netdata/netdata
-----
## Verify that the container is running
docker ps
---
## Access the Dashboard

Local Machine: http://localhost:19999
Ensure TCP Port 19999 is allowed in your Security Group.

## Monitor Metrics

1) CPU Usage

2) Memory Usage

3) Network Traffic

## Screenshot
---
Access Dashbord
---
![Branches](https://github.com/gawali-priyanka/Monitor-System-Resources-Using-Netdata/blob/main/screenshots/Access-dashbord1.png?raw=true)
---
Logs
----
![Branches](https://github.com/gawali-priyanka/Monitor-System-Resources-Using-Netdata/blob/main/screenshots/Logs.png?raw=true)
-----
Cloud watch Metrics
----
![Branches](https://github.com/gawali-priyanka/Monitor-System-Resources-Using-Netdata/blob/main/screenshots/Cloudwatch-matrix.png?raw=true)
----
Docker container
-----
![Branches](https://github.com/gawali-priyanka/Monitor-System-Resources-Using-Netdata/blob/main/screenshots/Docker-container.png?raw=true)



