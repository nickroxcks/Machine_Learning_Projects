# Dog Breed Image Classification

This project discusses how to train an image classification model from scratch to detect and correctly identify dog breeds. You will be able to utilize the model created to test against your own dog images to identify what breed of dogs are in your images. 

![image](https://github.com/user-attachments/assets/91652714-c54a-42d1-afff-ba42d12c24d9)

There are 2 Google Collab notebooks in this repository. 

1. DetectDogBreed.ipynb
2. end-to-end-god-vision.ipynb

DetectDogBreed.ipynb will allow you to utilize the trained model to test your own dog images, and end-to-end-god-vision.ipynb will go into full detail how the model is created

## How this model was built

This type of identification problem in machine learning is called **"multi-class image classification"**. It's multi-class because we're trying to classify mutliple different breeds of dog.

Our goal is to build a model capable of detecting and labeling dog breeds. So from a high level, our model needs to be capable of 2 things.

1. Be able to recognize different colors at different pixel locations in an image and identify patterns.
2. Use these pixel paterns and shapes to classify the breed of the dog.

Of course, building an entire machine learning model from scratch which specializes in classifying images is extremely time consuming. Since the goal is not to re-invent image classification models, 
but rather to focus on using image classification to detect dog breeds, we can utilize a technique called Transfer Learning.

**Transfer learning** is the idea of using an already existing model which specializes in a specific domain/function, and then applying it to another similar problem. In our case, TensorFlow Hub is a 
website which contains many pre-trained image classification models. There is also lot's of existing data out there on different dog breeds through websites such as Kaggle. So what we can do is download a 
model from TensorFlow Hub which specializes in classifying images, and then use transfer learning to further train that model on a dog breed dataset from Kaggle. 
This will result in a model which can look at images by analyzing RGB() patterns in pixels, and using the patterns to identify dog breeds. Therefore, the following 6 steps were taken to train this model:

1. Get data ready (download from Kaggle, store, import).
2. Prepare the data (preprocessing, the 3 sets, X & y).
3. Choose and fit/train a model (TensorFlow Hub, tf.keras.applications, TensorBoard, EarlyStopping).
4. Evaluating a model (making predictions, comparing them with the ground truth labels).
5. Improve the model through experimentation (start with 1000 images, make sure it works, increase the number of images).
6. Save, sharing and reloading your model (once you're happy with the results).
