

Specs:
CUDA 10.0
cuDNN 7.4.6
Tensorflow 1.14.0
Python 3.7.6
        
Getting the Nvifer.dll file
____________________________
Download TensorRT's C++ API according to he specs and copy the Nvifer.dll file from samples\lib\

Getting the Data:
________________

1. Open cmd/AnacondaPrompt and navigate to 'path_to_folder\Inference\data\mnist\'


2. Run the following command:
python donwload_pgms.py --output = path_to_folder\Inference\data\mnist\
3. This shall download the test image files of fashion_mnist dataset in '.pgm' format.
4. This file shall also download the labels of the file and store them in 'labels.txt'
5. Make sure your image and label file are in the same directory as above

NOTE: Make sure you complete this step first and verify that they are in the correct folder


The Setup:
________________


1. Make sure you have downloaded the necessary files from 'requirements.txt'
2. Open VS Studio and open VS C++ project 'sample_uff_mnist.vcxproj'
3. Build the project and you would create a cuda engine application in 'Inference\bin'.






Running the Project:
________________


1. Through your command terminal go to 'path_to_folder\Inference\bin\
2. Run the command:
sample_uff_mnist.exe --datadir=path_to_folder\Inference\data\mnist\
3. You shall get the accuracy and Latency of the model.
