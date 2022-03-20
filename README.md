# Überlebensvorhersage für den Titanic-Datensatz
 
## Predicting the Survival of Titanic Passengers
The RMS Titanic was a British passenger liner that sank in the North Atlantic Ocean in the early morning hours of 15 April 1912, after it collided with an iceberg during its maiden voyage from Southampton to New York City. There were an estimated 2,224 passengers and crew aboard the ship, and more than 1,500 died, making it one of the deadliest commercial peacetime maritime disasters in modern history. The RMS Titanic was the largest ship afloat at the time it entered service and was the second of three Olympic-class ocean liners operated by the White Star Line. The Titanic was built by the Harland and Wolff shipyard in Belfast. Thomas Andrews, her architect, died in the disaster.

### Overview

The data has been split into two groups:

    training set (train.csv)
    test set (test.csv)

The training set should be used to build your machine learning models. For the training set, we provide the outcome (also known as the “ground truth”) for each passenger. Your model will be based on “features” like passengers’ gender and class. You can also use feature engineering to create new features. The test set should be used to see how well your model performs on unseen data. For the test set, we do not provide the ground truth for each passenger. It is your job to predict these outcomes. For each passenger in the test set, use the model you trained to predict whether or not they survived the sinking of the Titanic. We also include gender_submission.csv, a set of predictions that assume all and only female passengers survive, as an example of what a submission file should look like.

We started with the data exploration where we got a feeling for the dataset, checked about missing data and learned which features are important. During this process we used seaborn and matplotlib to do the visualizations.

![Age%20and%20Sex](https://github.com/LiLiu1118/Survival-prediction-for-the-Titanic-dataset/blob/main/Age%20and%20Sex.png)

During the data preprocessing part, we computed missing values, converted features into numeric ones, grouped values into categories and created a few new features.
Afterwards we started training 8 different machine learning models, such as **Stochastic Gradient Descent (SGD)**, **Support Vector Machine**, **K Nearest Neighborn** and so on, picked one of them (**Random Forest**) and applied cross validation on it. Then we discussed how random forest works, took a look at the importance it assigns to the different features and tuned it’s performace through optimizing it’s hyperparameter values.
Lastly, we looked at it’s confusion matrix and computed the models precision, recall and f-score.

<p float="left">
  <img src="https://github.com/LiLiu1118/Survival-prediction-for-the-Titanic-dataset/blob/main/Precision%20Recall%20Curve.png" width="300" height="200"/>
  <img src="https://github.com/LiLiu1118/Survival-prediction-for-the-Titanic-dataset/blob/main/ROC%20AUC%20Curve.png"  width="300" height="200" /> 
</p>

For more details, please check out [titanic.ipynb](https://github.com/LiLiu1118/Survival-prediction-for-the-Titanic-dataset/blob/main/titanic.ipynb).
