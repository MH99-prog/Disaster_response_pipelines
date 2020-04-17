

# Installation

The project is supported by Python 3, preferred to directly install the Anaconda distribution. Below are a few libraries and packages to install:

  * Numpy 1.15.2
  * Pandas 0.23.4
  * IPython 6.5.0
  * Matplotlib 3.0.0
  * scikit-learn 0.20.0
  * sqlalchemy 1.2.12
  * nltk 3.3.0
# Project Motivation

In this project, I practiced skills of Data Engineering model to analyze disaster data from Figure Eight to build a model for an API that classifies disaster messages.

Firstly, we targeted the ETL pipeline.Then store the data into the database. Then secondly, we cleaned data from random anomalies to build a model, so that we can classify the messages, that includes in Machine Learning pipeline.

Our objective was to deploy model at the web application. So we can classify the messages that were basically asked from the website or internet.

# File Description
The project mainly discusses [ETL Pipeline Preparation](ETL_Pipeline_Preparation.ipynb), [ML Pipeline Preparation](ML_Pipeline_Preparation.ipynb), and [Web application](run.py).

 ## * ETL Pipeline
A Python script [process_data.py](process_data.py) can load and merge the [disaster_messages.csv](disaster_messages.csv) and [disaster_categories](disaster_categories.csv) datasets, then stores the data in a SQLite database [DisasterResponse.db](DisasterResponse.db), after cleaning.
  

 ## run below code to execute the ETL pipeline
python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db
  
 ## * ML Pipeline

A Python script [train_classifier.py](train_classfier.py) can load data from SQLite database. And it stores the final model [classifier.pkl](classifier.pkl), after training model.
  
 ## run below command in your terminal for building a model
 python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl
 
 ## * Web Application
 A Python scrip [run.py](run.py) and [HTML templated](HTML templates) provide the flask web app. We can check the dataset visualization and query the messages classification result.

## commands to run app
* cd app
* python run.py
* http://0.0.0.0:3001/


# Results
Result includes data visualization and messages classification. The web application is being by going into run.py in the directory and clicking the http://0.0.0.0:3001/ in the web browser

# Acknowledgement

Special thanks to organization **Figure Eight** and teaching platform **Udacity** for whole project. The pipelines are considered here for efficient code, fast and focusing on higher levels.


   
  
  
  
  
  
  
  
