# Oxford-IIIT Pet Breed Classification Using CNN

# Dataset

The Oxford-IIIT Pet Dataset was developed by the Visual Geometry Group at the University of Oxford. It contains approximately 7,000+ images belonging to 37 different cat and dog breed categories. The images contain considerable variation in pose, scale, lighting, and background. The dataset also provides breed and other image annotations.

# Problem Statement

The objective of this project is to develop a deep-learning image classification system capable of identifying the breed of a cat or dog from an input image. A custom Convolutional Neural Network (CNN) and a pretrained ResNet18 model were implemented and compared.

# Data Preprocessing

The images were resized to 224 × 224 pixels and converted into PyTorch tensors. Pixel values were normalized using ImageNet mean and standard deviation values. The dataset was divided into training, validation, and testing sets. The official test split was kept separate and was not used during model training.

# Data Augmentation

Several augmentation techniques were applied to the training images, including random resized cropping, horizontal flipping, small rotations, and color jittering. These transformations were selected to make the model more robust to changes in image position, orientation, scale, and lighting while reducing overfitting.

# CNN Architecture

A custom CNN was developed using multiple convolutional blocks. Each block contains convolution, batch normalization, ReLU activation, and max-pooling layers. Adaptive average pooling was then used to obtain a compact feature representation. Dropout was added before the final fully connected classification layer to reduce overfitting.

# Transfer Learning

Transfer learning was implemented using a pretrained ResNet18 model. First, the pretrained convolutional layers were frozen and the final classification layer was replaced with a 37-class output layer. After feature-extraction training, the deeper ResNet layer was unfrozen and fine-tuned using a smaller learning rate.

# Experiments

Several experiments were conducted by changing learning rate, augmentation, architecture, and training strategy. The custom CNN was compared with ResNet18 feature extraction and ResNet18 fine-tuning. Accuracy, precision, recall, F1-score, validation loss, and training time were used for comparison.

# Results

The final models were evaluated on the unseen test set using accuracy, macro-precision, macro-recall, macro-F1 score, classification reports, and confusion matrices. The actual numerical results obtained from the experiments were recorded in the model comparison table.

# Prototype

A working image-classification prototype was developed using the saved trained model. The prototype allows a user to upload a cat or dog image and returns the predicted breed together with the top predicted classes and their confidence scores.

# Conclusion

The project demonstrates a complete image-classification workflow, including exploratory data analysis, preprocessing, augmentation, data splitting, CNN development, transfer learning, fine-tuning, experimentation, evaluation, model saving, and deployment through a graphical interface. The experiments demonstrate how architectural choices, augmentation, learning rate, and transfer learning can affect the performance and training behavior of an image-classification system.
