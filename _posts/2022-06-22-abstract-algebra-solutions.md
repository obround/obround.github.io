---
layout: post
title: "Solutions to Abstract Algebra"
author: "Aditya Kumar"
categories: journal
tags: [math]
---

My solutions to select problems from the popular textbook, [Abstract Algebra by David Dummit, Richard Foote][1].
A word of caution: My proofs have not been reviewed. Bear in mind that a couple proofs have been inspired by posts on [math.stackexchange.com][2].

[1]: https://www.amazon.com/Abstract-Algebra-3rd-David-Dummit/dp/0471433349
[2]: https://math.stackexchange.com/

## Section 1.1

**#9(b)** Let $H = (G - \\{0 + 0\sqrt{2}\\}, \cdot)$. The operation $\cdot$ is clearly associative. The identity is $e = 1 + 0\sqrt{2}$. Provided an element $x \in H$ where $x = a + b\sqrt{2}$, the inverse is

$$
x^{-1} = \left(\frac{a}{a^2 - 2b^2}\right) + \left(\frac{b}{2b^2 - a^2}\right)\sqrt{2}
$$

**#22** If $x^n = e$, then by distribution $(g^{-1}xg)^n = e$. Let $(ab)^n = a^nb^n = e$. By the first statement $a^n = b^{-n}a^nb^n$, and hence $b^na^n = a^nb^n$ or $\|ba\| = \|ab\|$.

**#25** Fix $g, h \in G$. Because $gh = (gh)^{-1} = h^{-1}g^{-1}$ and  $g = g^{-1}$ and $h = h^{-1}$, it follows that $gh = hg$. Thus $G$ is abelian.

**#31** Let $t(G) = \\{g \in G \mid g \neq g^{-1}\\}$ be the set of elements of order not equal to two. $\|t(G)\|$ is even because if $g \in t(G)$, we have $g^{-1} \in t(G)$. The identity is not in $t(G)$ because $e = e^{-1}$. Thus $G - t(G) \neq \emptyset$ and $\|t(G)\| \le 2(k-1)$, which implies the existence of an element of order two in $G - t(G)$, and hence $G$.

## Section 1.2

**#16** We only need to show $x_1y_1 = y_1x_1^{-1}$. Because $x_1^2 + y_1^2 =1$, we have $x_1y_1 = y_1^{-1}x_1^{-1} = y_1x_1^{-1}$. Letting $r = x_1$ and $s = y_1$, the proposition is proved.

## Section 1.3

**#19** By exercise 1.3.15, the possible orders are $1, 2, 3, 4, 5, 6, 7, 10, 12$.

**#20** $S_3 = \langle a, b \mid a^2 = b^2 = (ab)^3 = 1 \rangle$ (in cycles, one possibility is $a = (1\;2)$ and $b = (2\;3)$). We now want to prove that this is a presentation for $S_3$. Because $a^2 = b^2 = 1$, all elements in $S_3$ are of the form

$$
abab\cdot\cdot\cdot\cdot\ ab \quad\text{or}\quad baba\cdot\cdot\cdot\cdot\ ba
$$

Because $(ab)^3 = 1$, we have

$$
S_3 = \\{a, ab, aba, abab, ababa, b, ba, bab, baba, babab, bababa\\}
$$

Using $a^2 = b^2 = 1$, we can simplify this to $S_3 = \\{1, a, b, ab, ba, aba\\}$.

## Section 1.4

**#8** The following matrices in $GL_n(F)$ do not commute:

$$
\pmatrix{1 & 1 \\ 0 &1} \quad\text{and}\quad \pmatrix{1 & 0 \\ 1 & 1}
$$

## Section 1.5

**#1** $\|1\| = 1$ and $\|-1\| = 2$ and $\|\pm i\| = \|\pm j\| = \|\pm k\| = 4$.

## Section 1.6

**#4** An isomorphism $\varphi : R - \\{0\\} \to C - \{0\}$ preserves the order of the elements: $\|\varphi(x)\| = \|x\|$. Let $x \in R - \{0\}$ be the number such that $\varphi(x) = i \in C - \{0\}$. Because $\|i\| = \|\varphi(x)\|$, the order of $x$ must also be $4$: a contradiction because $R - \{0\}$ has no elements of order $4$.

**#9** $D_{24}$ has an element of order $12$, while $S_4$ doesn't.

**#17** Let $\varphi : G \to G$ be the map such that $\varphi(g) = g^{-1}$. For $g, h \in G$, we have

$$
\varphi(gh) = (gh)^{-1} = h^{-1}g^{-1} = \varphi(h)\varphi(g)
$$

$G$ is abelian if and only if $\varphi(h)\varphi(g) = \varphi(g)\varphi(h)$.

**#20** Because function composition is associative, $\text{Aut}(G)$ is associative. The trivial automorphism ($x \mapsto x$) is the identity. Because each $\varphi \in \text{Aut}(G)$ is bijective, there is an inverse $\varphi^{-1} \in \text{Aut}(G)$ (the proof that the inverse is in $\text{Aut}(G)$ is trivial) such that $\varphi \circ \varphi^{-1} = \varphi^{-1} \circ \varphi = I$ where $I$ is the identity.

**#24** If $t = xy$, then $tx = xyx =  xt^{-1}$. Thus, $t$ and $x$ satisfy the same relations as $D_{2n}$ where $n = \|t\|$. The elements $t$ and $x$ clearly generate $G$ because $G = \langle x, y \rangle$ and $y = xt$. Summarizing, we have shown

$$
G = \langle t, x \mid t^n = x^2 = e, tx = xt^{-1} \rangle
$$

**#26** The presentation of $Q_8$ is $Q_8 = \langle i, j \mid i^4 = 1, j^2 = i^2, ij = ji^{-1} \rangle$. Because $\varphi(i)$ and $\varphi(j)$ satisfy the relations of $Q_8$ (i.e. $\varphi(i)\varphi(j) = \varphi(j)\varphi(i)^{-1}$, etc.), $\varphi$ is a homomorphism. Thus we can define something like $\varphi(k)$ as such:

$$
\varphi(k) = \varphi(ij) = \varphi(i)\varphi(j)
$$

$\varphi$ is clearly injective because $\ker(\varphi) = \{1\}$ (you can check this by trying all elements in $Q_8$).

## Section 1.7

**#18**

1. $a = 1_Ha \implies a \sim a$

2. $a \sim b \implies a = hb \implies b = h^{-1}a \implies b \sim a$

3. $a \sim b \land b \sim c \implies a = h_1b \land b = h_2c \implies a = h_1h_2c \implies a \sim c$

**#19** Let the map in consideration be $\varphi : H \to \mathcal O_x$. Define $\varphi^{-1} : \mathcal O_x \to H$ by $\varphi^{-1}(a) = ax^{-1}$. Then, $\varphi^{-1}$ is a two-sided inverse:

$$
\varphi(\varphi^{-1}(a)) = \varphi(ax^{-1}) = a
\qquad\quad
\varphi^{-1}(\varphi(h)) = \varphi^{-1}(hx) = h
$$

Thus $\varphi$ is bijective, and $\|H\| = \|\mathcal O_x\|$ (i.e. all orbits have cardinality $\|H\|$). Because the orbits partition $G$, we have $\|G\| = k\|H\|$ where $k$ is the number of orbits.

**#20** Call the group of rigid motions $T$, and label the four vertices of the tetrahedron $A = \{1, 2, 3, 4\}$. Then $T$ acts on $A$, and with every action $m \in T$, there is a corresponding permutation in $S_4$ of $A$. Thus $T$ is isomorphic to a subgroup of $S_4$. If you fix one vertex of the tetrahedron, you get the possible motions, and doing this for all four vertices, you get $\|T\| = 12$. Because the only subgroup of $S_4$ of order $12$ is $A_4$, we have $T \cong A_4$.

**#23** Let $G$ be the group of rigid motions of a cube. Because $\|G\| = 24$ and $\|S_3\| = 6$, the action cannot be faithful. The kernel consists of the identity and the three exhanges of opposite faces.

## Section 2.1

