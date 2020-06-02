In this repository it is saved code used to prepare the solution to Udacity Nanodegree capstone project. It is not allowed to share the data according to project conditions. 

The aim of this project is to segment and compare the population and customers base values, create prediction for the marketing campaign output. For the analysis purposes I used provided socio-demographic features of Arvato Financial Solutions.

The main notebook is divided into multiple steps. Firstly, get to know the data, features and prepare for further modelling, then apply PCA to go further with K-means clustering and finally to predict customers response to marketing campaign. 


# 1. Installations
The notebook was created using Python 3.7. 

#### Packages and libraries used:

- Data visualization: pandas, matplotlib.pyplot, seaborn
- Data wrangling: numpy, pandas
- Missing values imputer: SimpleImputer
- Values standartization: StandardScaler
- Principal Component Analysis: PCA
- Clustering: KMeans
- Parameters tuning and hyperparameters search: GridSearchCV
- Classification algorithms: RandomForestClassifier, XGBClassifier, catboost
- Data imbalance problems solving: SMOTE
- Import png: Image

Additional parameter to show all columns: 

pd.set_option('display.max_columns', None)

pd.set_option('max_colwidth', None)

# 2. Project Motivation
#### Udacity Capstone Project. Questions to answer:
- There are multiple questions to answer: how similar/different is Arvato customers base compared with Germany population.
- How can we predict which customers are going to respond to the company communications and become a user.

#### Structure of the project:
- Data load
- Data preprocessing: missing values, correlation, unknown values.
- Applied PCA and Kmeans
- Create predictions using CatBoost, RF, XgBoost
- Upload predictions to Kaggle.

# 3. Files Descriptions

#### The main file:
Arvato Project Workbook.ipynb

Provided files by the task (not included in the repository):
- Udacity_AZDIAS_052018.csv: Demographics data for the general population of Germany; 891 211 persons (rows) x 366 features (columns).
- Udacity_CUSTOMERS_052018.csv: Demographics data for customers of a mail-order company; 191 652 persons (rows) x 369 features (columns).
- Udacity_MAILOUT_052018_TRAIN.csv: Demographics data for individuals who were targets of a marketing campaign; 42 982 persons (rows) x 367 (columns).
- Udacity_MAILOUT_052018_TEST.csv: Demographics data for individuals who were targets of a marketing campaign; 42 833 persons (rows) x 366 (columns).

Additional files:
- DIAS Attributes — Values 2017.xlsx — attributes possible values and descriptions.
- DIAS Information Levels — Attributes 2017.xlsx — grouped attributes by the information level (Person, Household, Building, etc.)

#### Additionaly added files: 
- Elbow_plot_1_15.png.png - K-means simulation results. 
- kaggle_results.csv - predictions for Kaggle 
- kaggle.png - Kaggle submission results





# 4. Publication

Blog post could be found: https://medium.com/@ievad/udacity-capstone-project-arvato-bertelsmann-customer-data-analysis-and-results-c12826b621ee

# 5. Summary
To summarise, I take multiple steps to prepare data for modelling, dropped columns with high missing data share, checked correlations, mixed data types, identified unknown and undefined column values.

Then I applied PCA to reduce the data dimension even more after data preprocessing and spent some time to understand first components distribution. These components I used as an input for K-means clustering.

I selected K=1, .., 14 to define the best number of segments for population segments and then applied to the customers based, compared these segments. Customers and population segments have some similarities, but as expected more differences.

Finally, I created multiple models to predict if people will convert to customers after marketing campaign. For this step, I used CatBoost for the first time, and it was interesting to see the results.

# 6. Refinement
This project let me to touch a real world Data Science project and problems.

Moreover, I understood how it is important to compare and understand not only the user base but also the potential of growth if you analyse the population. Also, how the big picture understanding, helps business.

I think it would be easier to work with this data if I had specific business knowledge and understanding. In this case, the number of columns was huge and it was quite difficult to understand the meaning.

I am sure, there are many more things to do related with this project. I did not used Pipelines as this solution is not going to be used in the production. At least what I would like to try is to apply ensemble method which combines multiple classification models.

To improve the model performance, it would be important to check the most important features, iterate with the lower number of features. Maybe the different down-sampling techniques would have helped to predict with higher accuracy.

Lastly, I would like to thank Udacity for giving and teaching how to improve and solve real world business problems.

