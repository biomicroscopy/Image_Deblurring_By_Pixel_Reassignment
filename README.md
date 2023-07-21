# DPR-Project
Deblurring by pixel reassignment (DPR) is to perform PSF sharpening similar to deconvolution but in a manner less prone to noise-induced artifacts and without the requirement of a full model for the PSF. The basic principle of DPR is to reassignment the intensity value of pixels post-image acquisition. The pixel reassignment step size is dependent on the local log-image gradient. DPR relies solely on pixel reassignment. As such, no negativities are possible in the final image reconstruction. Moreover, intensity levels are rigorously conserved, with no requirement for additional procedures to ensure local linearity. 

## Contents
The repository comprises the Matlab functions for DPR
- DPR_demo.m
  Demo script for running the DPR function.
- DPR_function
  This folder consists of the functions of DPR.
  - DPRSetParameters.m
    This function is used to set the full width half maximum (FWHM) of the point spread function (PSF) of the imaging system, the gain level of DPR, the radius of the local-minimum filter, and the option of temporal analysis.
  - DPRStack.m
    This function is used to process an image stack.
  - DPR_UpdateSingle_mex.mexw64
    This function is used to process a single image and is developed for Windows computer using 64bits Matlab.
  - DPR_UpdateSingle_mex.maci64
    This function is used to process a single image and is developed for Macbook using Matlab.
  - save_tiff_img.m
    This function is used to save the DPR-enhanced image as Tiff.
 - Test_image
   There are two data sets in this folder.
   - sarcomere.tif consists of 15 frames of the engineered cardiac tissue imaged with a confocal microscope. The FWHM of PSF is around 4 pixels.
   - test_image.tif is a simulated data set. It consists of 60 frames of a simulated ring object imaged by a widefield microscope. Both Poisson noise and Gaussian are added to each frame. The FWHM of PSF is 4 pixels.

## Feedback
If you have any comments, suggestions, or questions, please do contact us at byzhao@bu.edu