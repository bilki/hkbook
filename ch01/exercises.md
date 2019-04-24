Chapter 1 exercises
===

1. b) λxy.xz = λmn.mz because x = m, y = n

2. c) λxy.xxy = λa.(λb.aab) because x = a, y = b

3. b) λxyz.zx = λtos.st because x = t, z = s

4. Combinators
    * λx.xxx = true because no free variables
    * λxy.zx = false because z
    * λxyz.xy(zx) = true
    * λxyz.xy(zxy) = true
    * λxy.xy(zxy) = false because z

5. Normal form or divergence
    * λx.xxx = normal form
    * (λz.zz)(λy.yy) = (λy.yy)(λy.yy) = ... = divergence
    * (λx.xxx)z = zzz = normal form

6. Beta reduce
    1. (λabc.cba)zz(λwv.w)
        * (λbc.cbz)z(λwv.w)
        * (λc.czz)(λwv.w)
        * (λwv.w)zz
        * (λv.z)z
        * z
    2. (λx.λy.xyy)(λa.a)b
        * (λy.(λa.a)yy)b
        * (λa.a)bb
        * bb
    3. (λy.y)(λx.xx)(λz.zq)
        * (λx.xx)(λz.zq)
        * (λz.zq)(λz.zq)
        * (λz.zq)q
        * qq
    4. (λz.z)(λz.zz)(λz.zy)
        * yy (alpha equivalent to 3)
    5. (λx.λy.xyy)(λy.y)y
        * yy  (alpha equivalent to 2)
    6. (λa.aa)(λb.ba)c
        * (λb.ba)(λb.ba)c
        * (λb.ba)ac
        * aac
    7. (λxyz.xz(yz))(λx.z1)(λx.a)
        * (λyz.(λx.z1)z(yz))(λx.a)
        * (λz.(λx.z1)z((λx.a)z))
        * λz.z1a