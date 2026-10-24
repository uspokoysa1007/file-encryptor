# file-encryptor

CLI-утилита на Rust для шифрования и расшифровки файлов паролем.

## Возможности (план)

- шифрование любого файла парольной фразой;
- AEAD-шифры: XChaCha20-Poly1305 / AES-256-GCM;
- потоковая обработка больших файлов (без загрузки в память);
- salt и nonce хранятся в заголовке зашифрованного файла;
- ключ через Argon2id;
- опция `shred` — перезапись и удаление оригинала.

## Стек

- Язык: Rust
- Планируемые библиотеки: `clap`, `rpassword`, `argon2`, `chacha20poly1305`, `aes-gcm`, `rand`

## Сборка и запуск

```bash
cargo build --release
cargo run -- encrypt secret.txt
cargo run -- decrypt secret.txt.enc
```

## Лицензия

MIT
