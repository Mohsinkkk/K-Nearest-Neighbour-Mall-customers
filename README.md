# K-Nearest-Neighbour-Mall-customers

**What is KNN?**
K Nearest Neighbour is a simple algorithm that stores all the available cases and classifies the new data or case based on a similarity measure. It is mostly used to classifies a data point based on how its neighbours are classified.

Let’s take below wine example. Two chemical components called Rutime and Myricetin. Consider a measurement of Rutine vs Myricetin level with two data points, Red and White wines. They have tested and where then fall on that graph based on how much Rutine and how much Myricetin chemical content present in the wines.
‘k’ in KNN is a parameter that refers to the number of nearest neighbours to include in the majority of the voting process.

**Few ideas on picking a value for ‘K’**
There is no structured method to find the best value for “K”. We need to find out with various values by trial and error and assuming that training data is unknown.
Choosing smaller values for K can be noisy and will have a higher influence on the result.
3) Larger values of K will have smoother decision boundaries which mean lower variance but increased bias. Also, computationally expensive.

4) Another way to choose K is though cross-validation. One way to select the cross-validation dataset from the training dataset. Take the small portion from the training dataset and call it a validation dataset, and then use the same to evaluate different possible values of K. This way we are going to predict the label for every instance in the validation set using with K equals to 1, K equals to 2, K equals to 3.. and then we look at what value of K gives us the best performance on the validation set and then we can take that value and use that as the final setting of our algorithm so we are minimizing the validation error .

5) In general, practice, choosing the value of k is k = sqrt(N) where N stands for the number of samples in your training dataset.

6) Try and keep the value of k odd in order to avoid confusion between two classes of data

**How does KNN Algorithm works?**
In the classification setting, the K-nearest neighbor algorithm essentially boils down to forming a majority vote between the K most similar instances to a given “unseen” observation. Similarity is defined according to a distance metric between two data points. A popular one is the Euclidean distance method



**Pros of KNN**
Simple to implement
Flexible to feature/distance choices
Naturally handles multi-class cases
Can do well in practice with enough representative data

**Cons of KNN**
Need to determine the value of parameter K (number of nearest neighbors)
Computation cost is quite high because we need to compute the distance of each query instance to all training samples.
Storage of data
Must know we have a meaningful distance function.

Refrences:-
https://stackoverflow.com/questions/11568897/value-of-k-in-k-nearest-neighbor-algorithm
