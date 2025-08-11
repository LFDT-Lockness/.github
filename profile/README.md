<div align="center">
<img src=../assets/lockness-positive-stroke.png alt=Lockness width=60% />
<p></p>
<p>
Part of the <b>Linux Foundation's Decentralized Trust</b> initiative.
</p>
<p>
Our mission is to make <b>Multi-Party Computation (MPC)</b> and <b>Threshold Signature Schemes (TSS)</b> simple, safe, and accessible for both implementors and end-users.
</p>
</div>

## What We Do

Modern cryptography, especially in distributed systems, can be notoriously difficult to implement
correctly. Lockness provides a suite of robust, audited, and easy-to-use libraries to build and
deploy advanced cryptographic protocols.

We focus on creating foundational building blocks that are secure, composable, and
developer-friendly.

## The Core: A [`round-based`] Framework

At the heart of our project is the [`round-based`] framework, a novel approach to implementing MPC
protocols. It's the foundation upon which our TSS protocols are built. It simplifies development by
allowing complex protocols to be expressed as clean `async` functions.

This design makes protocols:
* ✅ Easy to Implement: Follow a natural, function-like flow.
* 🔍 Easy to Review & Audit: Logic is clear, concise, and self-contained.
* 🛠️ Packed with Utilities: Comes with built-in protocol simulation, an optional synchronous API, and
  other essential tools to streamline development and testing.

## Featured Protocols

We provide production-ready implementations of state-of-the-art **Threshold Signature Schemes
(TSS)**.

A TSS protocol allows a group of parties to generate a shared public key while each party holds
only a secret share of the corresponding private key. Signatures are created through a collaborative
computation, meaning no single party ever learns the full key. This eliminates single points of
failure and dramatically increases security for digital assets.

### [`cggmp21`]: Threshold ECDSA

[`cggmp21`] is our state-of-the-art **Threshold ECDSA** protocol. Its implementation includes
significant performance optimizations, such as using the Chinese Remainder Theorem (CRT) and
precomputed multiexponentiation tables.

It features a highly optimized signing phase that completes in a **single round** if a presignature
is generated in advance, making it incredibly fast for frequent operations. This makes it an ideal
solution for securing high-value assets by creating distributed wallets for blockchains like **Bitcoin**
and **Ethereum**.

### [`givre`]: Threshold Schnorr/EdDSA (FROST)

[`givre`] is our implementation of **FROST** (Flexible Round-Optimized Schnorr Threshold signatures).

It enables threshold signing for **Schnorr** and **EdDSA** signatures, which are known for their efficiency
and elegant mathematical properties. FROST is a highly efficient and secure protocol, perfect for
modern cryptographic systems and privacy-preserving applications.

## Core Libraries & Utilities

Our protocols are built on a set of powerful, generic libraries.

* [`round-based`]: The core framework for building any round-based MPC protocol.
* [`generic-ec`]: A trait-based library that provides a generic API for **Elliptic Curve
  Cryptography**, allowing your code to be generic over the choice of curve (e.g., `k256`, `p256`).
* [`udigest`]: A simple library for creating **unambiguous cryptographic digests**, helping to prevent
  collision attacks across different data structures.
* ...and many others that you can explore in our repositories!

## Contribute Your Protocol

The **Lockness** ecosystem is designed to be open and extensible. Our `round-based` framework isn't just
for our own protocols—it's for the entire community.

Have you designed or implemented your own MPC or TSS protocol? We encourage you to contribute it to
Lockness! By joining our organization, your project can benefit from greater visibility, community
support, and the credibility of being part of a Linux Foundation initiative.

If you have a protocol you'd like to share, **please get in touch with us** to discuss how we can work
together.

## Join us in Discord!
Feel free to reach out to us in `#lockness` channel [in Discord][discord]!

[`cggmp21`]: https://github.com/LFDT-Lockness/cggmp21
[`givre`]: https://github.com/LFDT-Lockness/givre
[`round-based`]: https://github.com/LFDT-Lockness/round-based
[`generic-ec`]: https://github.com/LFDT-Lockness/generic-ec
[`udigest`]: https://github.com/LFDT-Lockness/udigest
[discord]: https://discordapp.com/channels/905194001349627914/1285268686147424388
