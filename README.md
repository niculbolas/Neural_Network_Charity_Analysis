# Neural_Network_Charity_Analysis

## Overview:
The purpose of this project was to review a large set of data for a charity and use neural net machine learning to see if a reasonable model could be fit to the data.  The purpose of the model is to make a binary decision for whether or not the charity, Alphabet Soup, should fund the request for aid from the requesting organization based upon chance of success.  The data provided for us to use consists of past charity data for over 34,000 organizations that have been previously funded by Alphabet Soup.  For the purposes of machine learning the tensorflow Python module was utilized along with scikitlearn.

## Results
- What variable(s) are considered the target(s) for your model?

  - The IS_SUCCESSFUL category from the csv was the target of the constructed model.  If the value is 1, the request was successful, 0 if it was not.

- What variable(s) are considered to be the features for your model?
  - The variables which are considered features for the model are application type, affilation, classification, use case, organization, income amount, special considerations, and asking amount.  The categorical variables here were given to OneHotEncoder to transform into useable data.
  
- What variable(s) are neither targets nor features, and should be removed from the input data? 
  - The variables EIN and Name were removed from the data after importing the csv because they are neither features or targets for the nn model.
  
- How many neurons, layers, and activation functions did you select for your neural network model, and why?
  - For the original model I chose to go with a sigmoid activation with 80 units as the first hidden layer, a relu activation with 30 units for the 2nd hidden layer, and for the output a linear activation with 1 unit.  I chose 80 as the starting hidden layer due to the 2-3 times your input guideline as a starter model.  I chose sigmoid and relu after playing around a bit to see which gave better initial results.
  
- Were you able to achieve the target model performance?
  - Sadly I was unable to reach the target performance level even after making several adjustments.
    - Initial run had an accuracy of 69.4%
    - The first optimization run had an accuracy of 71%.
    - The 2nd optimization run had an accuracy of 46.8%.  A disappointing drop in accuracy.  For this one I tried increasing the number of units in each layer.
    - The final optimization attempt had an accuracy of 71.2%.  For this one I added a few extra neural layers.
    
- What steps did you take to try and increase model performance? 
  - See points above this question.
  
## Summary

In conclusion, using the nueral net machine learning I was unable to get results above 71.2% despite making several tweaks to the model itself.  In the future, I might have more luck looking for noisy data and removing it.  Something else to consider is trying a more basic machine learning model first.  I would suggest trying the balanced forest classifier as it is good at making binary decisions.  If that didn't pan out, then perhaps try the nueral net machine learning again.
