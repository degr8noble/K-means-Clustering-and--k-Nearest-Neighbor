In this lesson, we introduce clustering, a machine learning task where one tries to identify groups or clusters of data. Clustering is generally an unsupervised learning technique, since we are simply using the data features to determine some concept of closeness. One common technique used to quantify clustering is to identify clusters by using a metric, or distance measure. For example, we can use the Euclidean metric when all the data have the same units (such as distance) and dimensions. Other distance measures can be used when appropriate for the given data to determine closeness or similarity.

Specifically, this notebook focuses on K-means clustering, where we seek to divide  𝑁  data points into  𝑘  clusters. First, the K-means algorithm will be introduced and demonstrated on the Iris data. Next, the elbow method is introduced as a technique for determining the best value for  𝑘 . Finally, we discuss one clustering evaluation metric.
ALSO
In this notebook, we introduce one of the simplest machine learning algorithms, k-nearest neighbors (KNN), and demonstrate how to effectively use this algorithm to perform both classification and regression. This algorithm works by finding the  𝐾  nearest neighbors to a new instance and using the features of these neighbors to predict the feature for the new instance. If the feature is discrete, such as a class label, the prediction is classification. If the feature is continuous, such as a numerical value, the prediction is regression.

The KNN algorithm is different than most other algorithms in several ways. First, the algorithm is a lazy learner in that no model is constructed. Instead, the predictions are made straight from the training data. Thus, the fit method in the relevant scikit-learn KNN estimator doesn't build a model; instead, it builds an efficient representation of the training data, in other words, it stores all training data. Since the KNN algorithm stores all of the training data in the model, when the dataset is large, KNN requires more memory. Second, this algorithm is non-parametric, which means it does not make any assumptions on the underlying data distribution.

To understand why this algorithm works, simply look at society in general. You likely live near people who are like you in income, educational level, and religious or political beliefs. These inherent relationships are often captured in data sets and can thus be used by neighbor algorithms to make reasonable predictions. At its simplest, one neighbor is used, and the feature from this neighbor is used to make the prediction. As more neighbors are added, however, a descriptive statistic can be applied to the nearest neighbor features. Often this is the mode for a discrete prediction or the mean value for a continuous prediction; but other statistics can also be used. In addition, we can weight the statistic to account for the proximity of different neighbors. Thus, we may use a weighted mean for a regression prediction.