**#6** Fix $x, y \in G_T$. Then $x^m = (y^{-1})^n = 1$. Clearly $(xy^{-1})^{mn} = 1$. Thus $xy^{-1} \in G_T$. Consider the matrices

$$
\left[
A = \pmatrix{-1 & 1 \\ 0 & 1},
\qquad
B = \pmatrix{-1 & 0 \\ 0 & 1},
\qquad
AB = \pmatrix{1 & 1 \\ 0 & 1}
\right] \in \text{GL}_2(R)
$$

$A$ and $B$ both have order $2$, but $AB$ has infinite order. Thus $\text{GL}_2(R)$ does not have a torsion subgroup.

**#8** If $H \subseteq K$ or $K \subseteq H$, then $H \cup K = H \; \text{or} \; K$. Thus it follows that $H \cup K \leq G$. Let $H \cup K \leq G$. If $H \subseteq K$, we are done. Assume $H \not\subseteq K$. Fix $h, k \in H \cup K$ such that $h \in H$ and $k \in K$. By closure, $hk \in H \cup K$. It follows that $hk \in H$ or $hk \in K$ which implies $k \in H$ or $h \in K$. Because $h$ was arbitrary and we assumed $H \not\subseteq K$, we must have $k \in H$. Because $k$ was arbitrary, we must have $K \subseteq H$.

## Section 2.2

**#5a** Because $A = \langle (1 \; 2 \; 3) \rangle$, we have $A \leq C_G(A)$. By Lagrange's theorem, $\|C_G(A)\|$ is a multiple of $3$. Because $\|S_3\| = 6$, and $(1 \; 2) \notin C_G(A)$, we have $\|C_G(A)\| = 3$, from which it follows that $C_G(A) = A$. Because $C_G(A) \leq N_G(A)$, by Lagrange's theorem, $\|N_G(A)\|$ is a multiple of $3$. Because $(1 \; 2)$ is also in $N_G(A)$, we know that $\|N_G(A)\| \geq 4$. Thus $\|N_G(A)\| = 6$, or $N_G(A) = G$.

**#5b** All elements in $A$ commute with each other. Thus $A \leq C_G(A)$. By Lagrange's theorem, $\|C_G(A)\|$ is $4$ or $8$. Because $r \notin C_G(A)$ (e.g. $rs \neq sr$), we have that $\|C_G(A)\| \leq 7$, or $\|C_G(A)\| = 4$. Thus $C_G(A) = A$. Because $C_G(A) \leq N_G(A)$, by Lagrange's theorem, $\|N_G(A)\|$ is $4$ or $8$. Because $r$ is also in $N_G(A)$, we know that $\|N_G(A)\| \geq 5$. Thus $\|N_G(A)\| = 8$, or $N_G(A) = G$.

**#5c** $A = \langle r \rangle$, so $A \leq C_G(A)$. By Lagrange's Theorem $\|C_G(A)\|$ is $5$ or $10$. Because $s$ does not commute with $r \in A$, we have $\|C_G(A)\| = 5$, or $C_G(A) = A$. Similarly, $\|N_G(A)\|$ is $5$ or $10$ because $C_G(A) \leq N_G(A)$. Because $s \in N_G(A)$, we have $\|N_G(A)\| = 10$, or $N_G(A) = G$.

**#7a, b** Because $rs \neq sr$, $s \notin Z(D_{2n})$. Assume $r^k \in Z(D_{2n})$. Because $r^k s = s r^{-k}$,

$$
r^k s = s r^k \implies s r^{-k} = s r^k \implies r^{2k} = e \implies |r| \text{ is even}
$$

This is a contradiction because $\|r\|$ is odd by assumption that $n$ is odd. Thus for odd $n$, $Z(D_{2n}) = \\{e\\}$. Assume that $n = 2k$ (i.e. $n$ is even). Then $Z(D_{2n}) = \\{e, r^k\\}$ by the reasoning above.

**#12a**

$$
\begin{align}
\sigma \cdot p &= 12 x_2^5 x_3^7 x_1 - 18 x_3^3 x_4 + 11 x_2^6 x_3 x_4^3 x_1^{23} \\
(\sigma \circ \tau) \cdot p &= 12 x_3^5 x_4^7 x_1 - 18 x_4^3 x_2 + 11 x_3^6 x_4 x_2^3 x_1^{23} \\
\tau \cdot (\sigma \cdot p) = (\tau \circ \sigma) \cdot p &=  12 x_3^5 x_1^7 x_2 - 18 x_1^3 x_4 + 11 x_3^6 x_1 x_4^3 x_2^{23}
\end{align}
$$

**#12b** Clearly $1 \cdot p = p$ for any $p \in R$. Also,

$$
\begin{align}
\sigma \cdot (\tau \cdot p(x_1, x_2, x_3, x_4)) &= \sigma \cdot p(x_{\tau(1)}, x_{\tau(2)}, x_{\tau(3)}, x_{\tau(4)}) \\
&= p(x_{\sigma\tau(1)}, x_{\sigma\tau(2)}, x_{\sigma\tau(3)}, x_{\sigma\tau(4)}) \\
&= (\sigma \circ \tau) \cdot p(x_1, x_2, x_3, x_4)
\end{align}
$$

Thus, we have a group action.

**#12c** Any permutation that fixes $4$ (e.g. $(1 \; 3 \; 2)$) stabilizes $4$. Thus, the stabilizer of $x_4$ is the set of all permutations on $\\{1, 2, 3\\}$; This is $S_3$.

**#12d** A permutation can stabilize $x_1 + x_2$ by either fixing $1$ and $2$, or exchanging them with each other. This corresponds to the subgroup $\\{(1), (1 \; 2), (3 \; 4), (1 \; 2)(3 \; 4)\\}$. Because every nontrivial element is of order $2$, this is an abelian subgroup of order $4$.

**#12e** The stabilizer is

$$
\begin{align}
\text{stab}(x_1 x_2 + x_3 x_4) &= {(1), (1 \; 2), (3 \; 4), (1 \; 2)(3 \; 4), (1 \; 3)(2 \; 4), (1 \; 4)(2 \; 3), (1 \; 3 \; 2 \; 4), (1 \; 4 \; 2 \; 3)} \\
&= \langle (1 \; 2), (1 \; 3 \; 2 \; 4) \rangle
\end{align}
$$

Letting $(1 \; 2) = s$ and $(1 \; 3 \; 2 \; 4) = r$, we get an isomorphism because $(1 \; 2)$ and $(1 \; 3 \; 2 \; 4)$ satisfy the same relations as $D_8$.

**#12f** The stabilizers are the same because addition and multiplication both commute. The second expression is the first expression with addition and multiplication switched. You could also check each possibility if you wanted to.

## Section 2.3

**#12a** $Z_2 \times Z_2 = \\{(0, 0), (0, 1), (1, 0), (1, 1)\\}$. It is clear that $Z_2 \times Z_2$ is not generated by any of its elements (this can be verified easily).

**#12b** If $Z_2 \times Z$ is cyclic, it is isomorphic to $Z$; Assume this is the case. The element $(1, 0) \in Z_2 \times Z$ has order $2$ but no element in $Z$ has order $2$. This is a contradiction, and hence they aren't isomorphic.

**#12c** Assume $Z \times Z = \langle (x, y) \rangle = \\{n(x, y) \mid n \in Z\\}$. Because $(x, -y) \notin \langle (x, y) \rangle$, we have a contradiction.

**#20** If $x^{p^n} = 1$, then $\|x\|$ divides $p^n$. Because the only divisors of $p^n$ are powers of $p$, it follows that $\|x\| = p^m$ for some $m \leq n$.

**#26a** Assume $(a, n) = 1$. $\sigma_a$ is a homomorphism because $\sigma_a(xy) = (xy)^a = x^a y^a = \sigma_a(x)\sigma_a(y)$, which follows from the fact that $Z_n$ is abelian. Due to $Z_n$ being finite, surjectivity implies injectivity. Because $(a, n) = 1$, $ax + ny = 1$ for $x, y \in Z$. Let $z \in Z_n$ be arbitrary. Then $\sigma_a(z^x) = z^{ax} = z^{1 - ny} = z(z^n)^{-y}$. We know that $\|z\|$ divides $n$ because $\|\langle z \rangle\| = \|z\|$ and Lagrange's Theorem; Thus $z^n = 1$, and $\sigma_a(z^x) = z$. Therefore, $\sigma_a$ is an automorphism.

Conversely, suppose $\sigma_a$ is an automorphism. Let $Z_n = \langle z \rangle$, and $(a, n) = d$. Then, $a = bd$ and $n = cd$. It follows that $\sigma_a(z^c) = z^{ac} = z^{bdc} = z^{bn} = 1$. Because $\sigma_a$ is an isomorphism, only $\sigma_a(z^n) = 1$, implying $n = c$ or $d = 1$. Therefore, $(a, n) = d = 1$.

**#26b** Assume $a \equiv b \pmod n$. This implies that $a = kn + b$. Thus $\sigma_a(x) = x^{kn + b} = (x^k)^n x^b = x^b$ because $x^n = 1$ (look to #26a for more details). Thus $\sigma_a = \sigma_b$. Conversely, assume $\sigma_a = \sigma_b$. Then $x^a = x^b$, or $x^ax^{-b} = x^{a - b} = 1$ for all $x \in Z_n$. Because $x^n = 1$, we have $n \mid (a - b)$, or equivelently $a \equiv b \pmod n$.

**#26c** Let $\tau : Z_n \to Z_n$ be an arbitrary automorphism. Let $Z_n = \langle x \rangle$; Then $\tau(x) = x^m$ (remember $x$ is the generator). Because $\tau$ is a homomorphism, $\tau(x^a) = (x^m)^a = (x^a)^m$. Thus $\tau(y) = y^m$ for all $y \in Z_n$, and hence $\tau = \sigma_m$.

**#26d** $(\sigma_a \circ \sigma_b)(x) = \sigma_a(\sigma_b(x)) = \sigma_a(x^b) = x^{ab} = \sigma_{ab}(x)$. Let $\varphi : \text{Z}/n\text{Z} \to \text{Aut}(Z_n)$ be the map $\varphi(\overline a) = \sigma_a$. Then, $\varphi$ is a homomorphism because

$$
\varphi(\overline a \cdot \overline b) = \varphi(\overline{ab}) = \sigma_{ab}
= \sigma_a \circ \sigma_b = \varphi(\overline a) \varphi(\overline b)
$$

By #26a, $\sigma_a$ is an automorphism if and only if $(a, n) = 1$. By the previous statement and the fact that $\|\text{Aut}(Z_n)\| \leq n$, we have $\|\text{Aut}(Z_n)\| = \varphi(n) = \|\text{Z}/n\text{Z}\|$. $\varphi$ is injective by #26b and surjective by #26c, and thus it is injective. Therefore, $\varphi$ is an isomorphism.

## Section 2.4

**#7** Let $x = (1 \; 2)$, $y = (1 \; 3)(2 \; 4)$, and $a = (1 \; 4 \; 2 \; 3)$; Then $H = \langle x, y \rangle$ is the subgroup of $S_4$ we are considering. $a \in H$ because $a = xy$. We now want to show that $a$ and $x$ satisfy the $D_8$ generator relations; For starters, clearly $a^4 = x^2 = e$. Also $xax^{-1} = (1 \; 3 \; 2 \; 4) = a^{-1}$. Thus, because $H$ satisfies all relations of $D_8$, the two are isomorphic.

## Section 2.5

**#2a** $\langle sr^2, r^4 \rangle, \langle sr^6 \rangle,  \langle sr^2 \rangle, \langle r^4 \rangle, 1$.

**#2b** $\langle sr^3, r^4 \rangle, \langle r^4 \rangle, \langle sr^3 \rangle, \langle sr^7 \rangle, 1$.

**#2c** $\langle r^4 \rangle, \langle sr^2, r^4\rangle, \langle s, r^4\rangle, \langle r^2 \rangle, \langle sr^3, r^4\rangle, \langle sr^5, r^4 \rangle, \langle s, r^2\rangle, \langle r \rangle, \langle sr, r^2 \rangle, D_{16}$.

**#2d** $\langle s \rangle, \langle s, r^4 \rangle, \langle s, r^2 \rangle, D_{16}$.

**#10** If $G$ has an element of order $4$, then $1, x, x^2, x^3$ must be in $G$; But $\|G\| = 4$, so

$$
G = \{1, x, x^2, x^3\} = \langle x \rangle \cong Z_4
$$

Thus assume $G$ does not have an element of order $4$. Let $G = \\{1, a, b, c\\}$. By Lagrange's Theorem, $a^2 = b^2 = c^2 = 1$ (i.e. all elements in $G$ are of order $2$). Without loss of generality, $c = ab$; This is because $ab \in G$ by the group axioms and:

1. $ab = 1 \implies a^{-1} = b \implies a = b$
2. $ab = a \lor ab = b \implies b = 1 \lor a = 1$

Thus $c = ab$ and $(ab)^2 = 1$. By similar reasoning, we can show $ac = ca = b$, $bc = cb = a$, and $ba = c$. Because $G$ has the same multiplication table as $V_4$, we conclude that $G \cong V_4$. Zooming out, there are only two group of order $4$ (up to isomorphism): $V_4$ and $Z_4$.

## Section 3.1

**#9** $\varphi$ is a homomorphism:

$$
\begin{align}
\varphi((a^2 + b^2)(c^2 + d^2)) &= \varphi(ac - bd + (ad + cb)i) \\
&= (ac - bd)^2 + (ad + cb)^2 \\ &= (a^2 + b^2)(c^2 + d^2) \\
&= \varphi(a + bi)\varphi(c + di)
\end{align}
$$

The image of $\varphi$ is $R^+$ because the sum of squares is always positive. $\ker(\varphi)$ is the set of all points that form a circle of radius $1$ centered at the origin in the complex plane. The fiber above $r \in R$ is the set of all points that forms a circle of radius $\sqrt r$ centered at the origin in the complex plane.

**#32** The subgroup $\langle -1 \rangle = \\{1, -1\\}$ is normal in $Q_8$ because it is contained in the $Z(Q_8)$. Now consider the subgroup $\langle i \rangle = \\{1, -1, i, -i\\}$. Fix $x \in Q_8$. If $x \in \langle i \rangle$, then $x \langle i \rangle = \langle i \rangle x$; Otherwise, $x = \pm j$ or $x = \pm k$. Because $\langle i \rangle$ contains both the positive and negative of each element, we only need to check $x = j, k$. Thus $\langle i \rangle \unlhd Q_8$. Similar reasoning shows that $\langle j \rangle, \langle k \rangle \unlhd Q_8$. Hence, every subgroup of $Q_8$ is normal. Now consider the quotient $Q_8 / \langle i \rangle = \\{\overline 1, \overline j\\}$. Because $j^2 = -1$, we have $(\overline j)^2 = \overline 1$; Hence $Q_8 / \langle i \rangle \cong Z_2$. By symmetry, $Q_8 / \langle j \rangle, Q_8 / \langle k \rangle \cong Z_2$. Finally, $Q_8 / \langle -1 \rangle = \\{1, \overline i, \overline j, \overline k\\}$; Because $Q_8 / \langle -1 \rangle$ is of order $4$ and acyclic, $Q_8 / \langle -1 \rangle \cong V_4$.

**#35** Fix $X \in GL_n(F)$ and $Y \in X SL_N(F) X^{-1}$; Then $Y = XSX^{-1}$ for some $S \in SL_n(F)$. It's determinant is

$$
\det(Y) = \det(XSX^{-1}) = \det(X)\det(S)\det(X^{-1}) = \det(XX^{-1}) = \det(I) = 1
$$

Thus $Y \in SL_n(F)$, and $X SL_N(F) X^{-1} \subseteq SL_n(F)$. Therefore $SL_n(F) \unlhd GL_n(F)$. Now we consider $G = GL_n(F) / SL_n(F)$. Each element of $G$ is of the form

