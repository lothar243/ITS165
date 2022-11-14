# CIA Triad

## Confidentiality

Information is safe from accidental or intential disclosure

## Integrity

Information is safe from accidental or intentional modification or alteration

## Availability

Information is available to authorized users when needed

What are some examples of a breach of each of the three parts?

# Protecting each attack surface

## Physical

Locked doors, security guards, safe enclosures

Offline attacks, cold-boot attack

## Network

Secured WIFI, secured network ports, firewalls

Man-in-the middle, session highjacking

## Operating System

Patching, good configuration

https://www.crowdstrike.com/cybersecurity-101/malware/types-of-malware/


## Application

Input validation, authentication

Code injection, authorization bypass

## Social

User awareness training, separation of duties - "check and balances"

Phishing, impersonation


# Encryption

Can provide both confidentiality and integrity

### Symmetric Encryption

Example: AES

### Asymmetric Encryption

Example: RSA

### Block Ciphers

Example: ECB, CBC

### Stream Cipher

Example RC4

### Hash functions

Message digest

Example: MD5, SHA1, SHA256

### Message-authentication code (MAC)

Uses a hashing algorithm and a secret key to verify authentication

Both parties share the same key (not good for public verification)

Anyone that can verify authenticity can also create the message

### Digital signatures

Take a hash of the message and encrypt it with a private key

Other people can indepently take a hash of the message and decrypt your signature - these should match when compared

This provides non-repudiation (only the person with the private key could have made the signature)

### Key Distribution

Trusted Certificate Authorities (CAs) provide digital certificates, vouching that certain public keys are correct

# User Authentication

Passwords, other factors of authentication (biometrics, specialized apps, hardware tokens)

## Storing passwords

Plain text is not good  
Hashed passwords are still not great  
Salted hashed passwords are what is used  

If someone obtains the SAM or shadow file, they can perform an offline attack to attempt to crack passwords

## How do you verify a correct password over a network without transmitting it?

Send it plaintext?
Send a hashed password?
Server provides a challenge, only transmit H(pw, ch) - essentially a one-time password

# Defense in depth

All security can be overcome. Use multiple layers to improve security

- Security policies should be in place, and followed
- Periodic penetration testing/security audits
- Don't rely on security through obscurity
