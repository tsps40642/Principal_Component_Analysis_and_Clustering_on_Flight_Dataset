# Principal_Component_Analysis_and_Clustering_on_Flight_Dataset

## Overview
This is a project to demonstrate Principal Component Analysis (PCA) for dimension reduction, then conduct clustering to investigate the different aircraft in Delta’s fleet. Which planes are similar? Which are dissimilar?  

## Curse of Dimensiona
Curse of dimensionality occurs in domains like numerical analysis, sampling, combinatorics, machine learning, data mining and databases. When the dimensionality increases, the volume of the space increases so fast that the available data become sparser. To obtain a reliable result, the amount of data needed often grows exponentially with the dimensionality.   

Also, organizing and searching data often relies on detecting areas where objects form groups with similar properties. However, in high dimensional data, all objects appear to be sparse and dissimilar in many ways, causing problems when ``SIMILARITY`` is required.  

## Principal Component Analysis (PCA)
Principal Component Analysis (PCA) is a powerful unsupervised learning technique to deal with this problem by extracting (potentially lower dimension) hidden structure from high dimensional datasets.  

PCA finds the linear combinations A=(a1, a2, ..., ap) on p-dim random vector X such that the variation in the new coordinate is maximized in descending order, and it make sure all the PCs (loading vectors) are orthogonal, i.e., transform the original correlated features into uncorrelated features, being able to reduce dimension and preserve as much information as possible.  

To sum up, PCA forms linear combinations of the features that preserve as much of the variance as possible in descending order, subject to orthogonality (transform from correlated from uncorrelated) and be able to reduce data dimension.  

## How to conduct PCA?
Mannually conducting PCA requires the following steps:  
1. Normalization: z-score normalization is usually recommended to be performed with PCA, so that the variance calculations will not be dominated by some attributes
2. Generate the covariance matrix of the dataset
3. Calculate eigenvectors and eigenvalues of the convariance matrix  
    • Eigenvectors are the principal components  
    • Eigenvalues are always positive. The larger the value, the more variance is captured by its eigenvector  
4. Choose the appropriate number of principal components and transform the data accordingly (shift and rotate)

Here we use PCA in sklearn.decomposition.  
Further information: https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.PCA.html  

## Dataset
The csv file of Delta flight dataset is provided.  
