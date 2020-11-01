# SalaryPrediction

# Project Description 


**Project Goal**: The goal of this project is to analyze a dataset of job listings with posted salaries and predict the salaries of job listings that neglected to post a salary.

**Use Case**: This type of model could be utilized by either recruiting firms or individual companies attempting to remain competitive in the job market.
 

![alt text](https://www.analyticsvidhya.com/wp-content/uploads/2015/05/landing.jpg)
## Data Description

The datasets given are as follows:

**train_features.csv**: This file contains one million observations, each one representing an individual job listing, along with 8 features. One of these features, "jobId", is a unique identifier and was not utilized in the models construction for prediction. The remaining 7 features are described below.

**train_salaries.csv**: This file contains the salaries for the observations in train_features.csv along with their corresponding identifier.

**test_features.csv**: Silimar to train_features, however, an accompanying "test_salaries" csv is not provided.

### Features
**companyId (categorical)** - A company identifier (not utilized in final model) 

**jobType (categorical)** - Junior, Manager, Vice President, CEO, etc.

**degree (categorical)** - High School, Bachelors, Masters, etc.

**major (categorical)** - Chemistry, Math, Physics, etc.

**industry (categorical)** - Auto, Health, Finance, Oil, etc.

**yearsExperience (numerical)** - Desired years of experience of candidate

**milesFromMetropolis (numerical)** - Job location's distance from metropolis

## Files
- **CSV datasets** can be found in the data folder
- Images of this **README** can be found in the images folder
- The model can be found in the **model.txt** file
- Feature importances can be found in the **feature_importances.csv** file
- Predictions on the test sets can be found in the **predictions.csv file**.

## Steps included in the model

**(1)Import relevant libraries**    
- pandas, NumPy, matplotlib, seaborn, sklearn, xgboost, and pickle  

**(2)Load the data into pandas DataFrames**  
- Examine the structure of the data sets
  
**(3)Clean the data**  
- Merge the features and salaries DataFrames on 'jobId' for easier handling  
- Check for missing values  
- Check for duplicate observations  
- Check for invalid data - rows with salaries equal to 0 are dropped
  
**(4)Visualize the data**  
- Bar plots for counts
- Box and whisker plots for each category by salary  
- Line graphs for numerical features vs salary  

**(5)Examine the correlation between features/features and features/target**  
- Heatmap correlation matrix  

**(6)Run baseline model** 
- A simple linear regression model
  
**(7)Hypothesize feature engineering to improve accuracy over the baseline model**  
- Data transformations  
- Binning  

**(8)Hypothesize different estimators to improve accuracy over the baseline model**
- PCA 
- Random Forest
- Gradient Boosting
  
**(9)Choose the most accurate model and fine-tune hyperparameters**  
**(10)Build a pipeline for deployment**  

## Conclusion  
The model with the lowest MSE was Gradient Boosting Regressor
Gradient Boosting Regressor was trained on the entire training set and scored on the test set to create predictions.


## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.


