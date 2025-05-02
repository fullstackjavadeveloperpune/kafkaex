# kafkaex

Spring Boot with Apache Kafka-
What is Apache Kafka-
Apache Kafka is a distributed event streaming platform designed for handling real-time data feeds. It is used for high-throughput, fault-tolerant, and scalable data streaming and messaging. Kafka is commonly used in event-driven architectures, microservices, log processing, and real-time analytics.

It was initially thought of as a message queue and open-sourced by LinkedIn in 2011. Its community evolved Kafka to provide key capabilities:
Publish and Subscribe to streams of records, like a message queue.
Storage system so messages can be consumed asynchronously.

Key Components of Kafka:
1. Producer – Publishes (writes) data to Kafka topics.
2. Broker – Kafka server that stores and manages messages.
3. Topic – A category to which records are sent by producers and read by consumers.
4. Partition – A topic is split into partitions to allow parallel processing.
5. Consumer – Reads data from Kafka topics.
6. Zookeeper – Manages Kafka cluster metadata and configurations

Key Features of Kafka:
1. High Throughput & Low Latency – Handles millions of messages per second.
2. Scalability – Can scale horizontally by adding more brokers.
3. Fault Tolerance – Ensures data durability using replication.
4. Persistence & Durability – Uses disk storage for reliable message retention.
5. Real-time Processing – Works with stream processing frameworks like Kafka Streams and Apache Flink.

Steps for Spring Boot with Apache Kafka-
1. Download Apache Kafka
 URL- https://kafka.apache.org/downloads
 
2. Extract the zip file and copy into folder

3. Open Powershell and move to Kafka Folder
 PS C:\WINDOWS\system32 cd C:\Kafka\kafka_2.13-3.9.0\
 
4. Set JDK Path as- $env:JAVA_HOME="C:\Program Files\Java\jdk-17"

5. Commands to start Zookeeper and Kafka :
 .\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
 .\bin\windows\kafka-server-start.bat .\config\server.properties

6. Go to https://www.kafkatool.com/
offsetexplorer_64bit download and install it

7. Open offsetexplorer software
cluster name- Full Stack Project Local Kafka
Bootstrap Server- localhost:9092
kafka cluster version- 3.3
   then create topic
   Next go to partition and add data as message key, value
   Ex- key- message, value- Welcome to Full Stack Java Developer, Pune 
   go to properties instead of byte Array select String type 
   and run/ retrieve message using play icon
  
8. Create Spring Boot Application for Producer & Consumer