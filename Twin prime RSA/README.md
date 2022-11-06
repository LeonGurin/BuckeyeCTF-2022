# Twin prime RSA

**xxx points**

Real winners use twin primes

*Given:* [chall.py]()

___

In this RSA challenge the gimmick is that the 2 chosen prime numbers are:

```python
    p = cun.getPrime(1024)
    q = p + 2
```

and of course we could exploit it.

If `p` was equal to `q` we could just take the square root of `n` and plug everything in an RSA calculator and be done, and so that's what I basically did with 2 iterations of trial and error.

I found some `StackOverflow` code for square root of large number and copied it.

*Note:* people said that the function was not spot on because it converted to integers, so I tried multiplying:

* `(p+1) * (p+1) == n`
* `p * (p+2) == n`

and as it turned out the second iteration worked.

Plugging into dcode.fr's RSA calculator we get:

>buckeye{B3_TH3R3_OR_B3_SQU4R3__abcdefghijklmonpqrstuvwxyz__0123456789}
