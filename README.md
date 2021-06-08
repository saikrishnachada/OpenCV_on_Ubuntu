# Install OpenCV 4.5.2 on Ubuntu 18.04

OpenCV is an open-source computer vision library. To install OpenCV 4.5.2 on Ubuntu 18.04, I have followed the below steps.

### 1. You need to install some packages

```bash
~$ sudo apt update
~$ sudo apt install python3-opencv
```

### 2. Clone the Github repositories

```bash
~$ git clone https://github.com/opencv/opencv.git
~$ git clone https://github.com/opencv/opencv_contrib.git
```

### 3. Navigate to the build folder

```bash
~$ cd opencv
~$ mkdir build 
~$ cd build
```

### 4. CMake

```bash
~$ cmake -DCMAKE_BUILD_TYPE=RELEASE -DCMAKE_INSTALL_PREFIX=/usr/local -DFORCE_VTK=ON -DWITH_TBB=ON -DWITH_V4L=ON -DWITH_QT=ON -DWITH_OPENGL=ON -DWITH_CUBLAS=ON -DCUDA_NVCC_FLAGS="-D_FORCE_INLINES" -DWITH_GDAL=ON -DWITH_XINE=ON -DOPENCV_EXTRA_MODULES_PATH=../../opencv_contrib/modules -DBUILD_EXAMPLES=ON ..
```

### 5. Finally, install 

```bash
~$ sudo make install
```
