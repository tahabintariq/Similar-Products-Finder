
# Real Time Price Optimizer 

This project aims to provide a scalable and real-time solution for analyzing Amazon metadata using streaming data processing techniques. It is designed for students in university-level courses focusing on big data processing, streaming analytics, and database integration.

## Concepts Used

- **Data Preprocessing:** Cleaning and formatting the Amazon metadata dataset for analysis, ensuring it is suitable for streaming and frequent itemset mining processes.
- **Streaming Pipeline Setup:** Developing a producer application to stream preprocessed data in real-time and creating consumer applications to subscribe to this data stream.
- **Frequent Itemset Mining:** Implementing the Apriori and PCY (Park-Chen-Yu) algorithms for discovering frequent itemsets in a streaming context, along with innovative analysis in the third consumer application.
- **Database Integration:** Utilizing a non-relational database such as MongoDB to store the results of the frequent itemset mining for further analysis and retrieval.
- **Bonus Bash Script:** Enhancing project execution with a Bash script to automate the setup of Kafka components, including Kafka Connect and Zookeeper, as well as running the producer and consumer applications.

## Required Technologies


### Hadoop
Hadoop was utilized in this project for distributed storage and processing of large volumes of data, facilitating efficient analysis and manipulation of the Amazon metadata dataset.

#### Start Hadoop
```bash
start-all.sh
```

### Spark

Spark was employed in this project for real-time data processing and analysis, enabling streaming analytics and frequent itemset mining on the Amazon metadata dataset.

#### Start Kafka Zookeeper
```bash
bin/zookeeper-server-start.sh config/zookeeper.properties
```

#### Start Kafka Server
```bash
bin/kafka-server-start.sh config/server.properties
```

### MongoDB
MongoDB was utilized in this project as a NoSQL database for storing the results of frequent itemset mining and facilitating efficient retrieval and analysis of streaming data from the Amazon metadata dataset.

### Install MongoDB by following tutorial from this link
```bash
https://www.mongodb.com/docs/manual/tutorial/install-mongodb-on-ubuntu/
```

## Overview of Code


After preprocessing the data, the `producer.py` script is utilized to stream the preprocessed data into Kafka, facilitating real-time data ingestion. Following this, the `consumer_apriori.py` script subscribes to the Kafka topic and implements the Apriori algorithm to identify frequent itemsets in the transaction data. 

Similarly, the `consumer_pcy.py` script processes Kafka messages, employing the PCY algorithm to efficiently identify frequent pairs within the streaming data.

The `consumerfinal_pcy.py` script refines the PCY algorithm implementation to identify frequent combinations within the streaming data. It utilizes advanced hashing and counting techniques to efficiently process large transaction datasets, providing valuable insights into complex purchase patterns and market trends.

Moreover, the `consumer_realtimepriceoptimizer.py` script integrates a dynamic pricing model, leveraging Kafka messages to update product demand and brand pricing information. It recommends optimal prices in real-time based on demand fluctuations and brand preferences, enabling responsive pricing strategies for maximizing revenue and customer satisfaction.




