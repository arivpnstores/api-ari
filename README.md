# 🚀 API ARISCTUNNEL V4 & V7

API sederhana berbasis **Node.js + Express** untuk auto create, trial, dan renew akun VPN (SSH, VMESS, VLESS, TROJAN, SHADOWSOCKS).

Didesain untuk kebutuhan:

* 🤖 Bot Telegram / Auto Order
* 💰 Panel jualan VPN
* ⚡ Integrasi script ArisTunnel V4 & V7

---

## 📂 Struktur Repository

```
.
├── api.sh          # Script install API
├── del.sh          # Script uninstall API
├── api-ari.zip     # Core API (Node.js)
└── README.md
```

---

## ⚙️ Fitur Utama

### ✅ CREATE AKUN

* `/createssh`
* `/createvmess`
* `/createvless`
* `/createtrojan`
* `/createshadowsocks`

### 🎁 TRIAL AKUN

* `/trialssh`
* `/trialvmess`
* `/trialvless`
* `/trialtrojan`
* `/trialshadowsocks`

### 🔄 RENEW AKUN

* `/renewssh`
* `/renewvmess`
* `/renewvless`
* `/renewtrojan`
* `/renewshadowsocks`

---

## 🔐 Security

Semua endpoint dilindungi dengan:

```
AUTH_KEY
```

Request wajib menyertakan:

```
auth=ISI_AUTH_KEY
```

Jika tidak valid → ❌ **Unauthorized**

---

## 📡 Default Port

```
5889
```

---

## 📥 Instalasi

```bash
bash api.sh
```

---

## 🗑️ Uninstall

```bash
bash del.sh
```

---

## 📌 Contoh Request

### 🔹 CREATE SSH

```
http://IP:5889/createssh?user=test&password=123&exp=1&iplimit=1&auth=KEY
```

### 🔹 CREATE VMESS

```
http://IP:5889/createvmess?user=test&exp=1&iplimit=1&quota=10&auth=KEY
```

### 🔹 TRIAL SSH

```
http://IP:5889/trialssh?auth=KEY
```

### 🔹 RENEW SSH

```
http://IP:5889/renewssh?user=test&exp=1&iplimit=1&auth=KEY
```

---

## 📦 Response JSON

Contoh response:

```json
{
  "status": "success",
  "message": "Akun berhasil dibuat",
  "data": {
    "username": "test",
    "domain": "example.com",
    "expired": "7 Days",
    "uuid": "xxxx-xxxx",
    "vmess_tls_link": "...",
    "vless_tls_link": "...",
    "trojan_tls_link": "..."
  }
}
```

---

## ⚠️ Requirement

* OS: Ubuntu / Debian / Kali Linux
* Node.js v20+
* Script backend:

  * create_ssh.sh
  * create_vmess.sh
  * dll (wajib ada di server)

---

## 🔥 Kelebihan

* ⚡ Super ringan & cepat
* 🔌 Mudah diintegrasikan ke bot / panel
* 🔐 Sudah pakai AUTH KEY security
* 📊 Output JSON (siap dipakai frontend/bot)
* 🧠 Support semua core VPN populer

---

## 👨‍💻 Author

**arivpnstores**

---

## ⭐ Support

Kalau suka project ini:

* ⭐ Star repo
* 🔁 Share ke teman
* 💬 Gunakan untuk bisnis VPN kalian

---

## 🚀 Notes

API ini hanya sebagai **bridge** ke script backend.
Pastikan semua script seperti:

```
create_ssh.sh
trial_vmess.sh
renew_vless.sh
```

sudah tersedia dan berjalan normal.

---

---

