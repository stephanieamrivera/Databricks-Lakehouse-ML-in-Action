## Databricks ML in Action
Begin working on the projects in Chapter 2. In each chapter that follows, we expand on each using the knowledge we gained during the beginning section of each chapter. The section named Applying our learning is where we focus on the projects. The projects primarily leverage Unity Catalog Metastore, but you can specify hive_metastore for the catalog to not use UC. However, not all features are avialble for use with HMS.

Be sure you open the global setup file, understand it, and customize it to your liking.

### Project 1: Synthetic Streaming Transactions Data
The synthetic dataset is generated to demonstrate the use of Auto Loader and streaming.

Chapter 2: 
* Generate JSON data and write it to a folder in cloud storage.

Chapter 3:
* Generate JSON data with a new column, product, and write it to a folder in cloud storage.
* Transform JSON data in a stream to Delta while handling the schema change. Data is written to a streaming table in one notebook and to cloud storage in another.

Chapter 4:
No exploration of the synthetic data.

Chapter 5:
* Reuse the data generator and Delta transformation from earlier chapters.
* Count the number of transactions over the last 2 minutes for each customer ID using stateful streaming.
* Using the stream of transaction counts, create a table with only the most up to date feature values and a historical transaction table. The feature table is created using Delta Change Data Feed.
* Create a feature UDF to calculate the difference between the maximum price for a product and the transaction price. This requires an additional feature of the max price for a product over the last __ amout of time.

Chapter 6:
* Create a snapshot training set of the streaming data using DFE. Include the feature UDF from chapter 5 and publish the feature table to the Databricks online store.
* Create and register a model.

Chapter 7:
* Deploy the registered model.
* Monitor the input and output tables.
* Create a webhook to trigger testing.

Chapter 8:
* Create a DBSQL dashboard.

### Project 2: Favorita Store Sales - Time Series Forecasting
This dataset is hosted on the [Kaggle website](https://www.kaggle.com/competitions/store-sales-time-series-forecasting/overview) for learning purposes. We want to be able to predict sales on each type of 

Chapter 2:
* Download the dataset from Kaggle and put into a volume. 

Chapter 3:
* Using pandas transform the CSV files into dataframes. Use Spark to write the dataframes to Delta tables.

Chapter 4:
* Use AutoML to explore the training_data table, open the autogenerate data exploration notebook.
* Use Pandas API on Spark to impute the missing days in the oil table with the previous day's oil price.

Chapter 5:
* Create three feature tables: holiday, stores, and oil.

Chapter 6:
* Create a training set using DFE.
* Create a model using AutoML and the feature tables.

Chapter 7:


Chapter 8:

### Project 3: American Sign Language Fingerspelling Recognition
Our second dataset is the ASL Fingerspelling dataset, also hosted on [Kaggle](https://www.kaggle.com/competitions/asl-fingerspelling).

Chapter 2:
* Download the dataset from Kaggle and put into cloud storage. (Shown with and without volumes)

Chapter 3:
* Using pandas transform the metadata CSV files into dataframes. Use Spark to write the metadata dataframes to Delta tables.
* Grant permission to someone on the ASL volume. The setup file creates the volume for you. Transformation shown includes moving files to the volume.

Chapter 4:
* Filter out the 

Chapter 5:

Chapter 6:

Chapter 7:

Chapter 8:

### Project 4: Parkinson's Freezing of Gait - Event Detection
In collaboration with The Michael J. Fox Foundation for Parkinson's Research, [Kaggle](https://www.kaggle.com/competitions/tlvmc-parkinsons-freezing-gait-prediction/overview) has a competition to detect freezing of gait (FoG).

Chapter 2:
* Download the dataset from Kaggle. 

Chapter 3:
Chapter 4:
Chapter 5:
Chapter 6:
Chapter 7:
Chapter 8:

### Project 5: SQL Bot

Chapter 5:
Chapter 6:
Chapter 7:
Chapter 8: