# Caesar Cipher Encryption/Decryption Tool

A simple Python command-line tool that implements the classic **Caesar cipher** to encrypt and decrypt text using a user-defined shift value.

## Features

- Encrypts plaintext by shifting each alphabetic character forward by a specified number of positions
- Decrypts ciphertext by shifting characters back by the same amount
- Preserves character case (uppercase stays uppercase, lowercase stays lowercase)
- Leaves non-alphabetic characters (numbers, spaces, punctuation) unchanged
- Demonstrates the full round trip: takes input, encrypts it, then decrypts it back to verify correctness

## How It Works

The Caesar cipher shifts each letter of the alphabet by a fixed number of positions (the "shift" or "key"):
- **Encryption**: `(character position + shift) % 26`
- **Decryption**: `(character position - shift) % 26`

The modulo operation ensures the shift wraps around the alphabet (e.g., shifting `Z` by 1 wraps back to `A`).

## Requirements

- Python 3.x
- No external libraries required

## Installation

```bash
git clone https://github.com/yourusername/caesar-cipher.git
cd caesar-cipher
```

## Usage

Run the script from the terminal:

```bash
python encryption.py
```

You'll be prompted to enter the text you want to encrypt and a numeric shift value.

### Example

```
Enter text: Hello World
Enter shift value: 3
Original: Hello World
Encrypted: Khoor Zruog
Decrypted: Hello World
```

## Known Limitations

- **Not cryptographically secure**: The Caesar cipher is a classical/educational cipher with only 25 possible shift values, making it trivial to break via brute force or frequency analysis. It should not be used to protect sensitive data.
- **No input validation** on the `shift` value (e.g., non-numeric input will raise an error).
- **Alphabet-only shifting**: Only English letters (A–Z, a–z) are shifted; accented characters or non-Latin alphabets are not supported.

## Author

Selasi

## License

This project is for educational purposes.
