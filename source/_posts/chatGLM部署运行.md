---
title: chatGLM部署运行
date: 2023-05-24 11:02:15
tags:
- chatgpt
- AI
---
## 下载

百度网盘下载 [链接](//pan.baidu.com/s/1XSjBZ6U3OiVZULEjvJbd2g?pwd=tvmc)

打开后将所有的包解压，我们可以看到
![Replaced by Image Uploader](//s2.loli.net/2023/04/14/CLvU65PjMbStNmx.png)  
打开`3-20日更新`这个包,可以看到`chatglm-6b`这个文件夹，将这个文件夹内部的所有文件拷贝覆盖到model文件中的`chatglm-6b`中
![Replaced by Image Uploader](//s2.loli.net/2023/04/14/Sk6b3cH5lpL82Fn.png)  
![Replaced by Image Uploader](//s2.loli.net/2023/04/14/vPjEHn5cra9b1W2.png)  
将解压好的`model`放到`ChatGLM-webui`文件中

将环境包内部的文件粘贴到`ChatGLM-webui`文件中
g
最终展示为
![Replaced by Image Uploader](//s2.loli.net/2023/04/14/bwF6EtXlOihqADV.png) 
此时点下强制更新，更新下最新代码

然后根据自己的显存选项选择使用哪个脚本
![Replaced by Image Uploader](//s2.loli.net/2023/04/14/axS5vIfuK9yNFqe.png)  
8g的显存点击运行，这种就是成功的情况

![Replaced by Image Uploader](//s2.loli.net/2023/04/14/Ca1F9dre25gTkfp.png)



## 报错分析
### 第一种

![202304141353512.png](//s2.loli.net/2023/04/14/7YuenfiFqTvk6aM.png)

点击同文件下的install.sh尝试

重新按照以上步骤安装

重启电脑

### `Symbol cudaLaunchKernel not found`

可以尝试不管他，多等一会，出现网址说明就能用

这种一般是int4 也就是显存小于8g的时候的报错，需要单独安装 [cuda](//developer.nvidia.com/cuda-downloads)

