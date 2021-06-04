
## 简介
本项目旨在提供深度学习实验环境，快速搭建常用的实验环境。我知道你搭环境很快，但是，有了它你可以更快！

目前已支持以下环境：
- [x] pytorch1.4
- [x] pytorch1.6
- [x] mmclassification

各个环境名对应的包版本如下：
|  环境名            | pytorch | cudatoolkit | mmcv | 说明 |
|  ---- | ---- | ---- | ---- | ---- |
| pytorch1.4        | 1.4  | 10.0 | 1.1.5 | 适用于较老版本的mmlab系列 |
| pytorch1.6        | 1.6  | 10.2 | 1.2.0 | 适用于较新版本的mmlab系列|
| mmclassification  | 1.6  | 10.2 | 1.3.3 | 适用于最新版本的[mmlab系列](https://github.com/open-mmlab) |

<!--
各个环境名对应的包版本如下：
|  环境名            | pytorch | cudatoolkit | mmcv | 说明 |
|  ---- | ---- | ---- | ---- | ---- |
| pytorch1.4        | 1.4  | 10.0 | 1.1.5 | 适用于较老版本的mmlab系列 |
| pytorch1.6        | 1.6  | 10.2 | 1.2.0 | 适用于较新版本的[mmdetection](https://github.com/open-mmlab/mmdetection)和[mmsegmentation](https://github.com/open-mmlab/mmsegmentation)|
| mmclassification  | 1.6  | 10.2 | 1.3.3 | 适用于[mmclassification](https://github.com/open-mmlab/mmclassification) |
-->

推荐使用mmclassification


## 安装

依次执行以下命令：
```
# 下载环境包
scp -P 44120 -r root@202.197.66.62:/root/commonfile/anaconda3.zip /root/userfolder/

# 解压
unzip anaconda3.zip

# 激活环境
eval "$(./anaconda3/bin/conda shell.bash hook)"
```

设置开机启动
```
echo 'export PATH=/root/userfolder/anaconda3/bin:$PATH' >> ~/.zshrc
source ~/.zshrc
```

## 使用

激活环境：
```
source activate mmclassification # conda activate mmclassification
```


## 常见问题

<!--
### 重启后无base环境

重新激活环境：
```
cd userfolder
eval "$(./anaconda3/bin/conda shell.bash hook)"
```
-->

### libGL.so.1
`ImportError: libGL.so.1: cannot open shared object file: No such file or directory`解决方法：

```
apt install libgl1-mesa-glx -y
```

如果遇到网络问题，无法下载，建议换源：
```
# apt换源 | 把apt源改为清华镜像，修改sources.list文件内容为清华源，版本选择16.04
sudo vim /etc/apt/sources.list # https://mirrors.tuna.tsinghua.edu.cn/help/ubuntu/
```
然后执行：
```
sudo apt-get update
apt-get install libgl1-mesa-glx -y
```


## 说明
环境包放在xp4上，下载需要xp4账号。有xp4账号的同学把端口号改成自己的，没有的同学找赵杨要密码。


<!--
## TODO
pycharm专业版 | 代码同步服务器教程
git版本管理教程
ddr | idird 数据集介绍、特点、难点
tct 数据集介绍、划分、特点、难点
-->
