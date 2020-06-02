# Algebraic model for Swaps

Let be 

`A={ <spotQuantity, [ (date(i),quantity(i) ] i=1,..N> \ N=0,1,...; spotQuantity is a real number, date(i) is a date, quantity(i) is real and if N=0 the second element of the pair is an empty list [] }`

and the composition operation `+` such that:

    a=<q, [ (d(i),q(i)) ],i=1..N>
    b=<p, [ (f(j),p(j)) ],j=1..M>

    a + b = c = <r, [ g(k),r(k) ],k=1..K>`

verifying:

1. `g(k)=q(i)+p(j)` for `d(i)=f(j)`, and in this case `g(k)=d(i)=f(j)`
2. `r(k)<r(k+1)` for all k=1..K
3. There is at least one `d(i)` or `f(j)` such that `d(i)=g(k)` (in this case
   `r(k)=q(i)`) or `f(j)=g(k)` (in this case `r(k)=p(j)`)
4. `K = N + M - card{ d(i)=f(j) i,j }`


## Monoid
Under the previous definition, the pair (A,+) is a Monoid, and its zero
is `<0, []>`.
