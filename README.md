# WIP - face_detection - A Face Detector in Rust

Face detection is very useful, but there's currently no Rust implementation. 

I've identified a [BSD-licensed face detection library](https://github.com/imazen/SeetaFaceEngine) in C++ that has no third-party dependencies, is cross-platform, and clocks in a 2,200 lines of code.

I'd like to port this to Rust, so that I (and the community) have a safe AND fast face detection library.

The C++ source code is located in the /seeta/ directory.

```

----------------------------------------------------------------------------------------------
File                                                       blank        comment           code
----------------------------------------------------------------------------------------------
src/feat/surf_feature_map.cpp                                 51             48            403
src/fust.cpp                                                  46             32            304
src/feat/lab_feature_map.cpp                                  25             30            128
include/util/math_func.h                                      18             30            121
include/util/image_pyramid.h                                  34             30            111
include/feat/surf_feature_map.h                               33             36            109
src/face_detection.cpp                                        25             30             85
include/classifier/mlp.h                                      23             30             76
src/test/facedetection_test.cpp                               18             30             63
src/io/surf_mlp_model_reader.cpp                              15             30             59
include/common.h                                              17             30             59
include/fust.h                                                18             30             57
src/util/nms.cpp                                              13             30             55
src/util/image_pyramid.cpp                                    15             30             54
CMakeLists.txt                                                11              6             52
include/classifier/lab_boosted_classifier.h                   21             38             52
include/feat/lab_feature_map.h                                16             35             51
src/io/lab_boost_model_reader.cpp                             13             30             44
src/classifier/lab_boosted_classifier.cpp                     11             30             43
src/classifier/mlp.cpp                                         9             30             37
include/classifier/surf_mlp.h                                 14             30             35
src/classifier/surf_mlp.cpp                                    9             30             31
include/feature_map.h                                         11             30             27
include/io/lab_boost_model_reader.h                           10             30             24
include/face_detection.h                                      15             69             23
include/classifier.h                                          10             30             22
include/detector.h                                            10             30             22
include/io/surf_mlp_model_reader.h                             9             30             20
include/model_reader.h                                         9             30             16
include/util/nms.h                                             7             30             11
----------------------------------------------------------------------------------------------
SUM:                                                         536            954           2194
----------------------------------------------------------------------------------------------

-------------------------------------------------------------------------------
Language                     files          blank        comment           code
-------------------------------------------------------------------------------
C++                             12            250            380           1306
C/C++ Header                    17            275            568            836
CMake                            1             11              6             52
-------------------------------------------------------------------------------
SUM:                            30            536            954           2194
-------------------------------------------------------------------------------

```

Build instructions

```shell
cd seeta
mkdir build
cd build
cmake ..
make
```