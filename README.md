**[Language Model Implementation using Recurrent Neural Network]**

System Requirements:

- Python, pip


```bash
# Clone the repo
git clone https://github.com/ayeshreddy227/Language_Model.git
cd Language_Model


# Install requirements
pip install -r requirements.txt
```

### Setting up a CUDA-enabled GPU instance on EC2:

```bash
# Install build tools
sudo apt-get update
sudo apt-get install -y build-essential git python-pip libfreetype6-dev libxft-dev libncurses-dev libopenblas-dev  gfortran python-matplotlib libblas-dev liblapack-dev libatlas-base-dev python-dev python-pydot linux-headers-generic linux-image-extra-virtual
sudo pip install -U pip

# Install CUDA 7
wget http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1410/x86_64/cuda-repo-ubuntu1410_7.0-28_amd64.deb
sudo dpkg -i cuda-repo-ubuntu1410_7.0-28_amd64.deb
sudo apt-get update
sudo apt-get install -y cuda
sudo reboot



# Set Environment variables
export CUDA_ROOT=/usr/local/cuda-7.0
export PATH=$PATH:$CUDA_ROOT/bin
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$CUDA_ROOT/lib64
export THEANO_FLAGS=mode=FAST_RUN,device=gpu,floatX=float32
export CUDA_LAUNCH_BLOCKING=1
