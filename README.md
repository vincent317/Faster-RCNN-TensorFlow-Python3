# tf-faster-rcnn
Environment setup list (required):
1. Python 3.6
2. CUDA 10.0
3. cuDNN 7.4 for CUDA 10.0
4. tensorflow_gpu-1.14.0
5. Visual Studio C++ Build Tools 2015

# How To Use This Branch
1. Install tensorflow, preferably GPU version. Follow [instructions]( https://www.tensorflow.org/install/install_windows). If you do not install GPU version, you need to comment out all the GPU calls inside code and replace them with relavent CPU ones.

2. Checkout this branch

3. Install python packages (cython, python-opencv, easydict) by running  
`pip install -r requirements.txt`   
(if you are using an environment manager system such as `conda` you should follow its instruction)

4. Go to  ./data/coco/PythonAPI  
Run `python setup.py build_ext --inplace`  
Run `python setup.py build_ext install`  
Go to ./lib/utils and run `python setup.py build_ext --inplace`

5. Follow [these instructions](https://github.com/rbgirshick/py-faster-rcnn#beyond-the-demo-installation-for-training-and-testing-models) to download PyCoco database.
I will be glad if you can contribute with a batch script to automatically download and fetch. The final structure has to look like  
`data\VOCDevkit2007\VOC2007`  

1. Download pre-trained VGG16 from [here](http://download.tensorflow.org/models/vgg_16_2016_08_28.tar.gz) and place it as `data\imagenet_weights\vgg16.ckpt`.  
For rest of the models, please check [here](https://github.com/tensorflow/models/tree/master/research/slim#pre-trained-models)

7. Run train.py

Notify me if there is any issue found.

