# CustomizablePluginCmd <自定义插件指令>

**自定义插件指令**  
本插件可以自定义插件指令  
自定义插件指令会将参数设置到变量，并执行公共事件  

**插件指令变量参数**  
在一条插件指令前加上`ConvertCmd`  
可以将插件指令中的 \V,\N 等控制字符转换成对应的值  
详见【插件指令】  
(需要将本插件置于插件管理器列表的末位)  

**MZ执行MV的插件指令**  
MZ中使用【插件指令】-【插件指令MV】 还可以执行MV的插件指令  
(不保证 MV的插件一定兼容MZ)  


## 使用方法

在插件参数【自定义插件指令】中添加自定义插件指令  
MV中 : 直接使用【插件指令】 调用自定义插件指令  
MZ中 : 使用【插件指令】-【插件指令MV】 调用自定义插件指令  


## 插件指令 (MV)

| description           | command                      |
| :-------------------- | :--------------------------- |
| 转换参数             | `ConvertCmd [原插件指令]`  |
| 转换参数并重新切分 | `ConvertCmdRe [原插件指令]` |

#### 转换参数
在一条插件指令前加上`ConvertCmd`  
可以将插件指令中的 \V,\N 等控制字符转换成对应的值  
就像【显示文本】的转换一样  
Ps:不会重新切分参数  
   如 \N[1]="ab cd" 转换后 "ab cd"将是一个整体 不会视作两个参数  

`ConvertCmd [原插件指令]`
  + 示例
    * 使用变量#2的值作为 SetBtnPic 的第一个参数 :
    * `ConvertCmd SetBtnPic \V[2] 3`
  + ConvertCmd
    - 主命令
    - 固定写法，区分大小写
  + [原插件指令]
    - 需要转换参数的插件指令

#### 转换参数并重新切分
类似【转换参数】，但会重新切分参数  
如 \N[1]="ab cd" 转换后 "ab cd"将会切分空格 而视作两个参数  

`ConvertCmdRe [原插件指令]`
  + ConvertCmdRe
    - 主命令
    - 固定写法，区分大小写
  + [原插件指令]
    - 需要转换参数的插件指令


## 插件指令 (MZ)

| description        |
| :----------------- |
| 转换参数           |
| 转换参数并重新切分 |


## Author
Mikan(MikanHako)  
Copyright (C) 2023-2024 Mikan(MikanHako)  