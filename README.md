# EX-8-ADVANCED-ENCRYPTION-STANDARD ALGORITHM
# Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

# ALGORITHM:
AES is based on a design principle known as a substitution–permutation.
AES does not use a Feistel network like DES, it uses variant of Rijndael.
It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.
AES operates on a 4 × 4 column-major order array of bytes, termed the state
# PROGRAM:
```
#include <stdio.h>
#include <string.h>

void xorC(char *in,char *k,char *out){
    for(int i=0;i<strlen(in);i++)
        out[i]=in[i]^k[i%strlen(k)];
    out[strlen(in)]=0;
}

int main(){
    char p[100],k[100],c[100],d[100];

    fgets(p,100,stdin); p[strcspn(p,"\n")]=0;
    fgets(k,100,stdin); k[strcspn(k,"\n")]=0;

    xorC(p,k,c);

    printf("Enc:");
    for(int i=0;i<strlen(c);i++)
        printf("%d ",(unsigned char)c[i]);

    xorC(c,k,d);
    printf("\nDec:%s",d);
}
```
```
212225040040
Balaji B
```

# OUTPUT:
<img width="1406" height="841" alt="image" src="https://github.com/user-attachments/assets/2257567a-f7c5-46d7-8f07-2d606c6a3c3e" />

# RESULT:


