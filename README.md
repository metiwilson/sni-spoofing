
# 🎛️ آموزش حرفه‌ای و مرحله‌به‌مرحله SNI Spoofing  
راهنمای کامل استفاده از **Patterniha** برای اجرای SNI Spoofing و اتصال آن به کلاینت‌های:  
**V2Ray / Xray / Nekobox / v2rayNG**

[![License](https://img.shields.io/badge/License-MIT-green.svg)]()  
[![Made By](https://img.shields.io/badge/Maintainer-%40metiwilson-blue)]()  
[![Platform](https://img.shields.io/badge/Platform-Windows-%230078D6.svg)]()  

---

# 📌 ویژگی‌های این آموزش
- کاملاً **مرحله‌به‌مرحله**  
- مناسب کاربران مبتدی تا حرفه‌ای  
- همراه با **config.json آماده**  
- تست‌شده روی کلاینت‌های مختلف  
- سازگار با آخرین نسخه Patterniha  

---

# 📥 1. دانلود Patterniha

آخرین نسخه برنامه را از لینک زیر دانلود کنید:

🔗 https://github.com/metiwilson/sni-spoofing/releases/tag/v1.0

فایل را به صورت **ZIP یا RAR** دریافت کنید.

---

# 📦 2. استخراج فایل‌ها

فایل را Extract کنید.  
در پوشه باید فایل زیر موجود باشد:

```
Patterniha.exe
```

---

# 🛠️ 3. ساخت و ویرایش config.json

در همان پوشه، فایل **config.json** را باز کنید یا اگر وجود ندارد ایجاد کنید.

سپس این محتوا را دقیقاً داخل آن قرار دهید:

```
{
  "LISTEN_HOST": "0.0.0.0",
  "LISTEN_PORT": 40443,
  "CONNECT_IP": "104.19.229.21",
  "CONNECT_PORT": 443,
  "FAKE_SNI": "www.hcaptcha.com",
  "QUEUE_NUM": 1000,
  "HANDSHAKE_TIMEOUT_MS": 2000
}
```

این فایل مشخص می‌کند Patterniha چگونه به سرور وصل شود و چه SNI جعلی ارسال کند.

---

# ⚙️ 4. اجرای برنامه (خیلی مهم)

بر روی فایل **Patterniha.exe** راست‌کلیک کنید و:

```
Run as administrator
```

را انتخاب کنید.

**بدون اجرای Admin برنامه کار نمی‌کند.**

اگر Windows Firewall اجازه خواست → Allow بزنید.

---

# 🛰️ 5. تنظیم کلاینت V2Ray / Xray / v2rayNG / Nekobox

در کانفیگ فعلی‌تان فقط ۲ مقدار را تغییر دهید:

```
Address: 127.0.0.1
Port: 40443
```

مهم:  
تمام موارد دیگر مثل:

- UUID  
- TLS / Reality  
- path  
- Security  
- transport  

تماماً باید همان تنظیمات قبلی باقی بمانند.

---

# 🔌 6. اتصال

• کانفیگ را ذخیره کنید  
• دکمه **Connect** را بزنید  

اگر همه چیز درست باشد، اتصال برقرار می‌شود.

---

# 🧩 نکات مهم و رفع مشکل

- همیشه برنامه را با Run as Administrator اجرا کنید  
- اگر اجرا نشد، از **config real delay** بگیرید تا شروع شود  
- اگر وصل نشد:
  - Patterniha را Stop/Start کنید  
  - یا یک IP جدید در config.json تست کنید  
- اگر پورت مشغول بود، Listen Port را عوض کنید (مثل 30443)

---

# 🌐 لیست SNI پیشنهادی (کامل و تست‌شده)

```
hcaptcha.com
newassets.hcaptcha.com
js.hcaptcha.com
imgs.hcaptcha.com
imgs2.hcaptcha.com
imgs3.hcaptcha.com
assets.hcaptcha.com
api.hcaptcha.com
analytics.hcaptcha.com
stats.hcaptcha.com
three-cust.hcaptcha.com
tg.hcaptcha.com
primary.hcaptcha.com
dashboard.hcaptcha.com
billing.hcaptcha.com
accounts.hcaptcha.com
proxy.hcaptcha.com
loader.hcaptcha.com
challenge-tasks.hcaptcha.com
serverless.hcaptcha.com
health-check.hcaptcha.com
email.hcaptcha.com
```

---

# 🧑‍💻 نگهداری و توسعه  
این مخزن توسط **@metiwilson** مدیریت می‌شود.

اگر درخواست افزودن ویژگی جدید، نسخه موبایل، یا آپدیت Config دارید Pull Request یا Issue ارسال کنید.

---

# ⭐ اگر مفید بود، ریپازیتوری را Star کنید!
