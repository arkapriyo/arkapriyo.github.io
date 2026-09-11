---
title: "Why group theorists keep encountering the number Two"
Date: 2026-06-25
weight: 100
draft: false
showAuthor: true
mathjax: true
showComments: true
---
{{< katex >}}

One quickly learns that abelian groups are the "nice" groups—the ones in which multiplication can be performed in any order. There is something suspicious about the number \(2\) in group theory. At first it appears in completely elementary places: groups of exponent \(2\) are abelian, subgroups of index \(2\) are automatically normal, and involutions produce immediate parity arguments. But the same number keeps returning in much deeper places — fixed-point-free automorphisms, centralizers of involutions, Brauer--Fowler, and eventually the structure of finite simple groups.

So perhaps \(2\) is not merely the smallest prime. All the groups we will be dealing with will be finite groups.

## 1. Exponent \(2\): noncommutativity disappears

Suppose \(G\) satisfies \(x^2=1\) for every \(x\in G\). Then \(x^{-1}=x\), and hence for \(x,y\in G\),

\[
xy=(xy)^{-1}=y^{-1}x^{-1}=yx.
\]

Thus every group of exponent \(2\) is abelian. In the finite case,

\[
G\cong (\mathbf Z/2\mathbf Z)^r,
\]

so such groups are simply finite-dimensional vector spaces over \(\mathbf F_2\).

Already \(2\) is unusually rigid: requiring every element to have order dividing \(2\) completely destroys noncommutativity.

The analogous statement is already false for exponent \(3\). Consider the Heisenberg group over \(\mathbf F_3\),

\[
G=\left\{
\begin{pmatrix}
1&a&c\\
0&1&b\\
0&0&1
\end{pmatrix}
:a,b,c\in\mathbf F_3
\right\}.
\]

Every nonidentity element has order \(3\). Indeed, each element has the form \(I+N\) with \(N^3=0\), and in characteristic \(3\),

\[
(I+N)^3=I+3N+3N^2+N^3=I.
\]

Yet \(G\) is not abelian. Taking

\[
x=
\begin{pmatrix}
1&1&0\\
0&1&0\\
0&0&1
\end{pmatrix},
\qquad
y=
\begin{pmatrix}
1&0&0\\
0&1&1\\
0&0&1
\end{pmatrix},
\]

we obtain

\[
xy=
\begin{pmatrix}
1&1&1\\
0&1&1\\
0&0&1
\end{pmatrix}
\neq
\begin{pmatrix}
1&1&0\\
0&1&1\\
0&0&1
\end{pmatrix}
=yx.
\]

Thus exponent \(2\) forces abelianity, whereas exponent \(3\) already allows genuinely nonabelian behaviour.

## 2. A power-map

Here is another place where \(2\) appears rather unexpectedly.

Suppose \(G\) is a finite group and \(m,n\) are positive integers such that both power maps \(x\mapsto x^m\) and \(x\mapsto x^n\) are homomorphisms. Assume moreover that

\[
\gcd\bigl(m(m-1),n(n-1)\bigr)=2.
\]

Then \(G\) must be abelian.

To see why, first suppose more generally that the \(k\)-th power map \(P_k(x)=x^k\) is a homomorphism. Comparing the two ways of taking the \(k\)-th power of \(xyx^{-1}\), we get

\[
xy^kx^{-1}=(xyx^{-1})^k=P_k(xyx^{-1})=x^ky^kx^{-k}.
\]

Hence \(x^{k-1}\) commutes with \(y^k\). Interchanging \(x\) and \(y\) also shows that \(x^k\) commutes with \(y^{k-1}\). Therefore \(x^{k(k-1)}\) commutes with both \(y^k\) and \(y^{k-1}\). Since \(\gcd(k,k-1)=1\), there exist integers \(a,b\) with \(ak+b(k-1)=1\), so \(y=(y^k)^a(y^{k-1})^b\). Thus

\[
x^{k(k-1)}\in Z(G)
\]

for every \(x\in G\).

Apply this for \(k=m\) and \(k=n\). Writing \(A=m(m-1)\) and \(B=n(n-1)\), we know that \(x^A,x^B\in Z(G)\). Since \(\gcd(A,B)=2\), Bézout gives integers \(r,s\) such that \(rA+sB=2\). Hence

\[
x^2=(x^A)^r(x^B)^s\in Z(G)
\]

for every \(x\in G\).

Therefore every element of \(G/Z(G)\) has order dividing \(2\). But, as we have already seen, every group of exponent \(2\) is abelian. Hence \(G/Z(G)\) is abelian, so

\[
[G,G]\subseteq Z(G).
\]

Thus \(G\) has nilpotency class at most \(2\), and commutators are central.

Now in any group of class at most \(2\),

\[
(xy)^k=x^ky^k[y,x]^{\binom{k}{2}}.
\]

