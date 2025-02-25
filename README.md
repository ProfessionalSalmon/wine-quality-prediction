# Wine Quality Prediction
Linear Regression for Red and White Wine Quality

## Dataset

The dataset used in this project is the **Red Wine Quality Dataset**, available on Kaggle: [Red Wine Quality Dataset](https://www.kaggle.com/datasets/uciml/red-wine-quality-cortez-et-al-2009). The dataset contains 1,599 samples of red wine and includes 11 features related to the wine’s chemical composition, such as:

- **Fixed Acidity**: Acidity that does not evaporate.
- **Volatile Acidity**: Acidity that can evaporate during the fermentation process.
- **Citric Acid**: An organic acid found in wines.
- **Residual Sugar**: The amount of sugar left after fermentation.
- **Chlorides**: The amount of salt in the wine.
- **Free Sulfur Dioxide**: The free form of SO2 that protects wine from spoilage.
- **Total Sulfur Dioxide**: The total amount of SO2 in the wine.
- **Density**: The density of the wine, which can be influenced by the alcohol content.
- **pH**: The measure of acidity or basicity of the wine.
- **Sulphates**: Additives that can contribute to wine stability.
- **Alcohol**: The percentage of alcohol content in the wine.

The target variable is the **quality** of the wine, which is a subjective rating given by experts on a scale from 0 to 10. Sadly, the performance of multiclass classification models (Logistic Regression, KNN, Fully connected Feed Forward Neural Networks) is still not acceptable, these models are still in developing progress. Here is the loss function of Neural Network model.
![picture](/image/entropy-loss.png)

In the meantime, I created a new binary label (bad vs good). I then use **Decision Tree** model to perform the prediction. The performance of red wine is evaluated using ROC and Area under the curve because the cost of false positives and false negatives is roughly equal; whereas, the white wine uses PR-AUC curve as the positive class is rare.

![picture](/image/red-roc.png)
![picture](/image/white-pr.png)

## Usage
To run the notebook locally, ensure you have the following dependencies installed:

- `pandas`
- `numpy`
- `scikit-learn`
- `matplotlib`
- `seaborn`
