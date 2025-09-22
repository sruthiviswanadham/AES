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

void xor_encrypt_decrypt(char *input, char *key) {
    int input_len = strlen(input);
    int key_len = strlen(key);
    for (int i = 0; i < input_len; i++) {
        input[i] = input[i] ^ key[i % key_len];
    }
}

int main() {
    char message[100];
    char key[100];

    printf("Enter the message: ");
    fgets(message, sizeof(message), stdin);
    message[strcspn(message, "\n")] = '\0';

    printf("Enter the key: ");
    fgets(key, sizeof(key), stdin);
    key[strcspn(key, "\n")] = '\0';

    printf("\nOriginal text: %s\n", message);

    xor_encrypt_decrypt(message, key);
    printf("Encrypted text: %s\n", message);

    xor_encrypt_decrypt(message, key);
    printf("Decrypted text: %s\n", message);

    return 0;
}
```

# OUTPUT:
<img width="1462" height="977" alt="image" src="https://github.com/user-attachments/assets/10684dc0-3997-4d5d-b93e-1f9d1dd2de25" />


# RESULT:

The program is verified and executed successfully.
