# NIDS-and-Anomaly-detection-with-AI

Tasks Performed:

The datasets downloaded were huge and more than 100MB each. Thus they had to be compressed in order to be uploaded to GitHub.
In order to run the code, the compressed files need to be extracted first.
The final dataset was created by combining the 4 datasets into a single .csv file using code in the python file.
The NUSW-NB15_features.csv file contains the names of the features and were used for the column names in the final dataset.
After the dataset was complete, it was checked for null values and filled with appropriate values.
Empty spaces in the 'ct_ftp_cmd' column were found and removed as the research paper of the data listed it as a numerical feature.
Further cross-checking were performed.
The binary columns containing values more than 1 were changed to 1.
'-' values found in 'service' column were changed to 'None'.
'backdoors' values in 'attack_cat' column were change to 'backdoor' to remove redundancy.
Feature selection was performed by finding out the correlation between the features. The columns with correlation more than 0.95 were dropped to reduce redundancy.
Categorical Encoding was performed to convert the text data ('proto', 'state', 'service' columns) to numerical data.
The label encoding were changed so that +1 would mean normal data and -1 would represent attack data.
The dataset was then split into features and labels and the features were standardized so that all columns would contain values between 0 and 1.
The dataset was then split into testing and training sets. 30% of the whole dataset was set aside for testing.
4 different classifers were vuilt and the data was tested on each of them and their performance metrics were calculated and recorded to determine the best performing classifier for NIDS.
The classifiers used were- Decision Tree, Logistic Regression, Gaussian Naive Bayes and Random Forest.
Anomaly detection was performed on the dataset by two different methods, Isolation Forest and Local Outlier Factor.
Hyperparameter tuning of the algorithms for anomaly detection were performed and represented usng graphs. Their perfromance metrics were measured and recorded.
Finally the research task was added to the python notebook as a requirement for the second task of the group project.
