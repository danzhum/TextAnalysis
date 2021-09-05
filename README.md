# TextAnalysis

Requirement 1: Text classification

In this part it was required to perform text classification given a train test set with news articles. We applied vectorization techniques to represent text data and applied such machine learning classification models as Random Forests, Support Vector Machines (SVM) and K-Nearest Neighbour (KNN) to predict the class of the given article in a test set.

Requirement 2: Nearest Neighbor Search and Duplicate Detection

Question 2α:​​ De-Duplication with Locality Sensitive Hashing
The aim of this task was to detect the number of duplicated documents given two sets of the documents, i.e. to identify how many similar documents in a test set are present in a train set. Each document is a Quora question, therefore the task can be referred to as the similarity score calculation between short sentences. The similarity threshold was set to 0.8.
Similarity scores were calculated using four different methods:
1. Exact-Cosine method
2. Exact-Jaccard method
3. Cosine Similarity: Random projection LSH family.
4. Jaccard Similarity: Min-Hash LSH family

Question​​ 2b: Same Question Detection
In this part we implemented the model which given a pair of two questions decides if they are identical or not. This task also can be considered as a sentence similarity problem however here our similarity evaluation should be based on a contextual meaning of the sentence rather than solely on a number of shared similar words. In other words, the semantic similarity between two sentences should be measured by recognizing the semantic relations between them [1].
Again, train and test datasets were given, containing a huge number of the Quora questions. Both datasets contain such information as a unique ID for each pair of the questions, the first question and the second question. The train set was already labeled for each pair, and the final model was supposed to be able to predict the labels of the test set. The goal was to experiment with various heuristic features related to the sentence similarity, train the model with the train set and output final predictions.
Two methods were used to complete this task. The first one is based on deriving simple features describing two sentences such as their length, the number of common and unique items for each pair. Also, Jaccard and Cosine similarity scores were computed. Although these features do not infer alone the semantic meaning of the sentences, the data-driven approach that we apply here makes it possible to distinguish sentences based on the learned patterns. The second method is an extension of the initial model. We tried to apply the method of semantic similarity measurement and add it as an additional feature to the model.
