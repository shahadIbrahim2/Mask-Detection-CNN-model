# Mask-Detection-CNN-model
# Mask-Classification-CNN-Model
As a result of training the model with convolutional neural networks to determine whether people wear masks or not, the model's accuracy on the test data is 0.98.

## Discovering Directory and Paths

After declaring the paths of the dataset,the directory contains three main folders already divided into three chunks to train, test, and validate, each of which contains two directory "withmask" or "withoutmask".
Dataset
     -train
             -Withmask
             -Withoutmask
     -test
              -Withmask
              -Withoutmask
     -validation
              -Withmask
              -Withoutmask
The dataset contains 11792 pictures and labels.
Using the "OS" library, I found out how many images have masks and how many don't.

## Plotting Images

To plot the images, i used the imread() function from CV library.
![image](https://user-images.githubusercontent.com/59733680/168488173-c6e24900-02f9-4676-9cc0-53d1ce71f58d.png)


## Image Processing 

The image processing phase now starts, using the ImageDataGenerator library. With the ImageDataGenerator() function we can rescale-multiply- the data by 1/255 ,rotate the pictures by 40 degrees ,shift  the height and width by 0.2 , shear intensity is 0.2 , zoom ranges is 0.2, and randomly flip the pictures.

![image](https://user-images.githubusercontent.com/59733680/168488184-60cd841a-b723-4ed1-8fe6-6163e4063fb9.png)



After applying image processing to all the images, executed by the flow_from_directory() function, which takes the path to a directory & generates augmented data. This function will resize the images to 95 x 95, batch size is set to 15, colour mode of the images goes to RGB, which means the pictures stay colourful, class mode is categorical, and we need to shuffle the data in order to avoid pattern cheating.

![image](https://user-images.githubusercontent.com/59733680/168488204-d3a7421d-5fb1-4693-9e88-0b76d80f71d8.png)


## The model 
The structure of the convolutional neural network model
![image](https://user-images.githubusercontent.com/59733680/168488240-522b5f8b-0423-4921-8d42-a83d1a807781.png)

## Train & Test

![image](https://user-images.githubusercontent.com/59733680/168488665-fc4af76a-de4e-49d4-a8f5-9389d21b6431.png)

## Evalution 

classification report showing the main classification metrics/ accuracy .. ect

![image](https://user-images.githubusercontent.com/59733680/168488276-1a024b61-af72-49c1-86e4-f4ecb6878777.png)
