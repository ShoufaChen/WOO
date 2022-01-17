# Installation

## Requirements
- Python >= 3.6
- PyTorch >= 1.5
- GCC >= 4.9
- cython: `pip install -U cython`
- simplejson: `pip install simplejson`
- PyAV: `conda install av -c conda-forge`
- iopath: `pip install -U iopath` or `conda install -c iopath iopath`
- psutil: `pip install psutil`
- OpenCV: `pip install opencv-python`
- tensorboard: `pip install tensorboard`
- moviepy: (optional, for visualizing video on tensorboard) `conda install -c conda-forge moviepy` or `pip install moviepy`


## Install Detectron2
```
git clone https://github.com/facebookresearch/detectron2.git
python -m pip install -e detectron2
```
If have to reinstall, first:
```
rm -rf build/ **/*.so
```

## Install Apex (optional)
```
git clone https://github.com/NVIDIA/apex
cd apex
pip install -v --disable-pip-version-check --no-cache-dir --global-option="--cpp_ext" --global-option="--cuda_ext" ./
```

For old env, (e.g.  cuda9.0, torch.15), you should rollback apex to earlier version
```
# https://github.com/NVIDIA/apex/issues/802#issuecomment-618699214
git checkout f3a960f80244cf9e80558ab30f7f7e8cbf03c0a0
```

## Build

After having the above dependencies, run:
```
git clone https://github.com/ShoufaChen/WOO.git
cd WOO
python setup.py build develop
```

Now the installation is finished.
