# cmpe-258-hw1
Homework 1 - Deep Learning Class

part 1 - Blackbox Deep Learning using Fast AI colab https://github.com/fastai/fastbook/blob/master/01_intro.ipynb
Write Colab for illustrating use of SOTA(state of the art) model architectures of fast ai using 
1. cnn_learner for image classification
2. unet_learner for segmentation, 
3. text_classifier_learner for sentiment analysis
4. tabular-learner for decision tree
5. collab_learner for ranking

part 2 - Whitebox Deep Learning read and perform the codelab https://codelabs.developers.google.com/codelabs/cloud-tensorflow-mnist#0
Follow the colab training instructions will updates only with the deliverables.
3.  Run through all the cells - no error encountered except it runs without GPU connect eventhough the runtime setting selected is GPU.
6.  Adding layer Sigmoid function resulted to poor model performance. 
7.  Special care for deep networks
    Replace all activation sigmoid function with RELU ( Rectified Linear Unit ), and optimizer = 'sgd' with optimizer = 'adam' 
    Result : 99% accuracy
8. Learning rate decay 
   a.Increase the learning rate default value of 0.001 to 0.01 with an actual instance of Adam optimizer
   optimizer=tf.keras.optimizers.Adam(lr=0.01)
   b. Change the zoom factor from 1 to 5
   Rerun the model and update the result.
   Result : The loss or training curve  is too bad like it is jumping from up to down.
   c. Implement a good solution using learning rate scheduler callback
   d. Add the lr_decay_callback to model.fit callbacks[plot_training, lr_decay_callback]
   Rerun the model and update the result.
   Result: Accuracy is above 98% and noise in the data is gone.

