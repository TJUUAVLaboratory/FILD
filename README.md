## Fast and Incremental Loop closure Detection using Proximity Graphs

This is the C++ implementation of our IROS 2019 paper:
**Shan An**, Guangfu Che, Fangru Zhou, Xianglong Liu*, Xin Ma, Yu Chen. Fast and Incremental Loop Closure Detection using Proximity Graphs.  The 2019 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS 2019) 

**Abstract:** Visual loop closure detection, which can be considered as an image retrieval task, is an important problem in SLAM (Simultaneous Localization and Mapping) systems. The frequently used bag-of-words (BoW) models can achieve high precision and moderate recall. However, the requirement for lower time costs and fewer memory costs for mobile robot applications is not well satisfied. In this paper, we propose a novel loop closure detection framework titled `FILD' (Fast and Incremental Loop closure Detection), which focuses on an on-line and incremental graph vocabulary construction for fast loop closure detection. The global and local features of frames are extracted using the Convolutional Neural Networks (CNN) and SURF on the GPU, which guarantee extremely fast extraction speeds. The graph vocabulary construction is based on one type of proximity graph, named Hierarchical Navigable Small World (HNSW) graphs, which is modified to adapt to this specific application. In addition, this process is coupled with a novel strategy for real-time geometrical verification, which only keeps binary hash codes and significantly saves on memory usage. Extensive experiments on several publicly available datasets show that the proposed approach can achieve fairly good recall at 100\% precision compared to other state-of-the-art methods. The source code can be downloaded at https://github.com/AnshanTJU/FILD for further studies.

An overview of the proposed loop closure detection method:
![Flowchart](./images/flowchart.jpg)

## License
The project is licensed under the New BSD license. It makes use of several third-party libraries:

hnswlib: https://github.com/nmslib/hnswlib

Theia Vision Library: http://theia-sfm.org/

## Related Publications
If you find this work useful in your research, please cite:
**Shan An**, Guangfu Che, Fangru Zhou, Xianglong Liu, Xin Ma, Yu Chen. Fast and Incremental Loop closure Detection using Proximity Graphs. The 2019 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS 2019) 


## install and use

**caffe 使用gcc5编译　FILD使用gcc4.9编译　！！！**

### install caffe-augmentation

```bash
 ## install hdf5 
 sudo apt-get install libhdf5-dev
 ## in the Makefile.config
 INCLUDE_DIRS := $(PYTHON_INCLUDE) /usr/local/include /usr/include/hdf5/serial 
 LIBRARY_DIRS := $(PYTHON_LIB) /usr/local/lib /usr/lib /usr/lib/x86_64-linux-gnu/hdf5/serial

 ## install leveldb  lmdb
 sudo apt-get install libleveldb-dev liblmdb-dev

  ## in the file  include/caffe/common.hpp  common
  // #ifndef GFLAGS_GFLAGS_H_
   namespace gflags = google;
  // #endif  // GFLAGS_GFLAGS_H_

```