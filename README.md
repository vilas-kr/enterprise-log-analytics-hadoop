# Log Analytics System for a Growing Enterprise
This project builds a local Hadoop-based system to ingest, store, and analyze growing web access logs using HDFS and MapReduce in order to study Hadoop’s scalability, fault tolerance, and performance in a real-world log analytics scenario.

## Project Overview
1. Local pseudo-distributed Hadoop cluster setup.
2. Web access log ingestion into HDFS.
3. HDFS block storage and scalability analysis.
4. Built-in MapReduce WordCount execution.
5. Custom Python MapReduce using Hadoop Streaming.
6. Error log analysis.
7. Hadoop architecture evolution.
8. Hadoop configuration and performance tuning.

## Tech Stack
```
Operatting System : Linux/Mac OS/ WSL for windows.
Platform : Apache Hadoop.
Storage : HDFS
Environment : Java JDK 8 or 11.
Programming Language : Python (for Streaming).
```

## Project Structure
```
enterprise-log-file-analysis-hadoop /
|-- scripts /
|   |-- setup.sh
|   |-- start_hadoop.sh
|   |-- stop_hadoop.sh
|   |-- word_count_inbuilt.sh
|   |-- word_count_streaming.sh
|   |-- log_analytics.sh
|   |-- log_ingestion.sh
|
|-- streaming /
|   |-- word_count_mapper.py
|   |-- word_count_reducer.py
|   |-- log_analytics_mapper.py
|
|-- docs /
|   |-- hadoop_architecture_evolution.txt
|   |-- configuration_performance_tuning.txt
|
|-- .gitignore
|-- README.md
|-- requirements.txt
```

## Installation
```
Clone the repository
-> git clone https://github.com/vilas-kr/enterprise-log-analytics-hadoop

Move to project folder
-> cd enterprise-log-analytics-hadoop

Install dependencies:
pip install -r requirements.txt

First download datasets from below links:
small_log_file : https://www.kaggle.com/datasets/avinhok/website-log-access
large_log_file : https://www.kaggle.com/datasets/eliasdabbas/web-server-access-logs?select=access.log

Then move this files to desired location and change the "*LOCAL_LOG_FILE" path in file_analyzer.sh according to your dataset path.

Now execute below commands in order:
1. ./scripts/setup.sh (install hadoop and set environment)
2. ./scripts/start_hadoop.sh (start hadoop services)
3. ./scripts/log_ingestion.sh (load file to HDFS)
4. ./scripts/word_count_inbuilt.sh
5. ./scripts/word_count_streaming.sh
6. ./scripts/log_analytics.sh
7. ./scripts/stop-hadoop.sh (stop hadoop services)
```

## Author
```
Vilas K R
GitHub username: vilas-kr
```