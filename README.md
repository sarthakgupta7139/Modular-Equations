# Modular-Equations
Python Program for Number of solutions to Modular Equations
Given A and B, the task is to find the number of possible values that X can take such that the given modular equation (A mod X) = B holds good. Here, X is also called a solution of the modular equation.

Examples:

Input : A = 26, B = 2
Output : 6
Explanation
X can be equal to any of {3, 4, 6, 8,
12, 24} as A modulus any of these values
equals 2 i. e., (26 mod 3) = (26 mod 4) 
= (26 mod 6) = (26 mod 8) =Output:2 

Input : 21 5
Output : 2
Explanation
X can be equal to any of {8, 16} as A modulus 
any of these values equals 5 i.e. (21 mod 
8) = (21 mod 16) = 5
If we carefully analyze the equation A mod X = B its easy to note that if (A = B) then there are infinitely many values greater than A that X can take. In the Case when (A < B), there cannot be any possible value of X for which the modular equation holds. So the only case we are left to investigate is when (A > B).So now we focus on this case in depth.

Now, in this case we can use a well known relation i.e.

Dividend = Divisor * Quotient + Remainder
We are looking for all possible X i.e. Divisors given A i.e Dividend and B i.e., remainder. So,

We can say,
A = X * Quotient + B

Let Quotient be represented as Y
∴ A = X * Y + B
A - B = X * Y

∴ To get integral values of Y, 
we need to take all X such that X divides (A - B)

∴ X is a divisor of (A - B)
So, the problem reduces to finding the divisors of (A – B) and the number of such divisors is the possible values X can take.
But as we know A mod X would result in values from (0 to X – 1) we must take all such X such that X > B.

Thus, we can conclude by saying that the number of divisors of (A – B) greater than B, are the all possible values X can take to satisfy A mod X = B
