# GCD 함수

```cpp
ll gcd(ll a, ll b) {
    if (b == 0) return a;
    return gcd(b, a % b);
}
```

또한, lcm은 $a * b / gcd(a, b)$.

## GCD 함수의 성질

- $a$와 $b$의 모든 공약수는 $gcd(a, b)$의 약수이다.
- $gcd(a, b)$는 ($a, b \neq 0$일 때) $ap + bq$ 꼴로 표현될 수 있는 가장 작은 양의 정수 $d$로 정의된다.
- $gcd(a, 0) = |a|$ ($a \neq 0$)이다. $a$의 가장 큰 약수가 $|a|$이고, 0은 모든 수로 나누어 떨어지기 때문이다.
- $a$가 $bc$를 나누고, $gcd(a, b) = d$면, $a \div d$는 $c$를 나눈다.
- 임의의 정수 $m$에 대해, $gcd(a, b) = gcd(a + md, b)$이다.
- $m$이 $a$와 $b$의 양의 공약수라면, $gcd(a \div m, b \div m) = gcd(a, b) \div m$이다.
- $a_1, a_2$가 서로소일 때, $gcd(a_1 \times a_2, b) = gcd(a_1, b) \times gcd(a_2, b)$이다.
- 최대공약수는 교환 법칙을 만족한다. 또한 결합 법칙도 성립한다.
- $gcd(a, b) \times lcm(a, b) = |a \times b|$이다.
- $gcd(a, lcm(b, c)) = lcm(gcd(a, b), gcd(a, c))$이다.
- $lcm(a, gcd(b, c)) = gcd(lcm(a, b), lcm(a, c))$이다.
- 좌표평면에서, $gcd(a, b)$는 $(0, 0)$과 $(a, b)$를 잇는 선분 위의 정수 격자점들 사이의 선분 개수로 해석할 수 있다.
- $a, b$가 둘 다 0이 아닌 음의 정수일 때, $gcd(n ^ a - 1, n ^ b - 1) = n ^ {gcd(a, b)} - 1$이다.
- $gcd(a, b)$는 $φ(k)$를 모두 합한 값이다. 즉, $gcd(a, b) = Σ φ(k)$이다. $k$는 $a$와 $b$의 모든 공약수이다.
