
# SmartFares: Predictive Pricing for Ride Services

###  By Tanuj Verma 

## Project Overview

### Introduction

In the competitive landscape of ride-hailing services, strategic fare pricing is critical for business success and customer satisfaction. This project taps into the potential of data science to create a predictive model for taxi fares, empowering ride-sharing companies to optimize their pricing models dynamically.

### About the Dataset

The dataset is a rich compilation of ride details from a ride-sharing service, with each entry capturing the essence of urban commutes. The key attributes include fare amount, pickup and drop-off coordinates, passenger count, and datetime information—each serving as a pillar for constructing our predictive analysis.

#### Dataset Columns:
- **key**: Unique identifier for each trip, derived from ride timestamps or generated hashes.
- **fare_amount**: Total fare charged, serving as the target variable for prediction.
- **pickup_datetime**: Start date and time of the ride, key for analyzing fare trends.
- **pickup_longitude**: Longitude of the pickup point, crucial for location-based analysis.
- **pickup_latitude**: Latitude of the pickup point, determines the ride's starting location.
- **dropoff_longitude**: Longitude of the drop-off point, aids in calculating travel distances.
- **dropoff_latitude**: Latitude of the drop-off point, completes the route data for analyses.
- **passenger_count**: Count of passengers, affects fare due to different pricing for passenger numbers.

Dataset Kaggle link: [Uber Fares Dataset](https://www.kaggle.com/datasets/yasserh/uber-fares-dataset)

### Objectives

The overarching goal of this project is to accurately predict taxi fares to aid ride-sharing companies in:
- Refining their pricing strategies.
- Improving the overall customer experience.
- Achieving operational excellence.

Specific objectives encompass data preprocessing to handle geospatial and temporal information, extensive exploratory data analysis to unveil underlying patterns, visualization to represent complex relationships, and rigorous model evaluation to ascertain predictive accuracy.

### Significance of the Project

This endeavor is significant for enabling data-driven decision-making, leading to:
- **Business Optimization**: Enhanced dynamic fare management for increased profitability and competitive advantage.
- **Customer Satisfaction**: Greater transparency in fare calculation boosts customer trust and retention.
- **Operational Efficiency**: Insights from the model inform better resource allocation and route optimization.

### Methodology

- **Data Preprocessing**: Transformed geospatial data for precise mapping and analysis.
- **Exploratory Data Analysis (EDA)**: Conducted in-depth statistical reviews to understand fare distribution and key contributing factors.
- **Visualization**: Employed a variety of graphical representations to showcase insights and foster a deeper understanding of the data.
- **Model Evaluation**: Assessed multiple regression models using key performance indicators to identify the most accurate predictive model.

### Key Achievements

- **Novel Engineering**: We split the date column into multiple columns like Year, Month, Weekday, Hour, Monthly_Quarter, and Hourly_Segments to enrich our dataset into valuable segments for clearer analysis.
- **Innovative Visualization Techniques**: Using folium for geographic analysis visualization.
  
  (![image](https://github.com/tanzealist/Uber-Fare-predictor/assets/114698958/571386b6-4d21-48cc-bd5c-391e07801520)


- **Interactive Dashboards**: Created dynamic, user-interactive dashboards for real-time data exploration using dash. Created an interactive dashboard where you can view the passenger count and fare amount comparison year and weekday-wise.
  
  (![image](https://github.com/tanzealist/Uber-Fare-predictor/assets/114698958/d1951e1d-519d-4ece-b08a-dd4e78f53bfc)


- **Novel Feature Engineering**: Devised new features like rush-hour and fare efficiency for nuanced insights.
- **Algorithmic Innovation**: `RandomizedSearchCV` and `GridSearchCV` methods for hyperparameter tuning in machine learning models.
- **Boosting Methods**: `HistGradientBoostingRegressor` and `GradientBoostingRegressor` exhibit superior performance in terms of test R-squared values, indicating their strong generalization capabilities.
  
  ![image](https://github.com/tanzealist/Uber-Fare-predictor/assets/114698958/0e06ae2b-1e9e-4e27-b65d-001b225823c6)


- **Creative Problem Framing**:
  1. **Dynamic Pricing**: Transition from mere analysis to real-time prediction of fare efficiency, incorporating factors like traffic, events, and surge pricing.
  2. **Passenger Centricity**: Refocus analysis on what drives passenger satisfaction, potentially incorporating comfort, safety, and sharing opportunities into our feature set.
  3. **Sustainability**: Redirect our analytical efforts to measure and promote rides with lower environmental impacts, motivating the use of eco-friendlier transportation options.

### Conclusion

Based on the analysis of the model performance, we can conclude the following:
1. **Boosting Methods Outperform Other Models**: The `HistGradientBoostingRegressor` and `GradientBoostingRegressor` exhibit superior performance in terms of test R-squared values, indicating their strong generalization capabilities. This suggests that for this dataset, boosting methods are beneficial due to their ability to iteratively correct errors from previous models.
2. **Overfitting in Complex Models**: There is a significant disparity between training and testing R-squared values for the `DecisionTreeRegressor`, which suggests overfitting. Although decision trees can capture complex patterns in the training data, they may not generalize well to unseen data. Ensemble techniques, as seen with the `Random Forest` and boosting algorithms, help overcome this by averaging multiple trees.
3. **Consistency Between Train and Test Performance**: Models like `XGBoost` and `Gradient Boosting` display a smaller gap between training and testing metrics, demonstrating a good balance between bias and variance. Such consistency indicates that these models are well-tuned to the problem at hand and are neither overfitting nor underfitting excessively.
4. **Simpler Models Have Merit**: Despite lower performance metrics, simpler models such as `Linear Regression` have their advantages, particularly in interpretability and faster prediction times. In situations where the explainability of a model is crucial, or when computational resources are limited, these models can be a good compromise, given their reasonable performance and efficiency.

These insights can guide future iterations of the modeling process, prompting considerations such as additional feature engineering, alternative model selection, or further hyperparameter tuning to enhance predictive performance.



