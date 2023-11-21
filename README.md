<p align="center"><img src="/assets/logo-repositioned.svg" width="160"></p>

<br>


## How lattices are used in encryption

Bob wants to send a message to Alice. In this encryption process, Alice creates two sets of basis vectors: a "good basis" and a "bad basis." Both of these bases need to define the same lattice structure. The "good basis" consists of vectors that are nearly perpendicular, while the "bad basis" comprises vectors that are nearly parallel.

The reason for having these two bases is that one serves as a private key, while the other is a public key. The "bad basis" is designed to make it harder to solve the ["shortest vector problem,"](https://en.wikipedia.org/wiki/Lattice_problem#Shortest_vector_problem_(SVP)) a key challenge in lattice-based cryptography. In contrast, the "good basis" allows for a more efficient solution to this problem. The idea is that even quantum computers would struggle to solve this problem effectively. Therefore, encoding with the public key (the "bad basis") becomes extremely challenging without access to the private key (the "good basis").

Here's how the process works: Once Bob has Alice's public key (the "bad basis"), he can locate a point on the lattice that represents his message using various methods. He knows the path to this point within the lattice, so he shifts it slightly and sends this new point to Alice. She can then use her private key (the "good basis") to run the "shortest vector problem" and recover the original point representing Bob's message. This approach results in post-quantum encryption, which is highly secure against quantum computing attacks.

## Key structure example
In the context of post-quantum encryption, a lattice is a mathematical structure used for cryptographic purposes. It involves complex geometric shapes and mathematical equations. Lattice-based cryptography relies on the hardness of certain lattice problems to create encryption schemes that are believed to be secure against attacks by quantum computers. This makes lattice-based encryption a promising candidate for ensuring data security in a post-quantum world.

![](/assets/basis-vectors.png) \
<sub>This is an example of a "good basis" and "bad basis" within a lattice structure.</sub>

## Possible Solutions

Upon initial consideration, it occurred to me that if the initial foundation proves challenging to work with, why not explore the option of identifying a starting basis that is closer to the origin and more perpendicular? This, in itself, presents a complex challenge known as the ["closest vector problem."](https://en.wikipedia.org/wiki/Lattice_problem#Closest_vector_problem_(CVP))
