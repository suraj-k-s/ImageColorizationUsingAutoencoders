# Image Colorization Readme

## 1. Preprocessing and Creating Dataset

Preprocessing the images to create the dataset of color and grayscale image pairs.
- Normalizing the image pixel value between 0 - 1
- Resizing images
- Splitting images into train and test sets

## 2. Data Transformation

Apply transformations to your images (resizing) to prepare them for the model.

## 3. Model Architecture

Creating an Autoencoder Architecture. Has an Encoder and a Decoder in it.
- Encoder:
  - Downsampling Images:
  - The Encoder has special filters that look at the details of a picture. These filters start simple and become more complex. Think of it like zooming out from a detailed view to a bigger picture. Each filter creates a new version of the picture with fewer details. So, it's like making the picture a bit blurry, but we keep the important parts.

- Decoder:
  - Upsampling Images:
  - Now, the Decoder takes these simplified pictures and tries to recreate the original detailed picture. It uses special tools to add details back, making the picture sharper. It's like zooming back in but trying to recover the important details.

## 4. Initialize Model, Loss, and Optimizer

- Loss Function: Think of the loss function as a score that tells the computer how much it needs to improve. A lower score means the computer is getting better at coloring the pictures.
- Optimizer: If the loss function is the score, the optimizer is the coach that guides the computer to take small steps in the right direction. It's like a coach helping you improve your basketball skills by adjusting your technique.

## 5. Training Loop

- Practice Sessions (Epochs): We're giving the model many practice sessions. In each session, it looks at pictures and tries to add colors.
- Breaking Practice into Steps (Batches): Each practice session is divided into smaller steps. In each step, the model looks at a bunch of pictures.
- Looking at Pictures: The model looks at both a grayscale picture (no colors) and a real-colored picture.
- Trying to Colorize: It tries to add colors to the grayscale picture using its current skills.
- Checking its Work (Loss): Checks how different the model's colored picture is from the real one. This difference is called "loss."
- Getting Feedback (Optimization): The optimizer tells the model how to adjust its coloring strategy to get closer to the real colors. This is the model's way of getting better.
- Many Rounds of Practice (Iterations): The model repeats these steps many times, practicing and adjusting its approach to coloring.
- Getting Better Each Time: After each round of practice, we check how much the model improved on average.
- Finally: After all the practice sessions, we say, "Training Finished!" The model has learned how to color pictures better.

## 6. Evaluation on Test Data

Evaluating the performance of your trained model on the testing data.

## 7. Predictions

Finally, use the trained model to predict colors for new grayscale images.

## 8. Saving the Model

Save the trained model for future use and integration into various applications.
