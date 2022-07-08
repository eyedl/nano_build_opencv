# OpenCV build script for Tegra

This script builds OpenCV from source on Tegra (Nano, NX, AGX, etc.).

Related thread on Nvidia developer forum 
[here](https://devtalk.nvidia.com/default/topic/1051133/jetson-nano/opencv-build-script/).

[How it Works](https://wiki.debian.org/QemuUserEmulation)

## Usage:
```shell
./build_opencv.sh
```

## Specifying an OpenCV version (git branch)
```shell
./build_opencv.sh 4.4.0
```

Where `4.4.0` is any version of openCV from 2.2 to 4.4.0
(any valid OpenCV git branch or tag will also attempt to work, however the very old versions have not been tested to build and may require spript modifications.).

**JetPack 4.4 NOTE:** the minimum version that will build correctly on JetPack 4.4 GA is 4.4.0. Prior versions of JetPack may need the CUDNN version adjusted (the `-D CUDNN_VERSION='8.0'` line can simply be removed).

## IMPORTANT
This installer should work for a fresh Jetson Nano that was build using the NVIDIA SD card image found here: https://developer.nvidia.com/embedded/learn/get-started-jetson-nano-devkit. 
- make sure that python 3.6(.9) is installed as this build only works using that. 
- Ensure that NVIDIA Jetpack is installed using sudo apt commands (https://docs.nvidia.com/jetson/jetpack/install-jetpack/index.html)
