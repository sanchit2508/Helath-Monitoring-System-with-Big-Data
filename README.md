# Helath-Monitoring-System-with-Big-Data

Project Report: Health Monitoring System using Big Data
1. Project Overview:
This project implements a Health Monitoring System that uses Big Data technologies to process real-time patient data (such as heart rate, blood pressure, and oxygen levels) and apply Machine Learning (ML) models for anomaly detection and predictive health insights. The system is designed to track patients' vitals continuously, detect abnormalities, and provide early warnings for health risks using data streaming and processing frameworks such as Apache Kafka, Apache Spark, Hadoop, and Machine Learning algorithms like Isolation Forest and LSTM (Long Short-Term Memory).

2. Objective:
The primary objective of this project is to create a real-time health monitoring system that can:

Process and Analyze Real-Time Data: Track patient vitals (heart rate, blood pressure, and oxygen levels) in real-time.
Detect Anomalies: Identify abnormal vitals using anomaly detection algorithms.
Predict Future Health Trends: Use predictive models like LSTM to forecast potential health issues.
Store Data in Scalable Storage: Store the processed health data in HDFS (Hadoop Distributed File System) for large-scale and fault-tolerant storage.

3. Technologies Used:
Apache Kafka: For real-time data streaming and communication between producers and consumers.
Apache Spark: A distributed processing framework used for real-time data analysis.
PySpark: Python API for Spark, allowing seamless integration with the Spark ecosystem.
Hadoop: For scalable and distributed storage of processed health data.
Isolation Forest: Machine learning algorithm for anomaly detection in patient vitals.
LSTM (Long Short-Term Memory): A deep learning model used for predictive analysis on heart rate data.
Matplotlib: Python library for data visualization to plot health trends over time.


4. System Architecture:
The system is structured in a way that multiple components work together to achieve real-time monitoring and analysis. The main components are:

Kafka Producer:

Simulates the generation of synthetic patient data in real-time.
Sends the patient vitals data (such as heart rate, blood pressure, and oxygen levels) to a Kafka topic (patient_vitals).
Kafka Consumer with PySpark:

Consumes real-time data from the Kafka topic and processes it using Apache Spark.
Transforms and analyzes the data in real-time to extract useful health insights.
Anomaly Detection:

Uses the Isolation Forest algorithm to detect anomalies in patient vitals such as heart rate and oxygen levels.
Flags abnormal data points that could signify potential health risks.
Predictive Analysis (LSTM):

Trains a Long Short-Term Memory (LSTM) model on historical patient data to predict future heart rate values.
Forecasts future trends in heart rate to provide early warnings of potential health risks.
Data Visualization:

Uses Matplotlib to visualize heart rate and other vitals over time, providing insights into the patient's health status.
Data Storage in HDFS:

Stores the processed data into the HDFS for distributed storage.
Ensures fault tolerance and scalability of the system as the amount of health data increases.


5. Workflow:
The workflow of the Health Monitoring System is as follows:

Data Generation: Synthetic patient data is generated periodically (e.g., every second) and sent to the Kafka topic patient_vitals.
Data Consumption: The Kafka consumer consumes the real-time data from the Kafka topic using PySpark and processes the incoming data.
Anomaly Detection: The data is passed through the Isolation Forest model to detect any anomalies or abnormal values in patient vitals.
Predictive Analysis: The heart rate data is passed through an LSTM model to predict future heart rate values based on the historical data.
Data Visualization: The heart rate and other vitals are plotted in real-time using Matplotlib for better insights.
Data Storage: The processed data is saved into HDFS for long-term storage and further analysis.

6. Key Features:
Real-Time Patient Data Processing:
The system processes real-time data streams using Apache Kafka and PySpark to track patient vitals, including heart rate, blood pressure, and oxygen levels.
Anomaly Detection:
Uses Isolation Forest, a machine learning algorithm, to detect anomalies in patient vitals.
Flags abnormal heart rate and oxygen levels to identify potential health risks.
Predictive Analysis:
The system employs an LSTM (Long Short-Term Memory) model to predict future health data, such as heart rate, using past data.
This enables the system to forecast potential health risks and offer early warnings.
Scalable Data Storage:
All processed data is stored in HDFS (Hadoop Distributed File System) for fault tolerance, scalability, and distributed storage.
Data is stored in Parquet format, providing a highly efficient and compressed storage solution.
Visualization:
Real-time data is visualized using Matplotlib, providing graphical trends of vitals such as heart rate.
This helps healthcare professionals monitor patient health in a more intuitive way.


7. Results and Analysis:
Real-Time Data Streaming:
The system can successfully process and analyze real-time patient data. It continuously consumes data from the Kafka topic and processes it in near real-time.
The processed data is displayed for further analysis and monitoring.
Anomaly Detection:
The Isolation Forest model effectively detects anomalies in health data, flagging outliers that may indicate abnormal health conditions.
This feature helps in alerting healthcare providers about potential health issues early.
Predictive Analysis:
The LSTM model provides accurate predictions of future heart rate values, enabling early intervention.
The model forecasts trends in heart rate and other vitals, assisting in predictive healthcare.
Visualization:
The system provides intuitive visualizations of heart rate trends over time, helping healthcare professionals easily monitor patient vitals.
Data Storage:
The processed data is stored efficiently in HDFS, ensuring it can scale as the amount of health data increases over time.
The use of Parquet format optimizes storage and retrieval of data.


8. Challenges and Limitations:
Data Quality:
The synthetic data used for simulation may not represent real-world patient data perfectly. The accuracy of anomaly detection and prediction models could be affected by this.
Model Accuracy:
The accuracy of the LSTM model depends on the quality and quantity of data used for training. The system may require hyperparameter tuning and more diverse data to improve performance.
Infrastructure Requirements:
The system relies on multiple components such as Kafka, Spark, and Hadoop, which require a distributed environment for effective execution.
Proper infrastructure and configuration are necessary to ensure scalability and fault tolerance.


9. Conclusion:
The Health Monitoring System using Big Data is an effective solution for real-time monitoring, anomaly detection, and predictive health analysis. By leveraging Apache Kafka, Apache Spark, Hadoop, and Machine Learning algorithms, the system can track patient vitals, identify potential health risks, and store data at scale. This system has the potential to improve patient care by providing early warnings, detecting abnormal conditions, and forecasting future health trends.

Future improvements can include:

Integration with real-world healthcare data.
Implementation of more advanced ML models for prediction and anomaly detection.
Expansion to track additional vitals and perform more in-depth health analysis
