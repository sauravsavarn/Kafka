#####

  * URL to launch control-center locally post kafka container spawned up using docker (REFER kafka_zookeeper/setup-kafka_zookeeper-as-docker)
    compose files

    http://localhost:9021/


  * COMMANDS :-
  * *  commands to spawn the docker containers
    *  #> docker-compose up -d
   
    *  commands to get/list help related to kafka topic
    * *  #> docker exec broker01 kafka-topics --help (** in case of multi broker setup)
    * *  #> docker exec broker kafka-topics --help (** in case of single broker setup)

    *  commands to get/list help related to kafka topic
    * *  #> docker exec broker01 kafka-topics --help (** in case of multi broker setup)
    * *  #> docker exec broker kafka-topics --help (** in case of single broker setup)

    *  commands to list kafka topic
    * *  #> docker exec broker01 kafka-topics --list --bootstrap-server localhost:29092 (** in case of multi broker setup)
    * *  #> docker exec broker kafka-topics --list --bootstrap-server localhost:29092 (** in case of single broker setup)

    *  commands to create kafka topic
    * *  #> docker exec broker01 kafka-topics --create --bootstrap-server localhost:29092 --partitions 3 --replication-factor 3 --topic test (** in case of multi broker setup when creating a topic having 3 partitions and replication factor set to 3 when having 3 broker clusters)
    * *  #> docker exec broker kafka-topics --create --bootstrap-server localhost:29092 --partitions 3 --replication-factor 1 --topic test (** in case of single broker setup)

    *  commands to alter kafka topic properties like partition or replication-factor, etc.
    * *  #> docker exec broker01 kafka-topics --alter --bootstrap-server localhost:29092 --partitions 3 --topic test (** in case of multi broker setup)
    * *  #> docker exec broker kafka-topics --alter --bootstrap-server localhost:29092 --partitions 3 --topic test (** in case of multi broker setup)

    *  commands to delete kafka topic
    * *  #> docker exec broker01 kafka-topics --bootstrap-server localhost:29092 --delete --topic testing (** in case of multi broker setup)
    * *  #> docker exec broker kafka-topics --bootstrap-server localhost:29092 --delete --topic testing (** in case of single broker setup)

    *  commands to start kafka-producer to send messages to topic 'test'.
    * *  #> docker exec -it broker01 kafka-console-consumer --bootstrap-server localhost:29092 --topic test (** in case of multi broker setup)
    * *  #> docker exec -it broker kafka-console-consumer --bootstrap-server localhost:29092 --topic test (** in case of single broker setup)

    *  commands to start kafka-producer to send messages to topic 'test'.
    * *  #> docker exec -it broker01 kafka-console-producer --bootstrap-server localhost:29092 --topic test (** in case of multi broker setup)
    * *  #> docker exec -it broker kafka-console-producer --bootstrap-server localhost:29092 --topic test (** in case of single broker setup) 
    
    * * [[OUTPUT]] from 'confluent control center'
        ![Alt text](assets/img/messages-in-topic-send-from-kafka-producer.png)

    *  commands to start kafka-consumer to receive messages from topic 'test'.
    * *  #> docker exec -it broker01 kafka-console-consumer --bootstrap-server localhost:29092 --topic test (** in case of multi broker setup)
    * *  #> docker exec -it broker kafka-console-consumer --bootstrap-server localhost:29092 --topic test (** in case of single broker setup)

    
    

    


    
