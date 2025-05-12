# john-the-ripper-basics
My learning and experiments with John the Ripper for ethical password cracking.

```markdown
# 🔐 John the Ripper – Password Cracking Basics

Welcome to my hands-on learning repository focused on **John the Ripper**, a widely used password cracking tool in cybersecurity. This project is part of my ethical hacking practice and cybersecurity training.

---

## 📌 About This Project

John the Ripper (JtR) is a powerful open-source tool used to identify weak passwords through brute force or dictionary attacks. In this repository, I demonstrate basic usage of JtR to understand how password hashes can be cracked for security testing and learning purposes.

---

## ⚙️ Tools & Environment

- **Operating System**: Kali Linux / Parrot OS (can also be used on Ubuntu)
- **Tool**: John the Ripper (Community Edition)
- **Wordlist**: rockyou.txt and custom wordlists
- **Support Tools**: `zip2john`, `gpg2john`, `unshadow`

---

## 🗂️ Repository Structure

```

john-the-ripper-basics/
├── hashes/
│   ├── shadow\.txt            # Sample Linux shadow hashes
│   ├── zip\_hash.txt          # Hashed output from a protected ZIP
├── scripts/
│   └── zip\_crack\_command.sh  # Bash script for ZIP cracking
├── wordlists/
│   └── custom\_wordlist.txt   # Custom wordlist for testing
├── screenshots/
│   └── john\_output.png       # Output from terminal
├── cracked/
│   └── cracked\_results.txt   # Successfully cracked passwords
└── README.md

````

---

## 🔧 How I Used John the Ripper

### 1️⃣ Cracking Linux Shadow File
```bash
unshadow /etc/passwd /etc/shadow > full_shadow.txt
john --wordlist=/usr/share/wordlists/rockyou.txt full_shadow.txt
````

### 2️⃣ Cracking ZIP File Password

```bash
zip2john secret.zip > zip_hash.txt
john --wordlist=wordlists/custom_wordlist.txt zip_hash.txt
```

### 3️⃣ Show Cracked Passwords

```bash
john --show zip_hash.txt
```

## 📚 What I Learned

* Fundamentals of password hashing and cracking
* Using common wordlists for dictionary attacks
* Basic usage of `zip2john` and `unshadow` tools
* Importance of strong passwords in real-world systems

---

## ⚠️ Disclaimer

> This project is intended strictly for **educational purposes** and ethical cybersecurity practice. Do not use any of these tools or techniques without **legal authorization**.

⭐ **Thank you for visiting! If you found this useful, feel free to star the repo.**