$$
\overline X = XSL_n(F) = \{XA \in GL_n(F) \mid \det(A) = 1\} = \{A' \in GL_n(F) \mid \det(A') = \det(X)\}
$$

(i.e. each element is the set of all matrices with determinant $\det(X)$). This suggests that $G$ is isomorphic to $F^\times$. Define $\varphi : G \to F^\times$ by $\varphi(\overline X) = \det(X)$. Clearly $\varphi$ is well defined. $\varphi$ is a homomorphism:

$$
\varphi(\overline X \cdot \overline Y) = \varphi(\overline{XY}) = \det(XY) = \det(X)\det(Y) = \varphi(\overline X)\varphi(\overline Y)
$$

$\varphi$ is also surjective because for any $c \in F$, we can find a matrix $A$ such that $\det(A) = c$ due to the surjectivity of $\det$. For $\overline X, \overline Y \in G$, if $\varphi(\overline X) = \varphi(\overline Y)$, then $\det(X) = \det(Y)$. By the set based definition of $\overline X$ and $\overline Y$, it follows that $\overline X = \overline Y$, or $\varphi$ is injective. Thus $\varphi$ is an isomorphism, and $GL_n(F) / SL_n(F) \cong F^\times$

**#36** Let $G/Z(G) = \langle x Z(G) \rangle$. Every coset is of the form $x^aZ(G)$. Fix $g, h \in G$; Then $g = x^a z_1$ and $h = x^b z_2$. Thus, because $z_1, z_2$ commute with $x^a, x^b$, we have

$$
gh = x^a z_1 x^b z_2 = x^{a + b} z_1 z_2 = x^b x^a z_1 z_2 = x^b z_2 x^a z_1 = hg
$$

Therefore, $G$ is abelian.

**#41** Fix $g \in G$ and $h \in gNg^{-1}$; Then $h$ is of the form

$$
h = gx^{-1}y^{-1}xyg^{-1} = gx^{-1}(g^{-1}g)y^{-1}(g^{-1}g)x(g^{-1}g)yg^{-1} = (gxg^{-1})^{-1}(gyg^{-1})^{-1}(gxg^{-1})(gyg^{-1}) \in N
$$

Thus $gNg^{-1} \subseteq N$, and $N \unlhd G$. We now consider $G/N$. If $x^{-1}y^{-1}xy \in N$, then $\overline x \ \overline y = \overline y \ \overline x$ because

$$
x^{-1}y^{-1}xy \in N \implies (x^{-1}y^{-1}xy)N = N \implies (xy)N = (yx)N \implies
\overline x \ \overline y = \overline y \ \overline x
$$

Therefore, $G/N$ is abelian because for every $\overline x, \overline y \in G/N$, we have $x^{-1}y^{-1}xy \in N$.

**#42** Let $x \in H$ and $y \in K$. Because $H$ is normal, $y^{-1}xy \in H$, and thus $x^{-1}y^{-1}xy \in H$. Because $K$ is normal, $x^{-1}yx \in K$; Inverting this, we get $x^{-1}y^{-1}x \in K$, and thus $x^{-1}y^{-1}xy \in K$. Therefore, $x^{-1}y^{-1}xy \in H \cap K$, and because $H \cap K = \\{1\\}$, it follows that $xy = yx$ for $x \in H$ and $y \in K$.

## Section 3.2

**#4** By Lagrange's theorem, $\|Z(G)\|$ divides $pq$; Thus either

1. $Z(G) = G$ which implies $G$ is abelian
2. $\|Z(G)\| = 1$ which implies $Z(G) = \\{1\\}$
3. $\|Z(G)\| = p \ \text{or} \ q$

Only the third case requires consideration. Let $\|Z(G)\| = p$. Then $\|G/Z(G)\| = q$, and because $q$ is prime, $G/Z(G)$ is cyclic. By exercise 3.1.36, this implies that $G/Z(G)$ is abelian. The proof for when $\|Z(G)\| = q$ follows by symmetry.

**#8** Because $H \cap K \leq H, K$, Lagrange's theorem implies that $\|H \cap K\|$ divides $\|H\|$ and $\|K\|$. But  $\|H\|$ and $\|K\|$ are relatively prime, so $\|H \cap K\| = 1$, and thus $H \cap K = \\{1\\}$.

**#22** $\|(Z/nZ)^\times\| = \varphi(n)$. Because $(a, n) = 1$, we have $\overline a \in (Z/nZ)^\times$. By *Corollary 9*, we have $\overline a^{\varphi(n)} = \overline 1$ which is equivalent to $a^{\varphi(n)} \equiv 1 \pmod n$.

**#23** We shall first consider $3^{100} \pmod{40}$. By Euler's theorem, $3^{16} \equiv 1 \pmod{40}$; Thus $3^{96} \equiv 1 \pmod{40}$, or $3^{100} \equiv 3^4 \equiv 81 \equiv 1 \pmod{40}$. This implies that $3^{100} = 40k + 1$ for some positive integer $k$. Now, we consider $3^{3^{100}} \pmod{100}$. By Euler's theorem, $3^{\varphi(100)} \equiv 3^{40} \equiv 1 \pmod{100}$. Therefore, $3^{3^{100}} \equiv 3^{40k + 1} \equiv 3 \pmod{100}$. In conclusion, the last two digits of $3^{3^{100}}$ are $03$.

## Section 3.3

**#3** Because $H \unlhd G$ and $K \leq [N_G(H) = G]$, the second isomorphism theorem implies that $KH \leq G$, $H \unlhd KH$, and $K \cap H \unlhd K$. By *Proposition 14*, $KH = HK$, or $HK \leq G$ and $H \unlhd HK$. Because $H \leq HK$, we have

$$
\begin{align}
|HK| = |H| \cdot |HK : H| &\implies |HK| \cdot |G : H| = |G| \cdot |HK : H| \\
&\implies \frac{|G|}{|HK|} = \frac{|G : H|}{|HK : H|}
\end{align}
$$

Because $HK \leq G$, it follows that $\|G\|/\|HK\| \in Z$; But $\|G : H\|$ is prime, so $\|HK : H\|$ is $1$ or $\|G : H\|$. If $\|HK : H\| = 1$, then $HK = H$; This implies that $K$ is equal to $H$ or $\\{1\\}$, implying (i). Let $\|HK : H\| = \|G : H\|$. Then $\|G\| = \|HK\|$, which leads to the conclusion that $G = HK$. The second isomorphism theorem also says that $KH/H \cong K/(K \cap H)$, or

$$
|H| \cdot |K| = |HK| \cdot |K \cap H| \implies |H| \cdot |K : K \cap H| = |HK| = |G|
$$

Dividing by $\|H\|$, we get $\|K : K \cap H\| = \|G : H\| = p$.

## Section 3.4

**#1** Because $G$ is abelian every subgroup is normal. Fix a nonidentity element $g \in G$; Then either $G \neq \langle g \rangle$ or $G = \langle g \rangle$. If $G \neq \langle g \rangle$, then $\langle g \rangle \unlhd G$. Because $\langle g \rangle$ is proper, this is a contradiction. Thus $G = \langle g \rangle$. If $\|G\| = \infty$, then $\langle g^2 \rangle \unlhd G$ is a proper subgroup, a contradiction. Thus $\|G\| = p < \infty$. For every divisor $k$ of $p$,  $\langle g^k \rangle \unlhd G$ is proper. Thus the only divisors of $p$ are $1$ and $p$, rendering $p$ prime. Therefore, $G \cong Z_p$.

## Section 3.5

**#3** We shall prove this by induction. Consider case $n = 2$. Then $S_n = \\{(1), (1 \; 2)\\}$, and the result clearly holds. Consider case $n = k$. Assume the result holds for $k - 1$. Every element in $S_n$ is the product of transpositions; Thus, we want to show that $S_n$ contains all transpositions on $n$ letters. In other words, we want to show $S_n = \langle P_n \rangle$ where $P_n = \\{(m \;\; m+ 1) \mid 1 \leq m \leq k\\}$. Fix an element $\sigma \in S_n$ such that $\sigma = (i \; j)$. We now condition on $i$ and $j$ to show that $\sigma \in \langle P_n \rangle$:

