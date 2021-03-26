# Face-Mask-Detection

<img width="1026" alt="image" src="https://user-images.githubusercontent.com/81297719/112594376-d6e67780-8e2e-11eb-95f5-85b2d9e6b91c.png">

## Defining YOLO
The YOLO model divides the image into an even grid and simultaneously predicts bounding boxes, confidence in those boxes, and class probabilities.

Unlike the detection algorithms YOLO reframes the object detection  problem as a regression problem and predicts the classes and bounding boxes of the whole image at a single run and thus detects multiple objects using a single neural network.

Therefore due to YOLO being based on regression problem , the use of a complex pipeline is not required which increases its speed.

In the CNN layers The initial convolutional layers of the network extract features from the image while the fully connected layers predict the output probabilities and coordinates.

The YOLO model is an algorithm that is an extension of the Darknet framework which is an open source Neural network framework written in C and CUDA. Using the Darknet framework we can localise the detection area that is to be fed to the YOLO model.

Here, I have created our own localisation script using OpenCv in Python, which uses the YOLO model for prediction.

## Data Set

The dataset was collected from Kaggle and Google images. The dataset was categorised into 2 classes:  with_mask  and without_mask.  A total of 1315 images were used in the training process and the model was tested on 194 images.

<img width="423" alt="image" src="https://user-images.githubusercontent.com/81297719/112594642-40668600-8e2f-11eb-881a-a74e3996d51f.png">|<img width="288" alt="image" src="https://user-images.githubusercontent.com/81297719/112594668-4a888480-8e2f-11eb-886e-25b5bf5b818e.png">|<img width="232" alt="image" src="https://user-images.githubusercontent.com/81297719/112594691-5116fc00-8e2f-11eb-8c99-6328be985fc6.png">|<img width="288" alt="image" src="https://user-images.githubusercontent.com/81297719/112594708-55431980-8e2f-11eb-9f08-4ae07cbfc2b8.png">|<img width="301" alt="image" src="https://user-images.githubusercontent.com/81297719/112594721-596f3700-8e2f-11eb-8474-1546b97db0f1.png">

## Analysis/Findings

As we can see , the model is able to detect the incorrect orientation of the mask also.  The model creates a red bounding box when the without_mask class is recognised with the no mask annotation.  Else it creates a green bounding box around the Region of Interest with the mask annotation

![image](https://user-images.githubusercontent.com/81297719/112594798-77d53280-8e2f-11eb-9f86-488833fb012b.png)|![image](https://user-images.githubusercontent.com/81297719/112594806-7b68b980-8e2f-11eb-8fd8-95dcb634d320.png)|![image](https://user-images.githubusercontent.com/81297719/112594839-89b6d580-8e2f-11eb-8c15-422cd16855f0.png)








