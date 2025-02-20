.. LearningSwift documentation master file, created by
   sphinx-quickstart on Thu Feb 20 14:50:18 2025.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Swift 基础
====================

一、简介
--------------------

Swift 是由 Apple 开发的一种多范式编程语言，旨在为 iOS、macOS、watchOS 和 tvOS 应用程序开发提供更强大、更安全、更高效的工具。
Swift 结合了现代编程语言的最佳特性，同时保持与现有 Objective-C 代码的兼容性。

**主要特点**：

* **安全性**
  
  Swift 设计时特别注重安全性，避免了许多常见的编程错误。例如，它强制使用可选类型（Optionals）来处理可能为空的值，从而减少了空指针异常的风险。

* **性能优化**
  
  Swift 的编译器和运行时环境经过高度优化，提供了接近 C 和 Objective-C 的性能，同时简化了语法和内存管理。

* **简洁的语法**
  
  Swift 的语法简洁明了，易于阅读和编写。它去除了许多冗余符号，如分号结尾，并引入了更直观的字符串插值、闭包表达式等特性。

* **交互式 playground**
  
  Swift 提供了 Playground 功能，允许开发者在实时环境中编写和测试代码，非常适合学习和快速原型设计。

* **跨平台支持**
  
  虽然 Swift 最初是为 Apple 平台设计的，但它现在也支持 Linux 和其他操作系统，甚至可以通过 WebAssembly 在浏览器中运行。

**应用场景**：

* **移动应用开发**
  
  Swift 是开发 iOS 和 macOS 应用的主要语言，广泛用于构建高性能、用户友好的应用程序。

* **服务器端开发**
  
  Swift 可以用于服务器端开发，借助 Vapor、Kitura 等框架，能够创建高效、可扩展的后端服务。

* **机器学习和 AI**
  
  Apple 推出了 Swift for TensorFlow（尽管已停止维护），但 Swift 仍然可以用于机器学习和人工智能领域，结合 Core ML 和 Create ML 工具链。

二、环境搭建
--------------------

如果你手里没有苹果设备，可以直接使用 Linux 或者 Windowd 作为学习语言的平台，无伤大雅。
等你练习两年半再买苹果设备来得及，防止买前生产力，买后爱奇艺。

以 Ubuntu22.04 为例， 搭建 Swift 编译环境。

访问 `安装 Swift <https://www.swift.org/install/>`_, 选择自己的平台，下载安装。

.. image:: images/swift_install.png
   :alt: 图片加载失败

下载完成后进行下面的操作(版本可能会有差异，注意细节):

.. code-block:: shell

   # 将安装包直接拷贝到 /opt 目录下
   sudo cp swift-6.0.3-RELEASE-ubuntu22.04.tar.gz /opt
   # 解压安装包
   sudo tar -xf swift-6.0.3-RELEASE-ubuntu22.04.tar.gz
   # 删除压缩包
   sudo rm swift-6.0.3-RELEASE-ubuntu22.04.tar.gz
   # 添加二进制路径到环境变量
   sudo vim ~/.bashrc
   # 添加如下内容
   export PATH=/opt/swift-6.0.3-RELEASE-ubuntu22.04/usr/bin:$PATH
   #保存退出后重新加载环境变量
   source ~/.bashrc
   # 使用命令检查是否否安装成功
   swift --version
   # 输出如下内容说明安装成功
   Swift version 6.0.3 (swift-6.0.3-RELEASE)
   Target: x86_64-unknown-linux-gnu
   
安装完成