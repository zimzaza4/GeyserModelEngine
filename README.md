# GeyserModelEngine

> GitHub仓库：https://github.com/zimzaza4/GeyserModelEngine

[English](README_EN.md) | [简体中文](README.md)

# 这是个什么玩意

能让你Geyser服务器支持MEG4

# 如何安装

根据服务端版本下载以下插件

[GeyserUtils](https://github.com/zimzaza4/GeyserUtils)

[GeyserModelEngine](https://github.com/zimzaza4/GeyserModelEngine)

[LibsDisguises](https://www.spigotmc.org/resources/libs-disguises-free.81/)

下载完后，将`GeyserModelEngine``LibsDisguises`放入插件文件夹

根据服务端版本把`geyserutils-spigot`/`velocity`/`bungeecord`放入插件文件夹

将`geyserutils-geyser`放入geyser的扩展文件夹，这时就安装好了

当然，先别急着用，现在你还得接着读下去

# 转换模型

打开你的bbmodel模型工程文件，将模型转换为基岩版模型

新版本BlockBench 导出的基岩版模型format_version 是1.21.0
需要手动改成1.12.0
否则你的客户端看不到模型

打开刚转换完的模型，把这个多余的hitbox删了（如果没有就不用管）

<img src="docimg/hitbox.png" width="500">

不然BE玩家看会看到这个hixbox碰撞箱

<img src="docimg/hitbox1.jpg" width="500">

然后记得导出模型的纹理

# 安装模型

打开Geyser的`extensions`文件夹创建一个文件夹名为`geyserutils`，接着再往里创建一个文件夹名为`skins`

这时我们再创建一个文件夹名为你模型的id。比如我使用的测试模型的id是`parry_knight`，就创建`parry_knight`文件夹

创建完后你的文件路径应该是这样 `plugins/Geyser-Spigot/extensions/geyserutils/skins/模型id/`

最后将模型和纹理贴图放进去

tips: 每个模型都要有独立的模型文件夹

<img src="docimg/example.jpg" width="500">

这时候重启服务器生成MEG4模型，你的BE玩家应该能正常看到模型了

接下来就是有关模型动画的部分了!

# 模型动画

将模型的动画导出json格式

将动画文件名称修改为`animation.模型ID.json`

之后放入你的资源包

<img src="docimg/example1.jpg" width="500">

现在我们打开动画文件开始修改动画文件里的动画id

原本所有的`动作id`基本都是`idle`、`walk`这样的，现在你得给他加个前缀

例如：`idle`

改为：`animation.模型ID.idle`

示例：`animation.parry_knight.idle`

改完后修改资源包版本号或者uuid，打包资源包

最后一步，重载Geyser或者重启服务器

# 完结

恭喜你现在学会如何使用了，如果还不会V我五毛帮你解决

# 当前限制

用了就知道, 一堆

# 常见问题

### 为什么生成模型后会变成史蒂夫?

你没好好读怎么安装模型

