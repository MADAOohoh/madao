## Madao 的备忘录

wubba lubba dub dub.

------

### macOS 通过“终端”批量解压文件

下了一堆老片，几百个文件都是压缩包，还带密码的。终端操作一波一次性解决了。

#### 终端安装 p7zip 和 unrar

##### 1、安装 homebrew，可以管理命令行程序。

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

##### 2、用 homebrew 安装解压程序

解压zip文件：p7zip

解压rar文件：unrar

```
brew install p7zip
brew install unrar
```

##### 3、进入要解压的文件目录：cd 文件路径

> 把文件夹拖到终端中即可获取路径

```
cd /Users/madao/Downloads
```

##### 4、执行解压

解压zip文件：7z x 文件名 -o/解压文件的存放路径

> 解压指定zip文件：'a.zip'
>
> 解压当前目录下的所有zip文件：'*.zip'

```
7z x '*.zip' -o/Users/madao/Downloads/1
```

解压rar文件：unrar x 文件名 -o/解压文件的存放路径

> 解压指定zip文件：'a.zip'
>
> 解压当前目录下的所有zip文件：'*.zip'

```markdown
unrar x '*.zip' -o/Users/madao/Downloads/1
```

##### 5、其他

如果是有密码的压缩包，执行之后会提示输入密码，输入+回车即可。

多个文件也只需要输入一次密码。