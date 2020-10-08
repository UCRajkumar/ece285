# Severstal Steel Defect Detection
## Authors: Chi-Hsin Lo, Subrato Chakravorty, Utkrisht Rajkumar

### This project is no longer maintained.
### Description

The dataset for this project can be found [here](https://www.kaggle.com/c/severstal-steel-defect-detection/data). To run with our default path setup, create a new folder called "inputs" in the same directory as the one containing this cloned respository. Download and extract the dataset inside "inputs." The kaggle submission kernel can be found [here](https://www.kaggle.com/urajkumar/ece285-project-d). It contains the code to upload submission.csv files and submit to Kaggle. Inside the kernel, load the dataset called `ece285_submissions` to access all generated submission files. The submissions can be directly downloaded from kaggle [here](www.kaggle.com/dataset/66e31f616a09a4017e2c56d9b42afdc515a971421e9bbc11d5f7f63cca8ca8c3).

### Requirements
All the package requirements can be found in requirements.txt. To install the requirements:

```
git clone https://github.com/UCRajkumar/Steel_Defect_Segmentation
cd Steel_Defect_Segmentation
pip install -r requirements.txt
```

If working in a conda environment, use: 

`conda install --file requirements.txt`

The required file structure to run with our default paths are as follows:
**File Structure**

* Current Directory
  * Inputs
    * Downloaded data from Kaggle
  * ece285 (this repo)
    
### Code organization


file name | Description of file 
--- | ---
Demo.ipynb | Qualitatively evaluate all models on validation and test set images
Figures.ipynb | Recreate figures from report
Train.ipynb | Train u-net, u-net with residual encoder, and u-net with inverted residual encoder
deeplabv3.ipynb | Train deeplabv3+
Inference.ipynb | Predict on test set and export results
data_gen.py | Data generator for loading train, validation, and test images
model.py | Code for building all 4 models
utils.py | Accuracy and loss metrics, conversion from mask to RLE and vice-versa, and post-processing
train_idx.npy | indices for training set
val_idx.npy | indices for validation set
-----------------------------------
folder name | Description of file 
--- | ---
ex_images | Example validation and test images for Demo.ipynb
history | Training history for each model
models | Trained model files
submissions | Exported results on test set

*Note: The submission for deeplab was too large to upload onto github. However, it is in `ece285_submissions` folder in Kaggle.
