# Prediction of Product Sales for a Major Grocer Retailer
An exploratoration of data analysis using supervised Machine Learning

![grocery store](https://github.com/NemesisCrociata/Prediction-of-Product-Sales/assets/132013562/2e0008a0-5be4-42d0-b56b-a55a9d9fbfd6)

**Author:** Nemesis Crociata

We've been tasked to analyze the most valuable factors contributing to profits. An analysis of products and outlets will be conducted following the CRISP-DM workflow.

## Data:
[Original Dataset](https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/)

### The data was cleaned and certain features were dropped due to irrelevance to the data
This includes the Item Identifier due to high cardinality.

Item Weight and Item Visibility were dropped due to a lack of correlation to the target.

## Exploratory Data Analysis
To explore the correlations between features and Item Sales, scatterplots and barcharts were created for comparison.

![outletidentifier count](https://github.com/NemesisCrociata/Prediction-of-Product-Sales/assets/132013562/7483e6d0-7604-4e59-a75e-c488b284b929)

![outletidentifier vs itemsales](https://github.com/NemesisCrociata/Prediction-of-Product-Sales/assets/132013562/9b1d90d6-55ec-476c-a269-44e0b2ab4e8f)

- Most outlets have similar Item Sales, but OUT027 stood out as a higher performer and can be prioritized to improve overall Item Sales.
- OUT010 and OUT019 have distinctly lower median outlet sales. They may be deprioritized due to their lack of contribution, or they can be prioritized to increase sales to the average.

![mrp vs itemsales](https://github.com/NemesisCrociata/Prediction-of-Product-Sales/assets/132013562/2b2890bf-9543-431f-be7c-6387a954dba0)

![mrp vs itemsales w outlettypes](https://github.com/NemesisCrociata/Prediction-of-Product-Sales/assets/132013562/742aeac9-3a78-417c-b372-78a795daf3ee)

- There is a moderate positive correlation between an item's Maximum Retail Price and the Item Sales.
- Grocery stores do not contribute to the positive correlation.
- Supermarket Type3 outperforms other Outlet Types based on their sales of higher Maximum Retail Price items. It is suggested to focus on Supermarket Type3 outlets to increase overall sales.

## Models
The following Machine Learning models were tested:
- Linear Regression Model
- Random Forest Regressor Model
- Tuned Random Forest Regressor Model

**The tuned Random Forest Regressor Model was chosen as the final model.**
- Looking at the mean absolute error, the model has a tendency to predict Item Outlet Sales with an error of $728.58.
- The Mean Absolute Error is chosen to reflect the model's errors instead of the root mean square error because the grocer focuses on sales of low-cost items (<\$267) and larger errors will not be as impactful.

## Limitations and Next Steps
- Although the tuned Random Forest model is the best model so far, it is still underfit. This could be due to the lack of relevant data to the target. There were also over 28% missing values under the Outlet Size feature that could influence the accuracy of the model.

**For any additional questions, please contact nemcrociata@gmail.com**
