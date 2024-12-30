# 1.如何在pycharm打开终端

终端右边有个小箭头，最好不要用pycharm终端

# 2.如何进入conda环境

conda activate 环境名

# 3.Typora有红线

点击文件，点击偏好设置，点击编辑器，在最下面选择不使用拼写检查

# 4.conda 不是内部或外部命令，也不是可运行的程序

右击我的电脑，属性，高级系统设置，环境变量，手动双击path添加环境变量。

# 5.使用anconda创建虚拟环境conda create -n 环境名 python = 3.9

conda env list检查环境是否创建

# 6.认先安装Qt5

pip install pyqt5 -i https://pypi.douban.com/simple/

pip install pyqt5-tools -i https://pypi.douban.com/simple/

pip install opencv-python -i https://pypi.douban.com/simple/

pip install opencv-contrib-python不加网址就成功了

# 7.Pycharm 外部工具配置

## Qtdesigner:designer.exe 

everything里面搜designer.exe

参数无

文件路径$FileDir$

## Pyuic5:pyuic5.exe

- Program：everything搜
- Arguments：$FileName$ -o $FileNameWithoutExtension$.py
- Working directory：$FileDir$ 

https://blog.csdn.net/qq_51210361/article/details/131582764

## Pyrcc5

- Program：$PyInterpreterDirectory$\Scripts\pyrcc5.exe
- Arguments：$FileName$ -o $FileNameWithoutExtension$_rc.py
- Working directory：$FileDir$ 

# 8.油猴插件的安装

百度搜索扩展迷

# 9.电脑用户名更改

电脑上没有此电脑图标：打开运行框，输入regedit,找到计算机\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\ProfileList\S-1-5-21-3756865991-3024836895-140044048-1001

双击更改用户名，重启电脑，在C盘中更改用户名，再次重启，完成。

设置-个性化-左边主题-点击桌面图标设置

# 10.更改开机用户名

控制面板\用户帐户\管理帐户\更改帐户\重命名帐户

# 11. 移除Pycharm解释器

右下角，全部显示，要点两次确定才会移除

# 12.下载pyqt5-tools卡在Preparing metadata (pyproject.toml) 

pyqt5-tools不支持python3.10以上版本，清华镜像下载anaconda  https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/?C=M&O=A

# 13.找不到conda可执行文件

找到condabin文件夹下的condad.bat，选中再重新加载虚拟环境。

# 14.opencv库安装不了

把梯子关掉

# 15.Pyqt5界面切换

from PyQt5.QtWidgets import QApplication, QMainWindow, QWidget
 from gui3 import Ui_mainWindow
 from 界面2 import Ui_MainWindow as Ui_Page1
 from 界面3 import Ui_MainWindow as Ui_Page2


 class Page1(QMainWindow):
   def __init__(self):
     super().__init__()
     self.ui = Ui_Page1()
     self.ui.setupUi(self)
     self.ui.pushButton_4.clicked.connect(self.fanhui)

   def fanhui(self):
     self.hide()
     window.show()

 class Page2(QMainWindow):
   def __init__(self):
     super().__init__()
     self.ui = Ui_Page2()
     self.ui.setupUi(self)
     self.ui.pushButton_3.clicked.connect(self.fanhui)

   def fanhui(self):
     self.hide()
     window.show()


 class MainWindow(QMainWindow):
   def __init__(self):
     super().__init__()
     self.ui = Ui_mainWindow()
     self.ui.setupUi(self)
     self.page1 = Page1()
     self.page2 = Page2()
     self.ui.pushButton.clicked.connect(self.show_page1)
     self.ui.pushButton_2.clicked.connect(self.show_page2)

   def show_page1(self):
     self.page1.show()
     self.hide()

   def show_page2(self):
     self.page2.show()
     self.hide()

 if __name__ == **"__main__"**:
   app = QApplication([])
   window = MainWindow()
   window.show()
   app.exec_()

# 16.设计一个好看的ui（一）

（1）qtdesigner拉入一个frame，属性编辑器设置长宽600*400，右键点击编辑样式表

#frame{

​	border-radius:30px;   圆角

​	background-color: rgb(255, 255, 255);

}

（2）再拉入两个frame，点击空白处右键设置水平布局，设置属性编辑器里sizePolicy为expanding，layout全部设置为0。再设置样式表。

\#frame_2{

​	border-top-left-radius:30px;

​	border-bottom-left-radius:30px;

}

\#frame_3{

​	border-top-right-radius:30px;

​	border-bottom-right-radius:30px;

}

（3）再拉入一个label到frame_2里，设置layout为0。

\#label{

​	border-top-left-radius:30px;

​	border-bottom-left-radius:30px;

}

\#frame_4{

​	border-top-right-radius:30px;

}

\#frame_6{

​	border-bottom-right-radius:30px;

}

（4）再拉3个frame到frame_3里设置垂直布局，设置layout为0。设置垂直策略为expanding。

设置垂直伸展分别为1：1：3。

（5）拉入2个水平间隔器，两个按钮，一个垂直线在frame_4里面。水平布局，设置layout为0。

（6）拉入一个堆栈stackwidge。水平布局，layout设为0。

# 17.Qtdesigner的预览按钮

ctrol+R

# 18.命令行指令

d：

cd改变目录

md创建目录

# 19.
