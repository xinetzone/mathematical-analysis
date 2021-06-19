---
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.10.3
kernelspec:
  display_name: ai
  language: python
  name: ai
---

# Advanced Expression Manipulation

[Advanced Expression Manipulation — SymPy 1.8 documentation](https://docs.sympy.org/latest/tutorial/manipulation.html)

```{code-cell} ipython3
import warnings
from sympy import *
import pydot
from IPython.display import SVG

warnings.filterwarnings('ignore')
init_printing('dot')

def display_dot(expr):
    g = pydot.graph_from_dot_data(dotprint(expr))[0]
    g.set_bgcolor('lightyellow')
    t = SVG(g.create_svg())
    return t
```

```{code-cell} ipython3
x, y, z = symbols('x y z')

z = x + y*x

display_dot(z)
```

```{code-cell} ipython3
g = pydot.graph_from_dot_data(dotprint(z))[0]
```

```{code-cell} ipython3

```

```{code-cell} ipython3
g
```

```{code-cell} ipython3

```
