![image](logo.jpg)

# Overview

This [docker-compose.yml](docker-compose.yml) launches all services in Confluent Platform and runs them in containers in your local host, enabling you to build your own development environments.
For an example of how to use this Docker setup, refer to the [Confluent Platform quickstart](https://docs.confluent.io/current/quickstart/index.html?utm_source=github&utm_medium=demo&utm_campaign=ch.examples_type.community_content.cp-all-in-one)

# Details: 

This docker-compose is especially configured with a JDBC connector which is connected to a mysql database. This connector takes every record from "transaction" topic and persist it into mysql database. If datatable is not created, it will autocreate.

# Prerequisite

1. Docker desktop
###### Important: set at least 8GB ram for it correct running
2. Mysql connection 
###### Create a local mysql server and a schema.
3. Add new user and host in mysql.user table.   
###### Host will represent the host docker. EX: HOST: host.docker.internal	User: root

# Add new connector
 1. [Edit file with connector properties ](connector_config.properties) to point to own database.
 2. From contorl-center, select current cluster and go to "connect" menu and select  " upload connector config file" ![image](doc%20images/add_connector.PNG)
 
 

#RUN docker from cmd
docker-compose up --build