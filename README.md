
## Project Description

A local farmer, seeking guidance on optimal crop selection for his field, approached our team of machine learning experts. Due to budget constraints, the farmer can only afford to measure two out of the four essential soil parameters:

1. Nitrogen content ratio in the soil
2. Phosphorous content ratio in the soil
3. Potassium content ratio in the soil
4. pH value of the soil

Recognizing this as a classic feature selection problem, our objective is to identify the most influential features to accurately predict the ideal crop for the given soil conditions. Can our machine learning expertise provide the necessary guidance?

## Approach
1. **Data Exploration:**
    - Loaded the dataset from "soil_measures.csv" and conducted initial checks.
    - Verified the number of crops, identified missing values, and ensured numeric data in potential feature columns.

2. **Data Splitting:**
    - Segregated the dataset into training and test sets, allocating 20% for testing, and utilizing a random seed of 42.

3. **Feature Importance Analysis:**
    - Implemented a loop to predict the "crop" type using each individual soil parameter.
    - Employed Logistic Regression models for each feature and calculated the corresponding F1 score.
    
4. **Correlation Analysis:**
    - Conducted a correlation analysis among pairs of features to mitigate the risk of selecting highly correlated features.

5. **Final Model Training:**
    - Identified the most influential features based on the above analysis (Nitrogen, Potassium, pH).
    - Trained a new Logistic Regression model named `log_reg` using the selected features.
    - Evaluated the model performance using the F1 score, saving the metric as `model_performance`.

## Results
The final model, incorporating the chosen features (Nitrogen, Potassium, pH), demonstrated promising predictive capabilities with an F1 score exceeding 0.5.
