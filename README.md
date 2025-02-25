# Predictive Analytics for Olympic Medal Counts using Machine Learning

## Overview
This project predicts Olympic medal counts using machine learning techniques. It leverages historical Olympic data and applies regression analysis to estimate the number of medals a country is expected to win based on various factors.

## Technologies Used
- Python 3.12
- Pandas
- NumPy
- Scikit-learn
- Seaborn

## Dataset
The dataset contains information about Olympic teams, including:
- `team`: Country code
- `country`: Country name
- `year`: Year of the Olympics
- `athletes`: Number of athletes representing the country
- `age`: Average age of the athletes
- `prev_medals`: Medals won in the previous Olympics
- `medals`: Actual medals won

## Data Preprocessing
1. The dataset is read using Pandas.
2. Only relevant columns (`team`, `country`, `year`, `athletes`, `age`, `prev_medals`, `medals`) are selected.
3. Correlation analysis is performed to understand feature importance.
4. Data visualization is conducted using Seaborn (scatter plots and histograms).
5. Missing values are identified and dropped.
6. Data is split into training (before 2012) and testing sets (2012 and later).

## Model Training
A **Linear Regression** model from Scikit-learn is used:
- Features: `athletes`, `prev_medals`
- Target: `medals`
- The model is trained on the training dataset.

## Predictions & Evaluation
- Predictions are made on the test dataset.
- Negative predictions are rounded to zero.
- The model's accuracy is evaluated using the **Mean Absolute Error (MAE)**, which was found to be **3.30**.

## Error Analysis
- The model's predictions are compared against actual results.
- The error ratio is calculated for each team to measure performance.
- A histogram is plotted to visualize the distribution of errors.

## Sample Predictions
### USA
| Year | Athletes | Previous Medals | Actual Medals | Predicted Medals |
|------|---------|----------------|--------------|------------------|
| 2012 | 689     | 317            | 248          | 285.21           |
| 2016 | 719     | 248            | 264          | 235.57           |

### India
| Year | Athletes | Previous Medals | Actual Medals | Predicted Medals |
|------|---------|----------------|--------------|------------------|
| 2012 | 95      | 3              | 6            | 6.92             |
| 2016 | 130     | 6              | 2            | 11.68            |

## Conclusion
- The model successfully identifies trends in Olympic medal counts.
- **Previous medals and number of athletes are strong predictors** of future medal counts.
- Further improvements can be made by incorporating additional factors such as GDP, sports funding, and athlete performance metrics.

## Future Enhancements
- Implement more advanced machine learning models (e.g., Random Forest, Neural Networks).
- Use feature engineering to extract more relevant predictors.
- Incorporate additional datasets to improve accuracy.

