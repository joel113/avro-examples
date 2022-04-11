# Avro Examples Project

https://avro.apache.org/docs/current/

https://avro.apache.org/docs/current/gettingstartedjava.html

## Avro Schema

avro.avsc

`avro-tools random --schema-file avro.avsc --count 2 random.avro`

`xxx random.avro`

## Kafka

https://developer.confluent.io/quickstart/kafka-docker/

```
kcat -P -b joel-kafka:9092 -t avro-examples -p 0 random.bin

kcat -b joel-kafka:9092 -t avro-examples -p 0 > random-kafka.avro

truncate -s -1 random-kafka.avro

avro-tools tojson random-kafka.avro
```