1. $1 \leq i < j \leq k - 1$: Result follows from induction hypothesis
2. $i = j - 1$ and $j = k$: Then $\sigma \in P_k$, and hence generated by it
3. $i < j - 1$ and $j = k$: By 1. and 2., $(i \;\; k - 1)$ and $(k - 1 \;\; k)$ are generated by $P_k$. Thus letting $\sigma = (k - 1 \;\; k)(i \;\; k - 1)(k - 1 \;\; k) = (i \; k)$, the result follows.

By induction the result holds for $n = k$, and hence the result is proved.

**#10** We claim that the composition series is $\\{1\\} \unlhd N \unlhd V_4 \unlhd A_4$ where $N = \langle (1 \; 2)(3 \; 4) \rangle$ (thus $N \cong Z_2$). It isn't difficult to prove that to be a correct normal subgroup hierarchy. $\|A_4/V_4\| = 12/4 = 3$, and because $3$ is prime, $A_4/V_4$ is isomorphic to a simple group of order $3$ (namely $Z_3$). The same holds for $V_4/N$ (isomorphic to $Z_2$) and $N/\\{1\\}$ (isomorphic to $N = Z_2$). Because all the quotients are isomorphic to an abelian group, they are abelian, and hence $A_4$ is solvable.

## Section 4.1

**#1** Fix $h \in G_a$; Then $h \cdot a = a$, and because $a = g^{-1} \cdot b$, it follows that $ghg^{-1} \cdot b = b$. Hence $gG_ag^{-1} \subseteq G_b$. Fix $h' \in G_b$; Then $h' \cdot b = b$, and because $b = g \cdot a$, it follows that $g^{-1}h'g \cdot a = a$. Thus $g^{-1}h'g \in G_a$, or $h' \in gG_ag^{-1}$, or $G_b \subseteq gG_ag^{-1}$. Therefore $gG_ag^{-1} = G_b$. Assume that $G$ acts transitively on $A$. Let $K$ be the kernel of this action. We know that the kernel is the intersection of the stabilizers. By the previous result, we know that for an arbitrary $b \in A$, there exists a $g \in G$ such that $G_b = gG_ag^{-1}$. This means

$$
K = \bigcap_{b \in A} G_b = \bigcap_{g \in G} g G_a g^{-1}
$$

## Section 4.2

**#1a** Let $\varphi : G \to S_4$. Then $\varphi(a)(1) = 2$, $\varphi(a)(2) = 1$, and so on. The same holds for the rest, leaving us with the mapping:

$$
a \mapsto (1 \; 2)(3 \; 4) \qquad b \mapsto (1 \; 4)(2 \; 3) \qquad c \mapsto (1 \; 3)(2 \; 4)
$$

**#1b** Let $\varphi : G \to S_4$. Then $\varphi(a)(1) = 4$, $\varphi(a)(2) = 3$, and so on. The same holds for the rest, leaving us with the mapping:

$$
a \mapsto (1 \; 4)(2 \; 3) \qquad b \mapsto (1 \; 2)(3 \; 4) \qquad c \mapsto (1 \; 3)(2 \; 4)
$$

This is the same subgroup as in part a.

**#8** Let $G$ act on the set $A$ of left cosets of $H$ in $G$, and let $\varphi : G \to S_A$ be the homomorphism defined by $\varphi(g)(g'H) = (gg')H$. Clearly, $K = \ker(\varphi)$ is a normal subgroup of $G$. By *Theorem 3*, $K \leq H$, and by Lagrange's theorem,

$$
|G| = |K| \cdot |G : K| \implies |G/K| = |G : K|
$$

By the first isomorphism theorem, $G/K$ is isomorphic to a subgroup of $S_A$. Because $\|S_A\| = n!$, It follows that $\|G : K\| = \|G/K\| \leq \|S_A\| = n!$.

## Section 4.3

**#5** Fix $g \in G$. Clearly $Z(G) \subseteq C_G(g)$, and thus $\|Z(G)\| \leq \|C_G(g)\|$. By *Proposition 6*, $\|G : C_G(g)\| = \|K_j\|$ where $K_j$ is the conjugacy class of $g$. By Lagrange's Theorem, $\|G\| = \|K_j\| \cdot \|C_G(g)\| \geq \|K_j\| \cdot \|Z(G)\|$, thus $\|K_j\| \leq \|G\|/\|Z(G)\| = \|G : Z(G)\| = n$. Thus the same holds for all conjugacy classes, and the theorem is proved.

**#21** Assume $\sigma \in S_n$ does not commute with any odd permutation. $\sigma$ commutes with every cycle in it's cycle decomposition, so the cycle type of $\sigma$ is all odds. Assume that two cycles have the same odd length $n$. Let $\sigma'$ be their product $\sigma' = (a_1 \; \ldots \; a_n)(b_1 \; \ldots \; b_n)$. If $\tau = (a_1 \; b_1) \ldots (a_n \; b_n)$, then $\tau \sigma' \tau^{-1} = \sigma'$ because

$$
\tau(a_1 \; \ldots \; a_n)\tau^{-1} = (b_1 \; \ldots \; b_n)
\qquad \text{and} \qquad
\tau(b_1 \; \ldots \; b_n)\tau^{-1} = (a_1 \; \ldots \; a_n)
$$

Because $\tau$ is the product of $n$ transpositions and $n$ is odd, we have a contradiction. Thus, no two cycles have the same odd length.

Conversely, assume that the cycle type of $\sigma$ consists of distinct odd integers. Let $\sigma$ commute with $\tau$: $\tau \sigma \tau^{-1} = \sigma$, and express $\sigma = \sigma_1\ldots\sigma_k$ as the product of cycles where $\|\sigma_i\| = p_i$. By *Proposition 10* it follows that $\sigma = \tau\sigma\tau^{-1} = (\tau\sigma_1\tau^{-1}) \ldots (\tau\sigma_k\tau^{-1})$. Thus,

$$
\tau\sigma_i\tau^{-1} = \sigma_j \implies p_i = p_j \implies i = j \implies
\tau \sigma_i = \sigma_i \tau
$$

(because the cycle type of $\sigma$ consists of distinct odd integers). In other words, $\tau$ commutes with every cycle $\sigma_i$ in $\sigma$. Fix a cycle $\tau_i$ of $\tau$. Because $\tau$ commutes with $\sigma_i$, we know $\tau_i$ commutes with $\sigma_i$. Thus $\tau_i \in C_{\text{Sym}(n)}(\\{\sigma_i\\})$. Because $\sigma_i$ commutes with it's powers, $\langle \sigma_i \rangle \subseteq C_{\text{Sym}(n)}(\\{\sigma_i\\})$, and because $\|\sigma_i\| = p_i$, it follows from *Proposition 10* that there exist $p_i$ such $\tau_i$s; This implies $\|C_{\text{Sym}(n)}(\\{\sigma_i\\})\| = p_i$, or $C_{\text{Sym}(n)}(\\{\sigma_i\\}) = \langle \sigma_i \rangle$. This implies that $\tau_i \in \langle \sigma_i \rangle$, or that for all $1 \leq i \leq k$, we have $\tau_i = \sigma_i^{a_i}$. This implies $\sigma$ only commutes with the group generated by the cycles in its cycle decomposition. In other words, $\sigma$ only commutes with even permutations, not odd permutations.

## Section 4.5

**#3** Let the prime factorization of the order of $G$ be $\|G\| = p_1^{e_1} \ldots p_k^{e_k}$. Let $p_i$ be a number dividing $\|G\|$. Then $p_i \in \\{p_1, \ldots, p_k\\}$, and the Sylow-$p_i$ group $H \leq G$ is of order $p_i^{e_i}$. Fix a nontrivial element $h \in H$. Then the order of $h$ is one of $p_i, p_i^2, \ldots, p_i^{e_i}$ because the order of an element in a group must divide the order of the group;  Let $\|h\| = p_i^j$ where $1 \leq j \leq e_i$. Then

