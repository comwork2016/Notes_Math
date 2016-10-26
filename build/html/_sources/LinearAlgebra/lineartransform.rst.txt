.. _lineartransform:

矩阵变换
==============

笔记参考自：`线性代数拾遗（三）：线性变换以及矩阵的意义 <http://mengqi92.github.io/2016/05/20/linear-algebra-3/>`_


变换
^^^^^^^^^^^

对于 :math:`Ax=b` 形式的方程：

.. math::
	
	\begin{bmatrix}
	4 & -3 & 1 & 3 \\
	2 & 0 & 5 & 1	\end{bmatrix}
	\begin{bmatrix} 
	1 \\ 
	1 \\ 
	1 \\
	1 \end{bmatrix}
	=
	\begin{bmatrix} 
	5 \\
	8 \end{bmatrix}

此形式可以看成是几个列向量的线性组合，即 :math:`1\begin{bmatrix} 4 \\ 2 \end{bmatrix} + 1\begin{bmatrix} -3 \\ 0 \end{bmatrix} + 1\begin{bmatrix} 1 \\ 5 \end{bmatrix} + 1\begin{bmatrix} 3 \\ 1 \end{bmatrix} = \begin{bmatrix} 5 \\ 8 \end{bmatrix}`，相当于将 :math:`A` 看成一个整体，整个方程就是一个 4 维向量 :math:`x` 乘以矩阵 :math:`A` 后得到一个 2 维向量 :math:`b`。

不难发现，当变换 :math:`T` 为 :math:`x \mapsto Ax` ，向量 :math:`x` 若有 :math:`n` 维，则变换的定义域就是 :math:`R^n` ， :math:`A` 就有 :math:`n` 列；向量 :math:`b` 若有 :math:`m` 维，则变换的上域就是 :math:`R^m` ， :math:`A` 就有 :math:`m` 行（ :math:`A` 每一列有 :math:`m` 个元素）。而变换的值域就是 :math:`A` 中列的所有线性组合组成的集合。


几何中的线性变换
^^^^^^^^^^^^^^^^^^^^^^

通过线性变换的性质，很容易理解图形学中一些专门用于变换的矩阵，比如 2 维平面上的旋转矩阵：

.. math::

	\begin{equation}
	\mathbf{A}=
	\begin{bmatrix}
	\cos\varphi & -\sin\varphi \\
	\sin\varphi & \cos\varphi \end{bmatrix} 
	\nonumber
	\end{equation}

把列向量拆开，就是 :math:`T(\mathbf{e}_1) = \begin{bmatrix}\cos\varphi \\ \sin\varphi \end{bmatrix}`， :math:`T(\mathbf{e}_2) = \begin{bmatrix}-\sin\varphi \\ \cos\varphi \end{bmatrix}`，也就是  :math:`\begin{bmatrix}1\\ 0\end{bmatrix}` 旋转到 :math:`\begin{bmatrix}\cos\varphi \\ \sin\varphi\end{bmatrix}` ，:math:`\begin{bmatrix}0\\ 1\end{bmatrix}` 旋转到 :math:`\begin{bmatrix}-\sin\varphi \\ \cos\varphi\end{bmatrix}` 。

旋转变换如图所示：

.. image:: ./images/rotation.png

