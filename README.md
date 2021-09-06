# Android-App-Authentication-

In our project, Android Authentication prediction, our problem statement was to build a prediction model that would detect Malware Apps given it's features like Name, Package, Rating, Various Permission that it requires upon installation. Our approach was to understand the domain, clean the dataset, perform the EDA for better understanding of the dataset, try out NLP Modelling for Text Columns, build the final model, evaluate and improve accuracy and  identify the future scopes.

Since we had a target class in the dataset, we went ahead with the typical methodology of solving a supervised Machine Learning Classification Problem. The first thing at hand was to clean the data by finding null values, dropping duplicates, handling outliers etc. After the cleaning, we tried out all possible visualizations for the different columns including count plots, word clouds for Text Columns, correlation plot with Target Class etc. 

After performing EDA and inferring insights, we also carried out Chi-square test to identify feature importance beforehand to have an idea of what could be the most relevant features. Since our dataset had both Text Columns and numerical columns, specific emphasis on NLP was given at the beginning itself. NLP Modelling was tried out to see if Text columns alone could predict a Malware App. To our surprise, after fine tuning hyperparameters, Text columns itself gave a result of 71% accuracy using an XGBoost Model. 

We were in a dilemma initially whether to include a Text column as dropping Text column would need enough reasoning and not dropping would add to complexity. Hence, we derived a new column from the NLP Model called Derived_prob_text that has predicted probabilities corresponding to a class for the whole dataset. We went ahead with two types of datasets, one with a text derived column and another one without it.

After having the 2 datasets, Modelling was given importance and out of all the models that we tried: KNN, Random Forest, GBM, XGBoost, Logistic Regression; XGBoost gave better accuracy, precision and recall. Plots like AUC-ROC Curve were also generated to validate this. Also, to our surprise, models performed well with the data frame having Text Derived Column and the feature importance was also high for this column.

To conclude, we were able to build a Malware App Classification Model with 89% accuracy (Text derived column increased accuracy by 8%). The future scopes and improvement of the project were also discussed in detail.

