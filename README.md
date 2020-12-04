# Starbucks Capstone Challenge
## Capstone Project for Udacity's Data Science Nanodegree Program

This capstone project to complete the Udacity's Data Science Nanodegree Program. 

## Table of Contents

1. [Project Motivation](#project_motivation)
2. [Files Descriptions](#files_descriptions)
3. [Python Libraries](#python_libraries)
4. [Results Summary](#results_summary)
5. [Acknowledgement](#acknowledgement)

<a name="project_motivation"></a>
## Project Motivation
This capstone project to complete the Udacity's Data Science Nanodegree Program. Starbucks has provided the simulated data that mimics the customers' behavior on different kinds of rewards sent through the mobile app. I have developed a machine learning model to 1) find the offer that a customer ends up un buying the products. 2) find the customer who buys the product without the influence of the offer. The description of the entire process adopted can be found in the file   **project_capstone.pdf** and a [bolgpost](https://anup-pandey123.medium.com/starbucks-capstone-challenge-4a763b207985).

<a name="files_descriptions"></a>
## Files Descriptions

The enitre process adopted are carried out in four notebooks.
    
        1.  Data_exploration.ipynb: Data exploration is carried out in this notebook.
        2.  Data_cleaning.ipynb: Data cleaning and feature engineering is carried out in this notebook.
        3.  EDA.ipynb: Exploratory data analysis of the cleaned data is carried out in this notebook.
        4.  Data_modeling: Data scaling and machine learning models are trained in this notebook
        
        The data files are explained in details in the notebooks as well as in the project_capstone.pdf file.

Step-by-step description of the entire process adopted in the project is explained in the file **project_capstone.pdf** and a [bolgpost](https://anup-pandey123.medium.com/starbucks-capstone-challenge-4a763b207985).

<a name="python_libraries"></a>
## Python Libraries

<a name="results_summary"></a>
## Results Summary

I have tried the following five models and considered the model **accuracy** score as the metric to evaluate the model quality.
           i.  **Neural Network**: A simple feed-forward neural network (NN) has been implemented to classify the response to the offers. This model is considered     			as a benchmark and all the other models’ performance is compared with it.
	   ii. ***Decision Tree Classifier**
          iii. **K-nearest Neighbors**
	   iv. **Random Forest**
	    v. **Support Vector Machine**
	    
The features used in training the models are a reward, difficulty, offer_duration_hrs, BOGO, discount, informational, mobile, social, web, age_group, became_member_on, income, income_group, F, M, N, O.


All the five models described above are trained on the training set and evaluated on the testing set. The size of the training set is 53393 and the testing set is 2284. The comparison of the models’ accuracy is shown in the table below. 
The benchmark model neural network has a training and testing accuracy of ~64%. Decision Tree has a training accuracy of 94.64% and a testing accuracy of 57.77%. Similarly, K-Nearest Neighbor has the training and testing accuracy of 68.82% and 61.48%, respectively. Random Forest has a training accuracy of 94.64% and a testing accuracy of 59.76%. Support Vector Machine has a training accuracy of 60.90% and a testing accuracy of 61.39%.
Out of five models, I have considered Random Forest and K-Nearest for further refinements. Random Forest has high train accuracy and relatively lower test accuracy. This means the model is behaving differently for the training and testing sets. On the other hand, the K-Nearest Neighbor has both the training and testing accuracy in the same range. 
	After refinements, the Random Forest has a training accuracy of 65.40% and a testing accuracy of 64.70%. Thus, the tuned parameters behave in a similar way for both data sets.

Similarly, after refinements, the K-Nearest Neighbor has the training and testing accuracy of 73% and 60.8%, respectively. 

Out of the two refined models, we take the Random Forest as the best classifier because of its better testing accuracy. 

For the nature of the problem chosen and the given data sets, we are convinced that the final model reached a good accuracy. The customers’ behavior for an offer can be varying and that could be a reason for the model to have medium accuracy.

<a name="acknowledgement"></a>
## Acknowledgement
* We want to thank [Udacity](https://www.udacity.com/) for this project and **Starbucks** for the data sets.