Since the \(m\)-th power map is a homomorphism, \((xy)^m=x^my^m\), and therefore

\[
[y,x]^{\binom m2}=1.
\]

Similarly,

\[
[y,x]^{\binom n2}=1.
\]

But


\(\gcd\left(\frac{m(m-1)}{2},\frac{n(n-1)}{2}\right)=1.
\)

Thus every commutator \([y,x]\) has order dividing two coprime integers, and so \([y,x]=1\). Hence

\[
\boxed{G\text{ is abelian}.}
\]

The numerical hypothesis first forces every square to become central; consequently \(G/Z(G)\) has exponent \(2\), and exponent \(2\) immediately forces commutativity.

## 3. Index \(2\): again, there is no room to move

Suppose \(H\leq G\) and \([G:H]=2\). There are only two left cosets: \(H\) itself and its complement. The same is true for right cosets. Hence for \(g\notin H\),

\[
gH=G\setminus H=Hg,
\]

and therefore \(H\triangleleft G\).

So every subgroup of index \(2\) is automatically normal. Equivalently, such a subgroup is the kernel of a homomorphism \(G\to C_2\). The familiar example is the sign map \(\operatorname{sgn}:S_n\to C_2\), whose kernel is \(A_n\).

Again, the number \(2\) leaves almost no freedom.

## 3. Involutions and parity

An element \(t\neq 1\) satisfying \(t^2=1\) is called an **involution**.

If an involution \(\sigma\) acts on a finite set \(X\), every orbit has size \(1\) or \(2\). Hence

\[
|X|\equiv |\operatorname{Fix}(\sigma)|\pmod 2.
\]

Everything comes in pairs, except the fixed points.

There is a nice consequence inside a finite group. Pair each element \(g\) with \(g^{-1}\). The only elements left unpaired satisfy \(g=g^{-1}\), equivalently \(g^2=1\). Thus if \(|G|\) is even, the number of solutions to \(x^2=1\) is even. Since the identity is one such solution, the number of involutions is odd.

So every finite group of even order has an odd number of involutions.

## 4. A unique involution must be central

Suppose \(G\) has exactly one involution \(t\). For every \(g\in G\), the element \(gtg^{-1}\) is again an involution, since conjugation preserves order. By uniqueness, \(gtg^{-1}=t\), so \(t\in Z(G)\).

Thus a tiny hypothesis — the uniqueness of one element of order \(2\) — forces that element to commute with the entire group.

There is another useful peculiarity. Since \(\langle t\rangle=\{1,t\}\),

\[
N_G(\langle t\rangle)=C_G(t).
\]

Indeed, if \(g\) normalizes \(\langle t\rangle\), then \(gtg^{-1}\in\langle t\rangle\). It cannot be \(1\), so it must equal \(t\).

The reason is simply that

\[
\operatorname{Aut}(C_2)=1.
\]

For an element \(x\) of order \(p>2\), an element normalizing \(\langle x\rangle\) may send \(x\) to \(x^a\) for some \(a\in(\mathbf Z/p\mathbf Z)^\times\). Thus normalizing and centralizing need not coincide.

## 5. A fixed-point-free automorphism of order \(2\)

Now suppose \(G\) is finite and \(\sigma\in\operatorname{Aut}(G)\) satisfies \(\sigma^2=1\). Assume moreover that \(\sigma\) has no nontrivial fixed points:

\[
\sigma(g)=g \Longrightarrow g=1.
\]

Then something surprisingly strong happens: \(G\) is abelian and has odd order.

Define \(f:G\to G\) by \(f(x)=x^{-1}\sigma(x)\). If \(f(x)=f(y)\), then

\[
x^{-1}\sigma(x)=y^{-1}\sigma(y),
\]

which rearranges to \(yx^{-1}=\sigma(yx^{-1})\). Since \(\sigma\) has no nontrivial fixed points, \(yx^{-1}=1\), so \(x=y\). Thus \(f\) is injective, and because \(G\) is finite, it is surjective.

Therefore every \(g\in G\) can be written as \(g=x^{-1}\sigma(x)\). Applying \(\sigma\),

\[
\sigma(g)=\sigma(x)^{-1}x=(x^{-1}\sigma(x))^{-1}=g^{-1}.
\]

So \(\sigma\) is simply inversion. But inversion is an automorphism only in an abelian group, since

\[
(xy)^{-1}=y^{-1}x^{-1}
\]

must equal \(x^{-1}y^{-1}\). Hence \(xy=yx\).

Moreover \(G\) cannot contain an involution \(t\), because then \(\sigma(t)=t^{-1}=t\), contradicting fixed-point-freeness. By Cauchy's theorem, \(|G|\) must therefore be odd.

So

\[
\boxed{\text{A finite group with a fixed-point-free automorphism of order }2
\text{ is abelian of odd order.}}
\]

## 6. Replace \(2\) by a prime \(p\)

