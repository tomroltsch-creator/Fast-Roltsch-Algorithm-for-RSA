def fra_rsa(e, L):
m, k = divmod(L - e, e)
q = pow(e, -1, k)
if q > k // 2: q -= k
w = (1 - e*q) // k
u = (m + 1)*w - q
return (-u) % L
