# Multi-level Efficient Extinction Perception Network(MLEEP)
This is the code for Multi-level Efficient Extinction Perception Network.
![图片17](https://user-images.githubusercontent.com/46095890/157889524-cd356d86-5473-4587-886c-4759bb2d117c.png)


## Cross-polarized Petrographic Image Datasets (CPPID) for Grain Edge Segmentation

The datasets are comprised of five different types of rock thin sections and were collected using a CAIKON XP-330C polarizing microscope and a DAHENG IMAGING MER-2000-19U3C camera. Each kind of rock thin section is photographed with 25 different fields of view, and images are collected with 7 different polarizing angles: 0°,15°,30°,45°,60°,75°,90° for each field of vision. As a consequence, the total datasets comprise 875 petrographic images with a size of 4666x3672x3.
![图片21](https://user-images.githubusercontent.com/46095890/156997744-001e6a82-81bf-4e97-a51b-496da75a979e.png)

Download the CPPID dataset here. [https://pan.baidu.com/s/1cBGJGWx6as2WjOVNFFcbOw?pwd=zc8i 
Key：zc8i]

## For training
1. Download the CPPID dataset.
2. Generate the train.txt and val.txt(train_max.txt and val_max.txt) using the generate_dataset.py, where you should change the data directory with your URL.
3. Training the model using train_multi_input.py for the full version of the proposed model or using train_max_input.py for max-input version of the model. Remenber to change your URL of train_max.txt and val_max.txt.

## For inference

1. Download the previously trained model on max-input petrographic images here.[https://pan.baidu.com/s/1-EpDYx1jQBv1bRiEIbrHhA?pwd=7cl4 
Key：7cl4]
2. Download the previously trained model on multi-input petrographic images here.[https://pan.baidu.com/s/1qhzmmhwfU30AFEmnbcQn7Q?pwd=r4wu 
Key：r4wu]
3. Evaluate the model using evaluation.py or evaluation_max.py.

## Results after post-processing
The predicted segmentation maps of image patches are merged directly to form the full segmentation results of size 2048×1536×3. Noting that because the train and validation dataset is divided randomly, the images patches used in the full segmentation results consist of both training and validating image patches. 
![图片23](https://user-images.githubusercontent.com/46095890/156997730-0e3bf266-d2ad-46c1-81cb-18a5276b9fc4.png)
