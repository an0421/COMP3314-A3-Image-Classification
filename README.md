# COMP3314-A3-Image-Classification

## Dataset analysis
1. Statistics on the number of categories:\
There are a total of 50,000 images and 10 categories/labels for the train images. The amount of the images for each label is shown through the image below:

   <img width="274" alt="Screenshot 2024-12-30 at 1 47 46 AM" src="https://github.com/user-attachments/assets/0882f02d-f994-4c20-a33e-b8341e0c798f" style="width:20%; height:20%;"/>

2. Visualizations of one example for each category:

   <img width="1379" alt="Screenshot 2024-12-30 at 1 51 32 AM" src="https://github.com/user-attachments/assets/4b297f1f-ec61-4050-a8ba-372a12ab4b4e" style="width:50%; height:50%;"/>

## Classifier exploration
In our image classification task, we implemented both KNN and SVM classifiers using Histogram of Oriented Gradients (HOG) features and Principal Component Analysis (PCA) for dimensionality reduction. The SVM classifier achieved an accuracy of approximately 71%, whereas the KNN classifier only reached about 50% accuracy. \
\
Support Vector Machine (SVM) Classifier is a supervised learning algorithm used for classification and regression tasks. It can use kernel functions (e.g., linear, polynomial, radial basis function) to transform data into a higher-dimensional space, making it possible to perform non-linear classification.\
\
K-Nearest Neighbors (KNN) Classifier is a non-parametric, instance-based learning algorithm used for classification and regression and it classifies new data points based on the majority class among its 'k' nearest neighbors in the feature space. The advantages of KNN are easy to understand and implement, no assumptions about data distribution, and can be used for both classification and regression problems. 
There are several reasons why SVM outperformed KNN in this task:\

1. High-Dimensional Feature Space\
For this dataset, even after applying PCA, the feature vectors from HOG features are high-dimensional (e.g., 256 dimensions) and high-dimensionality can pose challenges for certain algorithms. In high-dimensional spaces, the concept of proximity becomes less meaningful, as all points tend to be almost equidistant. All in all, the curse of dimensionality adversely affects KNN because it relies on distance calculations for classification.

2. Complex Decision Boundaries\
Image data often contains complex, non-linear relationships that require sophisticated modeling. Classes may overlap and have intricate boundaries that are not easily separable by simple models. The RBF kernel enables SVM to capture non-linear patterns by mapping data into a higher-dimensional space. This allows SVM to find a hyperplane that effectively separates classes with complex boundaries. On the other hand, KNN may struggle to capture the global structure of the data, leading to misclassification when the boundary between classes is complex.

3. Sensitivity to Noise and Irrelevant Features\
While HOG features may include redundant or irrelevant information that can act as noise, SVM aims to find the optimal hyperplane with maximum margin, which reduces the impact of outliers and noise. However, KNN considers all features equally when computing distances, making it sensitive to noise and can result in incorrect neighbor selection and poor classification performance.\
In conclusion, for image classification problems involving high-dimensional data and complex patterns, the SVM classifier outperformed the KNN classifier significantly. SVM, with its kernel trick and focus on maximizing the margin between classes, proved to be better suited for the task.

## Final solution description
1. Import the Necessary Libraries
2. Set Random Seed ( For reproducibility of results)
3. Define the HOGFeatureExtractor Class:
4. Load and prepare the dataset
5. Initialize the HOGFeatureExtractor
6. Extract HOG Features from Images
7. Scale Features using StandardScaler
8. Reduce Dimensionality with PCA
9. Train the SVM Model
10. Make Prediction on Test Data
11. Prepare and save the submission file
  





