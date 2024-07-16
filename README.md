
# Stateless Stream Processing Job with Apache Flink and Apache Kafka
This repo contains the sample code for the session presented during Frankfurt Kafka meetup on 11/June/2024.

## Generate a quickstart Java project  

mvn archetype:generate \
-DarchetypeGroupId=org.apache.flink \
-DarchetypeArtifactId=flink-quickstart-java \
-DarchetypeVersion=1.16.2 \
-DgroupId=kafka.meetup.flink \
-DartifactId=flink-quickstart-project \
-DinteractiveMode=false

env.fromSequence(1,10).map(i -> 2 * i).print();

## Create Kafka topics



## Produce data with `kcat` 

kcat -b localhost:19092 -t orders-raw -T -P -l data/orders.json