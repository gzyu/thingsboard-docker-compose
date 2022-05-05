# Thingsboard

### Docker Compose file

using Postgres HA Cluster + Zookeeper Cluster + Apache Kafka

[![Thingsboard Docker Compose](https://raw.githubusercontent.com/Stream-I-T-Consulting/thingsboard-docker-compose/main/thingsboard_docker-compose.png?token=GHSAT0AAAAAABT2IALKLXQ3XJV5TYFW6YGOYTTVUKQ)](https://raw.githubusercontent.com/Stream-I-T-Consulting/thingsboard-docker-compose/main/thingsboard_docker-compose.png?token=GHSAT0AAAAAABT2IALKLXQ3XJV5TYFW6YGOYTTVUKQ)

## PostgreSQL Architecture

[![PostgreSQL Architecture](https://raw.githubusercontent.com/Stream-I-T-Consulting/thingsboard-docker-compose/main/thingsboard_postgres_arch.png?token=GHSAT0AAAAAABT2IALKPYFH7Q7CYG6S6LPOYTTVXFA)](https://raw.githubusercontent.com/Stream-I-T-Consulting/thingsboard-docker-compose/main/thingsboard_postgres_arch.png?token=GHSAT0AAAAAABT2IALKPYFH7Q7CYG6S6LPOYTTVXFA)

## Thingsboard with Apache Kafka

[![Thingsboard with Apache Kafka](https://raw.githubusercontent.com/Stream-I-T-Consulting/thingsboard-docker-compose/main/thingsboard_kafka.png?token=GHSAT0AAAAAABT2IALLM4UCNY5DBVLQP6WAYTTVYGA)](https://raw.githubusercontent.com/Stream-I-T-Consulting/thingsboard-docker-compose/main/thingsboard_kafka.png?token=GHSAT0AAAAAABT2IALLM4UCNY5DBVLQP6WAYTTVYGA)

## Port using

- 2181-2183:2181 - connect local port 2181-2183 to exposed internal Zookeeper port 2181
- 9092:9092 - connect local port 9092 to exposed internal Apache Kafka port 9092
- 8080:9090 - connect local port 8080 to exposed internal HTTP port 9090
- 1883:1883 - connect local port 1883 to exposed internal MQTT port 1883
- 7070:7070 - connect local port 7070 to exposed internal Edge RPC port 7070
- 5683-5688:5683-5688/udp - connect local UDP ports 5683-5688 to exposed internal COAP and LwM2M ports

## Where

- ~/.mytb-data:/data - mounts the host’s dir ~/.mytb-data to ThingsBoard DataBase data directory
- ~/.mytb-logs:/var/log/thingsboard - mounts the host’s dir ~/.mytb-logs to ThingsBoard logs directory
- mytb - friendly local directory name of this machine
- thingsboard - friendly local name of this container
- restart: always - automatically start ThingsBoard in case of system reboot and restart in case of failure.
- image: thingsboard/tb-postgres - docker image
