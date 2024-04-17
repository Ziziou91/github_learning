# github_learning

## Secure Shell protocol (SSH)

The Secure Shell Protocol (SSH) is a network protocol for operating network services securely over an unsecured network. Popular applications for SSH are remote login and CLI execution.

### Public Key Authentication

The public key authentication method is one of the most popular applications of SSH. The idea is to have a **cryptographic key pair - public key and private key** - and configure the public key on a server to authorize access and grant anyone who has a copy of the private key access to the server. The keys used for authentication are called **SSH keys**. 

Public key authentication is also used with smartcards, such as the CAC and PIV cards used by US government.

![Diagram showing how public key authentication works using ssh](https://www.ibm.com/support/pages/system/files/inline-images/public_private_keys.png)

### SSH keygen
````bash
ssh-keygen -t rsa -b 4096 -C your_email@example.com
````
where:
- -t -> Specifices the type of key to to make. possible values are
  - “dsa”
  - “ecdsa”
  - “ecdsa-sk”
  - “ed25519”
  - “ed25519-sk”
  - “rsa”.
- -b -> Specifies the number of bits in the key to create. For RSA keys, the minimum size is 1024 bits and the default is 3072 bits.
- -C -> Comment

[SSH Keys - Linux programming interface manual](https://man7.org/linux/man-pages/man1/ssh-keygen.1.html)
