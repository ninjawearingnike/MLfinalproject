----------------------------------------------
COS 424: Fragile Families Task (Spring 2019)

By Kelvin Yu
----------------------------------------------

I wrote and used the scripts as follows:

fileprep.ipynb: Takes data.csv as input, drops irrelevant features, divides location and date features into two separate ones respectively (see paper), and fixes misspelled category names. Outputs cleandata.csv.

imputation.ipynb: Takes new_data.csv as input, imputes missing values of fundraising amount based on average amounts of of fundraising rounds (e.g. Seed, Series, etc.). Normalizes funding amounts to between 0 and 1. Performs one-hot encoding on categorical features and fills remaining NAs with 0. Creates new dataframes with imputed values into segmented data sets of year0, year1, year2, year3, and china, which contain all the samples from 2016, 2017, 2018, 2019, and China, respectively. Lastly, it splits the original data set into a training and testing set. Outputs year0.csv, year1.csv, year2.csv, year3.csv, china.csv, train.csv, and test.csv.

LDA.ipynb/GMMwithPCA.ipynb: Takes year0.csv, year1.csv, year2.csv, year3.csv, china.csv, train.csv, and test.csv as input. Performs feature selection for GMM, trains respective models on each data set and computes log-likliehood scores.