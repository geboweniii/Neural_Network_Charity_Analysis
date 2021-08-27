## Overview
Deep-learning neural networks were used with TensorFlow platform in Python to analyze and classify the success of charitable donations. The following actions were performed:
- preprocessing of data for the neural network model
- compiling, training and evaluating of model
- optimizing the model

## Resources
- Data Source: [charity_data.csv](https://github.com/geboweniii/Neural_Network_Charity_Analysis/blob/main/Resources/charity_data.csv)
- Software: Python 3.9, Jupyter Notebook

## Results

### Data Preprocessing
- The columns *EIN* and *Name* were removed from the input data.
- The column *IS_SUCCESSFUL* is the target for deep-learning neural network.
- Columns *APPLICATION_TYPE*, *AFFILIATION*, *CLASSIFICATION*, *USE_CASE*, *ORGANIZATION*, *STATUS*, *INCOME_AMT*, *SPECIAL_CONSIDERATIONS*, *SK_AMT* are the features for the model.
- Encoding of the categorical variables, splitting into training and testing datasets and standardization were applied to the features.

### Compiling, Training, and Evaluating the Model
- The model is made of two hidden layers with 80 and 30 neurons respectively
- The input data has 43 features and 25,724 samples
- The output layer is made of a unique neuron
- The activation function *ReLU* was used for the hidden layers. Because the output is a binary classification, *Sigmoid* is used on the output layer
- The optimizer is *adam* and the loss function is *binary_crossentropy*
- The model accuracy is below 75% and does not help predict the outcome of the charity donations.
- Bucketing applied to the feature *ASK_AMT*
- Number of neurons on one of the hidden layers was increased and a model with three hidden layers was used.
- *tanh* function did not improve the performance of the model

## Summary
The deep learning neural network model did not reach 75% accuracy indicating it is not outperforming. A supervised machine learning model to combine a multitude of decision trees in order to generate a classified output and evaluate its performance against our deep learning model could be used.
