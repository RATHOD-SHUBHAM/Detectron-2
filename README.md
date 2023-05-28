# Detectron2-on-Custom-Object-Detection-Data

Detectron2 to For custom objects :
  Detectron2 is a popular PyTorch based modular computer vision model library. \
  It is the second iteration of Detectron, originally written in Caffe2. \
  The Detectron2 system allows you to plug in custom state of the art computer vision technologies into your workflow.
  
  
Steps:
  1. Install Detectron2 dependencies.
  2. Download custom Detectron2 object detection data.
  3. Visualize Detectron2 training data.
  4. Write our Detectron2 training configuration.
  5. Run Detectron2 training.
  6. Evaluate Detectron2 performance.
  7. Run Detectron2 inference on test images.

---

### 1] Car VIN number detection

  1. Install Dependencies.
  2. Import Dependencies.
  3. Import the necessary packages in your Python script.
  4. Load Configuration and Model Weights: Initialize the Detectron2 configuration and load the pre-trained weights for the model.
  5. Load and Preprocess the Image: Load the image containing the VIN number and preprocess it for inference.
  6. Run Inference: Use the predictor to run inference on the preprocessed image.
  7. Visualize the Results: Visualize the predictions on the image using the Visualizer.
  8. Display or Save the Result: Display or save the resulting image with the bounding boxes around the VIN number.

Dataset:

  Vin detection:
  
  <img width="811" alt="Screenshot 2023-05-08 at 4 49 30 PM" src="https://user-images.githubusercontent.com/58945964/236944557-5d7879c0-bf92-4021-82e0-7e3684c1e1ff.png">
    
---

### 2] Car Damage Detection

Here's a step-by-step breakdown of how I did it:

  1. Data Collection: The initial phase was to collect images relevant to the object detection task. I used RoboFlow's custom dataset for this task.

  2. Data Preparation: The best aspect of Roboflow is that we can acquire the data in any format we like. I thus picked a format that was compatible with Detectron 2. I then preprocessed the data to ensure it was in a suitable format for training.

  3. Model Configuration: I configured the Detectron 2 framework by selecting the appropriate backbone architecture, such as Fast RCNN, and fine-tuning the hyperparameters according to the specific requirements of my object detection task. This step laid the foundation for the subsequent model training.

  4. Model Training: Using the preprocessed dataset and the configured Detectron 2 model, I started the training phase. The model was trained on the custom dataset, iteratively learning to identify and localize objects within the images. I employed techniques like learning rate scheduling to optimize the model's performance.

  5. Model Evaluation: After training, it was crucial to evaluate the model's performance to gauge its accuracy and robustness. I employed various evaluation metrics, including mean average precision (mAP), precision, recall, and F1 score, to assess the model's ability to detect objects accurately across different classes.

  6. Model Deployment: The final step will be to containerize and deploy it in an environment such as on-premises or the cloud.

The model output was an object detection system capable of accurately identifying and localizing objects within an image. This technology holds immense potential for various applications, including autonomous systems, surveillance, and more.



![download](https://github.com/RATHOD-SHUBHAM/Detectron/assets/58945964/73e1a429-6078-4c49-b821-de92d68985fb)
