# Typecho_material_theme

Typecho_material_theme 是一个 [Typecho](https://github.com/typecho/typecho) 模板。这是一个修改版本。


# Author

该主题的原始作者是 [kookxiang](https://ikk.me)。

**这份代码来自于 [HanSon](http://hanc.cc/)**，他仿造了 KK 的主题。

这里是一份我的拷贝，记录了一些简单的编辑。


# Notice

如果你喜欢该主题，请移步 KK 的[博客](https://ikk.me)或 [Github 仓库](https://github.com/kookxiang)。

如果你想要为自己的 Typecho 博客安装该主题，请移步 HanSon 的 [Github 仓库](https://github.com/Hanccc/typecho_material_theme)。

如果你对我的拷贝感兴趣，祝你喜欢。请注意：所有版本都与我自己实装版本有所不同，当然，也包括这一份。所以这是一份未经充分测试的代码。如有任何问题，请尝试修复它或知会予我。


# Features

None.

主要用来记录修改，所以在觉得有必要之前，大概不会有什么区别。
如果一定要说……以下显然是并无技术含量的举手之劳了：
- 根据事实修正了模板的版权信息，并设置选项。不显示 or 正确说明。
- 增加 billboard 图片的设置项，并修改了展示方式。
- 打包返回顶部按钮。
- 修复了回复评论会导致页面刷新，且取消回复不显示的 bug。
- 修复了副标语的设置项。

一份仅包含修复（而不含版权等其他任何更改）的分支已 pull，但被代码作者关闭。所以对于不想自行修复的人，clone 这份代码会是更便捷的选择。


# Install

```bash

# Initailly open the root document of your Typecho, then

# Change to the document of themes
cd ./usr/themes
# Clone from Github
git clone https://github.com/Yves-X/typecho_material_theme.git
```

Otherwise

```bash

# Initailly open the root document of your Typecho, then

# Change to the document of themes
cd ./usr/themes
# Download from Github
wget https://github.com/Yves-X/typecho_material_theme/archive/master.zip -O master.zip
# Unzip
unzip master.zip
```

# Other

1. 友情链接插件：

https://github.com/HanSon/Links_for_Material_Theme

安装后请修改 `./sidebar.php`，移除输出代码的注释符号

2. `回复`与`取消回复`按钮：

替换相关元素

```html
<!--用下面内容替换“回复”-->
<button type="button" class="btn btn-danger btn-xs mdi-content-reply reply-button"><div class="ripple-wrapper"></div></button>
<!--用下面内容替换“取消回复”-->
<button type="button" class="btn btn-primary btn-xs btn-fab mdi-content-clear pull-right"><div class="ripple-wrapper"><div class="ripple ripple-on ripple-out" style="left: 28px; top: 23px; transform: scale(6); background-color: rgba(255, 255, 255, 0.843137);"></div><div class="ripple ripple-on ripple-out" style="left: 34px; top: 32px; transform: scale(6); background-color: rgba(255, 255, 255, 0.843137);"></div></div></button>
```

或

在适当位置用 js 脚本替换
（如果你不知道这是什么意思，请把代码追加在 `./js/extra.min.js` 后）

```javascript
$("div .comment-reply").children().html('<button type="button" class="btn btn-danger btn-xs mdi-content-reply reply-button"><div class="ripple-wrapper"></div></button>');
$("div .cancel-comment-reply").children().html('<button type="button" class="btn btn-primary btn-xs btn-fab mdi-content-clear pull-right"><div class="ripple-wrapper"><div class="ripple ripple-on ripple-out" style="left: 28px; top: 23px; transform: scale(6); background-color: rgba(255, 255, 255, 0.843137);"></div><div class="ripple ripple-on ripple-out" style="left: 34px; top: 32px; transform: scale(6); background-color: rgba(255, 255, 255, 0.843137);"></div></div></button>');
```