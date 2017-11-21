# Semantic Segmentation

Hyperparameters used

1. Number of Epochs used - Total Number of epochs = 60
    1.  40 epochs with learning rate = 0.0001
    2.  10 epochs with learning rate = 0.00001
    3.  10 epochs with learning rate - 0.000001
2. Batch Size = 8. Experimented with batch_size of 1 for a NVIDIA 940MX GPU but it ran out of memory. Trained the FCN using CPU only ( which took 2 sitting of 6 hours each).
Tried batch size of 16 but that crashed.

3. There was no data augmentation and this still led to good results on the test data set.
But the results from the video indicate that augmentation would be really helpful.

4. The final loss of the model is shown in the image below -

![Alt text](./loss.png?raw=true "Final Loss")

A link to the video can be found here - https://youtu.be/Fvoe6KXnBns

### Setup
##### Frameworks and Packages
Make sure you have the following is installed:
 - [Python 3](https://www.python.org/)
 - [TensorFlow](https://www.tensorflow.org/)
 - [NumPy](http://www.numpy.org/)
 - [SciPy](https://www.scipy.org/)
##### Dataset
Download the [Kitti Road dataset](http://www.cvlibs.net/datasets/kitti/eval_road.php) from [here](http://www.cvlibs.net/download.php?file=data_road.zip).  Extract the dataset in the `data` folder.  This will create the folder `data_road` with all the training a test images.

##### Run
Run the following command to run the project:
```
python main.py
```
