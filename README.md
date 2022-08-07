# Neural_Network_Charity_Analysis

## Overview

Alphabet Soup is a foundation dedicted to helping organizations that protect the environment, protect people's wellbeing and unify the world.  The foundation needs a tool to determine which organizations are worth donating to and which are too high risk so they know their funds are being used effectively.  The purpose of this analysis is to develop a neural network to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

The dataset used for this analysis includes data from more than 34,000 organizations that have received funding from Alphabet Soup.  The following steps will be completed to build the neural network:

* Preprocess the data
* Compile, Train and Evaluate the Model
* Optimize the Model
    
## Results
    
### Data Preprocessing

* The target variable for this model is the "IS_SUCCESSFUL" category.  

* The variables considered to be features of the the model include all of the columns except "IS_SUCCESSFUL" as the target variable and "EIN" and "NAME" as they were       dropped.  These other variables include application type, affiliation, classification, use case, organization, status, income amount and ask amount.     

![features](https://user-images.githubusercontent.com/100876517/183309432-fa08233f-d710-493f-8407-82f3088006ee.png)


* Variables that were neither targets or features for the dataset were "EIN" and "NAME" as these 2 variables will have minimal impact of the outcome.

### Compiling, Training and Evaluating the Model

* The model includes two hidden layers with 80 neurons in the first layer and 30 in the second layer.  The neural network contains 2 hidden layers and an output layer with the activation functions being relu, relu and sigmoid.  The number of neurons was selected based on the input layer and decreasing the neurons for the second hidden layer.  The relu function was choose for the hidden layers to speed up the training process.


![model image](https://user-images.githubusercontent.com/100876517/183309435-bfc22fb2-ec85-45e4-b5e7-7575021745fb.png)


* The target model performance was not achieved with the original model.  The accuracy rate was 72.62%.

![model results](https://user-images.githubusercontent.com/100876517/183309436-074d2ada-6263-4b84-81b6-67f4869b348e.png)

* To increase the model performance, the model was optimzed with three scenarios. 
       
   _The first optimization removed an additional variable from the data set.  This variable was
    "SPECIAL_CONSIDERATIONS".  The accuracy rate was 72.49%.
       
   _The second optimization then changed the output layer from sigmoid to tanh.
    The accuracy rate was 72.48%.
       
   _The third optimization was updated to change the number of neurons.  Layer One was
     changed from 80 to 150.  Layer Two was changed from 30 to 75.  The accuracy rate was 72.51%

## Summary

The neural network did not reach the target accuracy of 75% with the original model or the 3 optimized attempts.  With all attempts, the accuracy rate was in the 72.5% range.  Since this is a binary classification, a random forest classifier may be an alternate solution to achieve the target accuracy of 75% and run more efficiently than the current neural network.


