# Prostate-Cancer-Detection

Applying various Machine Learning techniques and algorithms on Prostate Cancer Gene Dataset for outlier removal, feature selection, dimensionality reduction and classificaton. The original dataset used for this project can be found here: https://www.cbioportal.org/study/summary?id=prad_tcga_pub

In this project, two datasets are utilized, one is the patient gene dataset and the clinical dataset which consists of clinical features for each patient. Different machine learning techniques were applied to select bio-markers or genes out of 20k genes that are relevant to predict patients gleason score. The pipeline in Prostate_Cancer_detection.ipynb is as follows:

1. Outlier Removal: Outliers strongly influence the machine learning models training phase. Eliminated the outliers using tree ensembling technique called Isolation forests. This technique allows to explicitly identifies anomalies instead of profiling normal data points

2. Data preprocessing: Performed standard scaling to scale the dataset, used variance thresholding technique to eliminate the features that has less variance or no significant information. As the data was heavily imbalanced, SMOTEENN module from Imblearn was used to resample and balance the dataset.

3. Feature Selection: Perfromed feature selection using Random forest method which is an Embedded method that combine the qualities of filter and wrapper methods. 

4. Dimensionality Reduction: Utlizied Linear Discriminant Analysis from Sklearn module to reduce the dimensions of the dataset and to project the dataset on lower dimensions.

5. Target Prediction: Predicted Gleason Score stages using SVM, Naive Bayes and KNN algorithms. Model evaluation is done using 10 fold cross validation. Results are plotted using Matplotlib library. The overall model accuracy achieved to predict gleason score was 98%.
