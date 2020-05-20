# kafka-apps-intro
Kafka Apps Intro(Individual)
*by Michael Baumli*

##Commands for Kafka used in practice  

*All done within Powershell in the kafka directory in the C drive*

Window 1 - Run Zookeeper Service 

```.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties```   

Window 2 - Run Kafka Service

```.\bin\windows\kafka-server-start.bat .\config\server.properties```   

Window 3 (temporary) - Execute One-Time Commands - create, list, delete topics 

```.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --create --topic crewdragon2-messages```   
```.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --list```   

Window 4 - Run Kafka Producer for creating content. 
```.\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic crewdragon2-messages```   

Window 5 - Run Kafka Consumer with messages from the beginning 

```.\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic crewdragon2-messages --from-beginning```



