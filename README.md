# Credit_Risk_Analysis

## Project Overview

This project aims to utilize several machine learning algorithms to solve for credit card risk. The analysis is produced using the credit card credit dataset from LendingClub, a peer-to-peer lending services company. It is inherently known that the issue of credit risk is an unbalanced classification problem, due to the fact that good loans predominantly outnumber risky loans. Accordingly, various techniques and models will be applied and compared to evaluate unbalanced classes. Specifically, different resampling methods will be applied and the resulting models will be evaluated and compared in order to identify which one best minimizes bias most and predicts credit risk best. Finally, after these models are compared, it will be clear whether any (or all) are good at what they claim they do.

## Results 

Overall, there were six models that were run and applied to the data to predict for credit risk. Below is a detailed description of each model.

![](https://github.com/NoorAlKubati/Credit_Risk_Analysis/blob/main/Model1.png)
1. **Random oversampling**
    - In this model, the underrepresented class is oversampled in order to reach a comparable class to the larger one, and this is done using random sample from the smaller class that in return put back into the dataset. This model yielded a balanced accuracy score of 0.67. The average precision of this model was 0.99 and the average recall was 0.60.
![](https://github.com/NoorAlKubati/Credit_Risk_Analysis/blob/main/Model2.png)
2. **Synthetic Minority Oversampling Technique**

    - In the second model, another oversampling algorithm was employed, namely synthetic minority oversampling technique (SMOTE). This model, unlike random oversampling, new instances are interpolated into the minority class. The balanced accuracy score of this model was 0.663, which is slightly lower than the previous model. Additionally, the model's total precision was 0.99, and the average recall was 0.67. The recall rate in this model seem to be slightly better than the previous model.
![](https://github.com/NoorAlKubati/Credit_Risk_Analysis/blob/main/Model3.png)
3. **Undersampling**
    - The third model took a different approach from the previous two models. This time the majority class was undersampled in order to balance both classes. In particular is utilized cluster centroid undersampling, which is akin to SMOTE. This model produced a slightly less balanced accuracy score than the previous models, i.e., 0.53. The average precision of the model was 0.99 while the total recall across both classes was 0.39.  
![](https://github.com/NoorAlKubati/Credit_Risk_Analysis/blob/main/Model4.png)
4. **Combination (Over and Under) Sampling**
    - This particular model combines both approaches to solving the issue. It will test a combination of over- and under-sampling algorithm to determine if the algorithm results in the best performance compared to the other sampling algorithms above. It will resample the data using the SMOTEENN algorithm. This model produced a slightly less balanced accuracy score than the SMOTE model, i.e., 0.65. The average precision of the model was 0.99 while the total recall across both classes was 0.58.
![](https://github.com/NoorAlKubati/Credit_Risk_Analysis/blob/main/Model5.png)
5. **Balanced RandomForest Classifier**
    - This mdel is an ENSEMBLE model that randomly under-samples each boostrap sample to balance it. This model produced a much better balanced accuracy score than the SMOTE model, i.e., 0.93. The average precision of the model was 0.99 while the total recall across both classes was 0.85. This model by far is the best fitting model.
![](https://github.com/NoorAlKubati/Credit_Risk_Analysis/blob/main/Model6.png)
6. **Easy Ensemble AdaBoost Classifier**
    - This mdel is also another ENSEMBLE model that randomly under-samples each boostrap sample to balance it. This model produced a much better balanced accuracy score than the SMOTE model, i.e., 0.73. The average precision of the model was 0.99 while the total recall across both classes was 0.78. This model better than the SMOTE model, but is still second to the previous model.
