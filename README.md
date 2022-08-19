# Nonlinear optimization

The aim of this notebook is adjusting a multiple linear regression model to explain a variable $y$ as a function of other variables $X$, $y = X \beta + \epsilon$, where $\beta$ are the adjusted regression coefficients and $\epsilon$ the regression error. For this purpose, the **Ridge Regression** is used, where the objective is to minimize the function:

$$\begin{align*}
    \underset{\beta}{\min} \quad \lVert y - X \beta \rVert_2^2 + \rho \lVert \beta\rVert_2^2 
\end{align*}
$$

In order to clarify the elements and dimensions of the problem, if there are $n$ **samples** or instances and $k$ **variables**:

* Explained variable: $\underset{(nx1)}{y}$
* Variables used to explain $y$: $\underset{(nx(k+1))}{X}$
* Regression coefficients: $\underset{((k+1)x1)}{\beta}$
* Regression error: $\underset{(nx1)}{\epsilon}$

Different nonlinear optimization algorithms can be applied for this purpose.
