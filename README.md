# Predicting Biogenic Silica percentages in lake sediment cores from High Arctic settings 

## I. Background

Biogenic Silica (BSi) is used as a proxy for past temperatures in High Arctic settings. Typically, greater amounts of BSi in sediment cores indicate warmer temperatures. Recently paleoclimatologists have begun to use Fourier Transform Infrared (FTIR) spectroscopy to collect information on BSi. However, the offloaded relative absorbance data make comparison with other proxies difficult. The goal of this [project](https://www.causeweb.org/usproc/eusrc/2021/virtual-posters/7) is to develop a universal calibration model using PLS to convert absorbance spectra into percentages of BSi and TOC so as to provide paleoclimatologists with a more universal way of analyzing and understanding their results.

## II. Repo Organization 

The repository is organized into the following four folders: 

* [Code](https://github.com/people-r-strange/PLSmodel/tree/main/Code)

* [csvFiles]

* [dataViz](https://github.com/people-r-strange/PLSmodel/tree/main/dataViz)

* [Samples](https://github.com/people-r-strange/PLSmodel/tree/main/Samples)

### Code 

The code folder contains four scripts: 

* [01_createDataFrameScript.R](https://github.com/people-r-strange/PLSmodel/blob/main/Code/01_createDataFrameScript.R): This code takes the offloaded OPUS files and reformats them into a suitable data frame for the PLS model 

* [01_createDataFrame.R](https://github.com/people-r-strange/PLSmodel/blob/main/Code/01_createDataFrame.R) : This code does the same thing as the aforementioned script, only this code includes function which allow for more efficient processing

* [02_createModelScript.R](https://github.com/people-r-strange/PLSmodel/blob/main/Code/02_createModelScript.R) : This code loads the data frame created in the first script, inputs the dataframe into the PLS model, creates an RMSEP curve and loading plots. 

* [03_modelAccuracy.R](https://github.com/people-r-strange/PLSmodel/blob/main/Code/03_modelAccuracy.R) : This code assess the model accuracy by creating two plots: (1) plot that compares the actual percentages of BSi to the predicted percentages of BSI; (2) plot that calculates the residuals (actual minus observed) and detects any overfitting and underfitting 

### dataViz

The data viz folder contains all of the relevant data visualizations. Within this folder there are four additional sub-folders: 

* [crossValidation](https://github.com/people-r-strange/PLSmodel/tree/main/dataViz/Greenland/crossValidation)

* [LoadingPlots](https://github.com/people-r-strange/PLSmodel/tree/main/dataViz/Greenland/LoadingPlots)

* [modelAccuracy](https://github.com/people-r-strange/PLSmodel/tree/main/dataViz/Greenland/modelAccuracy)

* [residuals](https://github.com/people-r-strange/PLSmodel/tree/main/dataViz/Greenland/residuals)

Within each of these folders, there are visualizations for: 

* full spectrum: $~7500 - 368 cm^{-1}$ 

* truncated spectrum: $3750 - 368 cm^{-1}$

* specific spectrum: $435 - 480 cm^{-1}$

* specific spectrum : $790 - 830 cm^{-1}$

* specific spectrum : $1050 - 1280 cm^{-1}$

###  Samples 

For the samples folder there are two subfolders. The [alaskaSamples](https://github.com/people-r-strange/PLSmodel/tree/main/Samples/alaskaSamples) folder contains the 100 alaskan samples. The [greenlandSamples](https://github.com/people-r-strange/PLSmodel/tree/main/Samples/greenlandSamples) contains the 28 samples from Greenland. 
