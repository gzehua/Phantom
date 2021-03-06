
[环境类问题](#1) 


[配置类问题](#2) 

&nbsp;&nbsp;&nbsp;[ 1、使用系统组件加载异常](#1.1)  

[代码实现问题](#3) 

------------
<h2 id='1'> 环境类问题</h2>

------------
<h2 id='2'> 配置类问题</h2>

<h3 id='1.1'>1、使用系统组件加载异常</h3>

**问题描述：** 在插件中使用部分系统组件加载不出来，达不到预期效果。

**原因：** 可能使用到的系统组件未在宿主中进行权限声明。

**举例：** 如下场景

> *在插件中调用相机，扫描二维码，surfaceView无任何图像展示。*


**解决方法：** 权限的声明是以宿主为主的，因为在检测应用权限的时候，标识是以宿主权限为参考。所以上述场景中，使用相机时，如果未在宿主中进行权限声明，那么在插件中，仍然无法使用相应的系统组件。所以，此类问题的解决方法，只需要再宿主中申请相应的权限即可。

------------
<h2 id='3'> 代码实现问题</h2>

