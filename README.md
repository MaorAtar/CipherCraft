# CipherCraft
# Text Encryption and Decryption System

This project implements a system for encrypting and decrypting text based on a set of defined operations. The system supports word-level and text-level transformations and is designed with modular and reusable object-oriented programming principles. 

## Features

1. **Word-Level Operations**:
    - Replace characters based on specific rules (e.g., complement digits to 9, swap case, and map letters to their "complementary" counterparts).
    - Reverse the order of characters.
    - Perform circular left and right shifts on characters.
    - Add or remove characters at specific positions.
    - Access characters by index with support for modular indexing.

2. **Text-Level Operations**:
    - Apply word-level operations to all words in the text.
    - Reverse the order of words in the text.
    - Perform circular left and right shifts on words.
    - Add or remove words at specific positions.
    - Access words by index with support for modular indexing.

3. **EncryptedText Class**:
    - Supports encryption and decryption using a dynamic key.
    - Keys are composed of triplets defining operations, their scope (entire text or specific words), and parameters for the operation.
    - Encodes or decodes the text based on the provided key.

## Class Details

### `Word` Class
Represents a word and provides the following features:
- **Dynamic character array** with size management.
- Overloaded operators for:
  - `!`: Replace characters based on encryption rules.
  - `&`: Reverse character order.
  - `<<`: Circular left shift of characters.
  - `>>`: Circular right shift of characters.
  - `=+`: Add a random character at a specific position.
  - `=-`: Remove a character from a specific position.
  - `[]`: Access character by index with modular indexing.
  - `>> cout`: Print the word to the console.

### `Text` Class
Represents a collection of words and provides the following features:
- **Dynamic array of pointers to `Word` objects**.
- Overloaded operators for:
  - `!`: Replace characters in all words.
  - `&`: Reverse word order.
  - `<<`: Circular left shift of words.
  - `>>`: Circular right shift of words.
  - `=+`: Add a random word at a specific position.
  - `=-`: Remove a word from a specific position.
  - `[]`: Access a word by index with modular indexing.
  - `>> cout`: Print the text to the console.

### `EncryptedText` Class
Represents an encrypted or decrypted text object:
- Contains a pointer to a `Text` object, a status (encryption or decryption), and a dynamic array representing the encryption/decryption key.
- Overloaded operators for:
  - `=+`: Add an encryption/decryption key.
  - `!`: Encrypt the text using the key.
  - `&`: Decrypt the text using the key.
  - `>> cout`: Print the text and key to the console.
