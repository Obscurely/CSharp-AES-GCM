> **[ARCHIVED 2021]** Legacy cryptographic wrapper. Maintained for historical reference.

# C# AES-GCM Cryptographic Wrapper
A high-level C# wrapper around the native `System.Security.Cryptography.AesGcm` class, providing a simplified interface for 256-bit authenticated encryption with associated data (AEAD). Handles automatic nonce generation, tag concatenation, and Base64 serialization.

## API
1. Key Generation: Utilizes `RandomNumberGenerator` to provision cryptographically secure 256-bit (32-byte) keys, serialized to Base64.
2. Encryption: Derives a secure random nonce, encrypts the plaintext using AES-GCM, and concatenates the resulting ciphertext, nonce, and authentication tag into a single Base64 payload. Supports optional Associated Authenticated Data (AAD).
3. Decryption: Deserializes the Base64 payload, extracts the nonce and authentication tag, verifies cryptographic integrity, and returns the decrypted plaintext.