$$
\left|h^{p_i^{j-1}}\right| =
\frac{\left|p_i^j\right|}{\left|\left(p_i^j, p_i^{j-1}\right)\right|} = \frac{\left|p_i^j\right|}{\left|p_i^{j-1}\right|} = |p_i|
$$

Thus there exists an element of order $p_i$ in $H$, and hence $G$.

**#7** Because $\|S_4\| = 2^3 \cdot 3$, the order of each Sylow 2-subgroup is $8$. By the Third Sylow Theorem, $n_2 \mid 3$. Thus $n_2$ is either $1$ or $3$. Because the following three subgroups are all of order $8$ (and hence Sylow 2-subgroups), they make up all Sylow 2-subgroups of $S_4$:

$$
H_1 = \langle (1 \; 2 \; 3 \; 4), (1 \; 3) \rangle
\qquad
H_2 = \langle (1 \; 2 \; 4 \; 3), (1 \; 4) \rangle
\qquad
H_3 = \langle (1 \; 3 \; 2 \; 4), (1 \; 2) \rangle
$$

By conjugating on the generators of $H_1$ using *Proposition 4.3.10*, we find that $(3 \; 4)H_1(3 \; 4)^{-1} = H_2$ and $(3 \; 2)H_1(3 \; 2)^{-1} = H_3$.

**#13** $\|G\| = 2^3 \cdot 7$. Then, $G$ has a Sylow $7$-subgroup of order $7$; Call it $H_7$. By the third Sylow Theorem, $n_7$ is $1$ or $8$. If $n_7 = 1$, then by *Corollary 20*, $H_7 \unlhd G$, and we are done. Assume $n_7 = 8$. Because $\|H_7\|$ is prime, $H_7 \cong Z_7$, and thus $H_7$ has $6$ elements of order $7$. All Sylow $7$-subgroups are disjoint (this includes $H_7$) because they are cyclic. Thus $G$ has $6 \cdot 8 = 48$ elements of order $7$, with $8$ leftover spaces. $G$ has a Sylow $2$-subgroup of order $8$; Call it $H_2$. No element in $H_2$ is of order $7$ because $7 \not\mid 8$. Thus, the $8$ leftover spaces in $G$ are filled by $H_2$, and $n_2 = 1$, or $H_2 \unlhd G$.

**#29** My hands will commit suicide before I can complete the proof of this statement (but if you had to do one proof from this section, this would be it).

## Section 5.1

**#1** Let $g = (g_1, \ldots, g_n) \in G_1 \times \ldots \times G_n$ and $z = (z_1, \ldots, z_n) \in Z(G_1) \times \ldots Z(G_n)$. The result follows from the (trivial) fact that $zg = gz$ if and only if $z_ig_i = g_iz_i$ for all $i$. A group $G$ is abelian if and only if $Z(G) = G$. This means that the expression stated previously, $Z(G_1 \times \ldots \times G_n) = Z(G_1) \times \ldots \times Z(G_n)$ must be equal to $G_1 \times \ldots \times G_n$. This implies that $Z(G_i)$ must equal $G_i$, or that every group is abelian. If every factor is abelian (i.e. $Z(G_i) = G_i$), then

$$
G_1 \times \ldots \times G_n = Z(G_1) \times \ldots \times Z(G_n) = Z(G_1 \times \ldots \times G_n)
$$

and hence, $G_1 \times \ldots \times G_n$ is abelian.

**#4** Let $\|A\| = p^\alpha m$ and $\|B\| = p^\beta n$. Then $\|A \times B\| = p^{\alpha + \beta}mn$. If $P \in \text{Syl}_p(A)$ and $Q \in \text{Syl}_p(B)$, then $P \times Q \leq A \times B$, and because $\|P \times Q\| = p^{\alpha + \beta}$, we have $P \times Q \in \text{Syl}_p(A \times B)$. This implies

$$
\text{Syl}_p(A) \times \text{Syl}_p(B) \subseteq \text{Syl}_p(A \times B)
$$

Fix $X \in \text{Syl}_p(A \times B)$. By the Second Sylow Theorem, there exists an $(a, b) \in A \times B$ such that

$$
X = (a, b)(P \times Q)(a, b)^{-1} = aPa^{-1} \times bQb^{-1} \in \text{Syl}_p(A) \times \text{Syl}_p(B)
$$

Thus we also have $\text{Syl}_p(A \times B) \subseteq \text{Syl}_p(A) \times \text{Syl}_p(B)$, and that

$$
\text{Syl}_p(A \times B) = \text{Syl}_p(A) \times \text{Syl}_p(B)
$$

From this, we also immediately have $n_p(A \times B) = n_p(A)n_p(B)$. The generalized result follows by induction, which we omit here.

**#11** There are $p^n - 1$ non identity elements of order $p$ in $E_{p^n}$. Each of these generates a cyclic subgroup, so there are $p^n - 1$ cyclic subgroup of order $p$ in $E_{p^n}$. Because $p$ is prime, each subgroup of order $p$ has $p - 1$ generators; Thus the number of cyclic subgroups of order $p$ is $(p^n - 1) / (p - 1)$. Because all subgroups of order $p$ must be cyclic (by Lagrange's theorem), there aren't any we haven't counted.

## Section 5.2

**#1a** There are $4$ abelian groups of order $100$

**#1b** There are $22$ abelian groups of order $576$

**#1c** There is $1$ abelian group of order $1155$

**#1d** There are $9$ abelian groups of order $42875$

**#1e** There are $10$ abelian groups of order $2704$

## Section 5.4

**#2**

$$
\begin{align*}
H \unlhd G &\iff g^{-1}hg \in H       &&\forall g \in G, h \in H \\
           &\iff h^{-1}g^{-1}hg \in H &&\forall g \in G, h \in H \\
           &\iff g^{-1}h^{-1}gh \in H &&\forall g \in G, h \in H \\
           &\iff [g, h] \in H         &&\forall g \in G, h \in H \\
           &\iff [G, H] \leq H
\end{align*}
$$

**#4** The proper normal subgroups of $S_4$ are $V_4$ and $A_4$. $S_4/V_4 \cong S_3$ which is not abelian; On the other hand $S_4/A_4 \cong Z_2$ which is abelian. Thus $S'_4 = A_4$. The only normal subgroup of $A_4$ is $V_4$. Because $A_4/V_4 \cong Z_3$ which is abelian, $A_4' = V_4$.

**#5**

*Lemma:* $A_n$ is the only proper subgroup of $S_n$ for $n \geq 5$.

*Proof:* Let $N \unlhd S_n$ be proper. By the Diamond Isomorphism Theorem and the fact that $A_n \unlhd S_n$, we have $A_n \cap N \unlhd A_n$. Because $A_n$ is simple, $A_n \cap N \cong \\{1\\}, A_n$. This means $N = \\{1\\}, A_n, S_n$. Because $N$ is proper, we have $N = A_n$.

By the lemma, $A_n$ is the only normal subgroup of $S_n$ in this case. Beacuse $S_n/A_n \cong Z_2$, we have $S'_n = A_n$ for all $n \geq 5$.

## Section 7.1

**#6a,b** Yes

**#6c** No

**#6d** Let $f(x) = 0$ for $x \in \left[0, \frac{1}{2}\right]$ and $f(x) = 1$ for $x \in \left(\frac{1}{2}, 1\right]$. Similarly, let $g(x) = 0$ for $x \in \left(\frac{1}{2}, 1\right]$ and $g(x) = 1$ for $x \in \left[0, \frac{1}{2}\right]$. Clearly $f$ and $g$ have an infinite number of zeros. Then $(f + g)(x) = 1$ for all $x \in [0, 1]$, and hence doesn't have a finite number of zeros.

**#6e** Yes, by the limit laws.

**#6f** By the trigonometric identities, yes.

**#14a** If $m = 1$, then $x = 0$; Assume $m > 1$. Letting $y = x^{m-1}$, we have $xy = yx = x^m = 0$ by the fact that $x$ is nilpotent. Thus $x$ is a zero divisor for $m > 1$.

