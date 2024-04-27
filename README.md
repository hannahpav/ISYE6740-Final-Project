## Abstract
This paper looks at the Brain Tumor: Extracted Features for Brain Tumor \cite{accurate-detection} dataset from kaggle and builds **KNN**, **Support Vector Machine**, **Neural Network**, **Naive Bayes**, Ra**ndom Forest**, and **XGBoost** models on the MRI images and different selections of the Extracted Features dataset, which interprets the images based on visual components described in this paper. The metrics were measured on accuracy and sensitivity, as the cost of missing a tumor is greater than the cost of finding a false tumor. Ultimately, we find that the Neural Network Model using Principal Component Selection on the Feature Set performed best on this dataset, while Naive Bayes performed the worst. 

[Final Report]([https://github.com/hannahpav/foreclosure-study/blob/main/House%20Foreclosure%20Final%20Report.pdf](https://github.com/hannahpav/classification-methods-tumors-mri/blob/main/Final-Report-Tumor-Classification.pdf))

## Variables
    _Variance_ is a measure of the histogram width which represents the deviation of gray levels from the mean. 
    _Skewness_ is a measure of the degree of histogram asymmetry around the mean, and 
    _Kurtosis_ is a measure of the histogram sharpnes
    _Standard Deviation_ is the square root of the variance and, therefore, also measures deviation of gray levels from the mean.
    _Entropy_ is the degree of uncertainty in a random variable is termed entropy    Contrast -} splits the darkest and brightest area of an image. 
    _Energy_ is used in GLCM to calculate the total number of squared elements. Energy measures homogeneity. A high level of energy indicates that the image has excellent homogeneity or pixels of an image are very similar.
    _Angular Second Moment (ASM)_ represents the uniformity of distribution of gray level in the image.
    _Homogeneity_ is the quality or state of being homogeneous.
    _Dissimilarity_ is a linear measure of local variations in an image.
    _Correlation_ is calculated as the correlation coefficient between -1 and +1.
    _Coarseness_ a measure of grey level contrast that is used to establish descriptors of relative smoothness.

## Variable Selection
Principal Components Analysis (PCA) and Elastic Net are performed to identify the most important amongst the 13 first and second order statistical features that were extracted from the raw image files \cite{accurate-detection}. We performed these variable selection techniques to avoid some of the issues that would arise from violating the \textbf{four assumptions} by modeling all the variables together. In addition to building models with the most important variables identified through the PCA and Elastic Net selection processes, we'll also build models by utilizing the top four Principal Components. These top four Principal Components were found to explain as much as 91.32\% of the variability in the statistical features data.
