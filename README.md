![Alt text](https://www.northeastern.edu/graduate/blog/wp-content/uploads/2019/02/Disaster-response-Hurrican-Harvey.jpg?raw=true "Disaster Response Systems")
# Disaster Response Pipeline Project
In this project, I have built a machine learning pipeline to categorize the messages that were sent during disaster events, so that these messages can be sent to an appropriate disaster relief agency.
The project also includes a web app where an emergency worker can input a new message and get classification results in several categories.
## Instructions:
1. Run the following commands in the project's root directory to set up your database and model.
    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`
2. Run the following command in the app's directory to run your web app.
    `python run.py`
3. Go to http://0.0.0.0:3001/
## Installation
Beyond the Anaconda distribution of Python, the following packages need to be installed:
  nltk.punkt
  nltk.wordnet
  nltk.stopwords
## Datasets Introduction
The datasets for this project is provided by Udacity's partners at Figure Eight. There are two files, disaster messages and disaster categories
## File Description
### Readme
This file provides high level overview of the work done in project.
### Data
1. disaster_categories.csv: dataset including all the categories
2. disaster_messages.csv: dataset including all the messages
3. process_data.py: ETL pipeline scripts to read, clean, and save data into a database
4. DisasterResponse.db: output of the ETL pipeline, i.e. SQLite database containing messages and categories data
### Models
1. train_classifier.py: machine learning pipeline scripts to train and export a classifier
2. classifier.pkl: output of the machine learning pipeline, i.e. a trained classifer
### App
1. run.py: Flask file to run the web application
2. templates contains html file for the web applicatin
## Project Motivation
The goal of this project is applying data engineering, natural language processing, and machine learning skills to analyze message data that people sent during disasters to build a model for an API that classifies disaster messages. This can help emergency workers to categorize a meesage with one click and send it to respective relief agency.
## Result
1. ETL pipleline reads data from two files, normalizes it, applies appropriate NLP processes and stores output in SQLite database.
2. Machine Learning pipepline trains a classifier to perform multi-output classification on the 36 categories in the dataset.
3. Flask app provides data visualization, allows user enter the message on the web page and classifies it.
## Acknowledgement
Thanks to Udacity Data Scientist Nanodegree content creators for providing us the opportunity to work on this project and Figure Eight for providing the data.
