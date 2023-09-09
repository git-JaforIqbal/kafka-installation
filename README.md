# kafka-installation

### Kafka Default Port
```Zookeeper Port : 2181```
```Kafka Server/Broker Port : 9092```

# Command CLI:
###  Start the ZooKeeper service
```bin/zookeeper-server-start.sh config/zookeeper.properties```

###  Start the Kafka broker service
```bin/kafka-server-start.sh config/server.properties```

### To Create a kafka Topic:
```bin/kafka-topics.sh --bootstrap-server localhost:9092 --create --topic connect-plus-user-management --partitions 3 --replication-factor 1```

### To Get The List Of kafka Topic:
```bin/kafka-topics.sh --bootstrap-server localhost:9092 --list```

### To Get Details Of a kafka Topic:
```bin/kafka-topics.sh --bootstrap-server localhost:9092 --describe --topic connect-plus-user-management```

### To Produce a Message :
```bin/kafka-console-producer.sh --broker-list localhost:9092 --topic connect-plus-user-management```

### To Check Consumer on a Specific Topic Message :
```bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic connect-plus-user-management --from-beginning```


# Commands For Docker Env

### Move into Kafka container for docker
```docker exec -it <kafka_conatiner_id> /bin/sh```
### Go inside kafka installation folder
```cd /opt/kafka_<version>/bin```
