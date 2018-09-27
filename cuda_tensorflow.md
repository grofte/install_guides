# Install Tensorflow / CUDA on Ubuntu 18.04 with Nvidia Optimus 

1. have the proprietary Nvidia drivers installed - use the Nvidia software 
to switch to using the GPU rather than the Intel graphics (reboot)

2. go to https://developer.nvidia.com/cuda-downloads and get the CUDA 
toolkit - the network version installer is tiny and will get files from the net as needed

3. follow the install instructions for the toolkit - takes a while to run  

4. make a new conda environment. I used the following but you might want other packages  
`conda create -n cuda python=3 jupyter numba cudnn tensorflow-gpu numpy scipy matplotlib seaborn`  
The essentials are `cuda cudnn tensorflow-gpu`. You probably also want sklearn so `pip install sklearn`

5. `source activate cuda` obviously
