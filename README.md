# Credit Risk Analysis

# Overview
The purpose of this project is to use machine learning and a variety of algorithms to predict credit risk. The data used is from LendingClub, a peer-to-peer lending services company. The data is imbalanced, with a vast majority of the data being low risk. The data is cleaned and then split into training and testing data. The data is then run through a variety of algorithms to determine which is the most accurate. The algorithms used are: RandomOverSampler, SMOTE, ClusterCentroids, SMOTEENN, BalancedRandomForestClassifier, EasyEnsembleClassifier.

# Results
### Naive Random Oversampling
<details>
    <summary>Click to expand image</summary>

![Figure 1: Naive Random Oversampling](Figures/Fig1.png)
</details>

- The balanced accuracy score is 61.7%
- The precision for high risk is 1%
- The recall for high risk is 63%
- The precision for low risk is 100%
- The recall for low risk is 62%

### SMOTE Oversampling
<details>
    <summary>Click to expand image</summary>

![Figure 2: SMOTE Oversampling](Figures/Fig2.png)
</details>

- The balanced accuracy score is 62.1%
- The precision for high risk is 1%
- The recall for high risk is 54%
- The precision for low risk is 100%
- The recall for low risk is 70%

### Undersampling: Cluster Centroids
<details>
    <summary>Click to expand image</summary>

![Figure 3: Undersampling: Cluster Centroids](Figures/Fig3.png)
</details>

- The balanced accuracy score is 50.6%
- The precision for high risk is 0%
- The recall for high risk is 48%
- The precision for low risk is 100%
- The recall for low risk is 53%

### Combination Sampling: SMOTEENN
<details>
    <summary>Click to expand image</summary>

![Figure 4: Combination Sampling: SMOTEENN](Figures/Fig4.png)
</details>

- The balanced accuracy score is 62.7%
- The precision for high risk is 1%
- The recall for high risk is 63%
- The precision for low risk is 100%
- The recall for low risk is 62%

### Balanced Random Forest Classifier
<details>
    <summary>Click to expand image</summary>

![Figure 5: Balanced Random Forest Classifier](Figures/Fig5.png)
</details>

- The balanced accuracy score is 78.8%
- The precision for high risk is 3%
- The recall for high risk is 70%
- The precision for low risk is 100%
- The recall for low risk is 87%

### Easy Ensemble AdaBoost Classifier
<details>
    <summary>Click to expand image</summary>

![Figure 6: Easy Ensemble AdaBoost Classifier](Figures/Fig6.png)
</details>

- The balanced accuracy score is 93.2%
- The precision for high risk is 9%
- The recall for high risk is 92%
- The precision for low risk is 100%
- The recall for low risk is 94%

# Summary
Overall, most of the machine learning models do not preform particularly well. All 6 of the models had a precision rate of 100% for low risk, as precision is a measure of how reliable a positive classification is, this means that the models were able to correctly predict low risk 100% of the time. However, for this data this statistic is irrelevant. As the data is extremely imbalanced, with about 0.5% of the data being high risk, even if a model predicted all high risk as low risk, the precision rate would still be 100%.

Both of the oversampling models had recall rates from between 54%-70% and only 1% precision rate for high risk. Both of their balanced accuracy scores were around 62%. While this accuracy score is not particularly good, their precision rate for high risk also disqualifies them as usable models.

The undersampling model using cluster centroids had a high risk recall rate of 48%, a low risk recall rate of 53% and a high risk precision rate of 0%. With an even worse balanced accuracy score of 50.6%, this model is also not usable.

The final resampling model, SMOTEENN, which is a combination of over and under sampling, had a high risk recall rate of 63%, a low risk recall rate of 62% and a high risk precision rate of 1%. With a balanced accuracy score of 62.7%, this model is also not usable.

Finally, both ensemble models had a significant improvement over the resampling models. While both precision rates for low risk were still 100%, the balanced random forest classifier had a high risk recall rate of 70%, a low risk recall rate of 87% and a high risk precision rate of 3%. With a balanced accuracy score of 78.8%, this model is much better than the previous, but did not preform quite as well as the final model.

The easy ensemble AdaBoost classifier had a high risk recall rate of 92%, a low risk recall rate of 94% and a high risk precision rate of 9%. With a balanced accuracy score of 93.2%, this model is the best of the 6 models. With a balanced accuracy score of 93.2%, this is the best model of the 6 models. While other models not explored here may have a higher precision rate for high risk, of the 6 models here, this can be recommended as the best model to use.