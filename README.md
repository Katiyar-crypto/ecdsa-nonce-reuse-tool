# ECDSA Nonce Reuse Educational Tool

![ECDSA Nonce Reuse Tool logo](assets/logo.svg)

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-378ADD)](https://katiyar-crypto.github.io/ecdsa-nonce-reuse-tool/)
[![License](https://img.shields.io/badge/License-Apache%202.0-FAC775)](LICENSE)
[![Static](https://img.shields.io/badge/App-Static%20HTML-1D9E75)](index.html)

A standalone browser-based tool for demonstrating how ECDSA private keys can be recovered when the same nonce is reused across signatures.

## Use the tool

[Open the hosted tool](https://katiyar-crypto.github.io/ecdsa-nonce-reuse-tool/)

## Features

- ECDSA nonce reuse recovery for common curve orders.
- Built-in secp256k1 test vector with expected `k` and private key `d`.
- Clear input validation for decimal and `0x` hex values.
- One-click copy for recovered values.
- Exportable recovery report.
- Educational math walkthrough and mitigation guidance.
- Installable/offline-capable PWA.
- GitHub Pages deployment.

## Screenshots

![ECDSA nonce reuse tool desktop UI](assets/screenshots/tool-overview.png)

![ECDSA nonce reuse tool mobile UI](assets/screenshots/tool-mobile.png)

## Run locally

Open `index.html` in a browser.

For service worker testing, use a local static server:

```powershell
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Test Vector

The built-in demo uses `secp256k1` and should recover:

```text
k = 987654321987654321
d = 123456789123456789123456789
```

## GitHub Pages

The live site is published from the `gh-pages` branch:

[https://katiyar-crypto.github.io/ecdsa-nonce-reuse-tool/](https://katiyar-crypto.github.io/ecdsa-nonce-reuse-tool/)

## Safety Note

This tool is intended for educational and defensive security learning only. Use it only with signatures and systems you own or have permission to analyze.

## License

Licensed under the Apache License 2.0.
