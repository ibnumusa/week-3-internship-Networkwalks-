# NETWORKWALKS-WK3-PASSWORD-CRACKING

Week 3 Cybersecurity Internship Project — Password Cracking with John the Ripper (JTR) and NetworkWalks Tools.

## Project Overview

This project focused on building practical understanding of password security, hash extraction, and wordlist-based password recovery through two core modules:

- **Module 1 (WK3-PM1):** Password cracking using **John the Ripper (JTR)** in **Kali Linux** (including inspecting `~/.john/john.pot` and extracting PDF hashes using `pdf2john` / hash extraction tools)[cite: 1].
- **Module 2 (WK3-PM2):** Extracting and cracking a password-protected PDF hash using **NetworkWalks** online tools (**Hash Calculator** and **Password Cracker**)[cite: 3, 4, 5].

The goal was to see how password-protected PDFs yield crackable hashes and how dictionary/wordlist attacks demonstrate the real-world impact of weak or common passwords in authorized security testing.

## Modules Completed

- **WK3-PM1:** Password Cracking with John the Ripper (JTR) in Kali Linux[cite: 1].
- **WK3-PM2:** Password Cracking with NetworkWalks Tools (Hash Calculator & Password Cracker)[cite: 3, 4, 5].

## Tools and Technologies Used

| Tool / Environment | Purpose |
| :--- | :--- |
| **John the Ripper (JTR)** | Password security testing and recovery (`~/.john/john.pot` potfile inspection)[cite: 1] |
| **Kali Linux** | Linux environment used for JTR password-cracking work[cite: 1] |
| **pdf2john / Hash Extraction** | Extracting crackable `$pdf$` hashes from password-protected PDF files[cite: 2, 3] |
| **NetworkWalks Hash Calculator** | Browser-based extraction of crackable hashes (`pdf2john` / `hashcat` compatible format) from protected PDFs[cite: 3] |
| **NetworkWalks Password Cracker** | Testing extracted `$pdf$` hashes against wordlists via dictionary attacks[cite: 4, 5] |

## Tasks Completed

### 1. WK3-PM1 — Password Cracking with John the Ripper (Kali Linux)
- **Objective:** Extract hashes from password-protected PDF files and recover passwords using John the Ripper in Kali Linux[cite: 1].
- **Activities Performed:**
  - Prepared and worked with password-protected PDF files and saved extracted hash data (such as `hash1.txt`)[cite: 1].
  - Ran John the Ripper password recovery against the extracted hash format[cite: 1].
  - Checked the `~/.john` directory (`john.log` and `john.pot`) in Kali Linux to review cracked entries[cite: 1].
  - Unlocked the protected PDF using the recovered password and captured the resulting flag[cite: 6, 7].
- **Result:** Successfully cracked the target hash and verified access to the unlocked PDF content[cite: 1, 6, 7].

### 2. WK3-PM2 — Password Cracking with NetworkWalks Tools
- **Objective:** Use NetworkWalks' online Hash Calculator and Password Cracker to extract a PDF hash and recover its password[cite: 3, 4, 5].
- **Activities Performed:**
  - Opened **NetworkWalks Hash Calculator** and loaded the password-protected PDF (`My Locked PDF3.pdf`)[cite: 3].
  - Copied the extracted `$pdf$` hash (`Revision: R4`, `Version: V4`, `Key length: 128 bit`)[cite: 3].
  - Opened **NetworkWalks Password Cracker** (Dictionary Attack Lab), pasted the `$pdf$` hash, and ran the attack using the built-in 100-password list[cite: 4, 5].
  - Observed the dictionary attack attempts until a match was found (`1qaz2wsx`)[cite: 5].
  - Opened the protected PDF with the recovered password and captured the flag[cite: 5, 6, 7].
- **Result:** Successfully cracked the PDF password (`1qaz2wsx`) using the NetworkWalks Password Cracker and verified the unlocked PDF[cite: 5, 6, 7].

## Key Observations

- Password-protected PDFs can expose crackable hash strings (`$pdf$...`) that can be tested offline or via authorized tools[cite: 1, 3].
- Dictionary and wordlist attacks quickly test common or keyboard-pattern passwords (such as `1qaz2wsx`)[cite: 4, 5].
- Reviewing potfiles (`~/.john/john.pot`) and tool logs helps track recovered credentials cleanly during lab exercises[cite: 1].
- Weak or predictable passwords create clear security risks even on protected documents[cite: 5].

## What I Learned

- How to extract crackable hashes from password-protected PDF files[cite: 2, 3].
- How to run and verify password recovery with John the Ripper in Kali Linux and inspect `~/.john/john.pot`[cite: 1].
- How to use NetworkWalks' Hash Calculator and Password Cracker to perform a dictionary attack[cite: 3, 4, 5].
- Why strong, unique, and unpredictable passwords are essential for protecting sensitive files.

## Evidence and Documentation

Screenshots documenting the workflow, cracked output, and captured flags are organized in the project evidence folder:
- `WK3-PM1-JTR/` — Kali Linux terminal / John the Ripper execution and flag evidence[cite: 1, 6, 7].
- `WK3-PM2-NETWORKWALKS-TOOLS/` — Hash Calculator extraction, Password Cracker dictionary attack, and flag evidence[cite: 3, 4, 5, 6, 7].

## Ethical Considerations

All activities were performed strictly within an authorized educational internship lab using provided training files and tools. Password-cracking techniques should only be used on files, accounts, and systems where explicit permission is granted. Sensitive details such as recovered passwords, full hash values, and raw lab files are excluded or handled carefully in public documentation.

## Acknowledgment

Completed as part of the **NetworkWalks Cybersecurity Internship 2026**. Special thanks to **NetworkWalks** and instructor **Waqas Karim (CCIE)** for the hands-on labs, guidance, and learning environment.

Week 3 wrapped up—continuing to learn, practice, and grow in cybersecurity one step at a time, Insha'Allah. ⚡
