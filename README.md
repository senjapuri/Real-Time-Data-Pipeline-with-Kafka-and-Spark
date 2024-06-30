# Realtime Data Streaming | End-to-End Data Pipeline
## Real-Time Data Pipeline with Kafka and Spark
_________________________________________________________________________________________________________________________________________

##### Table of Contents
_________________________________________________________________________________________________________________________________________

- Introduction
- System Architecture
- Technologies/Tools
- Additional Details


###### Introduction 
_________________________________________________________________________________________________________________________________________

This project is an end-to-end Data Engineering solution utilizing Spark, Kafka, Airflow, Docker, Cassandra, and Python. It fetches data from an API via scheduled scripts, sends it to Kafka using Airflow, processes it with Spark Structured Streaming, and stores it in Cassandra. All components are containerized with Docker for seamless integration and scalability.


###### System Architecture
_________________________________________________________________________________________________________________________________________

![System Architeture](architecture.png)

This project features a comprehensive data pipeline designed with the following components:

-Data Source: The <randomuser.me> API is used to generate random user data, serving as the primary data source for the pipeline.
-Apache Airflow: Acts as the orchestrator, managing the workflow and scheduling tasks to fetch data from the API, which is then stored in a PostgreSQL database.
-Apache Kafka and Zookeeper: Facilitates the streaming of data from PostgreSQL to the processing engine, ensuring real-time data flow. -Zookeeper is used for managing Kafka cluster configurations.
-Control Center and Schema Registry: Provides monitoring capabilities and schema management for Kafka streams, ensuring data integrity and compliance with predefined formats.
-Apache Spark: Utilizes its master and worker nodes for efficient data processing, transforming incoming data and preparing it for storage.
-Cassandra: Serves as the final storage solution for processed data, offering scalability and high availability.

###### Technologies
_________________________________________________________________________________________________________________________________________

-Apache Airflow: 2.6.0 for workflow orchestration
-Python: >= 3.9 for scripting and data manipulation
-Apache Kafka: For data streaming
-Apache Zookeeper: For Kafka cluster management
-Apache Spark: 3.4.1 for distributed data processing
-Cassandra: For storing processed data
-PostgreSQL: 14.0 for initial data storage
-Docker: For containerization, ensuring seamless deployment and scalability
-Java: 11.0.22 for running Java-based components
-Scala: 2.12 for Spark and Kafka integration

###### Additional Details 
_________________________________________________________________________________________________________________________________________

- Integrate Jars: (https://mvnrepository.com/artifact)
  - spark-cassandra-connector_2.12:3.4.1 for connecting Spark to Cassandra
  - spark-sql-kafka-0-10_2.12:3.4.1 for Kafka integration with Spark SQL
  - kafka-clients-3.4.1.jar for Kafka client operations