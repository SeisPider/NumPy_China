# Python集成环境安装
* **[Anaconda:](https://www.continuum.io/downloads)** 免费开源版本的SciPy安装包并支持Linux,Windows和Mac。
* **[Enthought Canopy:](https://www.enthought.com/products/canopy/)** 含SciPy的核心安装包，存在免费版和商业版，支持Linux,Windows和Mac。
* **[Python(x,y):](http://python-xy.github.io/)** 含SciPy的免费分发版，基于 **[Spyder IDE](https://pythonhosted.org/spyder/)**，仅支持Windows。
* **[WinPython:](http://winpython.github.io/)** 含SciPy的免费分发版，仅支持Windows。
* **[Pyzo:](http://www.pyzo.org/)** 基于Anaconda和IEP交互环境的免费分发版本，支持Linux,Windows和Mac。

# Python模块包逐一安装
## pip安装
Mac和linux用户可通过 **[pip](https://pip.pypa.io/en/stable/)** 安装编译过的SciPy二进制包。该方法需确认系统中已安装过Python和pip。

1. 对于Mac或Linux用户，升级pip至最新版本：
```
python -m pip install --upgrade pip
```
2.  在pip中使用`--user`标志安装到用户而非系统（不使用`sudo pip`以避免问题）。使用该方法可安装软件包到本地用户，不需要额外的权限来写入文件至系统路径下：
```
pip install --user numpy scipy matplotlib ipython jupyter pandas sympy nose
```
3. 添加路径至PATH
> * Linux：
```
 export PATH="$PATH:/home/your_user/.local/bin" #更换your_user并添加语句至~/.bashrc文件尾
```
> * OSX：
```
export PATH="$PATH:/Users/your_user/Library/Python/3.5/bin" #更换your_user并添加语句至~/.bashrc文件尾
```
其中`3.5`是用户的Python版本

## 使用Linux软件包管理器进行系统级安装
用户也可通过Linux的软件包管理器进行系统级安装，但安装的SciPy的版本落后于pip可安装的版本。
本文仅介绍了部分Linux发行版的安装命令，其他版本请在本系统仓库中搜索组件并逐个安装。
* Ubuntu 和 Debian
```
sudo apt-get install python-numpy python-scipy python-matplotlib ipython ipython-notebook python-pandas python-sympy python-nose
```
本安装要求Ubuntu 12.10或更新版本而Debian则是7.0或更新版本。用户可以添加 **[NeuroDebian](http://neuro.debian.net/)** 以获得更多SciPy软件包。
* Fedora
```
sudo dnf install numpy scipy python-matplotlib ipython python-pandas sympy python-nose atlas-devel
```
安装要求Fedora 22或更新版本。

## 使用Mac软件包管理器进行系统级安装
MacOS本身不带有软件管理器，但用户可自行安装下列软件包管理器。
* [Macports](https://www.macports.org/): 在terminal中运行如下语句以安装适应于Python3.5的SciPy软件包：
```
sudo port install py35-numpy py35-scipy py35-matplotlib py35-ipython +notebook py35-pandas py35-sympy py35-nose
```
* [Homebrew](https://brew.sh/): 目前正在开发的版本中，用户无法使用`brew install <formula>`安装全部SciPy环境。用户仅可通过下列语句安装NumPy, SciPy和Matplotlib：
```
brew tap homebrew/python; brew install python numpy scipy matplotlib
```
## Windows安装包
Windows下没有类似于Linux和Mac的软件包管理器，因此推荐用户使用前述Python科学计算环境安装包进行安装，若无法进行上述安装。用户可以考虑从 **[pre-built Windows installers](http://www.lfd.uci.edu/~gohlke/pythonlibs/)** 获得Python模块包。

## 从源码自行编译
参考[scipy](https://github.com/scipy/scipy)。
