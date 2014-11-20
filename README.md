h1.Kafka Samples

Setup:
# start ZooKeeper on localhost with default port (2181), and create the "kafka" node at top level
# start 3 Kafka brokers on localhost using ports 9092, 9093, and 9094

Create the topic:

````
./bin/kafka-topics.sh --create --topic  page_visits --replication-factor 3 --zookeeper localhost:2181/kafka --partitions 5
````

Run SampleProducer

Get the messages:

````
./bin/kafka-console-consumer.sh --zookeeper localhost:2181/kafka --topic page_visits --from-beginning
````
