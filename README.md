# Ex-6-Pseudorandom-Number-Generation
## Aim:
To implement Pseudorandom Number Generation using the standard library functions in C.
## Algorithm:
1.    Seed the random number generator using srand() to initialize it with a starting value.
2.    Generate pseudorandom numbers using rand().
3.    To ensure different results on each execution, seed srand() with a dynamic value like the current time (time(NULL)).
4.    Use modulo operation to limit the range of generated numbers.
## Program:
```c
#include <stdio.h>
//Constants for LCG
#define A 1664525
#define C 1013904223
#define M 4294967296 // 2^32

//Linear Congruential Generator function
unsigned int lcg(unsigned int seed) {
    return (A * seed + C) % M;
}

int main() {
    unsigned int seed;
    int n, i;
    printf("*Pseudorandom number generator*\n\n");
    printf("Enter the seed value: ");
    scanf("%u", &seed);
    printf("Enter how many random numbers to generate: ");
    scanf("%d", &n);
    printf("Random numbers:\n");
    for (i = 0; i < n; i++) {
        seed = lcg(seed);
        printf("%u\n", seed);
    }
    return 0;
}
```
## output:
![Screenshot 2024-10-10 090715](https://github.com/user-attachments/assets/65f728a7-e4cc-4c2d-bebe-0ce4c95c3c48)
## result:
Thus, the pseudorandom number generation was successfully implemented using the standard library functions srand() and rand().

 
