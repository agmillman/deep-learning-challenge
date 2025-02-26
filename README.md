# Deep Learning Challenge - Alphabet Soup Funding Analysis

# Overview
Leverage a deep learning model to to analyze a CSV file containing more than 34,000 organizations to predict whether applicants will be successful if funded by Alphabet Soup.

# Results
- What variable(s) are the target(s) for your model?
  The single target is the IS_SUCCESSFUL column.  This column will be used to predict which applicants will be successful.

- What variable(s) are the features for your model?
  Features available are: EIN, NAME, APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT

- What variable(s) should be removed from the input data because they are neither targets nor features?
  Variables removed were EIN and NAME

- How many neurons, layers, and activation functions did you select for your neural network model, and why?
  - Original Code: 72.33 Predicted Accuracy
    - Activation function(s): relu
    - Layers: 2
    - Neurons: 80, 30

  - Optimization Attempt 1: 72.64% Predicted Accuracy
    - Activation function(s): relu
    - Layers: 3
    - Neurons: 128, 64, 32

  - Optimization Attempt 2: 72.68% Predicted Accuracy
    - Activation function(s): tanh
    - Layers: 4
    - Neurons: 128, 64, 64, 32

  - Optimization Attempt 3: 72.26% Predicted Accuracy
    - Activation function(s): relu, tanh, relu, tanh
    - Layers: 4
    - Neurons: 50, 256, 25, 64

  - Optimization Attempt 4: 72.59% Predicted Accuracy
    - Activation function(s): tanh, relu, tanh, relu
    - Layers: 4
    - Neurons: 150, 125, 110, 64

- Were you able to achieve the target model performance?
  I was not able to achieve the target of 75% predicted accuracy.

- What steps did you take in your attempts to increase model performance?
  Modifying the number of hidden layers, varying the number of neurons, different combinations of activation functions, and increasing the epochs to 100.

# Summary
The highest predicted accuracy achieved was 72.68% using the tanh activation function exclusively across 4 hidden layers with varying numbers of neurons.  I feel this model was the most appropriate since tanh is strong when working with binary data.  An alternative approach that may achieve the 75% is XGBoost.  XGBoost works well with structured data and often outperforms deep learning models in classification tasks.
