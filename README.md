# dpu - Xilinx DPU/DNNDK example

- __Environment__

  - DNNDK: v3.1
  - DPU: v3.0 (TensorFLow v1.12)
  - PetaLinux/XSDK: 2018.3
  - Python: 3.6.9 (miniconda)
  - CPU only (otherwise specified)

***

## Preparation

- __Tutorial__

  - Clone [Xilinx Edge AI Tutorials repo](https://github.com/Xilinx/Edge-AI-Platform-Tutorials)

  ```shell-session
  $ git clone https://github.com/Xilinx/Edge-AI-Platform-Tutorials.git
  ```

- __DNNDK (v3.1)__

  - Get DNNDK  _xilinx_dnndk_v3.1_190809.tar.gz_ from [Xilinx website](https://www.xilinx.com/products/design-tools/ai-inference/ai-developer-hub.html#edge)

  - Copy DNNDK library

  ```shell-session
  $ tar xf xilinx_dnndk_v3.1_190809.tar.gz

  $ cp -R xilinx_dnndk_v3.1/ZedBoard/pkgs/include/* pkg_zynq/include/
  $ cp -R xilinx_dnndk_v3.1/ZedBoard/pkgs/lib/*     pkg_zynq/lib/

  # Create symbplic link to dputils
  # Depending on OpenCV version on the board
  $ cd pkg_zynq/lib/
  $ ln -s libdputils.so.3.3 libdputils.so
  $ cd ../..
  ```

  - Install DNNDK tools

  - Install TensorFlow

- Then go to the project direrctory of your choice