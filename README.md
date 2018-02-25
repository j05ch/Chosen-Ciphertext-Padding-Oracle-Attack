# Chosen Ciphertext Padding Oracle Attack
A Java implementation of a chosen ciphertext padding oracle attack.

When messages are encrypted in CBC mode and then padded it is possible to use a server as a padding oracle. One chooses an own initial vector with a cipher block and alters it every time the server returns a padding error. As soon as the padding is valid the resulting byte of the block cipher can be calculated by XORing the padding with the chosen IV. Then the plaintext byte can be calculated by XORing this result with the original IV. This can be done byte by byte until the complete cipher is decrypted. For details please see the [original paper](https://www.iacr.org/cryptodb/archive/2002/EUROCRYPT/2850/2850.pdf) by Serge Vaudenay.

![example.jpg](https://github.com/j05ch/Chosen-Ciphertext-Padding-Oracle-Attack/blob/master/example.jpg)
