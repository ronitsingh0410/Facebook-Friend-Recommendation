# Facebook-Friend-Recommendation

# Data Overview
  The datset consist of 2 columns source node and destination node.

# Mapping the problem into supervised learning problem
  Based on the 2 columns we will featurize the dataset using networkx python library.
  To map to supervised learning we will asign all the row provided in dataset a value 1 and will randomly generate nodes and check if the pair of nodes is not present we will asign 0
  The dataset was converted in the below features
  1. Jaccard Distance
  2. Cosine Similarities
  3. Page Rank
  4. Shortest Path
  5. Connected Components
  6. Adar Index
  7. Kartz Centrality
  8. HITS Score
  9. Preferential Attachment
  10. Follow Back
  11. SVD
  12. SVD dot
  13. Weight

# Conclusion
  1. The above analysis we have created around 56 features for analysis from only 2 columns.
  2. On Running randon forest for getting the features importance we can see by taking only 20
features listed above we can get more the 99% of important feature.
  3. For training the main model which is Xgboost only 50% of the rows are used due to
computation constrain with 20 features.
  4. The Xgboost is performing pretty good but the is overtting which may be beacuse of using
less no of points.
  5. We got a ROC of 0.92 and f1 score of 0.91
  6. We can also see in feature importance that a simple follow back feature is the most important
among all of them.
