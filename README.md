# Module_19_Challenge
Module 19 Challenge - Neural Network Charity Analysis

## Overview of Project
This project involves using Python, Juypter Notebooks, and a number of different neural network libraries to analyze data related to organizations who have submitted funding requests to a charitable organizatio in an effort to determine the accuracy with which the neural network can predict whether an organization's request is granted or not. 

## Purpose of Analysis
The purpose of this challenge is to take a delimited text file containing a number of fields of information about each grant application, and to then utilize a neural network to determine the accuracy with which we can predict whether an organization's application is likley to be approved, adjusting our approach and our parameters as necessary in order to attempt to achieve an accuracy of greater than 75%.

## Results

- Data Preprocessing:

-- Target Variable(s)

The target variable for purposes of our analysis is the IS_SUCCESSFUL column in the dataset.

-- Features

The features we utilized to inform our neural network include:

 --- APPLICATION_TYPE
 --- AFFILIATION
 --- CLASSIFICATION
 --- USE_CASE
 --- ORGANIZATION
 --- STATUS
 --- INCOME_AMT
 --- SPECIAL_CONSIDERATIONS
 --- ASK_AMT

-- Compiling, Training, and Evaluating the Model

 --- Our Initial Parameters were:
 
![Parameters](/images/initial_params.png)

There was not any particular rationale behind the initial values which were selected; given the ease with which the parameters can be modified, and the high degree of uncertainty regarding the shape of the initial data set and the features which would be most informative, 'middle of the road' values were selected, with the understanding that there would almost certainly be a need to experiment with a number of different parameters.

--- Model Accuracy:

We were not able to obtain the requisite level of accuracy utilizing our initial model

![Initial accuracy](/images/initial_accuracy.png)

A number of efforts were undertaken to improve the accuracy of our model, including reducing the number of 'buckets' that were associated with the APPLICATION_TYPE and CLASSIFICATION features, as well as changing the activation functions that were utilized and trying a number of different permutations related to the number of layers, the composition of those layers, and the number of Epochs used to train the model.

## Sumary

Despite utilizing the kerastuner library to programatically compare a number of different parameters for our neural network, we were unable to achieve an accuracy rate above 75% with any combination of values and activation functions.

![Summary Parameters](/images/top_params.png)

![Summary Parameters](/images/top_results.png)

In an effort to determine whether or not a different machine learning approach might be more effective, we utilized the Random Forest Classifier model to serve as a point of comparison - it was no more effective than the neural network models that we tested.

At this point, there are two possible conclusions that can be drawn: 1.) our focus should turn to modifying the input features that our neural network utilizes - including the possibility of elimintating certain features which are having an adverse effect on accuracy, or changing the way in which values are binned, or, 2.) recognizing that it is possible that this is simply not an instance in which a machine learning algorithm can achieve a sufficently high degree of accuracy given the question posed and the data that is provided.
