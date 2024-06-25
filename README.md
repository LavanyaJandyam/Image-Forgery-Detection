# Image Splicing-Based Forgery Detection Using Discrete Wavelet Transform and Edge-Weighted Local Binary Patterns

## Project Overview

*Title*: Image Splicing-Based Forgery Detection Using Discrete Wavelet Transform and Edge-Weighted Local Binary Patterns

*Authors*: Rayan Joseph Bastine Irudayaraju, Lavanya Jandyam, Mahalaxmi Anumula

*Abstract*: This project addresses the challenge of detecting digital image forgeries, particularly splicing-based manipulations, using advanced digital signal processing and machine learning techniques. The methodology combines the Discrete Wavelet Transform (DWT), Edge Weighted Local Binary Patterns (DRLBP), and a Support Vector Machine (SVM) classifier to identify inconsistencies in manipulated images. The model is trained and validated on the Columbia Image Spliced Dataset and the CASIA v2.0 dataset.

## Introduction

The goal is to develop a model that autonomously determines whether an image has been tampered with, specifically through splicing. The approach involves:
- *DWT*: Decomposing images into sub-bands to identify inconsistencies.
- *DRLBP*: Coding these coefficients for texture description.
- *SVM*: Classifying images as tampered or authentic.

## Dataset

- *Columbia Image Spliced Dataset*: Used for its diverse range of images, encompassing fewer than 1000 images, each with annotations for extensive training and validation.

## Methods

1. *DWT-DRLBP Descriptor*: 
   - Combines DWT's frequency decomposition with DRLBP's texture description to detect subtle inconsistencies from splicing.
2. *Wavelet Decomposition*:
   - Applies DWT on chroma components, separating the image into high and low-frequency bands to capture contrast variations.
3. *DRLBP Histograms*:
   - Quantifies image patterns like edges and corners using histograms of local binary patterns, enhancing sensitivity to alterations.
4. *Computation of DWT-DRLBP Descriptor*:
   - Aggregates local DRLBP patterns from the image's sub-bands, creating a comprehensive descriptor that captures structural changes indicative of forgery.

## Model Training

- *Support Vector Machine (SVM)*: Trained to differentiate between authentic and spliced images, using a kernel trick to manage the non-linear characteristics of image forgery datasets.

## Model Performance

- *Validation Accuracy*: Achieved approximately 72.60% on both the Columbia and CASIA v2.0 datasets in 500 fits, indicating the model's capability but also suggesting potential overfitting issues.

## Results

- *Test Outcomes*: Varied performance across datasets, successfully identifying tampered images in some cases but failing in others, particularly when gradient differences between original and spliced areas were minimal.

## Conclusion

The project demonstrates a novel approach to detecting splicing-based image forgeries, achieving significant accuracy. It shows the effectiveness of combining DWT and DRLBP for capturing and quantifying image inconsistencies. However, distinguishing highly sophisticated forgeries remains challenging, suggesting areas for future research and improvement.

## Technical Contributions

This project significantly contributes to the field of digital image forensics by:
- Introducing a novel descriptor combining DWT and DRLBP for enhanced detection of image splicing.
- Demonstrating the application of machine learning, specifically SVM, in classifying images based on textural and structural inconsistencies.
- Offering a comprehensive evaluation using real-world datasets, providing a benchmark for future research in image forgery detection.
