# exoplanets
# Machine Learning - Exoplanets Exploration

This repo explores data by the NASA Kepler space telescope recollected over nine years.

Two machine learning models were created and tested for classifying exoplanet candidates from the dataset. The classifiers used are a random forest (rf), and a support vector machines(svm) .  Random forest reported better scores at all instances, with a final testing score for submition of 0.90. 

### Flow Process:
1. Preprocessing, including dropping duplicates and na.
2. Tuning, using 'GridSearch'
3. Comparing classifiers, rf and svm.


### Preprocessing

* Performed cleaning and feature selection. 
* Used `MinMaxScaler` to scale the numerical data.
* Separated the data into training and testing data.

### Tune Model Parameters

* Used `GridSearch` (CV)to tune model parameters.
* Tuned and compared the two classifiers.

### Results

Scores for the rf model are detailed in Table 1 and for the SVM model in Table 2 below. In case of rf, I ran the model 3 times. The first time, without deleting features, the second time, after removing features, and the third time, after cv tuning. Features were ranked, and the the top 10 largest were used for second run and cv tuning.

I did not found a major difference among the test scores for before and after cv after eliminating features.

Table 1
 |Score|Before Removing Feautures| After Removing Features | After CV|            
 |:---:|:---:|:---:|:---:|
 |Training Score |1.0| 1.0|1.0|
 |Testing Score  |0.900| 0.900|0.901|

Scores for the SVM are detailed in Table 2. In case of SVM, I ran the model 2 times, before and after cv tuning. The after cv tuning testing score was 0.879.

Table 2
 |Score|Before CV|  After CV|            
 |:---:|:---:|:---:|
 |Training Score |0.845| 0.886|
 |Testing Score  |0.841| 0.879|

### Summary
I found random forests easier for exploring machine learning models, their building, training and tuning. In this exploratory analysis of the NASA dataset, results show that the rf model performed better than the svm model. I think this rf model might be used for the classification of the exoplanets at a 0.9 accuracy rate.


### Dataset

* [Exoplanet Data Source](https://www.kaggle.com/nasa/kepler-exoplanet-search-results)




