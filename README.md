# face_detection_model

The project was implemented during my summer internship(2023) as a graduate research intern where i was saddled with the task of building a face detection model that can help detect and measure the attention of students in digital learning class. This is the intial implementation of the project as it hopes to detect more facial expressions of students in order to perfected classify their state of mind while learning. 

## Model Implementation 

When incorporating a model, it's advantageous to start with an existing predefined model that has been created using a similar dataset of your interest. This process is referred to as Transfer Learning. It involves utilizing an already pretrained model by employing its lower layers as a foundation and adjusting only the outermost layer (fully connected layer) based on the number of outputs or classification you're concerned with. For this model implementation, we will be building upon a pretrained model within the TensorFlow machine learning framework known as Visual Geometry Group 16 (Vgg16). Vgg16 constitutes a deep convolutional neural network architecture tailored for image classification. This model was trained with an extensive 16 million parameters (Simonyan, K., et al., 2014). 

## Data Collection and Data Preprocessing 

Keeping our model's objective in mind — accurately identifying and classifying individuals' faces through a webcam — we opted to construct a dataset of varied facial poses utilizing the OpenCV library and our webcam. While we initially aimed to capture diverse faces, we eventually chose to focus on a single individual's face and employed image augmentation methods to generate diverse versions of that face. Initially, our training dataset comprised 42 images of this individual's face, while the test and validation datasets each consisted of 9 images of the same individual. 

## Training the Model 

As previously mentioned, the model will be constructed using the pre-trained Vgg16 model from the TensorFlow framework. The model will be configured with the following hyperparameters: 

- Batch size: 8 
- Epochs: 10 
- Learning rate: 0.003 
- Optimizer: Adam 
- Loss function: Binary cross entropy loss


## Assessing Model Performance on the Test Dataset 

An additional measure to gauge the model's effectiveness involves evaluating it with a fresh set of data that it hasn't encountered before. This assessment was conducted through two methods. Initially, the test dataset partitioned during data preparation was utilized. Subsequently, the model's real-time performance was confirmed by applying it with a webcam. 

![Screenshot from 2023-08-12 18-25-37](https://github.com/aljebraschool/face_detection_model/assets/48502023/c1de4e05-d66a-4be5-a62c-d6165df12860)





