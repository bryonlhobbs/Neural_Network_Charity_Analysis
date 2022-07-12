# Neural_Network_Charity_Analysis

## Overview
The objective of this project was to analyze the success of Alphabet Soup's allocation of funds in its charitable endeavors.  With dat asupplied by the rganization, I built a Neural Network to analyze the data for trends and results.

## Results
This analysis was not strong.  The training maxed out at 0.5321 accuracy in any given epoch.  However, the overall accuaracy reported was even lower.

### Data Preprocessing
The target variable I discerned was the "IS_SUCCESSFUL" column in the raw data.  All of the other factors are suggested to lead to an outcome of successful or unsuccessful.  In this model, the features were the following data points: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT.  EIN and NAME were seen as identifiers for each record, and were removed before analysis.

### Compiling, Training, and Evaluating the Model

The initial layers were set up as follows:

<img width="952" alt="Hidden_Layers" src="https://user-images.githubusercontent.com/99457275/178535636-1d715664-e411-4801-abf7-5a6cbf2ecf0b.png">

The number of nodes is high, but the belief was that it would make the model compute faster and more accurately.  The speed was certainly realized, but the accuracy was not.  I used a "relu" function to help elimiate any possibility of negative numbers throuwing off the analysis.

First Attempt:
<img width="836" alt="Original_Accuracy" src="https://user-images.githubusercontent.com/99457275/178532780-0a20c37e-fee0-4369-9cf6-09d3210272e4.png">

With Optimiztion:
<img width="831" alt="Accuracy" src="https://user-images.githubusercontent.com/99457275/178532257-d3f4c9e2-bb32-4b28-9c4e-cbc3bb62f013.png">

Even with multiple attempts at optimization, nothing improved the results. I tried removing the "SPECIAL_CONSIDERATIONS" column, as well as adding an extra hidden layer with 10 nodes.  I also tried a different activation function, "sigmoid", to see if it would improve the results.  Unfortunately, while the loss shrunk considerably, the accuracy slightly decreased.

## Summary
In conclusion, this data did not offer a strong relationship between the inputs and the outcome of fund allocation.  It should be noted that more attempts at optimization may yield a stronger correlation.  Also, we may need other data to better understand the full picture.  One recpommendation is to try a Random Forests model.  I choose this model because it tends to succeed at classification tasks by leaning into repeatable correlations with a high success rate.

