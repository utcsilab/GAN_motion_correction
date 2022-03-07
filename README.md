# MRI Motion Correction
This repository is for the GAN based motion correction method for the MRI images. 

## Table of contents
* [Requirements](#Requirements)
* [Simulating_Motion](#Simulating_Motion)
* [GAN](#GAN)

## Requirements
Download all the required packages in a new conda enviornment. 
```
$ pip install -r requirements.txt 
```
You should have a GPU of sufficient memory if you want to run the training/evaluation in batches, for lower memory GPUs run using a batch size of 1. 

To run inference on the pre-trained methods download a subet of the validation dataset at: (need to update link for dataset)

Make sure to change the file paths in all the relevent locations in the code to ensure the correct location of data on your machine. 

## Simulating_Motion
To start the motion corruption of base images, first need to download data from the this link (). Then generate the data as per the given python script:
```
python motion_gen.py
```

## GAN
If you want to train either GAN from scratch, run the following bash script with selection of appropriate hyper-parameters:
```
bash bash_training_jobs.sh
```
This will run the training for different hyper-parameters and chooose the ones which give the best performance. 

If you just want to do inference, then download the pre-trained GAN model parameters from the following drive (Update link).

Further, if you just want to visualize some of the test set images in a loop, you can use the following command with updated file structure:
```
python visualizer.py
```
