# Docker setup for Kafka + NiFi + Schema Registry

## Apache NiFi

+ https://hub.docker.com/r/apache/nifi

## Confluent Platform Components

**Version 6.0.0 is used in this setup.**

For other versions, setup can have some differences.

+ https://hub.docker.com/r/confluentinc/cp-kafka
+ https://hub.docker.com/r/confluentinc/cp-schema-registry
+ https://hub.docker.com/r/confluentinc/cp-kafka-proxy


## Execution

Start the environment with `docker-compose up`. Once all services are up and running, there will be available several ports:

### Port 9092 - Kafka

Use this port to connect Kafka Producers, Kafka Consumers and other services directly communicating with Kafka.

+ Protocol: PLAINTEXT
+ Authentication: None

### Port 8082 - Kafka REST

REST interface to Kafka. 

Documentation for Kafka REST API: https://docs.confluent.io/current/kafka-rest/api.html

+ Protocol: HTTP
+ Authentication: None

#### Operations

+ Get list of topics http://localhost:8082/topics

### Port 8085 - Schema Registry

REST interface to Schema Registry.

Documentation for Schema Registry API: https://docs.confluent.io/current/schema-registry/develop/api.html

+ Protocol: HTTP
+ Authentication: None

### Port 8080 - NiFi

NiFi user interface.

http://localhost:8080/nifi 

+ Protocol: HTTP
+ Authentication: None
