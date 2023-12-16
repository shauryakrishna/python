### python
## practical 1 
# WAP to find the roots of a quadratic equation
     import math
     a = float(input("Enter coficient of x^2 : "))
     b = float(input("Enter coficient of x : "))
    c = float(input("Enter constant value : "))

    d = b**2 - 4*a*c
    print(d)
    if d>0:
    x1 = (-b - math.sqrt(d))/2*a
    x2 = (-b + math.sqrt(d))/2*a
    print("Root of the equation are: ",x1, "and", x2)
    else:
    print("roots are imaginary...!")
### practical 2

    # WAP to accept a number ‘n’ and

    # a) Check if ’n’ is prime
    def isPrime(n):
    is_Prime = True
    for i in range(2,n//2+1):
        if n%i==0:
            is_Prime = False
    return is_Prime

    # b. Generate all prime numbers till ‘n’
    def primeTillN(n):
    for i in range(2,n+1):
        if isPrime(i):
            print(str(i),end=", ")
    print()
    
    
    # c. Generate first ‘n’ prime numbers
    def generate_primes(n):
    primes, num = [], 2
    while len(primes) < n:
        if all(num % p != 0 for p in primes):
            primes.append(num)
        num += 1
    return primes


    num = int(input("Enter Numer: "))

    # calling to check prime
    if isPrime(num):
    print(num, "is a prime number")
    else:
    print(num,"is not a prime number")

    # calling for print prime till num    
    primeTillN(num)

    # callinf for print n prime number:
    n = int(input("Enter the number of prime numbers you want to generate: "))
    prime_numbers = generate_primes(n)
    print(f"The first {n} prime numbers are: {prime_numbers}")
