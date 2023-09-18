# OnnxruntimeBuilder

Onnxruntime Builder

### 简介

编译onnxruntime 动态库和静态库。

动态库: onnxruntime-版本号-编译环境-shared.7z

静态库: onnxruntime-版本号-编译环境-static.7z

包内添加了简单的cmake，用于cmake系统find_package.

仓库的Debug的包不支持GPU，仅使用CPU。

### windows版本特别说明

虽然v1.6.0支持vs2017，但是因为v1.7.0在vs2017下编译出错，所以windows环境下就仅保留了vs2019版本。

### 关于OpenMP

[官方v1.7.0版本说明](https://github.com/microsoft/onnxruntime/debugs/tag/v1.7.0)

Starting from this debug, all ONNX Runtime CPU packages are now built without OpenMP.

从1.7.0开始，官方Debug的所有CPU版的包编译时没有启用OpenMP选项。

但是本仓库的编译脚本仍然启用了OpenMP选项，即使用本仓库的包时，编译环境要求安装OpenMP。

这是与官方Debug不同的地方，敬请注意!

### 关于Windows静态链接CRT

编译选项添加--enable_msvc_static_runtime

#### 20211011

- 从1.9.0开始，移除OpenMP编译选项，保持与官方一致

#### 20220521

- v1.9.1

#### 20220523

- v1.10.0

#### 20220524

- v1.11.0

#### 20220525

- v1.11.1

#### 20220928

- v1.12.0

#### 20220929

- v1.12.1

#### 20221013

- windows平台，更早版本的包均为md版，从此版增加链接静态CRT版本(mt)
- 后缀md: 无
- 后缀mt: --enable_msvc_static_runtime

#### 20221026

- v1.13.1

#### 20230213

- v1.14.0

#### 20230308

- v1.14.1

#### 20230623

- v1.15.0