**#14b** Because $R$ is a commutative ring, $(rx)^m = r^mx^m = r^m \cdot 0 = 0$. Thus $rx$ is nilpotent.

**#14c** Let $a = 1 + x$ and $b = 1 - x + x^2 - x^3 + \ldots + (-1)^{m - 1} x^{m - 1}$ where $x^m = 0$ (remember $x$ is nilpotent). If $m$ is odd, then $ab = x^m + 1$; Otherwise, if $m$ is even, then $ab = 1 - x^m$. In any case, because $x^m = 0$, we have $ab = 1$, and hence, $a$ is a unit of $R$.

**#14d** Fix a unit element $y \in R$. By #14b, $y^{-1}x$ is nilpotent, and by #14c, $1 + y^{-1}x$ is a unit. Then, $y + x = y(1 + y^{-1}x)$ is a unit.

**#23** Clearly, $1 \in \mathcal O_f$, and $\mathcal O_f$ is closed under subtraction. Fix $x, y \in \mathcal O_f$; Then $x = a + bf\omega$ and $y = c + df\omega$. Hence,

$$
xy = \cases{
(ac + bdf^2D) + (ad + bc)f\omega & $D \equiv 2, 3 \pmod 4$ \\
(ac + bdf^2(D - 1)/4) + (ad + bc + bdf)f\omega & $D \equiv 1 \pmod 4$
}
$$

Thus $\mathcal O_f$ is closed under multiplication, and $\mathcal O_f$ is a subring of $\mathcal O$.

**#25a** You can check this by straightforward (albeit tedious) multiplication.

**#25b** $N(ab) = ab\overline{ab} = ab\overline b \overline a = aN(b)\overline a = N(a)N(b)$ because $N(b)$ is an integer.

**#25c** Let $x \in I$ be an element such that $N(x) = 1$. Then we have $x = a + bi + cj + dk$ if and only if $a^2 + b^2 + c^2 + d^2 = 1$ if and only if one of $a, b, c, d$ is $\pm 1$ (while the rest are zero) if and only if $x \in \\{\pm i, \pm j, \pm k, \pm 1\\}$ if and only if $x$ is a unit. The relations of the group of units of the Hamiltonian quaternions (which is $\\{\pm i, \pm j, \pm k, \pm 1\\}$)are the same as that of the quaternions group of order $8$. Because they also have the same size, $I^\times \cong Q_8$.

## Section 7.2

**#3a** Assuming you've proved it's a ring (simple, but tedious), we can clearly see multiplication is commutative:

$$
\begin{align}
\left(\sum_{n=0}^\infty a_nx^n\right)\left(\sum_{n=0}^\infty b_nx^n\right)
&= \sum_{n=0}^\infty (a_0b_n + a_1b_{n-1} + \ldots + a_nb_0)x^n \\
&= \sum_{n=0}^\infty (b_0a_n + b_1a_{n-1} + \ldots + b_na_0)x^n \\
&= \left(\sum_{n=0}^\infty b_nx^n\right)\left(\sum_{n=0}^\infty a_nx^n\right)
\end{align}
$$

and hence $R[[x]]$ is a commutative ring. If $a_0 = 1$ and $a_i = 0$ for $i > 1$, then $\sum_{n=0}^\infty a_nx^n = 1$; This is the identity element in $R$.

**#3b** Multiplying them out we get

$$
\begin{align}
(1 - x)(1 + x + x^2 + \ldots) &= (1 + x + x^2 + \ldots) - x(1 + x + x^2 + \ldots) \\
&= (1 + x + x^2 + \ldots) - (x + x^2 + x^3 + \ldots) \\
&= 1
\end{align}
$$

**#3c** Assume $\sum_{n=0}^\infty a_nx^n$ is a unit in $R[[x]]$. Then for some $\sum_{n=0}^\infty b_nx^n$, we have

$$
\left(\sum_{n=0}^\infty a_nx^n\right)\left(\sum_{n=0}^\infty b_nx^n\right) = \sum_{n=0}^\infty \left(\sum_{k=0}^n a_kb_{n-k}\right)x^n = 1
$$

This implies $a_i = b_i = 0$ for $n > 0$, and $a_0b_0 = 1$. This implies $a_0$ is a unit with inverse $b_0$. Assume $a_0$ is a unit. We wish to define $\sum_{n=0}^\infty b_nx^n$ such that $\sum_{k=0}^n a_kb_{n-k} = 0$ for $n > 0$. Solving for $b_n$, this recursively implies that

$$
b_n = -b_0\left(\sum_{k=1}^n a_kb_{n-k}\right)
$$

Therefore, we have constructed an inverse.

**#13a** First we show $g^{-1}Kg = K$ (or alternatively, $Kg = gK$). Because $K$ is the sum of the conjugacy class $\mathcal K$, and conjugation by a single element permutes $\mathcal K$, we have

$$
g^{-1}Kg = g^{-1}k_1g + \ldots + g^{-1}k_mg = K
$$

Fix $L \in R[G]$ so that $L = \sum_{j = 1}^t a_jg_j$ for $1 \leq a_j \leq n$. Then,

$$
\begin{align}
KL &= \left( \sum_{i=1}^m k_i \right)\left( \sum_{j=1}^t a_jg_j \right)
    = \sum_{i=1}^m \sum_{j = 1}^t k_i a_j g_j = \sum_{j = 1}^t \sum_{i=1}^m a_j k_i g_j
\\ &= \sum_{j = 1}^t a_j\left( \sum_{i=1}^m k_i \right)g_j
	  = \sum_{j=1}^t a_j K g_j = \sum_{j=1}^t a_j g_j K
\\& = LK
\end{align}
$$

Thus, $K$ is in the center of $R[G]$.

**#13b** Assume $\alpha = a_1K_1 + \ldots + a_rK_r$. Fix $\beta \in R[G]$ such that $\beta = \sum_{j = 1}^t b_jg_j$. Then

$$
\alpha\beta = \left( \sum_{i=1}^r a_i K_i \right) \left( \sum_{j=1}^t b_j g_j \right)
            = \sum_{j=1}^t \sum_{i=1}^r b_j g_j a_i K_i
            = \sum_{j=1}^t b_j g_j \left( \sum_{i=1}^r a_i K_i \right)
            = \beta\alpha
$$

Thus $\alpha \in Z(R[G])$. That aside, now assume $\alpha \in Z(R[G])$ such that $\alpha = \sum_{i=1}^n a_ig_i$ where $\|G\| = n$; Summing up to $n$ may seem artificial, but it is completely normal noting that the coefficients $a_i$ can be $0$. Fix $h \in R[G]$ (where $h \in G$, so that the coefficient of $h$ in $R[G]$ is $1$). Then, because $\alpha$ is in the center of $R[G]$, we have $h \alpha h^{-1} = \alpha$, or

$$
\sum_{i=1}^n a_i\left(hg_ih^{-1}\right) = \sum_{i=1}^n a_ig_i
$$

Thus, all conjugates share the same coefficient, and because we are summing up to $n = \|G\|$, the result is proved.

## Section 7.3

**#13** It is easily checked that $\varphi : M_2(\mathbb R) \to \mathbb C$ defined by

$$
\varphi\pmatrix{x & -y \\ y & x} = x + yi
$$

is a bijective ring homomorphism (and hence an isomorphism).

**#24a** First, we show $\varphi^{-1}(J)$ is a subring of of $R$. Fix an element $j \in \varphi^{-1}(J)$. Then $\varphi(j) \in J$, which implies that $-\varphi(j) \in J$. Because $\varphi$ is a homomorphism, this implies $\varphi(-j) \in J$, or $-j \in \varphi(J)$. Because each element and their inverses are in $\varphi^{-1}(J)$, it follows that is a group. Thus, we have shown $\varphi^{-1}(J)$ is a subgroup of $R$. To show it is a subring, we must show it is closed under multiplication. Fix elements $j, k \in \varphi^{-1}(J)$. Then $\varphi(j), \varphi(k) \in J$. Because $\varphi$ is a homomorphism, this implies $\varphi(j)\varphi(k) = \varphi(jk) \in J$, or $jk \in \varphi^{-1}(J)$. Thus, $\varphi^{-1}(J)$ is a subring of $R$.

