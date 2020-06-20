
# GPU set-up for Tensorflow/Pytorch

### 1.  Driver update - DO NOT SKIP THIS STEP !
a. Verify information related to your graphic card

b. Go to the following link: https://www.nvidia.com/download/index.aspx?lang=en-us 

c. Download and install driver

### 2. CUDA Toolkit download
##### NOTE: Before downloading cuda toolkit, it is necessary to check the compatibility match up between Tensorflow/Pytorch and version of cuda toolkit. As of 2020-05-20  tensorflow - 2.2.0 is compatible with CUDA10.1 . So as of  now installl CUDA toolkit 10.1 even though newer versions are available. Ref: https://stackoverflow.com/questions/50622525/which-tensorflow-and-cuda-version-combinations-are-compatible
a. Before downloading CUDA toolkit you need to  download visual studios, this is done to ensure all features of CUDA toolkit are downloaded. Go to the following link: https://visualstudio.microsoft.com/downloads/

b. Download CUDA toolkit from https://developer.nvidia.com/cuda-10.1-download-archive-base

### 3. cuDNN download

#### What is cuDNN? 
CUDA Deep Neural Network library (cuDNN) is a GPU-accelerated library of primitives for deep neural networks. cuDNN provides highly tuned implementations for standard routines such as forward and backward convolution, pooling, normalization, and activation layers.
 

a. Before downloading cuDNN you need to create account with nvidea. Go to the following link https://developer.nvidia.com/rdp/form/cudnn-download-survey and create your account, you will be prompted to verify account by sending you an email.

b. Download the cuDNN for the appropriate version of CUDA 

c. Unzip the file

d. MOVE <LOCATION OF cuDNN extraction>\cudnn-10.1-windows10-x64-v7.5.0.56\cuda\bin\cudnn64_7.dll to C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.1\bin\

e. MOVE <LOCATION OF cuDNN extraction>\cudnn-9.0-windows10-x64-v7.5.0.56\cuda\lib\x64\cudnn.lib to C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.1\bin\

f. MOVE <LOCATION OF cuDNN extraction>\cudnn-10.1-windows10-x64-v7.5.0.56\cuda\ include\cudnn.h to C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.1\bin\


### 4. ENVIROMENT VARIABLES

1. Check CUDA_PATH variable which will be set to point to the location of CUDA toolkit.
2. ADD the following locations to the PATH variable:
a. C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.1\bin

b. C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.1\libnvvp


### 5. INSTALL TENSORFLOW
pip install  tensorflow-gpu
(Currently stable release is 2.2.0)


### 6. INSTALL Pytorch
conda install pytorch torchvision cudatoolkit=10.1 -c pytorch

### 7. TEST Tensorflow
tf.test.is_built_with_cuda()

### 8. TEST Pytorch
torch.cuda.is_available()

#### REFERENCE:
1. https://towardsdatascience.com/installing-tensorflow-with-cuda-cudnn-and-gpu-support-on-windows-10-60693e46e781




```python

```
