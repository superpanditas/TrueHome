# TrueHome
______________________________________________________________________________________________________________________________
## Testing to apply as Senior Data Scientist at TrueHome 

I am a prisoner on an island. My jailer decided to give me an opportunity to get my freedom but I need to solve 3 challenges.


These are my answers!. I hope to get my freedom!. :stuck_out_tongue_closed_eyes: :muscle:

__*First of all, I need to mention some points that you need to consider if you want to be able to see my answers.*__

__*Note:*__ *To do more accessible my work, you always can open the files on google colab.* (The link is on each file :smile: )

## __*Prerequisites*__
______________________________________________________________________________________________________________________________

<ul>
  <li> Python 3.7.11 </li>
  <li> Libraries: pandas, numpy, seaborn, matplotlib.pyplot and sklearn </li>
</ul>

______________________________________________________________________________________________________________________________
## __*Summary about challenges*__
______________________________________________________________________________________________________________________________

__*First Challenge: Poisonous waters*__


**Goal:** Identify the most closer 50 samples to poison sample.

**Identify Key Problems** Find an optimal way to find the most closer samples of the target

**Approach*** 


First of all, review the dataset like distributions, outliers, empty values and so on.


I decided to apply k-means to generate de some clusters with the objective to know what is the most potential samples to use. 


One time with the cohorts, I used a grouping by cluster to know where is the most similarity with my target then used it to get the distance for finally sort by less distance. :thumbsup: :satisfied:

______________________________________________________________________________________________________________________________
__*Second Challenge: Para hacer la de Jamon*__



**Goal:** Implementation of a model with the objective of scoring a variety of types of hams according with a historical base.

**Identify Key Problems:** Imbalanced Data, Few Data & a lot of different labels.

**Approach:** This is a Supervised Problem. 



First of all we should to solve the problem of Imbalanced data, and one of the first techniques is create synthetic data with the disadvantage of increased noise. 



And other problem is that with frequent in this type of techniques take at least 2 or more samples to generate data but in this occassion we have labels with just 1 sample. 



It means that we are obligated to repetead samples (¡Althought is not so helpful!)



In the other hand, one of the highlights is that our 3 features are correlated with the score and this is a good point. And the distribution is not bad, not presented many outliers. (almost nothing!) It is another good point!


And since 2 of the variables are correlated to eliminate redundancy, I decided to use PCA which is also useful for visualization.


I decided to address this with XGBoost algorithm, many reasons to choose him. 


This is an ensemble it means that take advantage of differents weak models to give an answer.

XGBoost is interpretable (In case we wish know which thresholds are useful to take a decision), not previuos assumptions about data and works good for imbalanced data.


Finally we got a 75% of accuracy, although 2 points here. First I used a naive configuration and keep a good accuracy, applying grid search can found the best hyperparameters and get a better accuracy. (for limitation of time, not use grid search but the accuracy is good)


The second observation is measure just accuracy is not always good because we could have good prediction on some class but really bad on others. Recall and Precision are good alternatives but in this occasion in the matrix confusion we can evaluate in more deep our results. (And I think is good!) :thumbsup: :satisfied:


______________________________________________________________________________________________________________________________
__*Thrid Challenge: The Seductive Song of the Sirens*__



**Goal:** Implementation of a model with the objective of classifying between endemic sirens and migrant sirens according with a historical base.

**Identify Key Problems:** Not many problems as previous exercises. We have two class, not null values, and balanced data. We just can noted outliers, bi-modal distributions (in case we wish to use parametric models), really close distributions between class, and redundacy on our data.

**Approach:** This is a Supervised Problem


As a mentioned before, not found really big problems. The first approach is remove redundancy, and in this case use PCA (principal component analysis) followed of one visualization and immediately found that we have a data linearly separable.


In this case, I decided to use Linear SVM (support vector machine) for the potentical to create robust model with few data, and given just have 2 variables (I am using pca(n_components=2)) and without outliers. 


Again I am using a naive configuration but with good results. (personally the data is really linear separable then was enough ) but we can use grid search to find the best hyperparameters. The accuracy was super good! :thumbsup: :satisfied:
______________________________________________________________________________________________________________________________

#### For more details, you can always check the files.ipynb.
#### ¡Any comment is welcome!



