# Credit_Risk_Analysis

# Overview
The purpose of this analysis was to help LendingClub, a peer-to-peer lending services company, identify low-risk and high-risk loans using machine learning. I used three different machine learning models to make predictions: logistic regression, balanced random forest classifier and easy ensemble AdaBoost classifier. Since low-risk loans greatly outnumbered high-risk loans in the dataset, I had to resample the data to get an even amount of target values so that the machine learning algorithm would make more accurate predictions.

# Results
As stated above, low-risk loans greatly outnumbered high-risk loans:

<img width="115" alt="image" src="https://user-images.githubusercontent.com/79022140/231609428-c4c74dbb-aa79-4c16-b33c-fafe2a4b9dbf.png">

So before training the machine learning model, I had to resample the data.

Here are the results from oversampling the data and using logistic regression to make predictions...

## Oversampling

### Random Oversampling

<img width="502" alt="image" src="https://user-images.githubusercontent.com/79022140/231610863-3ac2de67-8678-43cf-b3de-d1e31d114ee9.png">

* 66% of the predictions were correct
* On average, precision was very high (99%) but this is misleading because the precision for high-risk and low-risk loans varied greatly (1% and 100% respectivly).
* Average recall was 60%. 72% for high-risk and 60% for low-risk  

### SMOTE Oversampling

<img width="483" alt="image" src="https://user-images.githubusercontent.com/79022140/231611734-5fd646d9-7543-4396-a3a9-de3104e76a5a.png">

* 66% of the predictions were correct
* Once again, average precision was very high at 99% but varied greatly between the high-risk and low-risk
* Average recall was 69%. 62% for high-risk and 69% for low-risk

## Undersampling

Here are the results from undersampling (also using logistic regression for predictions)

### Cluster Centroids

<img width="483" alt="image" src="https://user-images.githubusercontent.com/79022140/231613164-d3e760ab-f163-4b07-8fb4-73d484391979.png">

* Accuracy score was slightly lower at 54%
* Average precision was 99%. 1% for high-risk and 99% for low-risk
* Average recall was 40%. 69% for high-risk and 40% for low-risk


## Combination Sampling

Here are the results from combination sampling (oversampling and undersampling) (also using logistic regression for predictions)

### SMOTEENN

<img width="483" alt="image" src="https://user-images.githubusercontent.com/79022140/231613884-8d90fef4-f10a-4707-8eca-0fe4ab4125f9.png">

* Accuracy score was 63%
* Average precision was 99%. 1% for high-risk and 99% for low-risk
* Average recall was 60%. 65% for high-risk and 60% for low-risk

## Balanced Random Forest Classifier 

<img width="482" alt="image" src="https://user-images.githubusercontent.com/79022140/231617840-486add4a-aa33-4ffa-bd20-2616eac54bb8.png">

* Accuracy score was high at 79%
* Average precision was 99%. 3% for high-risk and 99% for low-risk
* Average recall was 87%. 70% for high-risk and 87% for low-risk

## Easy Ensemble AdaBoost Classifier

<img width="482" alt="image" src="https://user-images.githubusercontent.com/79022140/231618517-d115ac09-d243-48d9-96cd-6808d7306977.png">

* Accuracy was very high at 93%
* Average precision was 99%. 9% for high-risk and 99% for low-risk
* Average recall was 94%. 92% for high-risk and 94% for low-risk

# Summary
