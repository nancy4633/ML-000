	1. 读源码
		a. 拿过来就跑：优先用TensorFlow2，十分钟调不通就提issue。
		b. 学习：Pytorch（代码 vs 论文细节）
		c. 复现｜加速：Jax｜Flax ， 模仿PyTorch+论文
		d. 以下是注意：
		e. 大部分开源代码有错误，有时有严重错误:TF2 Sparsemax 是错的，PyTorch ghost batch normalization 是错的
		f. 很多知名代码库有很多很好的写法，模仿时候可以去学习
		g. 论文当中有很多错误!AdamW 和 RAdam 论文都是错的，尤其是不同版本结 果还经常不一样 
	2. 读论文
		a. 摘要
		b. 数据集：注意看是否典型，是否比较baseline有问题，数据是否有特殊性。
		c. 方法：看结构、看故意藏起来的trick，不一定要看数学，注意看不同版本的区别
		d. 对着代码看实现细节（一定要看官方）
	3. 课程准备
		a. 双系统（ubuntu 18.04）生产环境（CentOS 7.x）
		b. 云主机 Colab
		c. 铅笔&橡皮
		d. 学生账户：JetBrain 全家桶(https://www.jetbrains.com/) 
	4. 环境搭建：两种
		a. Colab
			环境现成，便宜，快，容易复现
			需要翻墙
		b. 自己搭环境
			别人不方便复现
	5. 本次训练营使用Colab
		a. 基本的GCC开发环境
			brew install gcc@4.9
			gcc-4.8 以上版本
			gcc --version
			xcode-select --install (xcrun: error: invalid active developer path)
			???
		b. Anaconda/Miniconda
			下载安装包
			环境变量
		c. R（Conda环境）
			不要用package manager安装Rstudio
			conda install r-essentials r-base    直接用命令安装，这样可以在jupyter notebook使用R和Python
		d. Docker
			post installation step
			docker镜像：docker pull image:tag
			如果需要GPU，则需要安装Nvidia Docker
			docker run -it -rm image:tag
				-it 表示采用交替式的运行
				-rm 表示运行完后删除container，节省硬盘资源。
				-v 表示将本地文件映射到docker中
				-p 将端口进行映射，使用jupyter notebook时使用。
		e. CUDA
			不看了，没兴趣，先用colab@@
	6. 开发工具
		a. PyCharm
			优点：
				代码补全、重命名
				Debug
				提取函数（refactor --> extract_method）
				自动实现PEP8
		b.  Jupyter Notebook
			优点：
				交互式运行，避免重复读区大量数据
				Jupyter有很多很方便的魔法函数：
