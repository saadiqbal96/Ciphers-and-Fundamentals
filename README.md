# Ciphers and Fundamentals (Work in Progress...)

# LESSON 1

**Encryption**

Encryption was introduced in order to communicate safely over the Internet.

*What encryption is*: plaintext (which basically contains the private information that needs to be sent confidentially) is encrypted and then made unreadable (cypher text) turning it into a string of numbers/letters, and can only be read as plaintext data again by those who have the decryption key.

There are two main ways of communicating through encryption:
- Private (symmetric): in this communication both the sender and receiver use one shared decryption key.
- Public (asymmetric): the sender encrypts plaintext using the receiver public key (lock) in this form of communication the receiver who is identified by the public key is the only one who knows the private key (unlock) and can use it to decrypt the data.

**Symmetric Encryption:**
As said, symmetric encryption uses a single shared key to encrypt and decrypt data. Both Alice and Bob must possess the same secret key before they can communicate securely.
For example, Alice encrypts a message using a shared key and sends it to Bob. Bob then uses that same key to decrypt and read the message.
The main advantage of symmetric encryption is that it is fast and efficient, making it suitable for encrypting large amounts of data.
*Examples:* AES, DES..

**Asymmetric Encryption:**
Asymmetric encryption uses a pair of keys: a public key and a private key.
Bob shares his public key with Alice while keeping his private key secret. Alice encrypts a message using Bob's public key, and only Bob can decrypt it using his private key.
This removes the need to share a secret key beforehand and makes secure communication possible between parties who have never met.
*Examples:* RSA, ECC..

**Alice and Bob Example**
1. Bob generates a public and private key pair.
2. Bob shares his public key with Alice.
3. Alice encrypts a message using Bob's public key.
4. Alice send the encrypted message to Bob.
5. Bob decrypts the message using his private key.

*Only Bob can read the message because only Bob possesses the private key.*

**Hashing**

Hashing is the process of converting data into a fixed-length value called a hash. Unlike encryption, hashing is a *one way process*, meaning the original data cannot be recovered from the hash.

A useful way to think of hashing is as a digital fingerprint. If the original data changes, even by a single character, the resulting hash will be completely different.

**Alice and Bob Example**
1. Alice writes a message: Hello Bob.
2. Alice generates a hash of the message: A1B2C3D4..
3. Alice sends both the message and the hash to Bob.
4. When Bob receives the message, he generates a hash of the received message.
5. If Bob's calculated hash matches Alice's hash, he knows the message has not been altered during transmission.

If the message was changed to: Hello B0b, the hash would be completely different, indicating that the data has been modified. 

**Key Point**

Hashing is used to verify integrity, not confidentiality.
- Encryption hides data
- Hashing checks whether data has been changed.

*Examples:* SHA-256, SHA-3..

# LESSON 2

**Main Topics**
- Symmetric (Secret Key) Encryption.
- Stream and Block Ciphers.
- Salting Techniques.
- Hash Functions.
- Password Security.
- HMAC Authentication.
- One-Time Passwords (OTP).

**Key Goal**

Understand how data is encrypted, stored securely, and verified for integrity.

**Symmetric Key Encryption**
- Same key used for encryption and decryption.
- Fast and efficient.
- Suitable for large amounts of data.

**Common Algorithms**

*Modern* 
- AES (Advanced Encryption Standard)
- AES-128.
- AES-192.
- AES-256.

*Legacy*
- DES (Data Encryption Standard).
- 3DES (Triple DES).
- Blowfish.
- RC4 (deprecated).

*Typical Uses*
- VPNs.
- File Encryption.
- Disk Encryption.
- Secure Communications.
