# Android

## Android的系统架构

<!--Android的系统架构大致可以分为4层架构:Linux内核层 , 系统运行库层 , 应用框架层和应用层-->

### Linux内核层

Android系统是基于Linux内核的 , 这一层为Android设备的各种硬件提供了底层的驱动 , 如显示驱动 , 音频驱动 , 照相机驱动 , 蓝牙驱动 , Wifi驱动 , 电源管理

### 系统运行库层

这一层通过一些C/C++库为Android系统提供了主要的特性支持. 如SQLite库提供了数据库的支持 , OpenGL|ES库提供了3D绘图的支持 , Webkit库提供了浏览器内核的支持等 . 在这一层还有Android运行时库 , 他主要提供了一些核心库 , 允许开发者使用 Java语言来编写Android应用 . 另外 , Android运行时库中还包含了Dalvik虚拟机(5.0系统之后改为ART运行环境)

### 应用框架层

这一层主要提供了构建应用程序时可能用到的各种API , Android自带的一些核心应用就是使用这些API完成的 , 开发者可以使用这些API来构建自己的应用程序

### 应用层

所有安装在手机上的应用程序都是属于这一层的 , 比如系统自带的联系人 , 短信等程序 , 或者是你从Google Play上下载的小游戏 , 当然还包括你自己开发的程序



## Android应用开发特色

### 四大组件

#### Activity 

是所有Android应用程序的门面 , 凡是应用中你看得到的东西 , 都是放在Activity中的

#### Service

在后台运行 , 即使用户退出了应用 , 仍然运行

#### BroadcastReceiver

允许你的应用接收来自各处的广播消息 , 电话, 短信等 , 也可以向外发出广播消息

#### ContentProvider

为应用程序之间共享数据提供了可能



## Activity

### 什么是Activity

Activity 是最容易吸引用户的地方 , 他是一种可以包含用户界面的组件 , 主要用于和用户进行交互 . 

一个应用程序中可以包含零个或多个Activity , 但不包含任何Activity的应用程序很少见

### 基本用法

创建Activity之后自动重写`onCreate()`方法

```kotlin
class FirstActivity : AppCompatActivity(){
    override fun onCreate(savedInstanceState : Bundle?){
        super.onCreate(savedInstanceState)
    }
}
```



