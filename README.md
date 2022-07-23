# supervised-learning-challenge
Supervised Machine Learning

## Introduction to Logistic Regression
Logistic Regression is a supervised learning classification algorithm used to predict the probability (outcome) of a binary target variable or a discrete set of classes/categories. The key function used in Logistic Regression is the *logistics function*. Logistic Regression is a linear model at its core with the outcome transformed using the logistics function to return a probablitiy value. It's similar to linear regression in that both use some kind of equation at the representation, except in Logistic regression the output values modelled are *binary values* (yes/no, old/young, 0/1) and in linear regression are *numerical values*. 

## Introduction to Random Forest Classifier
Random Forest Classifier is a supervised learning classification algorithm that utilises the BAGGing Ensemble Methods which relies on more than one Decision Tree. It's called  BAGGing or Bootstrapping and Aggregating because it combines **Bootstrapping**: multiple *bootstrapped* subsamples are taken from a sample of data and a Decision Tree is formed on each of the bootstrapped subsamples. 
And **Aggregating**: An algorithm is used to *aggregate* over the Decision Trees to form the most efficient predictor after each subsample Decision Tree is formed. Random Forest differs in that the models decide where to split the data based on **random features** whereas BAGGed Decision Trees split at the **same features**. The idea behind BAGGing is that a combination of learning models increases the overall accuracy.



### **My Prediction before I fit both models**

Knowing all this beforehand I predicted the Logistic Regression would do best with the dataset we are modelling as we are looking at whether a loan will be approved or not (Credit Risk). My prediction is based on LogisticsRegression doing better with categorical data than Random Forrest Classifiers even though RandomTrees can handle both categorical and numerical variables. I believe that Logistic Regression would outperform Random Forest even more on scaled data which woudl make it win out.

### Result
**Before scaling the data**

- LogisticRegression **Training score:**  0.9921240885954051

- LogisticRegression **Test score:**  0.9918489475856377

- RandomForestClassifier **Training score:**  0.9975409272252029

- RandomForestClassifier **Test score:**  0.9914878250103177

**After scaling the data**

- Scaled LogisticRegression ** **Training score:**  0.9942908240473243

- Scaled LogisticRegression **Test score:**  0.9936545604622369

- Scaled RandomForestClassifier **Training score:**  0.9975409272252029

- Scaled RandomForestClassifier **Test score:**  0.9915910028889806


## Conclusion

Strangely both models performed really well before and after scaling the data and there weren't great difference in between the two models or on the scaled vs unscaled data. There doesnt seem to be any overfitting either, test and training scores are very similar. My first impression after seeing this result I thought something went wrong as I'm not very experienced with Machine Learning but after looking into it further and creating a confusion matrix from both models test data I think both models performed well on this particular dataset loking at the accuracy scores but further training of data and different models could bring more clarity on this.

![Screenshot 2022-07-23 at 22 09 50](https://user-images.githubusercontent.com/67019030/180622971-5e5c4877-0098-47e5-b7a5-179c9418fc98.png)



# Supervised Machine Learning Homework - Predicting Credit Risk

In this assignment, you will be building a machine learning model that attempts to predict whether a loan will be approved or not. 

## Background

Lending services companies allow individual investors to partially fund personal loans as well as buy and sell notes backing the loans on a secondary market. This data will be used to 

You will be using this data to create machine learning models to classify the risk level of given loans. Specifically, you will be comparing the Logistic Regression model and Random Forest Classifier.

## Instructions

### Retrieve the data

The data is located in the Resources folder.

* `lending_data.csv`

Import the data using Pandas.

## Consider the models

You will be creating and comparing two models on this data: a logistic regression, and a random forests classifier. Before you create, fit, and score the models, make a prediction as to which model you think will perform better. You do not need to be correct! Write down (in markdown cells in your Jupyter Notebook or in a separate document) your prediction, and provide justification for your educated guess.

## Fit a LogisticRegression model and RandomForestClassifier model

Create a LogisticRegression model, fit it to the data, and print the model's score. Do the same for a RandomForestClassifier. You may choose any starting hyperparameters you like. Which model performed better? How does that compare to your prediction? Write down your results and thoughts.

## Rubric

[Unit 19 - Supervised Machine Learning Homework Rubric](https://docs.google.com/document/d/1eZcQul7s2gy6h9flygyPdajSPUtqOQUuGL1XXcuX6p4/edit?usp=sharing)

### References

Loan Approval Dataset (2022). Data generated by Trilogy Education Services, a 2U, Inc. brand, and is intended for educational purposes only.

- - -

© 2021 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.
