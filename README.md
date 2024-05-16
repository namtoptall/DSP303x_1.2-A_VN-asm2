# DSP303x_1.2-A_VN-asm2
*note* : 
#### So với yêu cầu đề bài : 
##### Bạn phải cố gắng TINH CHỈNH ÍT NHẤT 3 SIÊU THAM SỐ trên mỗi thuật toán, ngoại trừ soft voting và hard voting.
### Với model Knn, em sử dụng 4 tham số, bao gồm : 
- ```n_neighbors```: number of nearest neighbors used in predictions , common in knn
- ```weights ``` : weighting method for neighbors, whether 'uniform' or 'distance'
- ``` p ``` : parameter that controls the type of distance (p=1 for Manhattan distance, p=2 for Euclidean distance).
- ```algorithm``` : algorithm for selecting neighbors
### Với Desicion tree, em đã fine-tune tìm 5 tham số, bao gồm : 
- ```max_depth```: maximum depth of the decision tree
- ```min-samples-split```: minimum number of samples required for testing 
- ```min_samples_leaf```: minimum number of samples required per leaf 
- ```criterion``` : measure the quality of a work. ```gini``` and ```entropy``` are two different metrics to measure the purity of a node.ginimeasures the probability of a random sample being misclassified if it is assigned a labelentropymeasure uncertainty or confusion
- ```splitter```:  ```best``` choose the best node split according to the selected criteria (gini or entropy), ```random```choose a random node split among the best node splits. 
### Với SVM (Support Vector Machine), em sử dụng 7 tham số : 
- ```C``` : Smaller values specify stronger regularization. This parameter helps control overfitting by adding a penalty for larger coefficients in the model. Higher values of C correspond to less regularization.
- ```gamma``` : Parameter article determines the degree of influence of a sample 
- ```kernel``` : type of kernel function used to transform the data into a higher feature space, helping the data become separable.
- ```degree```: The degree of the polynomial function
- ```coef0``` : adjusts the effect of premium clauses relative to t-clauses
- ```class_weight```: add some balance between the class in the model 
-```break_tier```: classify based on unequal values
### Với Logistic Regression, em sử dụng 5 tham số: 
- ```C``` : Smaller values specify stronger regularization. This parameter helps control overfitting by adding a penalty for larger coefficients in the model. Higher values of C correspond to less regularization.
- ```solver```: Algorithm to use in the optimization problem.
- ```penalty```: Specifies the regularization term to be used. ```l2``` stands for ridge regression, which penalizes the sum of the squared coefficients.
- ```tol```: The algorithm stops when the improvement in the optimization objective is smaller than this threshold. Lower values mean the algorithm will run until it reaches a very precise solution, potentially taking longer.
- ```max_iter```: This sets a limit on the number of iterations the solver will take to find a solution. Higher values allow the solver more time to converge to a solution, which might be necessary for complex models or large datasets.
### Với Neural Network, em sử dụng 6 tham số: 
- ```learning_rate```: learning_rate of the optimization algorithm 
- ```units```: number of neurons in each hidden layers 
- ```layers```: numbher of hidden layers in the model 
- ```activation```: function use to activate between layers 
- ```solver```: algorithm to find the most optimal optimization
- ```alpha```: L2 regularization 
- ```beta1, beta2, epsilon```: Adam optimization parameters 
- ```hidden_layer_size```: the size of hidden layer 
##### Ngoài ra, đề bài còn yêu cầu : 
- F1 score trên dữ liệu kiểm tra phải cao hơn **0.6**, Jaccard score phải cao hơn **0.4** với *KNN* | *Decision Tree* | *SVM* | *Logistic Regression* | *Neural Network* Trên tập dữ liệu kiểm tra (testing)
### Kết quả : 
| Algorithm |Jaccard-testing | F1-score-testing |
|-----------|----------------|------------------|
| KNN | 0.470588 |  0.640000 |
| Decision Tree | 0.477273 |  0.646154 |
| SVM | 0.511628 | 0.676923 |
| Logistic Regression| 0.454545 |  0.625000 |   
| Neural Network| 0.452055 | 0.622642 |
#### Ngoài ra, F1 score phải lớn hơn **0.66**, Jaccard similarity score phải lớn hơn **0.5** với soft voting và F1 score trên phải lớn hơn **0.57**, Jaccard similarity score phải lớn hơn **0.45** với hard voting 
| Algorithm |Jaccard-testing | F1-score-testing |
|-----------|----------------|------------------|
| Hard Voting | 0.500000 | 0.666667 |
| Soft Voting | 0.521739 | 0.685714 |
