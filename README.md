Gold Price Prediction using Random Forest Prediction

Datasets:

We have a dataset downloaded from kaggle website. It is named as Gold_Price_Data. It contains gold prices from the year January 2008 to the year May 2018. This contains gold prices on daily basis. The data file is a Comma separated value file format with 2290 rows and 7 columns. It contains 5 columns which are numerical in datatype and one column in Date format. The dataset contains the values of the variables SPX,GLD,USO,SLV,EUR/USD against the dates in the date column. The following are: GLD - Gold price USO - United States Oil Price SLV - Silver Price EUR/USD - Currency pair i.e, value of 1 USD in EUR link - https://www.kaggle.com/datasets/altruistdelhite04/gold-price-data

PreProcessing:

We preprocess all the data by using basic techniques like dropping all the rows with missing values (there weren’t any!). The most preprocessing was done to the dates, since the data was collected from different sources, the dates were in different formats and they were formatted to a common format which would be understood by matplotlib for plotting it appropriately.

Random Forest Regressor:

We split the data into Training and Testing data. Then we evaluate the model by finding error score and accuracy score. We use Imputation method by finding correlation between data. Correlation are:

Positive correlation - one variable increases while the other increases i.e, they are directly proportional
Negative correlation - one variable increase while the other decreases i.e, they are inversely proportional
Then we find which variable has highest positive correlation with GLD. Then we split variables into Features and Target. Features include SPX, USO,EUR/USD and TARGET is GLD. Then Splitting data into training data and testing data. So put 80% of data into training and 20% into testing.

Model Training: Random Forest Regressor is an ensemble model of decision tree where there are multiple decision trees and we get different values from different decision trees. Then we find the value using the voting method by taking the mean or median of all values. Use R Square to check the efficiency of the model by taking the difference between Gold value voting and voting obtained from value based on other variables other than Date.
