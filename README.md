# Bankruptcy Prediction Using SAS Enterprise Miner

This repository contains the final project for Data Mine, focused on predicting bankruptcy using SAS Enterprise Miner. The project includes both the Neural Network and Gradient Boosting models, alongside various preprocessing techniques and model comparisons.

## About the Dataset

- **Independent Variables:** 64
- **Dependent Variable:** 1
- **Training Dataset:** Provided
- **Test Dataset:** Provided
- **Output:** EventProbability - the estimated probability that an observation belongs to the positive class.

## Initial Approach: Neural Network

### Data Partitioning and Initial Results

- **Initial Preprocessing:** Filtering data that’s 3 standard deviations away from the mean for all variables showed good results with training data.
- **Issue:** Model failed to achieve a reasonable AUC for the public test data.

### Learnings and Adjustments

1. **Preprocessing Adjustments:**
   - Filtered variables due to high kurtosis and skewness.
   - Changed data partitioning by filtering extreme percentiles for 10 variables and rejecting 10 variables with the lowest worth.
   - Result: No significant effect on valid ROC.

2. **Oversampling:**
   - Explored oversampling methods but did not yield significant improvements.

## Second-Best Model Approaches

1. **Neural Network:**
   - Data split: 60:40
   - Various preprocessing techniques applied.

2. **Logistic Regression**

3. **Gradient Boosting**

4. **Forward Regression**

5. **Backward Regression**

6. **Polynomial Regression**

### Results

- Despite various preprocessing and model adjustments, these methods did not outperform the best model approach.

## Our Best Model

### Model Comparison and Results

- **Ensemble Model:** Combination of Gradient Boosting and Neural Network.
- **Data Partition:** Careful data partitioning for optimal training and testing.
- **Metrics:** Evaluated various metrics to ensure the model's robustness.

### Key Takeaways

1. **Right Combination of Properties and Algorithms:** Crucial for achieving the best model performance.
2. **Evaluation of Various Metrics:** Important before assuming the model's goodness.
3. **Balance Between Underfitting and Overfitting:** Critical to model success.

## Conclusion

Through rigorous preprocessing, model testing, and evaluation, the best performing model was an ensemble of Gradient Boosting and Neural Network. This approach allowed for a more accurate prediction of bankruptcy, showcasing the importance of combining different algorithms and evaluating multiple metrics.

## Thank You

For further details, refer to the project slides and the provided SQL files for data loading and processing.
