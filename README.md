# Getting Started
Image_Patchyfy is used to generate patches of imgaes 

default settings
size: 256x256x3
step: 120

you can specify the size and step by calling patchify() function ; see third cell

## Dataset Preparation
```
Extract Dataset in the current directory
The directory Structure Must be like this

here i use MonuSeg Dataset

-Monuseg
    - Test
        - GroundTruth
        - TissueImages
    - Training
        - GroundTruth
        - TissueImages
 
```
 
open file
generate_patches/run_patchify.ipynb


--------- First Cell ---------
```
run first cell is to mount the google drive
```

--------- Second Cell ---------
```
second cell is used to generate patches of images and visualize them
initialize the path variable with directory  where images are loctaed 
run the cell to view the some patches of two images you can change the patches and image using their indices
second cell is not used to create the dataset it is just to visualize the dataset which is going to be generated
```

--------- Third Cell ---------
```
Third cell is used to generate the dataset
set in_path and out_path variable for each directory
in_path = from where the program is going to read the images
out_path = where program is going to save to save patches of images
you can also specify the file extenion in generate_patches() function
example:
in_path = "drive/My Drive/segmentation_monuseg/unet_MonuSeg/MonuSeg/Training/GroundTruth/"
out_path = "drive/My Drive/new_short_monuseg/Training/GroundTruth/"
generate_patches(in_path,out_path,".png")

It generates 49 patches of shape(256,256,3) for each image
```

