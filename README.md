# Dog_Breed_Identification
Our aim is to create a fine-grained image categorization machine-learning model, which can distinguish between similar dog breeds with high accuracy. 

The dataset we used for this project can be found on kaggle following this link:
https://www.kaggle.com/datasets/paras329/dog-images/data

Project components
-Data loading and preprocessing
-Transfer learning with MobileNetV2
-Model training and validation
-Performance evaluation
-Confusion matrix analysis
-CNN feature map visualization
-Feature vector display

Dataset
The dataset consists of dog images already separated into training, validation and test data. Each of thesee sets contain subfolders named after the dogbreed whhose images they contain. Each breed automatically gets assigned a numerical label during loading.

Model Architecture
The classifier uses:
-MobileNetV2 pretrained on ImageNet
-Global Average Pooling Layer
-Dropout layer for regularization
-Dense Softmax output layer

Transfer learning is used by freezing the convolutional base and training only the classification head.

Training Configuration
Image size: 224x224
Batch Size: 8  
Optimizer: Adam
Learning rate: 0.0001
Loss Function: Categorical Crossentropy
Metric: Accuracy

Callbacks:
-ModelCheckpoint
-EarlyStopping
-ReduceLROnPlateau

Evaluation
The traied model is evalated on the test dataset using:
-Test Accuracy
-Test Loss
-Confusion Matrix

A normalized cconfusion matrix is generated to visualize classificaion performance across breeds.

Feature Visualization
To better understand how the CNN pocesses images, the project includes:
-Input Image Visualizaton
-RGB channel visualization
-Feature maps
-Feature vectors

The project also includes a separate notebook dog_breed_visualizations containing additional examples, to better show the performance of the model.
This notebook focuses on evaluating prediction results. 
It contains examples using images from the database's test image folder, 
and also two additional examples from outside the database to show how the classifier can be applied in real life. 

The visualizations include: confidence score distribution across test predictions, examples of correctly and wrongly classified images, side-by-side comparison between misclassified images and example image of thee predicted breed, random predictions, top 5 prediction for a random image, and real world examples with predictions.

Running the project:
1. Download and organize the datase.
2. Update the paths in the notebook.
3. Run all notebook cells in sequence.
4. Train the model.
5. Evaluate performance and visualize results.

Results
The project outputs: 
-Trained MobileNetV2 classiffier
-Saved best model weights
-Test accuracy and loss
-Confusion matrix
-CNN feature maps
-Feature vector visualizations
-Dog breed predictions

Future Improvements
-Fine-tune MobileNetV2 layers
-Experiment with EfficientNet and ResNet architectures
-Hyperparameter Optimization
