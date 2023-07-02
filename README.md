# prec-definitions
Common definitions of primitive recursive functions

https://en.wikipedia.org/wiki/Primitive_recursive_function

## Nomenclature
- basis functions:
  - n-arg zero: $O_n: \mathbb{N}^n \rightarrow \mathbb{N}$
  - projection: $I_n^i: \mathbb{N}^n \rightarrow \mathbb{N}$
  - successor: $S: \mathbb{N} \rightarrow \mathbb{N}$
- composition:
  - assumptions:
    - $g: \mathbb{N}^n \rightarrow \mathbb{N}$
    - $h_i: \mathbb{N}^m \rightarrow \mathbb{N}$, for $i \in \mathbb{Z}_n$
  - definition
    - $f: \mathbb{N}^m \rightarrow \mathbb{N} = Comp(g, h_1, h_2, ..., h_n) = g \circ (h_1, h_2, ..., h_n)$
- primitive recursion:
  - assumptions:
    - $g: \mathbb{N}^n \rightarrow \mathbb{N}$
    - $h: \mathbb{N}^{n+2} \rightarrow \mathbb{N}$
  - definition
    - $f: \mathbb{N}^{n+1} \rightarrow \mathbb{N} = Prec(g, h) :=  f(x_1, ..., x_n, 0)  = g(x_1, ..., x_n) \textrm{ and } f(x_1, ..., x_n, S(x_{n+1}))  = h(f(x), *x) $
