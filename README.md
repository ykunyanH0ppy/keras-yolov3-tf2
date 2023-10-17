# YOLO3 (Detection, Training, and Evaluation)

## Installing

To install the dependencies, run
```bash
pip install -r requirements.txt
```
And for the GPU to work, make sure you've got the drivers installed beforehand (CUDA).

It has been tested to work with Python 3.8 and Tensorflow-macos 2.9.0 and tensorflow-metal 0.5.0

## PreTraining Model 

Download pretrained weights for backend at:
https://bit.ly/39rLNoE 

Download backend.h5 and put it at folder keras-yolov3

## Training data
Uzip the dataset.zip at folder keras-yolov3

## Training

`python train.py -c config.json`

By the end of this process, the code will write the weights of the best model to file best_weights.h5 (or whatever name specified in the setting "saved_weights_name" in the config.json file). The training process stops when the loss on the validation set is not improved in 3 consecutive epoches.
