# poc_kafka-node

Notes:
- Have Docker installed locally on your machine
- run docker run -p 2181:2181 -p 9092:9092 \
   --env ADVERTISED_HOST=localhost \
   --env ADVERTISED_PORT=9092 \
   --env CONSUMER_THREADS=1 \
   --env TOPICS=my-topic,some-other-topic \
   --env ZK_CONNECT=kafka7zookeeper:2181/root/path \
   --env GROUP_ID=mymirror \
   spotify/kafkaproxy

- optional: update producer.js files vars 'message' and 'keyedMessage' to your prefered messages
- optional: 
- run node ./producer.js to produce to Kafka topic 'my-topic'
- run node ./consume.js to consume from Kafka topic 'my-topic'