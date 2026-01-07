<p align="center">
  <img src="./assets/Logo.png" alt="Cloudflare Search Icon" width="150" style="border-radius: 20px;"/>
</p>

# ⚡️ Cloudflare Worker V2Ray Optimizer

[🇺🇸 English Version](#-english-description)
## 🇮🇷 توضیحات فارسی

این ابزار به شما کمک می‌کند تا کانفیگ‌های اختصاصی خود را که با Cloudflare Workers ساخته‌اید، بهینه‌سازی کنید و عملکرد نهایی آنها را به بهترین سرعت ممکن برسانید.

🔧 **ویژگی‌های جدید:**
- 🌐 **پشتیبانی از زبان فارسی و انگلیسی** - تغییر زبان با یک کلیک
- 🎨 **رابط کاربری مدرن و زیبا** - طراحی بهبود یافته با انیمیشن‌های جذاب
- 📱 **طراحی واکنش‌گرا** - سازگار با تمام دستگاه‌ها
- ⚡ **عملکرد بهینه** - سرعت بالا و تجربه کاربری بهتر
- 🔄 **سیستم اعلان‌ها** - بازخورد فوری برای کاربر
- 💾 **ذخیره تنظیمات** - به خاطر سپردن زبان انتخابی کاربر
- 🌐 **پشتیبانی چند پروتکلی** - VLESS, Trojan, VMESS, و JSON Fragmented
- 🔍 **اسکن IP تمیز Cloudflare** - یافتن بهترین IP‌های تمیز با پینگ کم
- 🎯 **دو حالت بهینه‌سازی:**
  - 🌍 **حالت دامنه** - استفاده از بهترین دامنه + بهترین پورت
  - 🔗 **حالت IP تمیز** - اسکن IP‌های Cloudflare + بهترین پورت
- ⚙️ **تنظیمات سفارشی** - Max Scan Count, Max Ping, IP Ranges
- 📊 **نتایج دقیق** - تغییر خودکار Address, Port, Remark
- --> با تشکر ویژه از [@EmadN87](https://github.com/emadn87) عزیز برای بازطراحی UI پروژه
- تشکر از تمامی کسانی که این وب اپلیکیشن رو در جهت کمک به هموطنانمون اشتراک گذاری کردند و همچنین تشکر ویژه از خانواده ی بزرگ IRCF

⚠️ **توجه :**  
قبل از شروع تست، لطفاً فیلترشکن یا VPN خود را خاموش کنید تا فرایند تحلیل بدون اختلال انجام شود.

🚀 [ورود به ابزار](https://najidevs.github.io/cf-v2ray-optimizer/)

---

## 🇺🇸 English Description

This tool helps you optimize your custom V2Ray configurations created using Cloudflare Workers and boosts their performance to the highest possible speed.

🔧 **New Features:**
- 🌐 **Persian & English Language Support** - Switch languages with one click
- 🎨 **Modern & Beautiful UI** - Enhanced design with attractive animations
- 📱 **Responsive Design** - Compatible with all devices
- ⚡ **Optimized Performance** - High speed and better user experience
- 🔄 **Notification System** - Instant feedback for users
- 💾 **Settings Persistence** - Remember user's language preference
- 🌐 **Multi-Protocol Support** - VLESS, Trojan, VMESS, and JSON Fragmented
- 🔍 **Cloudflare Clean IP Scanning** - Find the fastest clean IPs with low latency
- 🎯 **Two Optimization Modes:**
  - 🌍 **Domain Mode** - Use the best domain + best port
  - 🔗 **Clean IP Mode** - Scan Cloudflare IPs + best port
- ⚙️ **Custom Settings** - Max Scan Count, Max Ping, IP Ranges
- 📊 **Accurate Results** - Automatic modification of Address, Port, Remark
- --> Special Thanks For Dear [@EmadN87](https://github.com/emadn87) For Redesigning Project`s UI

⚠️ **Important Note:**  
Before starting the analysis, make sure to turn off any active VPN to ensure accurate testing.

🚀 [Launch the Tool](https://najidevs.github.io/cf-v2ray-optimizer/)

---

## 📁 Project Structure

```
cf-v2ray-optimizer/
├── cf-v2ray-optimizer.html  # Main optimizer HTML file
├── cf-ip-scanner.html       # IP Scanner tool (helper)
├── css/
│   └── style.css            # Styles and animations
├── js/
│   └── app.js               # JavaScript functionality & optimization logic
├── assets/
│   └── Logo.png             # Project logo
├── config-samples.txt       # Sample configurations (VMESS, Fragmented JSON)
├── LICENSE                  # Project license
└── README.md                # Project documentation
```

## 🛠️ Technologies Used

- **HTML5** - Semantic markup
- **CSS3** - Modern styling with animations
- **JavaScript ES6+** - Dynamic functionality & config parsing
- **Font Awesome** - Icons
- **Google Fonts** - Typography (Vazirmatn, Fira Code)

---

## 📖 How to Use

### **Step 1: Choose Optimization Mode**
- **Domain Mode**: Finds the best accessible domain and port
- **Clean IP Mode**: Scans Cloudflare IP ranges for the lowest latency IPs

### **Step 2: Paste Your Config**
Supported formats:
- `vless://userid@domain:port?params#name`
- `trojan://password@domain:port?params#name`
- `vmess://[base64-encoded-json]`
- `{json-fragmented-config}`

### **Step 3: Configure (if using IP Mode)**
- **Max Scan Count**: Maximum number of IPs to scan (default: 500)
- **Max Ping**: Maximum acceptable latency in ms (default: 200)

### **Step 4: Optimize & Copy**
Click "بهینه‌سازی کن" (Optimize Now) and the tool will:
1. Test domains/IPs for latency
2. Test ports for compatibility
3. Generate optimized config with Remark: `☁️ | Optimized With CF V2ray Optimizer | @NajiDevs[GITHUB]`

---

## 🔄 Supported Protocols

| Protocol | Support | Auto-Detection |
|----------|---------|-----------------|
| VLESS | ✅ Full | ✅ Yes |
| Trojan | ✅ Full | ✅ Yes |
| VMESS | ✅ Full (Base64) | ✅ Yes |
| JSON Fragmented | ✅ Full | ✅ Yes |

---

## 🌟 Key Functions

### Config Parsing
- `parseVLESS()` - Parse VLESS protocol
- `parseTrojan()` - Parse Trojan protocol
- `parseVMESS()` - Decode and parse VMESS (Base64)
- `parseJSON()` - Parse JSON fragmented configs
- `detectConfigType()` - Auto-detect config format

### Optimization
- `optimizeWithDomain()` - Optimize using best domain
- `scanAndOptimizeWithIP()` - Scan and optimize using clean IPs
- `buildOptimizedConfig()` - Build final optimized config

### IP Scanning
- `getRandomIpFromRanges()` - Generate random IP from CIDR
- `measureIPLatency()` - Measure ping for IP
- `CLOUDFLARE_RANGES` - Pre-defined Cloudflare IP ranges

---

## 🎨 Features Highlight

✨ **Smart Optimization**
- Automatically detects config type
- Chooses best domain or IP based on latency
- Tests multiple ports for compatibility
- Preserves all original parameters

🚀 **Performance**
- Parallel testing (batch processing)
- Configurable scan limits
- Real-time progress feedback
- Instant notifications

🔒 **User-Friendly**
- Bilingual interface (Persian/English)
- One-click language switching
- Dark theme UI
- Responsive design

---

## 📝 License

This project is open-source and available under the LICENSE file.

---

## 🙏 Credits

- Special thanks to [@EmadN87](https://github.com/emadn87) for UI redesign
- Thanks to all contributors who helped spread this tool
- Special thanks to the IRCF community

---

**Made with ❤️ for bypassing internet censorship**
