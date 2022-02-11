# Australia Raining Forecast By Applying Machine Learning

The dataset used contains about 10 years of daily weather observations from many locations across Australia.
Observations were drawn from numerous weather stations. The daily observations are available from http://www.bom.gov.au/climate/data.

### 1.Data Cleaning and EDA
* The orignal dataset's shape is 145460 rows x 23 columns (22 independent variables and 1 dependent variable) with null values.
![original data set shape](https://user-images.githubusercontent.com/92283861/153620841-05c29774-4145-42db-b1af-c0518ca7e803.png)

* Fill the numerical null values with the mean and categorical null values with the most frequent value.
![fill null](https://user-images.githubusercontent.com/92283861/153620845-89ad642b-9a6c-48b4-9930-6cf8fde9a50a.png)

* Split the data into two sub-tables - Numerical and Catagorical.
![numerical and catagorical](https://user-images.githubusercontent.com/92283861/153620879-1d2c27c6-a392-4eaf-bce8-e7a80e4dada9.png)

* Turn catagorical values into numerical values by using One-hot Encoding. 
![onehot](https://user-images.githubusercontent.com/92283861/153620886-fca13e31-dd76-4414-b7fc-5c6eb81ab276.png)

Concatenate the two sub-tables.
![concat](https://user-images.githubusercontent.com/92283861/153620896-7f5f155b-fad9-4a6e-aa96-b9513918d349.png)

### 2.Pre-modelling 
* Standardizes the data.
* Reduce the dementionality of the dataset to 20 with PCA since the independent variables sinificantly increased to 110 from One-hot Encoding.
![standardize and PCA](https://user-images.githubusercontent.com/92283861/153624210-d081b9f4-ff9f-4753-9bbd-eb74b6439389.png)

* Data is highly imbalanced, to rebalance the dataset by SMOTEENN in order to prevent bias.
![SMOTEENN](https://user-images.githubusercontent.com/92283861/153624220-f7150688-80fc-4b99-93a8-b8d481e8b570.png)

### Modelling
* Create the training set and testing set.
* Train a Logistic Regression Model (with 84% accuracy).
* Train a Random Forest Model (with 93% accuracy).
