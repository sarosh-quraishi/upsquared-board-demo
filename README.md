# upsquared-board-demo
Demo of upsquared board (different hardware targets) with openvino and plaidml


## System requirement

- 6th-8th Generation Intel® Core™
- Intel® Xeon® v5 family
- Intel® Xeon® v6 family
### Operating Systems

- Ubuntu* 16.04.3 long-term support (LTS), 64-bit
- CentOS* 7.4, 64-bit
- Windows* 10, 64-bit

## How to Run
Require [Python 3.5+](https://www.python.org/ftp/python/3.6.4/python-3.6.4.exe) and [Jupyter notebook](https://jupyter.readthedocs.io/en/latest/install.html) installed
### Clone or download this repo
```
git clone https://github.com/sarosh-quraishi/upsquared-board-demo
```
### Install OpenVINO
Setup OpenVINO on your machine, choose your OS on [this page](https://software.intel.com/en-us/openvino-toolkit/choose-download), follow the instruction to download and install it.

### download and install miniconda from https://docs.conda.io/en/latest/miniconda.html and start an environment with
'''
conda create -n py35 python=3.5
'''

### Install required libraries
`pip3 install -r requirements.txt`

### set up PlaidML to use a preferred computing device:

plaidml-setup

### Install ncssdk (if you have Movidius Myriad processor)
'''
git clone -b ncsdk2 http://github.com/Movidius/ncsdk && cd ncsdk && make install
'''

Run the `setupvars.bat` before launching jupyter notebook.
```
C:\Intel\computer_vision_sdk\bin\setupvars.bat
```
Or in Linux
add the following line to `~/.bashrc`
```
source ~/intel/computer_vision_sdk/bin/setupvars.sh
```
In a terminal run,
```
jupyter notebook
```

In the opened browser window open
```
keras-openvino-ImageNet.ipynb
```





