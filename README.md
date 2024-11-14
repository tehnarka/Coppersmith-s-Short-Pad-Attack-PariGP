# Paricopper

## Description
This script implements Coppersmith's algorithm to find small integer roots of polynomials modulo an integer. It is designed for cryptographic research, particularly in analyzing the security of cryptographic protocols.

## Key Functions
- `genpoly(N, d, eps)`: Generates a random polynomial of degree `d` with small coefficients.
- `gen_messages(N)`: Generates random messages and their corresponding encrypted values (`C1`, `C2`).
- `coppersmith_roots(f, N, X)`: Finds integer roots of the polynomial `f mod N` that are smaller than `X`.
- `fr_attack(f, C1, C2, N)`: Recovers message `M2` based on the given polynomial.
- `coppersmith_attack(C1, C2, N, X)`: Complete Coppersmith's attack to recover messages.

## Usage
1. Install PARI/GP.
2. Import the script into the PARI/GP environment.
3. Use the provided functions to generate test data and perform attacks.

## Examples
```gp
N = 82345678006271 * 102345678004883; 
X = floor(N^(1/3));
gen_messages(N);
M2 = coppersmith_attack(C1, C2, N, X);
print(M2);
