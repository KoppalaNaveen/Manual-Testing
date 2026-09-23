# 1.Write a Python program which accepts a sequence of comma separated 4 digit
binary numbers as its input and then check whether they are divisible by 5 or not.
The numbers that are divisible by 5 are to be printed in a comma separated
sequence.
Example:
0100,0011,1010,1001
Then the output should be:
1010


# code 

```
def check(s):
    r = []
    for x in s:
        if int(x, 2) % 5 == 0:
            r.append(x)
    return ",".join(r)
s = input().split(",")
print(check(s))
```
# 2.Write a Python program that accepts a sentence and calculate the number of
letters and digits.
Suppose the following input is supplied to the program:
hello world! 123
Then, the output should be:
LETTERS 10
DIGITS 3

# Code

```
def count(s):
    letters = 0
    digits = 0
    for x in s:
        if x.isalpha():
            letters += 1
        elif x.isdigit():
            digits += 1
    print("LETTERS", letters)
    print("DIGITS", digits)
s = input()
count(s)
```

# 3. Write a program which can compute the factorial of a given numbers.The
results should be printed in a comma-separated sequence on a single
line.Suppose the following input is supplied to the program:8
Then, the output should be:40320

# Code

```
def fact(n):
    factorial = 1
    for i in range(1, n + 1):
        factorial *= i
    return factorial
s = input().split(",")
r = []
for x in s:
    r.append(str(fact(int(x))))
print(",".join(r))
```
