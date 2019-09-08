**数据可视化系列-Seaborn之直方图系列**

# seaborn.distplot() 直方图，质量估计图，核密度估计图

解析：

该API可以绘制分别直方图和核密度估计图，也可以绘制直方图和核密度估计图的合成图
通过设置默认情况下，是绘制合成图，设置情况图下：

hist=True:表示要绘制直方图(默认情况为True)，若为False，则不绘制

kde=True:表示要绘制核密度估计图(默认情况为True),若为False,则绘制

函数原型：
```
seaborn.distplot(a, bins=None, hist=True, 
                 kde=True, rug=False, fit=None, 
                 hist_kws=None, kde_kws=None, rug_kws=None,
                 fit_kws=None, color=None, vertical=False,
                 norm_hist=False, axlabel=None,
                 label=None, ax=None)
```

a: Series, 一维数组或列表

要输入的数据，如果设置name属性，则该名称将用于标记数据轴；

<font color=red>以下是可选参数:</font>

bins: matplotlib hist()的参数 或者 None

作用：指定直方图规格，若为None，则使用Freedman-Diaconis规则,该规则对数据中的离群值不太敏感，可能更适用于重尾分布的数据。它使用 bin 大小 $[2*IQR(X(:))*numel(X)^(-1/4), 2*IQR(Y(:))*numel(Y)^(-1/4)]$，其中 IQR 为四分位差。

hist:bool

是否绘制(标准化)直方图

kde:bool

是否绘制高斯核密度估计图

rug:bool

是否在支撑轴上绘制rugplot()图

{hist，kde，rug，fit} _kws：字典

底层绘图函数的关键字参数

color:matplotlib color

该颜色可以绘制除了拟合曲线之外的所有内容

vertical:bool

如果为True,则观察值在y轴上，即水平横向的显示
















原理与代码整理修改：数据分析与可视化学研社

微信公众号：

<img src="https://github.com/Vambooo/zz/blob/master/visual.jpg" width="150" />

知识星球：机器学习交流学习圈：

<img src="https://github.com/Vambooo/zz/blob/master/dlzhishixingqiu.jpg" width="150" />
