# Prediction of Kurtosis Artifacts in dMRI

This repo is authored by Clio G and Mithun T, as a part of course requirement for EE541 'A Computational Introduction to Deep Learning' at University of Southern California Fall 2022.

Diffusion MRI (dMRI) measures the water displacement on the living tissue. Particularly, in the brain it is used to quantitatively characterize the trajectory and composition of the bundles of axons that form the white matter (WM). There are different mathematical models to approximate the diffusion signal, and despite several limitation, the most common technique used in clinical settings is the diffusion tensor approximation (it is not able to resolve crossing fibers, ignores nongaussian movement of water, etc.). In recent years, new mathematical models that improve the quantification and resolution of different WM trajectories have been proposed. The simplest of these models is the diffusion kurtosis approximation, a dimensionless measure that quantifies the non-Gaussian distribution of water in a voxel and can resolve crossing fibers. However, the kurtosis tensor estimation using least squares suffers from poor robustness, especially in voxels containing tightly packed aligned axons, such as the corpus callosum. If the scientific community would be able to resolve this downside, kurtosis could be widely used in the clinical settings, as the standard dMRI acquisition for patients (kurtosis MRI acquisition does not add much more extra time to the tradition tensor acquisition and provides a more robust measurement and biomarkers of WM). 

In this work we plan to outline the areas of the kurtosis maps (FAK, MK, AK and RK), where the signal is quantified as negative (artifacts) and use those areas as the labels from where the “outliers” are coming from and use the original dMRI file as the input data. Then, the idea is to identify the problematic areas of kurtosis in the raw dMRI file. For this classification problem, we use convolutional neural networks.


# Files

## untitled3.ipnyb

The Py notbook containing the entirety of the project work.

## gray_scale_train_128_VAE_ISEL.py

Reference Variational Auto Encoder as described in reference ''.

## Dataset

### dMRI
Sample input images used to train the Network.

### RK
Sample resulting images post segmentation, used to train the Network.

# License

[Apache License 2.0](https://github.com/cliog/EE541_Test1/blob/main/License.md)
