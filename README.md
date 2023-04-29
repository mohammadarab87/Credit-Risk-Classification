# Credit Risk Classification

## Credit Risk Analysis :

## ***Overview:***
* The purpose of this analysis is to develop a machine learning model that can predict whether a loan applicant is at high risk of defaulting on a loan.

* The data used for this analysis includes financial information on loan applicants, including

***loan size***, ***interest rate***, ***borrower income***, ***debt-to-income ratio***, ***number of accounts***, ***derogatory marks***, ***total debt***, and ***loan status***.

* The ***loan status variable*** is our target variable and it has two values: 

***(0) represents a healthy loan*** and ***(1) represents a high-risk loan***.

* The ***value counts*** of the target variable show that we have an imbalanced dataset, with 75036 healthy loans and only 2500 high-risk loans.


* I went through several stages of the machine learning process, including data cleaning and preparation, feature selection, model selection, and model evaluation.
For the model selection, we used the Logistic Regression algorithm and oversampling using the Random Over Sampler technique

## ***Results:***

I used two classification reports to evaluate the performance of the model: ***testing_report*** and ***ros_testing_report***.

***1-testing_report Original Data***

![image](https://user-images.githubusercontent.com/113273722/235303705-9e3d0853-ecd3-4ca3-9f10-0e18103cdfbd.png)

The precision score for predicting high-risk loans is 0.85, which means that out of all the loans predicted as high-risk, 85% are actually high-risk.
The recall score for predicting high-risk loans is 0.91, which means that out of all the high-risk loans, 91% are correctly identified by the model.

***2-ros_testing_report Resampled Training Data (ROS)***

![image](https://user-images.githubusercontent.com/113273722/235304041-5faf4546-0818-4426-b508-c2abcf810f60.png)

shows that the accuracy score of the model is also 0.99.
The precision score for predicting high-risk loans is 0.84, which means that out of all the loans predicted as high-risk, 84% are actually high-risk.
The recall score for predicting high-risk loans is 0.99, which means that out of all the high-risk loans, 99% are correctly identified by the model

## ***Summary:***

Based on the evaluation results, both models perform well in terms of accuracy, with an accuracy score of 0.99.

However, when comparing the precision and recall scores, ***ros_testing_report*** seems to perform better in predicting high-risk loans, with a higher recall score of 0.99, which means that the model is able to correctly identify almost all of the high-risk loans. In contrast, testing_report has a slightly lower recall score of 0.91, indicating that some high-risk loans might be missed by the model.

With incorrect predictions we have two issues:
False positives (where users are flagged as risky, but are actually healthy) and 
False negatives (where users are not flagged as risky but are actually risky)

***In conclusion*** 

I recommend using the model trained using the Random Over Sampler technique, as it has better performance in identifying high-risk loans. However, it is important to note that the model may still miss some high-risk loans, and it may be beneficial to collect more data on high-risk loans to improve the model's performance
