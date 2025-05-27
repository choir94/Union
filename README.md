# Panduan Lengkap Instalasi Union Bot Telegram

---

## 1. Clone Repository Union

```bash
git clone https://github.com/choir94/Union.git
cd Union
```

---

## 2. Instal Node Version Manager (NVM)

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
source ~/.bashrc
```

---

## 3. Instal Node.js Versi 20

```bash
nvm install 20
nvm alias default 20
```

---

## 4. Verifikasi Instalasi

```bash
node -v
npm -v
```

---

## 5. Instal npm (jika belum tersedia)

```bash
sudo apt install npm
```

---

## 6. Inisialisasi dan Instalasi Dependensi

```bash
npm init -y
npm install ethers axios moment-timezone readline node-telegram-bot-api dotenv
```

---

## 7. Buat Bot dan Dapatkan Token dari BotFather

1. Buka Telegram.
2. Cari dan mulai chat dengan [@BotFather](https://t.me/BotFather).
3. Ketik `/start` lalu ketik `/newbot`.
4. Masukkan nama bot (bebas).
5. Masukkan username bot yang diakhiri dengan `bot` (contoh: `unionnotifier_bot`).
6. Setelah berhasil, BotFather akan memberikan **TOKEN**, contohnya:

```
Use this token to access the HTTP API:
123456789:AAH4YQ8z-example-token-dari-botfather
```

7. Salin token tersebut dan masukkan ke dalam `.env`.

---

## 8. Buat File `.env`

```bash
nano .env
```

### Isi file `.env` seperti berikut:

```env
TELEGRAM_BOT_TOKEN=Ambil di botfather
TELEGRAM_CHAT_ID=
PRIVATE_KEY_1=pk wallet
BABYLON_ADDRESS_1=address babylon
```

> **Catatan:** Untuk mendapatkan `TELEGRAM_CHAT_ID`, buka Telegram, cari dan mulai chat dengan `@userinfobot`. ID kamu akan muncul di sana.

---

## 9. Jalankan Bot

```bash
node bot.js
```

---

## 10. Jalankan bot.js di Latar Belakang dengan Screen

Install screen jika belum:

```bash
sudo apt install screen
```

Buat session screen baru dan jalankan bot:

```bash
screen -S unionbot
node bot.js
```

Untuk keluar dari screen tanpa menghentikan bot, tekan:

```
Ctrl + A, lalu tekan D
```

Untuk kembali ke screen:

```bash
screen -r unionbot
```

---

## 11. Bergabung dengan Komunitas

Ingin berdiskusi atau tanya jawab? Gabung ke channel komunitas:
[https://t.me/airdrop_node](https://t.me/airdrop_node)
