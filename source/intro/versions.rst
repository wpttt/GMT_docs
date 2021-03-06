GMT版本
=======

版本号
------

GMT 版本号遵循 `语义化版本号规范 <https://semver.org/lang/zh-CN>`_\ ，其版本号格式为:

    *major.minor.patch*

其中 *major* 为主版本号，\ *minor* 为次版本号，\ *patch* 为补丁版本号。例如 5.4.5。

根据语义化版本规范的要求：

- 当有极大更新，例如重写底层代码时，会增加主版本号 *major*\ 。
  因而 *major* 不同的两个版本的API接口，以及语法、功能上可能有差异
- 当有较大更新，比如新增模块或者新增功能时，会增加次版本号 *minor*
- 若只是修复代码BUG或修复文档描述，则增加补丁版本号 *patch*

因而，GMT 6.x.x 与 5.x.x 在底层存在很大差异，两个版本的语法不完全兼容。
GMT 5.4.x 相对于 5.3.x 增加了更多的功能，而 GMT 5.4.5 相对于 5.4.4
则主要是修复了一些BUG。

.. note::

    GMT 开发版的版本号略有不同，其格式为: *major.minor.patch*\_\ *hash*\_\ *yyyy.mm.dd*\ 。
    其中 *hash* 为当前版本的 git commit hash，\ *yyyy.mm.dd* 是当前版本的更新日期。
    例如：6.1.0_267ce55_2020.01.21\ 表示你使用的是 更新于 2020年1月21日、
    hash 代码为 267ce55 的 6.1.0 开发版。

GMT主流版本
-----------

GMT目前主流版本有GMT6、GMT5和GMT4三个主版本。这几个版本有什么区别呢？用户该如何选择呢？

**GMT6**
    GMT6是GMT目前的最新版本，也是开发者在持续维护和更新的版本。

    GMT6特点在于：

    -   兼容GMT4和GMT5语法，因而老脚本无需修改或仅需少量修改即可在GMT6下使用
    -   新增现代模式语法，极大简化了绘图脚本，且避免了GMT使用中的常见错误
    -   新增模块

        - **movie** 模块用于方便地制作动画
        - **docs** 模块用于直接打开模块的网页文档
        - **subplot** 模块可以方便地绘制多子图
        - **inset** 模块则可以绘制小图

**GMT5**
    GMT5的最终版本为5.4.5，发布于2019年1月4日。GMT5将不会再更新，所有BUG将不会得到修复。

    GMT5相对于GMT4有诸多改进，其命令语法更统一，选项设计更合理，还增加了
    很多新功能。其中，有用且常用的功能包括：

    - **-Bafg** 自动确定坐标轴的标注、刻度和网格间隔
    - 支持透明色，且支持透明图层
    - **-X** 和 **-Y** 支持多种指定坐标原点的方式，画多子图的组合图时更加简单
    - 使用 **-p** 可以绘制任意3D视角图

**GMT4**
    GMT4的最终版本为4.5.18，发布于2018年7月。
    开发者不再对GMT4进行任何维护或更新，所有BUG将不会得到修复。

GMT6兼容GMT4和GMT5语法，且GMT6新增的现代模式语法更加简洁易用。
因而，建议所有GMT新用户学习并使用GMT6的现代模式。
GMT老用户可以在GMT6下运行老脚本，但建议学习并使用GMT6现代模式写新脚本。

本文档中所有示例均使用GMT6的现代模式语法。
