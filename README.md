# CYBERDATA

**Terminal cybersecurity multitool (TUI)** — 89 tools: network recon, crypto, OSINT, red team, cracking, file encryption and anonymity/OPSEC, in an underground interface with a glitch boot animation, fsociety watermark, themes, ranks and XP.

> Written in **Rust** (ratatui + crossterm). Network is 100% over HTTPS/SOCKS (DoH, RDAP, crt.sh, ipinfo.io/ipwho.is, archive.org, GitHub API, Shodan, Mullvad API, Tor) — no system dependency.
> **Authorized / educational use only**: lab, CTF, engagements with written authorization.

```
 ██████ ██    ██ ██████  ███████ ██████  ██████   █████  ████████  █████
        CYBERSECURITY MULTITOOL · v1.8 · grimh3xx
```

## Highlights

- **Glitch boot** (code rain → "Decrypting" → banner), faint **fsociety watermark**.
- **2 themes** (no purple): **Amber CRT** (default) and **Mono + Red**, switched in Settings, saved.
- **Global search** (`/`), **repeat last** (`r`), **save a result to .txt** (`w`), **scrolling** long pages.
- **Ranks & XP**: from Intern to `Ghost // root`.

## The 9 pages

| # | Page | Tools |
|---|------|-------|
| 1 | **NETWORK · WEB** | DNS, IP/Domain Lookup, Email Security, WHOIS/RDAP, URL Analyzer, Subnet Calc, Port Scanner, HTTP Headers, TLS Certificate, GeoIP/ASN, 403 Bypass, RDP Probe |
| 2 | **CRYPTO · DATA** | Hash Gen/ID, Password Analyzer (+HIBP)/Generator, Encoder/Decoder (B64/32/58, Hex, URL, ROT13), Timestamp, TOTP, HMAC, Passphrase, Hash File, AES-256-GCM, UUID, QR Code |
| 3 | **CRACK · ADV** | JWT Decoder, Hash Cracker (list/file), Cipher Bruteforce, Caesar Auto-Solve, Entropy Scanner, Multi-Decoder, Password Mutator, Morse/Bin/Dec, Vigenere Analyzer |
| 4 | **RED TEAM** | Subdomain Discovery, Username/Email Permutator, Default Creds, Payload Cheat-Sheet, User-Agent, Pentest Methodology, Reverse Shell Builder, Nmap Builder, Hashcat/John Builder, Payload Encoder |
| 5 | **OSINT** | crt.sh Subdomains, Username Finder, Email OSINT, Wayback, GitHub Recon, Google Dorks, Phone Lookup, Tech Fingerprint, Shodan Host |
| 6 | **VAULT · CRYPT** | AES-256-GCM, ChaCha20-Poly1305, AEGIS-256 (files), XOR, Secret Vault, Account Recovery Kit, Secure Wipe |
| 7 | **ANON · OPSEC** | My Public IP, Tor Check, Tor New Identity, Proxy Tester, Proxy Hunter, Anonymity Check (Mullvad), Anonymity Toolkit, Tor Bridges Helper, AutoTor |
| 8 | **PENTEST KIT** | MSFvenom, MSF Handler, xfreerdp3, sqlmap, Hydra, Dir/DNS Fuzz, Web Scanners, Wireshark/tshark, Burp Helper, Tool Detector, Wi-Fi Audit Builder, DLL Hijack Audit, Windows Privesc Audit |
| 9 | **PRIVACY** | Steganography (hide/extract), EXIF Remover, EXIF Viewer, IP Masking, USB Inspector |
| 10 | **SYSTEM** | Theme, Options (incl. Shodan key), Statistics, About |

## Keys

| Key | Action |
|-----|--------|
| `1`–`9` | Run tool (10th+ via arrows) |
| `↑` / `↓` + `Enter` | Select / run |
| `n` / `p` · `←` `→` · `Tab` | Next / previous page |
| `/` · `r` · `s` | Search · repeat last · theme |
| `w` (on a result) | Save to `.txt` |
| `Esc` · `q` | Cancel/back · quit |

## Anonymity notes

- **Tor Check / New Identity** need a local Tor running (Tor Browser on 9150/9151, or `tor` on 9050/9051).
- **Anonymity Check** uses the free Mullvad API and auto-routes through local Tor if present.
- **Proxy Hunter** fetches free proxies (flaky by nature) and tests them — never send credentials through untrusted proxies.

## Themes & config

- **Amber CRT** (default) — amber on black, phosphor-monitor look.
- **Mono + Red** — grayscale, red as the only accent.

Config in `%APPDATA%\cyberdata.cfg` (Windows) or `~/.config/cyberdata.cfg`. Saved `.txt` results go to `cyberdata-logs/`.

## Build

```bash
cargo run --release
```

### Windows

```powershell
cargo build --release
.\target\release\cyberdata.exe
```

Use **Windows Terminal** for the block glyphs. Dependency-free binary (system DLLs only).

## Disclaimer

The offensive and anonymity modules are provided for **authorized testing, learning and defense**. Only query/test systems you own or are authorized to test.
