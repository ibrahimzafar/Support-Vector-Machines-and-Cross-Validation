# Support Vector Machines and Cross Validation

This repository explores the Cross Validation and implements sklearn's KFold and GridSearchCV. 


## Author
You can get in touch with me on <a class="btn-linkedin" href="https://www.linkedin.com/in/ibrahim-zfr/">LinkedIn</a>!

If you liked my repository, kindly support my work by giving it a ⭐!


## About this Repository
Cross Validation sets are used to prevent overfitting of the model. <br>

They are also used to search for the parameters that result in the lowest error on our test set. <br>

There are a few strategies for Cross Validation. 

## Train-Validation-Test Split 
One strategy is dividing the dataset into three sets - Training, Validation and Testing. <br>
This may be in a 60-20-20 fashion, 70-15-15. <br>

![alt text](https://github.com/ibrahimzafar/Support-Vector-Machines-and-Cross-Validation/blob/master/60_20_20.PNG "Train Validation Test") <br>
Picture taken from https://mc.ai/machine-learning-basics-train-test-and-validation-datasets/ <br>

This strategy works really well for most applications. <br>
The Train-Validation-Test split for means that the examples that are in the Validation nd Test sets would not be used for training. <br>
The K-Fold Cross Validation strategy overcomes this drawback. <br><br>

## K-Fold Cross Validation
In K-Fold CV, we specify the value of K. 

*  Dataset is divided into K chunks. 
*  K-1 chunks are used for training, and the Kth chunk is used as the Test set.
*  Average the results of the K-1 experiments 

![alt text](https://github.com/ibrahimzafar/Support-Vector-Machines-and-Cross-Validation/blob/master/kfold.PNG "K-Fold Cross Validation") <br>
Picture taken from https://scikit-learn.org/stable/modules/cross_validation.html

### Note 
The Training, Validation and Test sets must have a balanced distribution of the training examples, without which the model may not perform well. <br>
A balanced distribution means that if in a multiclass classification problem of 5 classes, all 5 classes must be present in all three sets. <br>  
Shuffling the data may be very useful. <br>


## Sensible values of parameters
Gamma and C values should ideally be on a geometric series, such as: <br>

![alt text](https://github.com/ibrahimzafar/Support-Vector-Machines-and-Cross-Validation/blob/master/c_gamma.PNG "Parameter values") <br>

References: 
<br>
*   https://stats.stackexchange.com/questions/43943/which-search-range-for-determining-svm-optimal-c-and-gamma-parameters
*   https://www.csie.ntu.edu.tw/~cjlin/papers/guide/guide.pdf (Chih-Wei Hsu, Chih-Chung Chang, and Chih-Jen Lin)


