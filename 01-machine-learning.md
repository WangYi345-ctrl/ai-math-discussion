
## 第一章：机器学习基础

机器学习：寻找一个能够描述输入与输出关系的函数。

- 函数输出为连续数值 → 回归（Regression）。
- 函数输出为有限个类别之一 → 分类（Classification）。
- 函数输出为较复杂的结构 → 结构化学习（Structured Learning）。

### 一、机器学习的过程

1. 构建模型，写出包含未知参数的函数 $f$。
2. 定义损失函数 $L$，作为未知参数的函数。损失用于衡量模型预测与目标之间的差异。
3. 寻找使损失函数 $L$ 尽可能小的参数 $w$ 和 $b$。

### 二、梯度下降方法

假设先固定参数 $b$，只优化参数 $w$。

$$
w^{1}=w^{0}-\eta\left.\frac{\partial L}{\partial w}\right|_{w=w^{0}}
$$

其中：

- $w^{0}$：更新前的参数。
- $w^{1}$：更新后的参数。
- $\eta$：学习率，控制每次更新的步长。
- $\frac{\partial L}{\partial w}$：损失函数关于参数 $w$ 的偏导数。

当 $\frac{\partial L}{\partial w}>0$ 时，$w$ 应减小；当 $\frac{\partial L}{\partial w}<0$ 时，$w$ 应增大（假设学习率为正）。

### 三、两个参数的梯度下降

当损失函数为 $L(w,b)$ 时，需要同时计算两个偏导数：

$$
\frac{\partial L}{\partial w},\qquad \frac{\partial L}{\partial b}
$$

更新公式为：

$$
w^{1}=w^{0}-\eta\left.\frac{\partial L}{\partial w}\right|_{w=w^{0},b=b^{0}}
$$

$$
b^{1}=b^{0}-\eta\left.\frac{\partial L}{\partial b}\right|_{w=w^{0},b=b^{0}}
$$

