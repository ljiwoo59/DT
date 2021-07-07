# Decision Tree Classifier
* Decision tree is one of the easiest and popular classification algorithms to understand and interpret.
* A decision tree is a flowchart-like tree structure where an internal node represents feature(or attribute), the branch represents a decision rule, and each leaf node represents the outcome.
* Can be utilized for both classification and regression.
* Partitions the tree recursively.
* Handle high dimensional data with good accuracy.

## Algorithm
1. Select the best attribute using Attribute Selection Method (ASM) to split the records.
2. Make that attribute a decision node and breaks the dataset into smaller subsets.
3. Starts tree building by repeating this process recursively for each child until one of the condition will match:
    - All the tuples belong to the same attribute value.
    - There are no more remaining attributes.
    - There are no more instances

## ASM
* Provides a rank to each feature (attribute).
* Best score attribute will be selected as a splitting attribute.
* **Information Gain, Gain Ratio, Gini Index**

### Information Gain
* The decrease in entropy (impurity in a group of examples).
* Computes the difference between entropy before split and average entropy after split of dataset based on given attribute values.
* The attribute with highest information gain is chosen as the splitting attribute.
* Biased : prefers the attribute with a large number of distinct values.
  - ex) unique identifier (customer_id) has pure partition, thus maximizing information gain and creating useless partitioning.

### Gain Ratio
* Handles bias by normalizing the information gain.
* The attribute with highest gain ratio is chosen.

### Gini Index
* Considers a binary split for each attribute.
* In the case of a discrete-valued attribute, the subset that gives the minimum gini index is selected as a splitting attribute.
* In the case of continuous-valued attributes, selects each pair of adjacent value as a possible split-point and point with smaller gini index is chosen as a splitting point. 




## Practice

#### [Pima Indians Diabetes Database](https://www.kaggle.com/uciml/pima-indians-diabetes-database)

### Decision Tree Classifier with Gini Index
![pima_indians_diabetes_clf](https://user-images.githubusercontent.com/54715744/123961487-603bb600-d9eb-11eb-8b7f-a5d9f487476f.png)
<img width="631" alt="스크린샷 2021-06-30 오후 9 36 01" src="https://user-images.githubusercontent.com/54715744/123961554-721d5900-d9eb-11eb-8d14-f028902a992d.png">


### Decision Tree Classifier with Information Gain, max depth 4
![pima_indians_diabetes_clf2](https://user-images.githubusercontent.com/54715744/123961514-692c8780-d9eb-11eb-944a-4e889c1e4b9a.png)
<img width="628" alt="스크린샷 2021-06-30 오후 9 36 16" src="https://user-images.githubusercontent.com/54715744/123961584-777aa380-d9eb-11eb-8f7f-61526a2d34e1.png">

## References
* https://www.datacamp.com/community/tutorials/decision-tree-classification-python
