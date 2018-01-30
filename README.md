# mdrs
docker镜像打包工具

适用于python2.6和python2.7

# 使用方法
```
python setup.py install
```

之后使用mdrs命令进行创建和构建docker镜像

# 构建原理
使用busybox作为最基本的rootfs 然后分析制作对象的依赖 将依赖打包到rootfs中 
之后使用docker镜像的标准结构来打包为docker能load的镜像
比如制作nginx的镜像 将nginx的二进制文件和nginx的所有依赖都打包到rootfs中 所以生成的镜像就非常小了