Next, we want to show that $\varphi^{-1}(J)$ is not only a subring of $R$, but an ideal too. Fix an element $r \in R$, and $s \in \varphi^{-1}(J)$. Then $rs \in r\varphi^{-1}(J)$, or $\varphi(rs) \in \left[ \varphi(r) J = s'J = J \right]$ because $J$ is an ideal. Therefore, $rs \in \varphi^{-1}(J)$. Because $rs \in r\varphi^{-1}(J)$, it follows that $r\varphi^{-1}(J) \subseteq \varphi^{-1}(J)$. We have shown that $\varphi^{-1}(J)$ is a left-ideal of $R$. An analogous proof exists to show it to be a right-ideal, thus proving $\varphi^{-1}(J)$ to be an ideal of $R$.

Using what we proved in the previous few paragraphs, $\varphi^{-1}(J)$ is an ideal of $R$. Because $\varphi$ is an inclusion homomorphism $\varphi^{-1}(J) = J \cap R$, and thus we have $J \cap R$ to be an ideal of $R$.

**#24b** Clearly $\varphi(I)$ is a subgroup of $S$ (because $I \leq R$ and $\varphi$ is a group homomorphism). Fix $s \in S$; We want to show $s\varphi(I) \subseteq \varphi(I)$. Because $\varphi$ is surjective, there exists an $r \in R$ such that $\varphi(r) = s$. Thus, because $I$ is an ideal in $R$,

$$
s\varphi(I) = \varphi(r)\varphi(I) = \varphi(rI) = \varphi(I)
$$

This implies that $\varphi(I)$ is closed under multiplication (and hence a subring) and $\varphi(I)$ is ideal in $S$.

**#29** Fix $x, y \in \mathfrak R(R)$ such that $x^m = y^n = 0$. Clearly $-x \in \mathfrak R(R)$. We now expand $(x + y)^{m + n}$ using the binomial theorem:

$$
(x+y)^{m+n} = \sum_{k = 0}^{m+n} \binom{m + n}{k} x^k y^{m + n - k}
$$

We see that the power of $x$ is always greater than $m$ *or* the power of $y$ is always greater than $n$; Thus $(x + y)^{m + n} = 0$, and $x + y \in \mathfrak R(R)$. Because $R$ is a commutative ring, $(xy)^m = x^my^m = 0$, and we have that $xy \in \mathfrak R(R)$. Therefore, $\mathfrak R(R)$ is a subring of $R$. If $r \in R$, then $rx \in r\mathfrak R(R)$, and $(rx)^n = r^nx^n = 0$. This implies that $rx \in \mathfrak R(R)$, or $r\mathfrak R(R) \subseteq \mathfrak R(R)$. Hence, $\mathfrak R(R)$ is an ideal of $R$, and we are done.

## Section 7.4

**#10** Suppose $x \in R$ is a zero divisor. Then, there exists a $y$ such that $xy \in P$. Because $P$ is a prime ideal, either $x \in P$ or $y \in P$, contradicting the fact that $P$ has no zero divisors.

**#15a** If $p \in \overline E$, then $p = q(x^2 + x + 1) + r$. We know that $\deg(r) < 2$, so possible values for $r$ are $r = 0, 1, x, x + 1$. Because $r$ and $p$ are from the same coset, the four elements in $\overline E$ are $\overline 0, \overline 1, \overline x, \overline{x + 1}$.

**#15b** Addition table for $\overline E$ (visually isomorphic to $V_4$):

| $+$                | $\overline 0$      | $\overline 1$      | $\overline x$      | $\overline{x + 1}$ |
| ------------------ | ------------------ | ------------------ | ------------------ | ------------------ |
| $\overline 0$      | $\overline 0$      | $\overline 1$      | $\overline x$      | $\overline{x + 1}$ |
| $\overline 1$      | $\overline 1$      | $\overline 0$      | $\overline{x + 1}$ | $\overline x$      |
| $\overline x$      | $\overline x$      | $\overline{x + 1}$ | $\overline 0$      | $\overline 1$      |
| $\overline{x + 1}$ | $\overline{x + 1}$ | $\overline x$      | $\overline 1$      | $\overline 0$      |

**#15c** Multiplication table for $\overline E$ (visually isomorphic to $Z_3$):

| $\times$           | $\overline 0$ | $\overline 1$      | $\overline x$      | $\overline{x + 1}$ |
| ------------------ | ------------- | ------------------ | ------------------ | ------------------ |
| $\overline 0$      | $\overline 0$ | $\overline 0$      | $\overline 0$      | $\overline 0$      |
| $\overline 1$      | $\overline 0$ | $\overline 1$      | $\overline x$      | $\overline{x + 1}$ |
| $\overline x$      | $\overline 0$ | $\overline x$      | $\overline{x + 1}$ | $\overline 1$      |
| $\overline{x + 1}$ | $\overline 0$ | $\overline{x + 1}$ | $\overline 1$      | $\overline x$      |

$Z_3$ is commutative, so $\overline E$ is a commutative ring with $1 \neq 0$. We also have $\overline{E}^\times = \overline E - \\{0\\}$. This is the definition of a field (and hence the result).

## Section 8.1

**#1c** Their gcd is $3$:

$$
(11391, 5673) = (45, 5673) = (45, 3) = 3
$$

**#2c** They are relatively prime:

$$
(1891, 3797) = (1891, 15) = 1
$$

To find the inverse, we wish to solve $1891x \equiv 1 \pmod{3797}$; Put another way, we want to solve $1891x - 3797y = 1$. Solving this, we find $1891^{-1} = x = 253$.

**#3** Let $b$ denote an element of norm $m$ (where $m$ is a as defined in the problem). Then $1 = qb + r$. Because $N(r) < N(b) = m$, we have $r = 0$, or $1 = qb$. Thus $b$ is a unit with inverse $q$. Now for the second statement. If $b' \neq 0$, but $N(b') = 0$, then by the proof above, $b'$ is a unit.

**#10** Because every ideal in $\mathbb Z[i]$ is principal, we have $I = (\alpha)$ for some $\alpha \in \mathbb Z[i]$. Fix $\overline \beta \in \mathbb Z[i]/I$ where $\beta$ is a representative for $\mathbb Z[i]/I$. Because we have $\beta = q\alpha + \gamma$ where $q, \gamma \in \mathbb Z[i]$, by the definition of the norm in a Euclidean domain, we know that $N(\gamma) < N(\alpha)$. But $\gamma$, must also be in $\overline \beta$ because $\overline \beta = I + x$. Thus, we have shown that every coset in $\mathbb Z[i]$ can be represented by an element of norm less than $\alpha$. Because there are only finitely amount $x \in \mathbb Z[i]$ such that $N(x) < N(\alpha)$, $\mathbb Z[i]/I$ has finitely many elements.

**#12** We start of by noting $dd' = x\varphi(N) + 1$. Then, by Euler's theorem, we have the desired result:

$$
M_1^{d'} \equiv M^{dd'} \equiv M^{x\varphi(N)}\cdot M \equiv M \pmod N
$$

## Section 8.2

**#1** Assume ideals $(a)$ and $(b)$ are comaximal in ring $R$. That is, $(a) + (b) = R$. This implies $ax + by = r$ for *every* $r \in R$. By Bézout's identity, all possible values of $ax + by$ are multiples of the gcd of $a$ and $b$. Because $ax + by$ can be any value in $R$, it follows that $a$ and $b$ are coprime. The proof of the converse if analogous (in the reverse direction).

## Section 8.3

**#2** I think its clear that the lcm exists. Define

$$
\begin{align}
a &= up_1^{e_1} \ldots p_n^{e_n} \\
b &= vp_1^{f_1} \ldots p_n^{f_n} \\
l &= p_1^{\max(e_1, f_1)} \ldots p_n^{\max(e_n, f_n)}
\end{align}
$$

Clearly, $a, b \mid l$, and $l$ is the smallest such number.