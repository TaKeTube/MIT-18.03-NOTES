### Some Complement

#### 稳定性

二阶线性ODE所有系数为正 系统稳定

**劳斯–赫尔维茨稳定性判据 Routh-Hurwitz conditions for stability**

对于实系数多项式$p(z) = a_0z^n + a_1z^{n-1} + \cdots + a_{n-1}z + a_n$

的**赫维兹矩阵**

![Routh-Hurwitz](.\Complement\Routh-Hurwitz.png)

的行列式的所有主子式  principal minors 为正则系统稳定

#### 待定系数法

##### 多项式输入

 n阶ODE n次输入 有且仅有一个多项式解

用待定系数法求解

n次多项式 一般得到n次的响应

若p(D)最小微分数是k 那得到的是n+k次的响应/或者设最小微分为u 解完再积分

##### $xe^x$型

也是待定系数法

或者待定一个t的多项式$u(t)e^t$带入 转换为多项式输入的问题

#### 算子

微分多项式算子有乘法交换律

shifting rule 对含指数类的函数（$e^tf(t)$）求导有极大帮助

substitution rule 对复指数类的函数求导有极大帮助

#### 平移不变性/线性时间不变性

对于微分多项式算子有平移不变性

If $p(D)$ is a constant-coefﬁcient differential operator and $p(D)x = q(t)$, then $p(D)y = q(t − c)$, where $y(t) = x(t − c)$.

#### 频率响应和实际共振

对于系统$mx''+bx'+kx = Bcos(\omega t)$

增益gain $g = g(\omega) = \frac{1}{\sqrt{(k-m\omega)^2+b^2\omega^2}}$ 称为**振幅响应**

相位差phase lag $\phi = \phi(\omega) = Arg(p(i\omega)) = tan^{-1}(b\omega/(k-m\omega^2))$ 称为**频率响应**

如果振幅有peak 则我们称达到peak的频率$\omega_r$为实际共振频率 practical resonance frequency

如果阻尼过大 则不会有peak

通过求导 可得
$$
\omega_r = \sqrt{\frac{k}{m}-\frac{b^2}{2m^2}}
$$
**spring-driven mechanical system 共振频率和阻尼有关**

**dashpot-driven mechanical system 对于缓冲器驱动系统**

共振频率是固有频率 此时gain = 1, 相位差为0

该系统和RLC电路是一类系统

**对于spring-dashpot-driven system (同时驱动)**

$x''+bx'+kx = ky+by'$

共振频率和阻尼有关 有相位差
$$
g(\omega) = \sqrt{\frac{k^2+b^2\omega^2}{(k-m\omega^2)^2+b^2}}
$$

#### RLC电路

复阻抗 complex impedance 满足串并联欧姆定律

#### 傅立叶级数

调傅立叶级数各个成分的相位的时候 虽然波形不一样 但是听起来是一样的 可能是因为耳朵里的细胞对于傅立叶成分特定频率产生共振 和相位无关

**单位冲激响应 unit impulse response 施加δ(t)的响应**  写成v(t)

**单位跃阶响应 unit step response 施加u(t)的响应** 写成w(t)

pre-initial conditions (at 0−) and postinitial conditions (at 0+)

一阶单位跃阶响应$u(t)(1/k)(1-e^{-kt})$

一阶单位冲激响应$u(t)e^{-kt}$

一阶冲激响应是不连续的 而二阶的是连续的 为什么？

高阶冲激响应 相当于在n-1阶导数造成了一个跃阶 jump 为什么？

单位冲激响应是单位跃阶响应的导数

#### 指数阶

exponential order a

$|f(t)| < Me^{at}$

#### 解析延拓 analytic continuation

#### 闭环系统 black's formula

$$
Y = \frac{W}{1+gW}
$$

#### 极点 Pole

最简分式的零点

#### 指数增长率 exponential growth rate

最小的a
$$
\lim\limits_{t \to \infty}\frac{f(t)}{e^{bt}} = 0\quad \text{for all b > a}
$$
f(t)的指数增长率是其拉普拉斯变换极点的最大实部
