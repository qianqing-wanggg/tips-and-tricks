# tensorflow
## GPU setup
The procedure for Ubuntu 18.04 can be found [here][Install CUDA with apt]

[Install CUDA with apt]:https://www.tensorflow.org/install/gpu#install_cuda_with_apt

## cuDNN
install the cuDNN library with the correct version, refer to the documentation [2.3.4.1 Ubuntu network Installation][NVIDIA CUDNN]

[NVIDIA CUDNN]:https://docs.nvidia.com/deeplearning/cudnn/install-guide/index.html

to check the package version in the repository, use:

  apt-cache search <packagename>
  apt-cache policy <packagename>
 
  
## errors
* cannot find libcusolver.so.11
  
  export LD_LIBRARY_PATH=/usr/local/cuda-11.0/lib64:/usr/local/cuda-11.0/lib64
  
  sudo ln -s /usr/local/cuda-11.0/targets/x86_64-linux/lib/libcusolver.so.10 /usr/local/cuda-11.0/targets/x86_64-linux/lib/libcusolver.so.11
  
* cannot find libcusolver.so.11 (22/nov/2021)
  
  reinstall cuda with deb(local) option
  
  https://developer.nvidia.com/cuda-downloads?target_os=Linux&target_arch=x86_64&Distribution=Ubuntu&target_version=20.04&target_type=deb_local
