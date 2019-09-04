# Facial-Recognition-Engine
A robust design facial recognition engine based on Google facenet model. Major advantage of this model over others is that it's based on one shot learning algorithm that is it does not require a big dataset of an individual for recognition. You can find the link to google facenet research [here](https://arxiv.org/pdf/1503.03832.pdf).

Another advantage of this system is that it does not required to be trained again and again, every time a new face is added to the database. The model takes the embedding of the face and embed the face-vector in multi dimensional space. The verification and recognition process takes the eucledian distance between the faces. A KNN classifier classifies the same faces in a cluster. A simple example is shown below.

![Alt Text](https://github.com/quickcatcher/Facial-Recognition-Engine/blob/master/Capture2.JPG)

## Pre-requisite
I recommend all of you to go through the research paper first before using this. Tensorflow, keras and dlib are the standard dependencies for this project. I have attached a requirement.txt file which contains the list of all the liberaries required.

## Face detection and alignment
For detection we have used the alignment.py file. We can also use other methods for detection like MTCNN model but remeber to resize the image according to the required dimensions. The dlib liberary is used for alignment of the face. After the alignment the face is fed to the neural networks for embedding.
