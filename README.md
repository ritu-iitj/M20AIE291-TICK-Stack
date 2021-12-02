# M20AIE291-TICK-Stack
TICK stack is a platform composed of open source components which makes collection, storage, graphing and alerting on time-series data which are metrics and events. Following are the TICK stack components.

1. Telegraf: A server agent for collecting and reporting metrics.
2. InfluxDB: A high performance time-series database. It is the heart of the system.
3. Chronograf: A user interface for data in InfluxDB, it set graph and dashboard of data in InfluxDB
4. Kapacitor: A data and event processing engine that can process, stream and batch data from InfluxDB. It crunch time-series data into actionable alerts.

Steps for TICK implementation:

Create a yaml file with the description of all the images. Docker-compose.yml
Create folder telegraf and write configurations in telegraf.conf
Configuration files for each component are stored using the volumes section of the docker compose file. Docker volume creates a new volume that container can consume and store data in it.

Run command: $sudo docker-compose up

Open influxdb in browser http://localhost:8086

Open chronograf in browser http://localhost:8888
Goto connection Configuration, connect to InfluxDB and kapacitor here by assigning API tokens respectively. Here also a unique token is required to access the influxdb from chronograf which makes it secure connection.