At this point a natural question is: what if the automorphism has prime order \(p\) instead?

For \(p=2\), the proof above is elementary and gives the very strong conclusion that \(G\) is abelian. For arbitrary prime \(p\), one encounters a deep theorem of Thompson:

\[
\boxed{\text{A finite group admitting a fixed-point-free automorphism of prime order is nilpotent.}}
\]

The contrast is striking. The case \(p=2\) collapses to a short argument; replacing \(2\) by an arbitrary prime leads to serious finite-group theory.

This is perhaps one of the best examples of why \(2\) behaves differently.

## 7. Two involutions already generate something special

Suppose \(a^2=b^2=1\) and set \(r=ab\). Then

\[
ara=a(ab)a=ba=(ab)^{-1}=r^{-1}.
\]

Thus \(\langle a,b\rangle\) is dihedral in nature: two involutions can never interact completely arbitrarily.

This innocent observation becomes important when one starts counting involutions in finite groups. It is one of the ideas lurking behind the Brauer--Fowler theorem.

## 8. Brauer--Fowler: one involution can control a whole simple group

Let \(G\) be a finite nonabelian simple group and let \(t\in G\) be an involution. Write

\[
c=|C_G(t)|.
\]

Brauer--Fowler says, in particular, that \(|G|\) is bounded in terms of \(c\). The exact numerical bound is less important here than the philosophy:

\[
\boxed{\text{information about }C_G(t)\text{ gives global information about }G.}
\]

Why should the elements commuting with one involution tell us so much about the entire group?

Let \(N=|G|\) and let \(M\) be the total number of involutions in \(G\). Since the conjugacy class of \(t\) has size

\[
|t^G|=[G:C_G(t)]=\frac{N}{c},
\]

we have \(M\geq N/c\). Thus a small involution centralizer forces the existence of many involutions.

The heart of the Brauer--Fowler argument is a counting result showing that sufficiently many involutions force some nonidentity element \(x\) to have a small conjugacy class, roughly of size

\[
|x^G|<\left(\frac{N}{M}\right)^2.
\]

Since \(N/M\leq c\), this gives \(|x^G|<c^2\). But

\[
|x^G|=[G:C_G(x)],
\]

so \(G\) has a proper subgroup \(H=C_G(x)\) of bounded index.

Now let \(G\) act on the cosets \(G/H\). We obtain a homomorphism

\[
G\longrightarrow S_{[G:H]}.
\]

Because \(G\) is simple and the action is nontrivial, the kernel is trivial. Thus \(G\) embeds into a symmetric group of bounded degree, which in turn bounds \(|G|\).

So the broad mechanism is

\[
\text{small }C_G(t)
\Longrightarrow
\text{many involutions}
\Longrightarrow
\text{small conjugacy class}
\Longrightarrow
\text{small-index subgroup}
\Longrightarrow
\text{bounded }|G|.
\]

The clever part lies in the counting step. The fact that pairs of involutions generate such tightly controlled subgroups is one reason the argument can work at all.

## 9. Why involutions become unavoidable in simple groups

There is one final theorem worth mentioning. The Feit--Thompson Odd Order Theorem says

\[
|G|\text{ odd}\Longrightarrow G\text{ solvable}.
\]

Consequently, every finite nonabelian simple group has even order. By Cauchy's theorem, every such group therefore contains an involution.

So

\[
\text{finite nonabelian simple group}
\Longrightarrow
\text{even order}
\Longrightarrow
\text{involutions exist}.
\]

Involutions are therefore not merely convenient objects that happen to occur in some examples. If one wants to understand finite simple groups, they are unavoidable.

This helps explain why centralizers of involutions became so important in finite-group theory and why \(2\)-local analysis played such a large role in the subject.

## So why does \(2\) keep appearing?

We began with the innocent identity \(x^2=1\), which immediately forced commutativity. Index \(2\) forced normality. Involutions produced parity arguments, a unique involution became central, and \(N_G(\langle t\rangle)=C_G(t)\) simply because \(C_2\) has no nontrivial automorphisms.

Then a fixed-point-free automorphism of order \(2\) forced an entire finite group to be abelian, while replacing \(2\) by a general prime led to Thompson's theorem. Finally, involutions led us toward Brauer--Fowler and the structural study of finite simple groups.

Perhaps the common theme is that \(2\) sits at a peculiar boundary: it is large enough for nontrivial symmetry to exist, but small enough that there is often almost no room for that symmetry to move.

There are only two cosets. An involution is its own inverse. A \(C_2\)-orbit has only one or two points. The group \(C_2\) has no nontrivial automorphisms. Two involutions already generate dihedral behaviour.

Again and again, the number \(2\) leaves a group with very few choices — and in group theory, having very few choices often means having a lot of structure.

We began with \(x^2=1\), and somehow ended up at the doorstep of the theory of finite simple groups.