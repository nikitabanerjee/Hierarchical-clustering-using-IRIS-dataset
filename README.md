# Hierarchical-clustering-using-IRIS-dataset
Hierarchical clustering is an unsupervised machine learning algorithm, where the data are grouped into cluster.


Library requried:
Numpy, Pandas, Matplotlib, linkage has been imported from scipy.cluster.hierarchy package,Kmeans has been imported from scipy.cluster package,dendrogram has been imported from scipy.cluster.hierarchy package
cophenet has been imported from scipy.cluster.hierarchy package, pdist has been imported from scipy.spatial.distance.

Dataset: Iris dataset has been used for solving hierarchical clustering.

Explanation

First the requried library are imported after that "class" that are setosa, virginica, and versicolor are droped from the dataset using variablename.drop(attribute). for this case csv file was read and stored in variable called data.
so code for removing the attribute is data.drop(['class'])

After removing the label from scipy.cluster.hierarchy package linkage method is called, in scipy.cluster.hierarchy package there are various type of linkage method like single, average, complete, centroid, but here single and 
average method was used.
linkages describe the different approaches to measure the distance between two sub-clusters of data points. when single linkage is applied between two cluster A and B it return the minimum distance between two point a
 and b such that a belong to A and b belong to B. When average linkage is applied for two clusters A and B, then first distance between any data point in a for A and data-point b in B and then the arithmetic mean of 
these distances are calculated. the value of single linkage is stored in variable Z and value of average linkage is stored in variable Y.

Then elbow method is used to find the number of cluster. Elbow method was calculated using K means clustering. based on the elbow method total 3 cluster was taken beacuse in the graph it can be seen that peak is high
at three and after that values has started dropping. Then dendrogram was plot. A Dendrogram is a type of tree diagram showing hierarchical relationships between different sets of data. initially dendrogram was plot for all the
dataset without taking any cluster.
 
Then dendrogram was evaluated by applying Cophenetic correlation coefficient from scipy.cluster.hierarchy.cophenet. cophenet is clacuated using euclidean distance for finding euclidean pdist(pair wise distance) was
imported from scipy.spatial.distance. At the end  “truncate_mode” Truncation is used to condense the dendrogram. for truncate_mode lastp mode was applied, number of clusters is taken as 3, number of cluster is taken from
elbow method, by applying truncate_mode and number of cluster again dendrogram was plot for Z and Y.
