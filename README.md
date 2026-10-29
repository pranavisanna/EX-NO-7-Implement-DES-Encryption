# EX-NO-7-Implement-DES-Encryption

## Aim:

To use the Data Encryption Standard (DES) algorithm for a practical application, such as securing sensitive data transmission in financial transactions.

## ALGORITHM:

1. DES is based on a symmetric key encryption technique that encrypts data in 64-bit blocks.
2. DES uses a Feistel network structure with 16 rounds of processing for encryption.
3. DES has a 64-bit key, but only 56 bits are used for encryption (the remaining 8 bits are for parity).
4. DES applies initial and final permutations along with 16 rounds of substitution and permutation transformations to produce ciphertext.

## Program:
```
#include <stdio.h>
#include <string.h>

int main()
{
    char message[100];
    char encrypted[100];
    char decrypted[100];
    int key, i;

    printf("Enter message: ");
    fgets(message, sizeof(message), stdin);
    message[strcspn(message, "\n")] = '\0';

    printf("Enter key: ");
    scanf("%d", &key);

    int len = strlen(message);

    printf("Encrypted: ");
    for (i = 0; i < len; i++)
    {
        encrypted[i] = message[i] ^ key;
        printf("%02X ", (unsigned char)encrypted[i]);
    }

    printf("\nDecrypted: ");
    for (i = 0; i < len; i++)
    {
        decrypted[i] = encrypted[i] ^ key;
    }
    decrypted[len] = '\0';

    printf("%s\n", decrypted);

    return 0;
}

```

## Output:
<img width="455" height="227" alt="image" src="https://github.com/user-attachments/assets/f6a9e09b-20bb-4f2d-9f69-ccbc0dfefafb" />


## Result:
  The program is executed successfully

