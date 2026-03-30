# ⚡ TheTechSavage WP Auto-Installer (Premium Edition)

![Version](https://img.shields.io/badge/Version-1.0_Premium-cyan?style=for-the-badge) 
![Platform](https://img.shields.io/badge/Platform-Ubuntu_24.04_LTS-orange?style=for-the-badge)
![Tech Stack](https://img.shields.io/badge/Stack-LEMP_(PHP_8.3)-blue?style=for-the-badge)
![Security](https://img.shields.io/badge/Security-Ghost_Architecture-red?style=for-the-badge)

**The Ultimate 1-Click WordPress LEMP Stack Installer.** Built for extreme performance, absolute security, and zero-touch configuration. Features a futuristic terminal dashboard, military-grade credential generation, automated Let's Encrypt SSL, and Telegram cloud backups.

---

## 🚀 Key Features

### 💎 Core Stack & Performance
* ✅ **Modern LEMP Stack:** Installs Nginx, MariaDB, and PHP 8.3-FPM optimized for Ubuntu 24.04.
* ✅ **Automated PHP Tuning:** Aggressively increases `memory_limit` (1024M), `upload_max_filesize` (512M), and execution times right out of the box so you never face theme upload errors.
* ✅ **Smart Domain Routing:** Dynamically builds Nginx server blocks. Automatically detects root domains and forces strict `www` to non-`www` HTTPS redirects to permanently prevent `ERR_TOO_MANY_REDIRECTS`.

### 🛡️ Smart Automation & Security
* ⚡ **WP-CLI Integration:** Bypasses the manual "5-Minute Install" browser screen entirely. WordPress core is downloaded, configured, and installed silently via the command line.
* 🔐 **The Secure Vault:** Randomly generates highly complex, 16-character passwords for both MariaDB and the WordPress Admin account. Stores them safely in a root-locked vault.
* ☁️ **Smart Telegram Backups:** Instantly dump your database and compress your site. Uploads a master file to Catbox and smartly detects size—if over 45MB, it automatically splits the archive into chunks to bypass Telegram bot limits and loops them to your chat.
* 🔄 **Dual-Method Restore:** Easily restore your entire site and database either via a direct cloud link (Catbox) or by uploading your split `.z01` parts manually via SFTP. The script stitches, extracts, and imports everything automatically.
* 🩺 **Interactive Dashboard:** Manage your entire web server through a sleek, custom `wp-menu` terminal UI.

---

## 📥 Installation

Run this command on a fresh **Ubuntu 24.04 LTS** VPS.

```bash
apt update -y && apt install -y wget && wget -qO install https://raw.githubusercontent.com/TheTechSavant/WPOneClickInstaller/main/install && chmod +x install && ./install
```

### 🛠️ Setup Steps

1.  **Point Your Domain:** Configure your DNS records to point to your VPS IP address. **(CRITICAL: Must be set to DNS Only / Grey Cloud on Cloudflare during installation).**
    * **For a Root Domain (e.g., mysite.com):** Create an **A Record** for `@` pointing to your VPS IP, and a **CNAME Record** for `www` pointing to your root domain.
    * **For a Subdomain (e.g., blog.mysite.com):** Create an **A Record** with your subdomain name (e.g., `blog`) pointing directly to your VPS IP.
2.  **Run the Installer:** Paste the installation command above into your terminal.
3.  **Input Domain:** Enter your domain name and specify if it is a Root Domain (`y/n`).
4.  **Sit Back & Relax:** Wait for the system to download the LEMP stack, compile dependencies, configure WP-CLI, and generate SSL certificates.
5.  **Completion:** The script will output your WordPress Admin URL and randomized login credentials. 

---

## 🎮 The Dashboard

Type `menu` at any time to access the futuristic control panel.

```bash
menu
```

### 🖥️ Menu Overview
| Menu Option | Function |
| :--- | :--- |
| **[01] View Vault Credentials** | Instantly retrieve your randomized MariaDB and WP Admin passwords. |
| **[02] Tune PHP Upload Limits** | Easily increase PHP max upload and memory limits without using `nano`. |
| **[03] Force Renew SSL** | Quickly stop Nginx, force a Certbot SSL renewal, and restart services. |
| **[04] Telegram Cloud Backup** | Smartly compresses, uploads to Catbox, and splits files >45MB for Telegram delivery. |
| **[05] Check Running Services** | Live monitor of core web services (Nginx, MariaDB, PHP 8.3-FPM). |
| **[06] Restore From Backup** | Stitch split files, extract the archive, and automatically import your database. |
| **[07] Configure Auto-Reboot** | Schedule the server to reboot automatically at specific intervals to clear RAM. |
| **[08] View Reboot Logs** | Check the system history to see exactly when the VPS last restarted. |

---

## ⚠️ Credits & Disclaimer

**Developed & Maintained by:** [TheTechSavage](https://t.me/thetechsavage)

> *This project is for educational purposes and rapid server deployment only. The developer is not responsible for misuse.*

---

## 🆘 Need Help?
If you encounter any issues with the installation or need premium server resources:
* **Technical Support:** [@TheTechSavageSupport](https://t.me/thetechsavagesupport)
* **Community:** [@TheTechSavageTelegram](https://t.me/TheTechSavageTelegram)