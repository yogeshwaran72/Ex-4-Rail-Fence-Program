# Ex-5 Rail-Fence-Program

# IMPLEMENTATION OF RAIL FENCE – ROW & COLUMN TRANSFORMATION TECHNIQUE
## Name: YOGESHWARAN A
## Reg.No:212223040249
# AIM:

# To write a C program to implement the rail fence transposition technique.

# DESCRIPTION:

In the rail fence cipher, the plain text is written downwards and diagonally on successive "rails" of an imaginary fence, then moving up when we reach the bottom rail. When we reach the top rail, the message is written downwards again until the whole plaintext is written out. The message is then read off in rows.

# ALGORITHM:

STEP-1: Read the Plain text.
STEP-2: Arrange the plain text in row columnar matrix format.
STEP-3: Now read the keyword depending on the number of columns of the plain text.
STEP-4: Arrange the characters of the keyword in sorted order and the corresponding columns of the plain text.
STEP-5: Read the characters row wise or column wise in the former order to get the cipher text.

# PROGRAM
```
#include <stdio.h>
#include <string.h>

int main()
{
    char plaintext[100], rail1[100], rail2[100], ciphertext[200];
    int i, j = 0, k = 0, index = 0;

    printf("Enter the Plain Text: ");
    scanf("%s", plaintext);

    /* Arrange characters alternatively in two rails */
    for (i = 0; plaintext[i] != '\0'; i++)
    {
        if (i % 2 == 0)
            rail1[j++] = plaintext[i];
        else
            rail2[k++] = plaintext[i];
    }

    rail1[j] = '\0';
    rail2[k] = '\0';

    /* Generate Cipher Text */
    for (i = 0; rail1[i] != '\0'; i++)
        ciphertext[index++] = rail1[i];

    for (i = 0; rail2[i] != '\0'; i++)
        ciphertext[index++] = rail2[i];

    ciphertext[index] = '\0';

    printf("\nRail 1      : %s", rail1);
    printf("\nRail 2      : %s", rail2);
    printf("\nCipher Text : %s\n", ciphertext);

    return 0;
}
```
# OUTPUT
<img width="1916" height="921" alt="Screenshot 2026-09-02 104222" src="https://github.com/user-attachments/assets/08454b38-f507-4cab-8dc0-c148fecb78e7" />


# RESULT
Thus, the Rail Fence Transposition technique was successfully implemented
using C language and the corresponding cipher text was obtained.
