# Module 21 Challenge: Neural Network and Deep Learning
---

<b>Programming language:</b> Python <br />
<b>Package used:</b>sklearn, tensorflow, pandas and numpy <br />
<b>Main script:</b> [deep-learning-py.ipynb](https://github.com/wingylui/deep-learning-challenge/blob/main/deep-learning-py.ipynb), [Optimisation-deep-learning-py.ipynb](https://github.com/wingylui/deep-learning-challenge/blob/main/Optimisation-deep-learning-py.ipynb)<br />
<b>Dataset:</b> [charity_data.csv](https://static.bc-edx.com/data/dla-1-2/m21/lms/starter/charity_data.csv)

---
## Overview

In this challenge, a model is built to help selecting applicants that have a better chance of success. A nonprofit foundation, Alphabet Soup, has funded more than 34,000 organisations in the past. Using the successful and unsucessful cases from previous data, a deep learning mdoel is developed to predict an organisation will be more likely to be successful or not. The model will consider several characterisitic of organisation, such as, application type, organisation type, affiliated sector of industry etc.

---
## Results

### Data Preprocessing

In data preprocessing, the columns were modified as follow:
* <b>Target variable of this model:</b> IS_SUCCESSFUL </br>
* <b>Features variables of this model：</b>APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT </br>
* <b>Rmoved variables from the dataset:</b> EIN, NAME </br>
</br>

### Compiling, Training, and Evaluating the Model

At the beginning, I started with a small number of neurons and layers
* <b>Number of layers:</b> input layer, two hidden layers and output layer
* <b>Number of neurons:</b> 30, 10 and 1</br>
Reason: the output layer always require only one neuron because there will be only one result output from the model (success or not success)
* <b>Activation functions:</b> ```relu``` for input and hidden layer, ```sigmoid``` for output layer; </br>
Reason: All the features variables are positive and the target variable is a binary variable


<b>Steps attempt to imporve model performance: </b>
* Increased the numbers of nuerons
* Increased the numbers of hidden layers
* Adjusted the ratio of trainning and testing data
* Creating more bins for rare occurrences in columns
* Adding the number of epochs to the training regimen

Unfortunately, the model performance still not improved after all the changes 

---

## Summary

The loss and accuracy of this model are 0.831 and 0.729, which is not great because accuracy is low and loss is high. The loss does not decrease while training this model, indicating that this model was not learning. I will recommend using random forrest or decision tree to solve this classification problem because it is another model that can handle both both numerical and categorical data and preformed well with large datasets.


---
<b>Score for this assessment:</b> has not been graded yet <br />
<b>References:</b><br />
IRS. Tax Exempt Organization Search Bulk Data Downloads. https://www.irs.gov/


