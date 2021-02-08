# Disaster PIPELINE

In this project, I analyzed the disaster data in Figure eight to build a model to classify disaster messages in an API.

The dataset used contains actual messages that were sent during some disasters. For this, a machine learning pipeline was developed to categorize these events and that can send the messages to a disaster relief agency.

I also included a web application where an emergency professional can enter a new message and get ranking results in 36 different categories. The web application displays some visualizations of the ranking data.

**Project Components**

1. ETL Pipeline In process_data.py, it has a data cleaning pipeline that: Loads the messages and categories datasets Merges the two datasets Cleans the data Stores it in a SQLite database.

2. Machine Learning - ML, Pipeline In train_classifier.py: \
    a. Loads data from the SQLite database Splits the dataset into training and test. \
    b. Sets Builds a text processing and machine learning pipeline. \
    c. Trains and tunes a model using GridSearchCV Outputs results on the test set. \
    d. Exports the final model as a pickle file.

3. Flask Web App In the last step, I'll display my results in a Flask web app. There is an interface where you can classify the message.

**Execution instructions**

1. Run the following commands in the project's root directory to set up your database and model. \
    a. To run ETL pipeline that cleans data and stores in database 'python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db' \
    b. To run ML pipeline that trains classifier and saves 'python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl' \

2. Run the following command in the app's directory to run your web app. 'python run.py'

3. Go to http://0.0.0.0:3001/

**RESULTS**

![Screenshot](screenshot.png)


