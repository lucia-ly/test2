# win10下用anaconda安装TensorFlow
### 1.安装anaconda
#### （1）下载anaconda,点击[这里](https://www.anaconda.com/download/#windows)下载,系统是多少位的就下多少位的版本
 ![image](https://github.com/lucia-ly/test2/blob/master/pic/1.PNG)

#### （2）注意在安装时勾选将anaconda加入环境变量，其他步骤就按照默认选项来就可以
 ![image](https://github.com/lucia-ly/test2/blob/master/pic/2.png)

这样就安装好了

### 2.安装tensorflow

#### （1）打开Anaconda Prompt，输入清华仓库镜像，这样更新会快一些：(这一步不做也是可以的)

```
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/ 
conda config --set show_channel_urls yes
```

#### （2）同样在Anaconda Prompt中利用Anaconda创建一个python3.5的环境，环境名称为tensorflow ，输入下面命令：
```
conda create -n tensorflow python=3.5
```
 ![image](https://github.com/lucia-ly/test2/blob/master/pic/3.png)
 ```
 activate tensorflow #打开环境
 deactivate tensorflow #关闭环境
 ```

打开Anaconda Navigator，点击左侧的Environments，可以看到tensorflow的环境已经创建好了。

 ![image](https://github.com/lucia-ly/test2/blob/master/pic/4.PNG)

#### （3）安装cpu版本的TensorFlow
```
pip install --upgrade --ignore-installed tensorflow
```
#### （4）测试tensorflow 
在Anaconda Prompt中启动tensorflow环境，并进入python环境。 
测试代码：
```python
import tensorflow as tf 
hello = tf.constant('Hello, TensorFlow!') 
sess = tf.Session() 
print(sess.run(hello))
```
运行结果：

 ![image](https://github.com/lucia-ly/test2/blob/master/pic/5.png)

恭喜~安装成功喽！

#### P.S.
有大神说不建议通过装anaconda来装tensorflow，但通过anaconda来安装基本不会遇到太麻烦难以解决的问题，对于初学者也不失为一种可行的方法，笔者水平有限，如果有问题，欢迎指正~
