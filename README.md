# paramSOS
A simple Maple program for expressing 3-variable symmetric polynomials of degree six as Sum of Squares (SOS) form.

This work will be helpful for students (or even researchers) interested in Maths and assists them in solving problems, especially algebraic inequalities.
### What can this program do?
Let $F\left(a,b,c \right)$ be a non-negative symmetric polynomials of three real variables $(a,b,c)$ such that $\text{deg}(F)=6$ and $F(a,a,a) \equiv 0$. This program allows to express $F(a,b,c)$ as sum of some squares, if it is possible.
### Requirements:
* Maple 17 installed, or later versions.
### Usages:
1. On the Maple's worksheet interface, read the script file, for example: ```> read "F:/Maple/scripts/paramSOS.txt"```.
2. Define your polynomial, for example: ```> f := a^6+b^6+c^6-a*b*c*(a+b+c)```.
  $$f:=a^6+b^6+c^6-abc\left(a^3+b^3+c^3\right)$$
3. ```getSOS()``` function needs a parameter as the second input, which is nothing just the way the program works. To obtain this parameter, use the ```getParam()``` function: ```> getParam(f)```. The result would display the range where this parameter could belong to. In this case, we have: \
 $$\{-1.619258506 \le x, x \le -0.2484229730\}$$
4. Take $x=-1$ as an input option: ```> getSOS(f, -1)```. It turns out:
 $$\frac{1}{72}(a-b)^2\left(3a^2+7ab+3ac+3b^2+3bc-c^2 \right)^2+\frac{1}{72}(b-c)^2(-a^2+3ab+3ac+3b^2+7bc+3c^2)^2 +\frac{1}{72}(c-a)^2(3a^2+3ab+7ac-b^2+3bc+3c^2)^2+\frac{5}{54}(a-b)^2(ab-c^2)^2+\frac{5}{54}(b-c)^2(-a^2+bc)^2+\frac{5}{54}(c-a)^2(ac-b^2)^2+ \frac{1}{432}(18a^3-7a^2b-7a^2c-7ab^2-12abc-7ac^2+18b^3-7b^2c-7bc^2+18c^3)^2+\frac{49}{144}(b-c)^2(-c+a)^2(a-b)^2$$
This is what we desired.

Please refer to the attached [PDF](https://github.com/duong-db/paramSOS/blob/main/pdf/paramSOS-A%20demo%20with%20examples.pdf) file for additional information and examples. \
Have an enjoy! 😊
