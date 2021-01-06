kafka-connect-cli
=====

A Command-line Kafka Connect client based on curl, written in bash.

# How to use

```sh
# Check the installed plugins, available with localhost:8083 endpoint.
kafka-connect-cli plugin list

# Can change the Kafka Connect endpoint. (e.g., kafka-connect-service:8080)
KAFKA_CONNECT_URL=kafka-connect-service:8080 kafka-connect-cli plugin list

# Dry run: shows appropriate curl command only.
KAFKA_CONNECT_URL=kafka-connect-service:8080 DRY_RUN=1 kafka-connect-cli plugin list

# Result with JQ: show installed connectors
KAFKA_CONNECT_URL=kafka-connect-service:8080 DRY_RUN=1 kafka-connect-cli connector list

# Input with stdin: Create a new connector (Under Construction)
cat connector-name-with-config.json | KAFKA_CONNECT_URL=kafka-connect-service:8080 kafka-connect-cli connector create
```

