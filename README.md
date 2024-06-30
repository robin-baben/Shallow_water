# Solving one-dimensional equation of shallow water by CABARET scheme
## Одномерные уравнения мелкой воды

$$
\begin{split}
&\dfrac{\partial H}{\partial t} + \dfrac{\partial Hu}{\partial x} = 0 \\
&\dfrac{\partial Hu}{\partial t} + \dfrac{\partial Hu^2}{\partial x} + \dfrac{g}{2}\dfrac{\partial H^2}{\partial x} = 0
\end{split}
$$

#### В характеристической форме

$$
\begin{split}
&\dfrac{\partial R}{\partial t} + (u+c)\dfrac{\partial R}{\partial x} = 0 \\
&\dfrac{\partial Q}{\partial t} + (u-c)\dfrac{\partial Q}{\partial x} = 0 \\
&R = u+2c, \space Q = u -2c \\
&c=\sqrt{gH}
\end{split}
$$

## Постановка задачи

Будем рассматривать дозвуковое течение мелкой воды в бассейне $x \in [0, 10]$.

$g=1$

#### Начальные условия
$$
\begin{split}
&u(x, 0) = 0 \\
&H(x, 0) = \begin{cases}
2, \space x \le 5 \\
1, \space x > 5
\end{cases}
\end{split}
$$

#### Граничные условия
Для крайней правой ячейки

$$
\begin{cases}
R_N^{n+1}=u_N^{n+1}+2 \sqrt{gH_N^{n+1}} \\
u_N^{n+1} = 0
\end{cases}
$$

Для крайней левой ячейки

$$
\begin{cases}
Q_1^{n+1}=u_1^{n+1}-2 \sqrt{gH_1^{n+1}} \\
u_1^{n+1} = 0
\end{cases}
$$
