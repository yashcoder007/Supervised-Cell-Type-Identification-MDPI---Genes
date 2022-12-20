# Cell Type Annotation Model Selection: General-purpose vs
Pattern-aware Feature Gene Selection in Single-cell RNA-seq
Data

**Introduction**
This work compares and evaluates the performance of two best practices in cell type 9
annotation, XGBoost and SVM, with information gain as a feature selection method
1) Preprocessing step 
2) Hyperparameter Tuning (Bayesian Search) 
3) Model Creation with best parameters (XGBoost, SVM)
4) Feature selection (using Annova, Chi2 and Information Gain)
5) Model Training with selected features
6) Evauation of the models
 
Before applying machine learning techniques, the primary step is to preprocess the data for downstream analysis. Once the data is preprocessed, a parameter space is defined and the best parameters are selected after using an exhaustive bayesian search method. Model is prepared with the best parameters and the most effective features are selected using different feature selection techniques. The model is then trained on the training set using the best parameters and the selected features. In the last step prediction is made on the test set and models are evaluated on the basis of performance metrics.

**Pipeline of the proposed framework**

<img src="Single-Cell Sequencing.png">

**Version Requirements for this project**

1) python 3.8
2) XGBoost 1.7
3) scikit-learn 1.2
4) numpy 1.14.2
5) pandas 1.5.2

**Dataset Used**

Single-cell RNA sequencing dataset
The normalized datasets can be found in the datasets folder
| Dataset | Tissue |  Accession | #Cells |  #Genes
| --- | --- | --- | --- | --- | 
| Baron-human1 | Human-Pancreas | GSM2230757 | 1,937 | 20,125
| Baron-human2 | Human-Pancreas | GSM2230758 | 1,724 | 20,125
| Baron-mouse2 | Mouse-Pancreas | GSM2230762 | 1,064 | 14,878

**Comparison Study**
In this work we have compared the XGBoost model with feature selection and XGBoost without feature selection with the SVM with Information gain method. The model files can be found in their respective folder by names. For convenience jupyter notebook files are uploaded.

**Acknowledgements**
This project is developed under the supervision of , Dr. Luis Rueda, and in collaboration with, Akram Vasighizaker, a PhD student, and the University of Windsor Office of Research and Innovation.
