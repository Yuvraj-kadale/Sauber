# Team Sauber

- [Aditi0102](https://github.com/Aditi0102)  
- [Swagat47](https://github.com/Swagat47)  
- [Yuvraj-kadale](https://github.com/Yuvraj-kadale)

## Setup

```
git clone https://github.com/Yuvraj-kadale/Sauber.git  # clone repo
```
>change to required directory
```
cd Sauber
```
```
cd yolov5
```
>Install Required Dependencies
```
pip install -qr requirements.txt  # install dependencies
```

## Training on Custom Data set

The custom [`Dataset`](./Dataset) built contains 121 images. These same 121 images are used for both training and validation to verify our training pipeline is capable of overfitting. [Bosch_data.yaml](./Bosch_data.yaml), shown below, is the dataset configuration file that defines 
1. A path to a directory of training images (or path to a *.txt file with a list of training images) 
2. The same for our validation images. 
3. The number of classes. 
4. A list of class names: Furniture, Door, Cable, cloth

```
# Team Sauber

train: ../Dataset_BoschAI/images/train/  # 109 images
val: ../Dataset_BoschAI/images/val/  # 27 images

# number of classes
nc: 4

# class names
names: [ 'Furniture', 'Door', 'cable', 'cloth' ]

```
## Labeling of Images

The used dataset is labelled on [makesense.ai](https://makesense.ai) and exported into YOLO format, with one *.txt file per image (if no objects in image, no *.txt file is used).   

The *.txt file specifications are:

1. One row per object (The classes specified)
2. Each row is class `x_center y_center width height` format.
3. Box coordinates must be in normalized xywh format (from 0 - 1). 
4. If your boxes are in pixels, divide `x_center` and `width` by image width, and `y_center` and `height` by image height.
5. Class numbers are zero-indexed (start from 0).

## Training and Testing

The `Training and Testing` of the Model is done in real time on [Google collab](./Team_Sauber.ipynb) with the help of its run time GPU.


## Need more help to get started?
You can refer to the following articles on basics of Git and Github.
- [Forking a Repo](https://help.github.com/en/github/getting-started-with-github/fork-a-repo)
- [Cloning a Repo](https://help.github.com/en/desktop/contributing-to-projects/creating-an-issue-or-pull-request)
- [How to create a Pull Request](https://opensource.com/article/19/7/create-pull-request-github)
- [Getting started with Git and GitHub](https://towardsdatascience.com/getting-started-with-git-and-github-6fcd0f2d4ac6)
- [Learn GitHub from Scratch](https://lab.github.com/githubtraining/introduction-to-github)





