# Caesar Cipher in Cryptography

## Department of Information Technology  
**Sreenidhi Institute of Science and Technology**  
(An Autonomous Institution approved by UGC and Affiliated to JNTUH)  
Yamnampet, Ghatkesar, Hyderabad – 501 301.

## Project Overview
This project involves the implementation of the Caesar Cipher algorithm, one of the oldest and simplest encryption techniques in cryptography. The aim is to understand the basic principles of encryption, and how simple modifications can enhance the security of this classical algorithm.

## Student Details
- **Name:** Rahul Teja B
- **Roll Number:** 18311A12J8
- **Branch:** IT-D

## Abstract
The Caesar Cipher algorithm is a basic substitution cipher where each letter in the plaintext is replaced by a letter some fixed number of positions down the alphabet. Despite being easy to implement and fast to execute, the algorithm is insecure due to its predictability. This project proposes an enhancement using a simple Diffie-Hellman key exchange scenario to derive a shared key, which is then used to encrypt the message with additional security. The key obtained is multiplied with the character’s position and then modulated with 26 to determine the ciphered character, thus adding a layer of complexity without significantly increasing execution time.

## Introduction
The Caesar Cipher, attributed to Julius Caesar, shifts each character of the plaintext by a fixed number down the alphabet. The technique is a type of substitution cipher and can be mathematically represented using modular arithmetic. The project explores this technique and demonstrates how it can be enhanced for better security.

## Program Description
The program is written in Python and implements the Caesar Cipher encryption technique. The code encrypts both uppercase and lowercase characters based on a given shift value.

### Python Code:
```python
def encrypt(text, s):
    result = ""
    for i in range(len(text)):
        char = text[i]
        if char.isupper():
            result += chr((ord(char) + s - 65) % 26 + 65)
        else:
            result += chr((ord(char) + s - 97) % 26 + 97)
    return result

# Example usage
text = "ATTACKATONCE"
s = 4
print("Text : " + text)
print("Shift : " + str(s))
print("Cipher: " + encrypt(text, s))
```

## Output
When executed, the program will encrypt the given text "ATTACKATONCE" with a shift value of 4, producing the ciphered text.

### Example Output:
```
Text : ATTACKATONCE
Shift : 4
Cipher: EXXEGOEXSRGI
```

## Conclusion
The Caesar Cipher is a foundational algorithm in the field of cryptography. This project enhances the algorithm by incorporating a key derived from the Diffie-Hellman exchange, making the encryption process more secure while retaining the algorithm's simplicity and speed.
