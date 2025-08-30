# arch+gnome美化

最终效果如图![fianal1](/picture/final-1.png)![fianal2](/picture/final-2.png)
![fianal1](/picture/final-3.png)![fianal4](/picture/final-4.png)

## 前期准备

OS：archlinux  
终端解释器：zsh &ensp;`sudo panman -S zsh`&ensp;  
终端模拟器：ghostty &ensp;`sudo pacman -S ghostty`&ensp;
软件：gnome-tweaks（中文名称为“**优化**”）&ensp;`sudo pacman -S gnome-teaks`&ensp;  
&emsp;&emsp;&ensp;&ensp;gnome-software（中文名称为“**软件**”）&ensp;`sudo pacman -S gnome-software`&ensp;  
&emsp;&emsp;&ensp;&ensp;扩展管理器&ensp;gnome-software中搜索下载&ensp;  
&emsp;&emsp;&ensp;&ensp;Refine&ensp;gnome-software中搜索下载&ensp;
&ensp;  
&ensp;  
&ensp;

## 扩展

打开扩展管理器安装以下扩展

- Input Method Panel （解决fcitx5输入法在gnome上的显示问题，不使用fcitx5不用安装）
- AppLndicator and KStatusNotifierItem Support（显示后台应用图标）在插件管理器已安装选项中选择左对齐
- Lock Keys&ensp;显示键盘大小写和数字区的锁定情况
- Lock screen background&ensp;修改锁屏壁纸，我使用了files文件夹中的lockscreen.jpg。![lockscreen](/files/lockscreen.jpg)
- Blur my Shell&ensp;模糊透明边框等，具体功能可自行搜索，设置如下![blur1](/configurations/Blur-my-shell-1.png)![blur1](/configurations/Blur-my-shell-2.png)![blur1](/configurations/Blur-my-shell-3.png)![blur1](/configurations/Blur-my-shell-4.png)
- User Themes&ensp;允许用户安装主题（我没使用，不太清楚🤔）
- Logo menu 可以在左上角显示一个系统图标，设置中可以配置图标外观以及自定义一些左键点击后的功能
- Compiz windows effect&emsp;窗口拖动特效
- Compiz alike magic lamp effect&emsp;窗口最小化特效
- Rounded Corners&emsp;调整窗口圆角大小
- Vitals&emsp;显示当前系统资源使用情况
&ensp;  
&ensp;  
&ensp;

## 壁纸

右键桌面更换壁纸，选择自己喜欢的壁纸（我使用的是file文件夹中的wallpaper.jpg）
![wallpaper](/files/wallpaper.jpg)
&ensp;  
&ensp;  
&ensp;

## 去除窗口关闭按钮，用快捷键关闭窗口（可选）

在`设置-->键盘-->快捷键`中设置自己的关闭窗口快捷键
打开`Refine-->shell和合成器-->Window Button Layout`，拖走叉叉
（实际这里也可以为窗口增加最小化和最大化）
&ensp;  
&ensp;  
&ensp;

## 光标主题

打开[Gnome Looks](https://www.gnome-look.org/)，选择自己喜欢的鼠标光标，下载后解压（注意解压后文件夹嵌套的问题），移动到`home/username/.local/share/icons`（.local需要开启显示隐藏文件夹才能看到），打开`优化`，在外观中选择光标。
我使用了files文件夹中的`oreo_spark_violet_cursors`。  
&ensp;  
&ensp;  
&ensp;

## 图标主题

1. 打开[Gnome Looks](https://www.gnome-look.org/)，选择自己喜欢的图标主题，下载后解压（注意解压后文件夹嵌套的问题），移动到`/usr/share/icons/`，打开`优化`，在外观中选择光标。
2. 我使用了files文件夹中的`candy-icons`。  
&ensp;  
&ensp;  
&ensp;

## 终端美化

1. 安装一个终端字体`sudo pacman -S ttf-jetbrains-mono-nerd`
2. 安装zsh`sudo pacman -S zsh`
3. 修改默认shell为zsh`chsh -s /usr/bin/zsh`并重新开启终端
4. 安装starship`sudo pacman -S starship`
5. 可以在网上找starship配置文件（.toml文件）或用我的files中的starship.toml，并将文件移动到/home/username/.config文件夹中
6. 编辑/home/sunlinghao/.zshrc&ensp;写入`eval "$(starship init zsh)"`，重启终端即可生效。
&ensp;  
&ensp;  
&ensp;

## ghostty美化

1. 下载自己喜欢的颜色配置文件（我用的是configurations文件夹下的catppuccin-macchiato.conf），移动到/home/username/.config/ghostty文件夹中
2. 编辑配置文件`/home/username/.config/ghostty/config`，写入以下内容

   ```config
    theme = /home/username/.config/ghostty/catppuccin-macchiato.conf  #这里要改成你的文件名，启用颜色配置
    window-decoration = none        #设置无边框，无边框后可以按住super键拖动窗口
    background-opacity = 0.85       #设置不透明度
    font-family = "Adwaita Mono"    #设置字体种类
    font-size = 15                  #设置字体大小
   ```

完成终端美化与ghostty美化后，终端界面如下![ghostty](/picture/final-3.png)
&emsp;
&emsp;  
&emsp;  

## sddm美化

我使用了[arona](https://github.com/Machillka/arona-sddm-login)主题,按照其教程下载安装即可
&emsp;
&emsp;  
&emsp;  

## grub美化

我使用了<https://github.com/vinceliuice/grub2-themes> 中的vimix,2k,color选项,按照教程安装即可  
