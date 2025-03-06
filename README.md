# tenseal-homomorphic-encryption
A simple, barebones implementation of Homomorphic Encryption

This repository demonstrates a simple example of homomorphic encryption using the TenSEAL library in Python. 

## Description

Homomorphic encryption allows computations to be performed on encrypted data without decrypting it first. This example showcases basic arithmetic operations (addition and multiplication) on encrypted numbers using the BFV scheme provided by TenSEAL.

## Requirements

- Python 3.6 or higher
- TenSEAL library

## Explanation

The code performs the following steps:

1. **Context Creation:** A TenSEAL context is created with the BFV scheme, specifying the polynomial modulus degree, plain modulus, and coefficient modulus bit sizes. Galois and relinearization keys are generated for ciphertext operations.

2. **Encryption:** Two plain numbers (5 and 7) are encrypted using the context.

3. **Encrypted Operations:** Addition and multiplication are performed on the encrypted numbers.

4. **Decryption:** The results of the encrypted operations are decrypted using the secret key.

5. **Output:** The decrypted results are printed to the console.

## Note

- The `plain_modulus` parameter should be chosen according to the range of values you expect to work with.
- The `context.make_context_public()` line is commented out to keep the secret key for decryption. Remove the comment if you need to share the context for computations by other parties without revealing the secret key.

## Contributing

Feel free to open issues or pull requests for improvements or suggestions.
