# CodeClause_Brain_Tumor_Detection_with_Data_Science

  This is my second task for the CodeClause Data Science Internship programme. In this project, Brain tumor detection using transfer learning involves utilizing the VGG19 model, a pre-trained convolutional neural network (CNN), as a base model. 
  
  The VGG19 model is initialized with weights from the ImageNet dataset and the top layer is excluded. Additional layers are added to the model, including a flattening layer, a dropout layer for regularization, and a dense layer with a sigmoid activation function for binary classification. The weights of the pre-trained model are frozen to prevent them from being updated during training. The model is compiled with a binary cross-entropy loss function, Adam optimizer, and accuracy as the evaluation metric.
  
  To train the model, a training data generator is created using the training dataset and data augmentation techniques such as rescaling, rotation, shifting, shearing, zooming, flipping, and filling. This generator generates batches of augmented training data.

A callback is defined to reduce the learning rate when the validation accuracy plateaus, which helps fine-tune the model. Another callback is implemented to stop the training when the validation accuracy reaches 90%.

Similarly, a validation data generator is created using the validation dataset and appropriate data preprocessing. This generator generates batches of preprocessed validation data.

The model is trained using the training data generator, validation data generator, and the defined callbacks. The training is performed for a specified number of epochs, with the model's performance and accuracy monitored during training.
