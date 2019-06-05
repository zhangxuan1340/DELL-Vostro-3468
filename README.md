# Dell Vostro 3468黑苹果

基础准备：
* 最新版本的Clover
* 更新Clover Config中的三码数据。

文件介绍：
* drivers64UEFI：中包含可使用稳定一个月的驱动文件
* Kexts：包含3468所需驱动
* Hotpatch：针对Dell-3468做的定制Patch。

## 文中配置
* I5 7200U
* 8G DDR4 2666M
* BCM94360CS
* AMD R430（已屏蔽）
* USB端口已经针对进行定制
* 瑞煜千兆网卡
* B140HAN01.3 1080P 72%NTSC并顺手开启Retina

## 查看屏幕型号
``` bash
ioreg -lw0 | grep IODisplayEDID | sed "/[^<]*</s///" | xxd -p -r | strings -6
B140HAN01.3 ## 这块屏幕跟着我三台电脑了
```

## 注意事项
>触摸板偶尔出现睡眠唤醒不能使用的情况，但是本人只遇到过一次，往各位遇到的情况下，帮忙上传日志。

亮度调整未修正；
* FN+B亮度大
* FN+S亮度小



## 结束
本配置已经在macOS 10.14.5 下跑了一个多月才进行上传。