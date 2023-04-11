---
mathjax: false
katex: true
---

# sotfmax回归
softmax回归用于分类问题，预测离散值。softmax的输出单元是多个，且引入了softmax运算使输出更适合离散值的预测和训练。
## 分类问题
假设一个2 * 2 * 1的图片，即单通道灰度图片。其四个像素分别为$x_{1},x_{2},x_{3},x_{4}$。假设图片对应的动物分别为狗、猫、鸡，那么我们可以将图片的像素值作为输入，将动物作为输出，这就是一个分类问题。分类问题的输出是离散值，即狗、猫、鸡。分别为$y_{1}, y_{2}, y_{3}$。
通常用离散的数值来代表类别
## softmax回归模型
$\begin{aligned} & o_1=x_1 w_{11}+x_2 w_{21}+x_3 w_{31}+x_4 w_{41}+b_1 \\ & o_2=x_1 w_{12}+x_2 w_{22}+x_3 w_{32}+x_4 w_{42}+b_2 \\ & o_3=x_1 w_{13}+x_2 w_{23}+x_3 w_{33}+x_4 w_{43}+b_3 .\end{aligned}$

使用$o_{1},o_{2},o_{3}$的值大大小对比来作为判断指标，但存在输出值范围不确定的原因，我们使用**sotfmax**运算符来解决，将类别转化为值为正且合为一的概率分布。

公式为$y_{i}=\frac{e^{o_{i}}}{\sum_{j=1}^{3}e^{o_{j}}}$
## 单样本分类的矢量计算表达式
$O^{(i)}=x^{(i)}W + b$

$y^{(i)}=softmax(O^{(i)})$

$W=\begin{bmatrix}
 \omega_{11}&\omega_{12}&\omega_{13} \\
 \omega_{21}&\omega_{22}&\omega_{23} \\
 \omega_{31}&\omega_{32}&\omega_{33} \\
 \omega_{41}&\omega_{42}&\omega_{43}
\end{bmatrix}$

<div>
  <h1>Hello, World!</h1>
  <p>This is some HTML code embedded in a Markdown file.</p>
</div>
<img>   
