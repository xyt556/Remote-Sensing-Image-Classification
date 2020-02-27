# Remote-Sensing-Image-Classification
Official implementation for [Remote Sensing Image Classification via Improved Cross-Entropy Loss and Transfer Learning Strategy Based on Deep Convolutional Neural Networks](https://ieeexplore.ieee.org/abstract/document/8844264), IEEE Geoscience and Remote Sensing Letters 2019

## Citation
Please cite our project if it is helpful for your research
```
A. Bahri, S. G. Majelan, S. Mohammadi, M. Noori and K. Mohammadi, "Remote Sensing Image Classification via Improved Cross-Entropy Loss and Transfer Learning Strategy Based on Deep Convolutional Neural Networks," in IEEE Geoscience and Remote Sensing Letters.

```

<p align="center">
    <img src="https://github.com/AliBahri94/Remote-Sensing-Image-Classification/master/docs/d5a84f12-91af-4b3d-8096-2d4a5e641ecc-usa.png">
</p> 
<p align="center">
    21 class UC Merced land-use Dataset (RGB)
</p>

<p align="center">
    <img src="https://github.com/AliBahri94/Remote-Sensing-Image-Classification/master/docs/08191186-61c0-4298-80f0-85825f8ba2b4-udsd.png">
</p> 
<p align="center">
    Our Architecture
</p>

## Dependencies
- 1 Nvidia GPU (4h training on Titan Xp)
- ``Python3``
- ``tensorflow 1.15``
- ``numpy 1.17.5``
- ``keras 2.2.5``

## Download datasets
- AID (Aerial Image Dataset)
- Download (https://drive.google.com/file/d/1D8gvnEvzbyNlZHLLD3zqLGiUaxgqp0yN/view?usp=sharing)
- NWPU-RESISC45 (Northwestern Polytechnic University Remote Sensing Image Scene Classification 45)
- Download (https://drive.google.com/file/d/1eOMQ7zF19KRvjxZqVESMYzAd9X6gZfar/view?usp=sharing)
- UC Merced land-use
- Download (https://drive.google.com/file/d/1rzNVDsRn3JcVNnAYCI_eyd43ZoU_5vuq/view?usp=sharing)
- WHU-RS19
- Download (https://drive.google.com/file/d/1KuTwHU9Yumswrp9K1_FK0dlMN8QRjN-y/view?usp=sharing)

### Pretrained models
- Download trained model on AID dataset (train: 70% , valid: 30%) with accuracy score: 98.10 (https://drive.google.com/file/d/1-2sb1gBU9oYN4SF-iZ4Xab1mwVnmk0AD/view?usp=sharing)
- Download trained model on AID dataset (train: 50% , valid: 50%) with accuracy score: 97.08 (https://drive.google.com/file/d/1-1fHZODRLKUvRwlCBHLVCMo4e7E-32HX/view?usp=sharing)
- Download trained model on UC Merced land-use dataset (train: 80% , valid: 20%) with accuracy score: 99.52 (https://drive.google.com/file/d/1-20x38XGckZCNM-wsV7Gvpif4jaCVRQN/view?usp=sharing)
- Download trained model on NWPU-RESISC45 dataset (train: 20% , valid: 80%) with accuracy score: 93.56 (https://drive.google.com/file/d/1-Ey8NkAa0HksmSrw7opIB1oATGD5_jH5/view?usp=sharing)
- Download trained model on NWPU-RESISC45 dataset (train: 30% , valid: 70%) with accuracy score: 94.44 (https://drive.google.com/file/d/1hYcdtJHrviuDLGYwoodzJC9b23FnUj2q/view?usp=sharing)

## Project layout (recommended)
```
Remote_Sensing_Image_Classification/
├── checkpoint
├── data
│   ├── AID (train:70%, valid:30%)
│   ├── AID (train:50%, valid:50%)
│   ├── UCMerced (train:80%, valid:20%)
│   ├── NWPU-RESISC45 (train:30%, valid:70%)
│   └── NWPU-RESISC45 (train:20%, valid:80%)
├── docs
└── model_pretrained
    ├── NasNet_Mobile_New_Loss3.02-0.9810(AID_70_30).h5
    ├── NasNet_Mobile_New_Loss3.19-0.9708(AID_50_50).h5
    ├── NasNet_Mobile_New_Loss3.117-0.9952(UCMerced_80_20).h5
    ├── NasNet_Mobile_New_Loss3_Dore_3.06-0.9356(NWPU_20_80).h5
    └── NasNet_Mobile_New_Loss3_94.43(NWPU_30_70).h5

```
## Quick start
1. Download dataset and put into ``data/`` directory
2. Unzip dataset
2. Run ``python devide_dataset.py`` to split dataset to train and valid folder
3. Download pretrained models and put into ``checkpoint/`` directory
3. Run ``python predict.py``
4. Results will be shown
Note: Configurations is in the config.py file.



