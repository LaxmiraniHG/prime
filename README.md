#include <stdio.h>
#include <math.h>{
  int first = 0, second = 1, next;
    printf("Fibonacci Series: ");
    for (int i = 0; i < n; i++) {
        if (i == 0) {
            printf("%d ", first);
        } else if (i == 1) {
            printf("%d ", second);
        } else {
            next = first + second;
            first = second;
            second = next;
            printf("%d ", next);
        }
    }
    printf("\n");
}
int isPrime(int num) {
    if (num <= 1) return 0; // 0 and 1 are not prime
    for (int i = 2; i <= sqrt(num); i++) {
        if (num % i == 0) {
            return 0; // Not prime
        }
    }
    return 1; // Prime
}
long long powerOfXtoX(int x) {
    return pow(x, x);
}

int main() {
    int n, x;
    printf("Enter the number of terms for Fibonacci series: ");
    scanf("%d", &n);
    printFibonacci(n);
    
    printf("Enter a number to check if it's prime: ");
    scanf("%d", &n);
    if (isPrime(n)) {
        printf("%d is a prime number.\n", n);
    } else {
        printf("%d is not a prime number.\n", n);
    }

    printf("Enter a number to calculate x^x: ");
    scanf("%d", &x);
    printf("%d^%d = %lld\n", x, x, powerOfXtoX(x));

    return 0;
}




