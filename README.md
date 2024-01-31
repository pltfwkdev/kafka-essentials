# kafka-essentials - LinkedIn course. 

> Back pressure handling.
>> Consumers can consume messages at their own page.

> horizontally scalable.

Use cases.
- async messaging.

#Zookeeper Service.
  zookeeper:
    image: 'bitnami/zookeeper:latest'
    restart: "no"
    ports:
      - '2181:2181'
    environment:
      - ALLOW_ANONYMOUS_LOGIN=yes
    container_name: zookeeper

#Kafka Service
  kafka:
    image: 'bitnami/kafka:latest'
    restart: "no"
    ports:
      - '9092:9092'
      - '29092:29092'


'9092:9092' host machine to communicate with kafka.
'29092:29092' for other docker containers to communicate with kafka.
