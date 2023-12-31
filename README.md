# Lung cancer Detection
\
The following dependencies are needed:
- numpy >= 1.11.1
- SimpleITK >=1.0.1
- opencv-python >=3.3.0
- tensorflow-gpu ==1.8.0
- pandas >=0.20.1
- scikit-learn >= 0.17.1

## How to Use

**1、Preprocess**

**nodule detection**

* convert annotation.csv file to image mask file:run the LUNA_mask_extraction.py
* analyze the ct image,and get the slice thickness and window width and position:run the dataAnaly.py
* generate lung nodule ct image and mask:run the data2dprepare.py
* generate patch(96,96,16) lung nodule image and mask:run the data3dprepare.py
* save lung nodule data and mask into csv file run the utils.py,like this:G:\Data\segmentation\Image/0_161....

**nodule classify**

* convert candidates.csv file to nodule and not-nodule image(48,48,48):run the LUNA_node_extraction.py
* Augment the nodule image data: run the Augmain.py
* split data into train data(80%) and test data(20%):run the subset.py
* save lung nodule data and label into csv file like this:1,G:\Data\classify\1_aug/0_17.npy

**2、Nodule Detection**
* the VNet model

![](3dVNet.png) 

* train and predict in the script of vnet3d_train.py and vnet3d_predict.py




## ROC Metrics

![](roc.PNG)

![](metric.PNG)

Refer:
* https://github.com/prathamsehgal
* email: prathamsehgal1223@gmail.com
* Contact +91 76668645081
