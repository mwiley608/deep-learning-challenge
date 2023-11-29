# deep-learning-challenge
Bootcamp Module 21 Challenge

## Requirements
This project was created using Google Colab.

![application](./Resources/application.jpg)

## Overview of the Analysis
This project uses machine learning and neural networks to create a tool for a fictinal nonprofit foundation, Alphabet Soup. The tool creates a binary classifier that can predict whether or not applicants for funding will be successful.

![form](./Resources/form.jpg)

## Results
The deep learning model created in this project used 3 steps. The AlphabetSoupCharity.ipynb file used steps 1 and 2. Methods to optimize the model in step 3 were used in the AlphabetSoupCharity_Optimization.ipynb file.

### 1 - Data Preprocessing
    * The "IS_SUCCESSFUL"variable is the target for the model

    * The features for the model are:
        * APPLICATION_TYPE—Alphabet Soup application type
        * AFFILIATION—Affiliated sector of industry
        * CLASSIFICATION—Government organization classification
        * USE_CASE—Use case for funding
        * ORGANIZATION—Organization type
        * STATUS—Active status
        * INCOME_AMT—Income classification
        * SPECIAL_CONSIDERATIONS—Special considerations for application
        * ASK_AMT—Funding amount requested

    * The varibales "EIN" and "NAME" were removed from the input data because they were neither targets nor features in the original model.

### 2 - Compile, Train, and Evaluate the Model
    * Multiple neurons, 3 layers and 2 activation functions were used in the original model. Multiple neurons and layers were used to appropriately weight the input information. The relu function was used for the two hidden layers to transform any negative input to 0, allowing for faster learning and simplified output. The sigmoid function was used for the output layer because it transforms the neuron's output to a range between 0 and 1, useful for predicting probabilities. 

    * The orignal model only achieved a target model performance of 72.5%; however, through optimization the model was able to meet the >75% accuracy target.

### 3 - Optimize the Model
    * Through optization, the accuracy of the model increased from 72.5% to 79.8%.

    * Several steps were taken to increase the accurancy of the model:

        * First, the number of epochs was reduced from 100 to 50 to retrain the model since it was a smaller, simpler dataset, but this did not affect the accuracy.

        * Second, an additional hidden layer was added, but again it did not improve the accuracy to >75%

        * Finally, the "NAME" variable was reintroduced as a feature and included in the model if it appeared 2 or more times in the dataset. Including "NAME" as a feature can train the model on the liklihood that repeat applicants would be successful. 

    * The final adjustment to the model increased the accuracy to 79.8%.

## Summary
Overall the optimization model has a 79.8% chance of accurately predicting whether an applicant will be successful if funded by Alphabet Soup, leading to more successful ventures. 

An alternative classification model for this project would be a Decision Tree or more specifically a Random Forest model to increase the accuracy. A Random Forest model combines the output of multiple decision trees to reach a single result. In this case, success rate of the funded venture. 

![success](./Resources/success.jpg)

## Resources
* Data for this dataset was sourced from the IRS. Tax Exempt Organization Search Bulk Data Downloads. https://www.irs.gov/Links to an external site.

* Royalty free clipart was found at pexels.com

* Information on Random Forest model was found at: https://www.ibm.com/topics/random-forest