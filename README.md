# DNF-

点个star呗

DNFpython脚本开发
使用过程种的注意事项：

1.电脑设置为1920X1080，100%缩放(理论上不设置好像也行)，dnf设置为800X600

2.把特效关掉，快捷栏1放置“米娅的通讯器”，需要这玩意儿传送到比拉谢尔号上面，没有的在比拉谢尔号的米娅那里买

3.如果是在物理机上跑，请将配置.ini的在线推理改为0，如果是在虚拟机上且推理性能不够，可以将配置.ini中的在线推理改为1，然后在物理机种运行服务端.py,再在虚拟机种运行main.py，这样可以将虚拟机中的图片传到物理机中训练，再将结果传回虚拟机中。不过网络传输这块我刚弄好，还没测，也不知道会不会出问题

4.python版本是3.8.19,其他的库看报错来装吧，或者你用requirements.t也行

5.一键聚物用的是v键，buff放在y键，社交-角色信息设置-款式3

6.本脚本用的是wegame自动登录，所以你需要自己手动登录wegame一次，让wegame记住密码才能用本脚本，记得在配置.ini中更改wegame目录

7.补丁的话，用了之后可以识别到史诗，不用的话就只能一直撞门了，撞3秒过图

本项目需要改进的地方

1.模型还有些不完善的地方，我个人觉得，佩戴觉醒称号“力量觉醒”或者“无上传奇”训练成角色坐标再减去角色身高，这样当作角色真实坐标要好用点，本脚本虽然在识别不到人物坐标时进行了相应的处理，但总归有些浪费时间

2.模型的物品训练，用补丁要好一些，就训练补丁那个方块，现在的脚本地上爆的东西都会捡

3.刷完角色还需要添加一个自动分解和存仓库的功能(可以添加到main.py 49行)

4.裂缝那里我设置的直接返回城镇(海伯伦的预言所.py 第356行)，我打算改成直接停止游戏重新上号，毕竟等虚弱的时间有点长，不如重新上号

5.疲劳判断我使用的是图色判断，那个点的颜色是黑色了我就默认疲劳刷完了，建议改成识字判断(函数功能类.py 562行)

6.跟怪判断我写的是往怪那个方向跑的时候，边跑边放技能，如果你改成了我1，2所说的模型，可以考虑改成跑到怪附近(删除函数功能类.py 190,191,192行)或者中心点附近再放技能（在函数功能类.py 169行，将取最近怪物替代为取怪物中心坐标，需要自己实现）

7.目前只支持海伯伦，想要其他的图，自行添加到刷图脚本文件夹中，可以模仿海伯伦的预言所.py

8.如果需要打包，请把识字模块中的paddle替换成你自己想用的其他模块，paddle打包有点问题
