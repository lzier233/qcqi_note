#### 求证： $R_x(\theta)$ 是使得某布洛赫球向量 $\hat{n}=(n_x,n_y,n_z)$ 绕 $x$ 轴旋转 $\theta$ 的矩阵

&emsp;&emsp;我们从平面上的向量绕原点旋转的简单情况开始讨论，设平面有一复数 $z=x+yi$ ，它旋转 $\theta$ 后就会得到一个新的复数：
$$ze^{i\theta}
=(x+yi)\cos\theta+i(x+yi)\sin\theta \\
=x\cos\theta-y\sin\theta+i(x\sin\theta+y\cos\theta)$$

&emsp;&emsp;现在我们考虑布洛赫球上的任意单位向量的球坐标表示：
$$\hat{n}=(n_x,n_y,n_z)=(sin\theta cos\phi, sin\theta sin\phi, cos\theta)$$

&emsp;&emsp;它对 $x$ 轴旋转 $\beta$ 后得到：
$$\hat{n}'=(sin\theta cos\phi, sin\theta sin\phi cos \beta - cos\theta sin\beta, cos\theta cos\beta + sin\theta sin\phi sin\beta)$$

&emsp;&emsp;设 $\hat{n}'$ 对应的已经去除全局相位叠加态向量为 $\left[a,b\right]^T$ ，其中 $a$ 是实数，那么我们可以用含有 $a,b$ 的式子表示 $\hat{n}'$ ：

$$
    \begin{cases}
        n_x=a(b+\overline{b}) \\
        n_y=-ia(b-\overline{b}) \\
        n_z=2a^2-1
    \end{cases}
$$

&emsp;&emsp;这里的主要思想主要有两点：其一，用复数和它的共轭相加减从而得到其实部和虚部；其二，对于叠加态向量中的 $\frac{\theta}{2}$ 需要用倍角公式处理成球坐标系下的 $\theta$ .


&emsp;&emsp;接着我们考虑去除全局相位的任意波函数 $\ket{\psi}=cos\frac{\theta}{2} \ket{0}+sin\frac{\theta}{2} e^{i\phi}\ket{1}$ ，它的向量表示左乘上 $R_x(\beta)$ 后得到：

$$
\ket{{\psi}'}=
R_x(\beta)\ket{{\psi}}=
\left[
\begin{matrix}
\cos\frac{\beta}{2} &-i\sin\frac{\beta}{2}\\
-i\sin\frac{\beta}{2} &\cos\frac{\beta}{2} 
\end{matrix}
\right]
\left[
\begin{matrix}
\cos\frac{\theta}{2} \\
\sin\frac{\theta}{2} e^{i\phi}
\end{matrix}
\right]
=\left[
\begin{matrix}
\cos\frac{\beta}{2}\cos\frac{\theta}{2}-i\sin\frac{\beta}{2}\sin\frac{\theta}{2}e^{i\phi}\\
-i\sin\frac{\beta}{2}\cos\frac{\theta}{2}-\cos\frac{\beta}{2}\sin\frac{\theta}{2}e^{i\phi} 
\end{matrix}
\right]
=\left[
\begin{matrix}
p \\
q
\end{matrix}
\right]
$$

&emsp;&emsp;现在向量 $\ket{{\psi}'}=\left[p,q\right]^T$ 仍然可能包含全局相位，设不包含全局相位的向量为 $\left[a,b\right]^T$ ，由于 $a$ 是实数，我们将 $\ket{{\psi}'}$ 上下同乘 $\frac{\overline{p}}{\parallel p\parallel}$ 后有：

$$
    \begin{cases}
        a=\parallel p\parallel \\
        b=\frac{q\overline{p}}{\parallel p\parallel}{}
    \end{cases}
$$

&emsp;&emsp;接着我们可以代入 $a,b$ 求解出 $n_x,n_y,n_z$ 的值了：

$$
    \begin{cases}
        n_x=a(b+\overline{b})=p\overline{q}+q\overline{p} \\
        n_y=-ia(b-\overline{b})=i(p\overline{q}-q\overline{p}) \\
        n_z=2a^2-1=2\parallel p\parallel^2-1
    \end{cases}
$$

&emsp;&emsp;分别化简三项：

$$
    n_x=2(\sin\frac{\theta}{2}\cos\frac{\theta}{2}\cos^2\frac{\beta}{2}\cos{\phi}   
    +
    \sin^2\frac{\theta}{2}\sin\frac{\beta}{2}\cos\frac{\beta}{2}\cos{\phi} \\
    +
    \cos\frac{\theta}{2}\sin\frac{\theta}{2}\sin^2\frac{\beta}{2}\cos\phi
    -
    \sin^2\frac{\theta}{2}\sin\frac{\beta}{2}\cos\frac{\beta}{2}\cos{\phi} )\\
    =
    2\sin\frac{\theta}{2}\cos{\frac{\theta}{2}}\cos{\phi}=\sin{\theta}cos{\phi}
$$

$$
    n_y=2(\sin{\frac{\theta}{2}}\cos{\frac{\beta}{2}\sin{\phi}-\sin{\frac{\beta}{2}\cos{\frac{\theta}{2}}}})(\cos{\frac{\theta}{2}\cos{\frac{\beta}{2}+\sin{\frac{\theta}{2}\sin{\frac{\beta}{2}}}\sin{\phi}}})+2\sin{\frac{\theta}{2}}\cos{\frac{\beta}{2}}\cos{\phi}\sin\frac{\theta}{2}\sin{\frac{\beta}{2}}\cos{\phi}   \\
    =\sin{\theta}\sin{\phi}\cos^2{\beta}-\sin{\theta}\sin{\phi}\sin^2{\beta}+\sin^2\frac{\theta}{2}\sin\frac{\beta}{2}\sin^2{\phi}-\sin\beta\cos^2\frac{{\theta}}{2}+\sin^2\frac{\theta}{2}\sin\frac{\beta}{2}\cos^2{\phi}  \\
    =\sin\theta\sin\phi\cos\beta-\sin\beta\cos\theta
$$

$$
    n_z = 2[(\cos\frac{\theta}{2}\cos\frac{\beta}{2}+\sin\frac{\beta}{2}+\sin\frac{\theta}{2}\sin\frac{\beta}{2}\sin{\phi})^2+\sin^2\frac{\theta}{2}\sin^2\frac{\beta}{2}\sin^2\phi]-1    \\
    =2\cos^2\frac{\theta}{2}\cos^2\frac{\beta}{2}+2\sin^2\frac{\theta}{2}\sin^2\frac{\beta}{2}-1 + \sin\theta\sin\beta\sin\phi  \\
    =2\cos^2\frac{\theta}{2}\cos^2\frac{\beta}{2} - \cos^2\frac{\theta}{2} - \sin^2\frac{\theta}{2} +  2\sin^2\frac{\theta}{2}\sin^2\frac{\beta}{2} + \sin\theta\sin\beta\sin\phi \\
    =\cos\theta\cos\beta + \sin\theta\sin\beta\sin\phi
$$

&emsp;&emsp;至此我们完成了证明。
