TGPM malformed-file test pack

These files contain NO real TGPM secrets or credentials. They are synthetic and intentionally invalid.

Expected vault-file behavior:
01 not JSON -> TGPM could not open this vault / not valid JSON
02 wrong format -> TGPM could not open this vault / not TGPM
03 unsupported version -> TGPM could not open this vault / unsupported version
04 missing KDF -> TGPM could not open this vault / KDF metadata missing
05 invalid iterations -> TGPM could not open this vault / iteration count invalid or unsupported
06 invalid salt Base64URL -> TGPM could not open this vault / invalid Base64URL
07 wrong wrap IV length -> TGPM could not open this vault / invalid length
08 missing ciphertext -> TGPM could not open this vault / ciphertext missing

Expected Recovery Key behavior:
09 not JSON -> Invalid TGPM Recovery Key / not valid JSON
10 wrong format -> Invalid TGPM Recovery Key / not TGPM Recovery Key
11 unsupported version -> Invalid TGPM Recovery Key / unsupported version
12 wrong decoded key length -> Invalid TGPM Recovery Key / invalid length
13 invalid Base64URL -> Invalid TGPM Recovery Key / invalid Base64URL

Important: these synthetic vault shells are deliberately not decryptable. They are for pre-decryption structural validation only.
