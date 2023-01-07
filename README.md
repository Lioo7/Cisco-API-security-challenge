# Cisco-API-security-challenge
Cisco - Ariel University API Security Detection Challenge 2023

![Python](https://img.shields.io/badge/python-3.6+-3670A0) ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg) ![NumPy](https://img.shields.io/badge/numpy-%23013243.svg) ![Seaborn](https://img.shields.io/badge/seaborn-%23282B2C.svg) ![json](https://img.shields.io/badge/json-%232F3F4F.svg) ![XGBoost](https://img.shields.io/badge/XGBoost-%23D7A741.svg) ![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg) ![matplotlib](https://img.shields.io/badge/matplotlib-%2324292E.svg) ![collections](https://img.shields.io/badge/collections-%2324292E.svg)

## Description
This competition is focused on predicting and classifying malicious and benign API traffic using machine learning models. There are four datasets provided, with the goal of achieving the highest prediction scores. Each dataset is divided into Train (70%), Test (15%), and Validation (15%) sets. The train-test split is done within the code, and the validation split is provided without labels for later grading.

All the datasets contain HTTP traffic of API requests and responses. The datasets differ in the number and type of attacks and endpoints, and the complexity of the parameters in the requests.

## Attacks
The datasets in this competition contain API traffic with both malicious and benign requests. Malicious requests, also known as attacks, are designed to disrupt or exploit the functionality of an API or the underlying system. Examples of attacks that may be included in the datasets are:

* SQL injection attacks: These attacks involve injecting malicious code into an SQL query in order to gain unauthorized access to data or disrupt the operation of the database.

* Directory traversal attacks: These attacks involve using basic terminal traversal strings to reach folders on the server's host that were not meant to be accessed by the user.

* Remote code execution (RCE) attacks: These attacks allow the attacker to run code remotely on the local machine, potentially giving them full control over the system.

* Cookie injection attacks: These attacks involve injecting cookies into a session that were not originated from it, potentially allowing the attacker to access another user's account illegitimately.

* Cross-site scripting (XSS) attacks: These attacks involve injecting malicious code into a website, often through a form field or URL parameter, in order to execute code in the browser of a user who visits the site.

* Log4J attacks: A recently patched vulnerability in JAVA servers that used the Apache logging library, enabling the attacker to run code remotely on the server (a form of RCE).

* Log forging attacks: A technique used to print fake or fraudulent logs, potentially enabling the attacker to "inject" other user logs or fake their own attack logs in order to cover their tracks.

Our mission was to accurately identify and classify these attacks in order to secure APIs and protect against potential threats.
For more information, please read the attacks glossary and features glossary files that we have written.

## Solution
Our solution to this competition involves building six machine learning models, one for each dataset, using the XGBoost library. XGBoost is a popular and powerful library for gradient boosting, which has shown to be effective for many types of prediction tasks.

There are several advantages to using XGBoost for this task:

* Efficiency: XGBoost is known for its fast training times and ability to handle large datasets. This is important for a task like this, where we are working with multiple datasets of API traffic.

* Accuracy: XGBoost has been shown to achieve high levels of accuracy on a wide range of prediction tasks, including those involving structured or tabular data.

* Flexibility: XGBoost allows for the use of a wide range of parameters and configurations, making it possible to fine-tune the model to the specific characteristics of the dataset.

## Results
After training and testing our models on the provided datasets, we achieved perfect scores for all the models, with 'Accuracy': 1.0, 'Precision': 1.0, 'Recall': 1.0, and 'F1': 1.0.

<div style="text-align:center">
  <img src="https://i.ibb.co/nn8t9xK/Untitled-6.jpg" width="50%" />
  <img src="https://i.ibb.co/qByGGSG/Untitled-5-copy.jpg" width="50%" />
</div>

## Datasets Download Link:
[All Datasets zip file](https://drive.google.com/file/d/15MxHRAdwPXCENACwn8wLMkb98ZCjDeh6/view?usp=share_link)

## Requirements
* Python 3.6 or higher
* Pandas library for data manipulation and analysis
* NumPy library for numerical computing
* Seaborn library for data visualization
* json library for working with JSON data
* XGBoost library for gradient boosting
* GridSearchCV class for hyperparameter tuning
* scikit-learn library for machine learning, including:
   * train_test_split function for splitting data into training and test sets
   * CountVectorizer, HashingVectorizer, and LabelEncoder classes for feature extraction and preprocessing
   * confusion_matrix and classification_report functions for evaluating model performance
* matplotlib library for plotting
* collections library for counting occurrences of items in a list