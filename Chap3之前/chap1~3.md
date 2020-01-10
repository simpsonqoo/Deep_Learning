## 純量、向量、矩陣及張量
### 純量(scalar)
&emsp;&emsp;即為單一數值，以小寫英文字母做表示，e.g. $x$。通常要敘述純量時會加上其值域，e.g. $x \in \Bbb R$

### 向量(Vector)
&emsp;&emsp;即為由純量構成的數列(陣列)，也可以想成是一維陣列，會以粗體小寫描述向量，e.g. $\boldsymbol x$，而若是要指定$\boldsymbol x$中第i個元素，則表示為$\boldsymbol x_i$

### 矩陣(Matrix)
&emsp;&emsp;由向量構成的陣列，也可以稱為二維陣列，以大寫粗體字表示，若陣列$\boldsymbol A$高度為m，寬度為n，元素為實數，則可表示為 $\boldsymbol A\in \Bbb R^{m\times n}$。而以下標表示陣列中的元素，第一個下標為水平座標數，第二個下標為鉛直座標數。若有座標以:表示，則為所有其他指定維度之元素。

e.g.
$ \boldsymbol A = \left[\begin{matrix}
{{x_{11}}} & {{x_{12}}}\\
{{x_{21}}} & {{x_{22}}}\\
{{x_{31}}} & {{x_{32}}}
\end{matrix} \right]$

$\boldsymbol A_{:1}= \left[\begin{matrix}
{{x_{11}}}\\
{{x_{21}}}\\
{{x_{31}}}
\end{matrix} \right]$

$\begin{bmatrix}a & b\\ c & d\end{bmatrix}$

### 張量(tensor)
&emsp;&emsp;用來泛指所有多維度的陣列，表示方式如矩陣形式，

本篇直接忽略轉置、乘法、加法等運算。

### 點積(dot)
兩相同維度之向量個元素相乘後相加之動作稱為點積。若做點積之兩向量為$\boldsymbol x,\boldsymbol y$，則點積可表示為$\boldsymbol x^T\boldsymbol y$。

e.g.
$\boldsymbol x=\left[\begin{matrix}
{{x_{1}}}\\
{{x_{2}}}\\
{{x_{3}}}
\end{matrix} \right]$,$\boldsymbol y=\left[\begin{matrix}
{{y_{1}}}\\
{{y_{2}}}\\
{{y_{3}}}
\end{matrix} \right]$
則$\boldsymbol x^T\boldsymbol y = {x_1}{y_1} + {x_2}{y_2} + {x_3}{y_3}$

由於純量的轉置還是純量，故$\boldsymbol x^T\boldsymbol y=\boldsymbol y^T\boldsymbol x$

線性方程式($\boldsymbol Ax=\boldsymbol b$)、單位矩陣、反矩陣、線性相依、span皆跳過

### 範數(norm)
範數(norm)中$L^2$ norm可寫成$||\boldsymbol x||$，其平方常以$\boldsymbol x^T\boldsymbol x$表示。而很多時候，使用$L^2$ norm不見得是個好選擇，因為其在零點增加的速度不夠快，在很多種領域的應用中，重要的是區分零或是非零，這種方法比不上使用等速率增長的$L^1$ norm，$L^1$ norm可簡化成
$$|\boldsymbol x|{|_1}{\rm{ = }}\sum\limits_i {|{x_i}|} $$

如果是想知道長度相關的應用，可使用Fobenius norm
$$|\boldsymbol A|{|_F} = \sqrt {\sum\limits_{ij} {{A_{ij}}^2} } $$

特殊矩陣、特徵分解、奇異值分解、虛反矩陣、trace及行列式皆跳過

### 主成分分析
假設存在於n為空間($\boldsymbol A\in \Bbb R^n$，或是一筆資料有n個特徵，且存在m筆資料，想對這些資料進行壓縮，也就是保存重要的部分，丟棄不重要的部分。e.g. 要描述一個人的氣質，假設描述一個人有很多種特徵，例如身高、體重、談吐、眼睛大小。但如果我們想要保存一個仁是否有氣質的資訊，眼睛大小相較之下就是比較不重要的特徵，將其捨棄也不太影響資料的完整性。
所以假設我們希望將特徵壓縮到$l$個特徵，其中$l<n$