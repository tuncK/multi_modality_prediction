# Multi modality prediction
Multi modality prediction is a representation learning-based tool that aims to correctly predict the classes of previously unseen data by machine learning on high-throughput high-dimensional data. If data from multiple data acquisition methods are available, their statistical power is combined to improve the classification accuracy.

Inspired by [DeepMicro](https://www.nature.com/articles/s41598-020-63159-5).


## Quick Setup Guide

**Step 1:** Change the current working directory to the location where you want to install `multi_modality_prediction`.

**Step 2:** Clone the repository using git command.
```
git clone https://github.com/tuncK/multi_modality_prediction
cd multi_modality_prediction
```

**Step 3:** Create a virtual environment using conda.
```
conda create --name mmp python=3.11
```

**Step 4:** Activate the created virtual environment.
```
conda activate mmp
```

**Step 5:** Install required packages
```
pip install hpbandster==0.7.4 keras==2.12.0 matplotlib==3.7.1 numpy==1.23.5 pandas==2.0.2 scikit-learn==1.2.2 scikit-optimize==0.9.0 scipy==1.10.1
```

**Step 6:** Install tensorflow.
* If your machine is *not* equipped with GPU, install tensorflow CPU version
```
pip install tensorflow-cpu==2.12.0
```
* If it is equipped with GPU, then install tensorflow GPU version
```
pip install tensorflow==2.12.0
```

**Step 7:** Set environment variables
* Due to various incompatibility reasons, the installation above may not work out of the box or execute with a lower performance than it could. It might generate some warnings such as "tensorrt not found". If so, set the following environment variables. This makes them persistent within this conda env each time it is activated:
```
conda env config vars set PATH="$PATH:/usr/local/nvidia/bin:/usr/local/cuda/bin"
conda env config vars set LD_LIBRARY_PATH="$LD_LIBRARY_PATH:$CONDA_PREFIX/lib/python3.11/site-packages/tensorrt_libs/"
```

