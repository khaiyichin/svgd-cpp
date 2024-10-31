# SVGDCpp: Stein Variational Gradient Descent in C++

## Introduction
This library provides the [Stein Variational Gradient Descent](https://arxiv.org/abs/1608.04471) algorithm in C++. In brief, SVGD is a hybrid (variational + sampling) method that estimates an assumed model using particles. The original work proposed SVGD as a _general purpose Bayesian inference algorithm_.

## Requirements
- [Eigen 3.3+](https://eigen.tuxfamily.org/dox/index.html) - _can be installed using `apt install libeigen3-dev`_
- [CppAD v20240602+](https://github.com/coin-or/CppAD) - _from source; when installing, configure your CMake with the following flags:_
    - `-D cppad_testvector=eigen`
    - `-D include_eigen=true`
    - `-D CMAKE_BUILD_TYPE=Release`
- [OpenMP v4.5+ (201511)](https://www.openmp.org/) - _should be shipped with your compiler_
- [Doxygen](https://www.doxygen.nl/) - _required only if documentation is desired_

## Installation
1. Clone this repository and enter it.
2. Create a build directory.
    ```
    $ mkdir build
    $ cd build
    ```
3. Configure build flags (the provided values are the default).
    ```
    $ cmake .. -D BUILD_EXAMPLES=FALSE \
        -D BUILD_DOCUMENTATION=FALSE \
        -D CMAKE_BUILD_TYPE=Release
    ```
4. Build and install.
    ```
    $ make -j
    $ make install # may require sudo privileges depending on your CMAKE_INSTALL_PREFIX
    ```

## Getting Started
See the [examples directory](examples/) for tutorials on how to use them and see [here](doc/instuctions.md) for detailed instructions.