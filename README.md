# SVM
All the possible kernel along with other parameters have been tested and executed in this repository.
<br><br>
**Dataset** - iris data has been used in here which can be accessed from - https://scikit-learn.org/stable/auto_examples/datasets/plot_iris_dataset.html  
**Data Exploration and Preparation:**
  I have used Python libraries like pandas and scikit-learn, for data manipulation and preprocessing.   
  Loading the Dataset: load_iris() from scikit-learn has been used and converted into a pandas DataFrame for easier manipulation.  
  Initial Exploration: info() and head() methods provide a quick overview of data types and the first few rows of the dataset.  
  Handling Missing Values: It was found that Iris dataset typically has no missing values.  
  Scaling Features: StandardScaler has been used to normalize the feature columns so that they have a mean of 0 and a standard deviation of 1.  
  Encoding Categorical Variables: The LabelEncoder has been used to transform categorical labels (species names) into integers.  
  
**SVM Implementation** - SVM.ipynb has the implemention where -    
  The function evaluate_svm_config is particularly structured to assess the performance of the SVM under varying parameters and kernel types.  
  Parameters:  
    X: The feature matrix.  
    y: The target vector.  
    svc__C: Sets the regularization parameter.   
    svc__kernel:Type of the SVM kernel ( 'linear', 'rbf', 'poly').  
    Svc__gamma: Kernel coefficient for 'rbf', 'poly', and 'sigmoid' kernels. Determines the influence of individual training samples on the decision boundary.  
    svc__degree: Degree of the polynomial kernel; it is only relevant when using the 'poly' kernel.  
  Metrics:  
    Accuracy: Fraction of correctly predicted samples.  
    Precision: Measures the accuracy of positive predictions.  
    Recall: Measures the ability to find all relevant instances in the dataset.  
    F1 Score: Weighted average of precision and recall, a balance between them.  
  Grid Search : Automates the process of tuning parameters to find the best model configuration. Parameters for grid search:  
    cv=5: Performs 5-fold cross-validation.  
    scoring: Evaluates using the defined metrics.  
    refit='f1_score': Refits an estimator to the whole dataset using the parameter setting that provided the best results based on the F1 score.  
    verbose=1: Provides detailed progress output during the execution.  
    





