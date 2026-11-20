# Week 3 – Project Module 1: Password Cracking with JTR

![Platform](https://img.shields.io/badge/Platform-Windows-0078D6)
![Tool](https://img.shields.io/badge/Tool-John%20the%20Ripper-black)
![Tool](https://img.shields.io/badge/Tool-Johnny%20GUI-red)
![Status](https://img.shields.io/badge/Status-Educational%20Lab-success)

A practical lab from the **NetworkWalks Cybersecurity & Ethical Hacking Program**: recovering the password of a protected PDF using **John the Ripper (JTR)** and its graphical front-end **Johnny**.

## Table of Contents

1. [Overview](#overview)
2. [Lab Information](#lab-information)
3. [Tools Used](#tools-used)
4. [Repository Structure](#repository-structure)
5. [Lab Workflow](#lab-workflow)
6. [Technical Concepts](#technical-concepts)
7. [Screenshot Evidence](#screenshot-evidence)
8. [Result](#result)
9. [Learning Outcomes](#learning-outcomes)
10. [Ethical Disclaimer](#ethical-disclaimer)
11. [Author](#author)

## Overview

John the Ripper is a well-known password-cracking tool used to test how strong a password is. It runs on Windows, Linux and Mac, and can crack password hashes from many file types, including PDF, ZIP and Office documents. Johnny is its graphical interface, so the same cracking work can be done by clicking through a simple screen instead of typing commands.

In this lab, the task was to recover the password of a protected file, `My Locked PDF1.pdf`, using JTR and Johnny on a Windows PC.

## Lab Information

| Field | Detail |
|---|---|
| Program | Cybersecurity & Ethical Hacking Internship / Practical Training |
| Organization | NetworkWalks Academy |
| Week | Week 3 |
| Module | Project Module 1 |
| Platform | Windows |
| Target File | `My Locked PDF1.pdf` |

**Authorization and Scope:** This exercise was assigned by my instructor as part of the NetworkWalks training program and performed only on the file provided for the lab. The techniques shown here should only be used on files and systems you have explicit permission to test.

## Tools Used

| Tool | Role |
|---|---|
| **John the Ripper (JTR)** | Core password-cracking engine that tests candidate passwords against a hash |
| **Johnny** | Graphical front-end for JTR, so the attack can be run without command-line syntax |
| **Online Hash Extractor** | Used to convert the locked PDF into a crackable `$pdf$...` hash before feeding it to JTR |

## Repository Structure

```text
week3-pm1-password-cracking-jtr/
├── README.md
└── screenshots/
    ├── 01-johnny-settings-empty.png
    ├── 02-browsing-downloaded-files.png
    ├── 03-selecting-john-exe.png
    ├── 04-extracting-hash-onlinehashcrack.png
    ├── 05-opening-password-file-in-johnny.png
    └── 06-password-cracked-result.png
```

## Lab Workflow

**Step 1 – Install JTR and Johnny**
Downloaded John the Ripper and the Johnny GUI, and installed Johnny on a Windows PC.

**Step 2 – Point Johnny to the JTR executable**
Opened Johnny's Settings tab, which initially showed no valid John the Ripper executable path. Browsed to the extracted JTR folder and selected `john.exe` from its `run` folder so Johnny could use it.

**Step 3 – Extract the hash from the locked PDF**
Uploaded the protected PDF to an online PDF hash extractor, which generated the file's password hash in the `$pdf$...` format. Copied the hash and saved it to a text file.

**Step 4 – Load the hash into Johnny**
Opened the saved hash file in Johnny as the password file to attack.

**Step 5 – Run the attack**
Started the attack in Johnny and let it test candidate passwords against the hash.

**Step 6 – Recover and verify the password**
Johnny returned the cracked password. Used it to open the original locked PDF and confirmed it unlocked successfully.

## Technical Concepts

- **Password-protected PDF:** A PDF encrypted so opening it requires a password, enforced by the PDF's own security handler.
- **Hash extraction:** Converting a file's password protection into a hash value, so a cracking tool can test guesses against it without repeatedly opening the real file.
- **Hashing vs. encryption:** Encryption is reversible with the right key; the extracted hash is one-way and used only for testing guesses, not for decrypting the file directly.
- **Dictionary/brute-force cracking:** JTR hashes each candidate password and compares it to the target hash, rather than reversing the hash itself.

## Screenshot Evidence

### 1. Johnny – Initial Setup
![Johnny settings](screenshots/01-johnny-settings-empty.png)
*Johnny opened for the first time, with no valid JTR executable path set.*

### 2. Locating the JTR Installation
![Browsing files](screenshots/02-browsing-downloaded-files.png)
*Browsing to the downloaded and extracted John the Ripper folder.*

### 3. Selecting john.exe
![Selecting john.exe](screenshots/03-selecting-john-exe.png)
*Selecting `john.exe` from the `run` folder to set as Johnny's executable.*

### 4. Hash Extraction
![Hash extraction](screenshots/04-extracting-hash-onlinehashcrack.png)
*Using an online PDF hash extractor to generate the crackable `$pdf$...` hash from the locked PDF.*

### 5. Loading the Hash in Johnny
![Opening password file](screenshots/05-opening-password-file-in-johnny.png)
*Opening the saved hash file in Johnny to begin the attack.*

### 6. Password Cracked
![Password cracked](screenshots/06-password-cracked-result.png)
*Johnny showing the recovered password after the attack completed.*

## Result

The password for `My Locked PDF1.pdf` was successfully recovered using John the Ripper and Johnny, and verified by reopening the PDF with the cracked password.

## Learning Outcomes

- Understanding how password-protected PDFs enforce access control.
- Learning how to extract a crackable hash from a protected file.
- Setting up and configuring Johnny to work with the JTR engine.
- Running a password-cracking attack and interpreting the results.
- Understanding why password complexity directly affects how long cracking takes.
- Practical experience documenting a security exercise in an authorized training environment.

## Ethical Disclaimer

This practical was conducted for educational purposes within an authorized NetworkWalks training environment. Password-cracking tools demonstrated here should only be used against files, systems and data you have explicit permission to test. This repository does not endorse unauthorized password cracking of any kind.

## Author

**Muhammad Talha**
Cybersecurity Intern — NetworkWalks Cybersecurity & Ethical Hacking Program

- GitHub: [@infomuhammadtalha](https://github.com/infomuhammadtalha)
- LinkedIn: [Muhammad Talha](https://www.linkedin.com/in/muhammad-talha-98b39b279/)
