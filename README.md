# Phycom_Arduino

🧩 วิธีที่ใช้ได้แน่นอนในห้องสอบพรุ่งนี้

🟢 วิธีที่ 1 — ใช้คอมของคณะ “แชร์ Wi-Fi 2.4 GHz” แทน iPhone
💡 วิธีนี้ดีที่สุด และ UNO R4 WiFi ต่อได้แน่นอน 100%

ขั้นตอน:
1. ต่อคอม Windows เข้ากับ iPhone Hotspot ตามปกติ
    * บน iPhone: เปิด Personal Hotspot → เปิด “Allow Others to Join”
    * บนคอม: ไปที่ Wi-Fi → เลือกชื่อ iPhone ของเรา → ใส่รหัส
2. ให้คอม “ปล่อย Wi-Fi ใหม่” แบบ 2.4 GHz ออกมา
    * บนคอม Windows:
        * ไปที่ 👉 Settings → Network & Internet → Mobile hotspot
        * เปิดสวิตช์ “Mobile Hotspot”
        * ตรง “Share my Internet connection from” → เลือก “Wi-Fi”
        * คลิก “Edit” แล้วตั้งชื่อ SSID และรหัสผ่านใหม่ (เช่น ArduinoLab / 12345678)
    * Windows จะปล่อย Hotspot 2.4 GHz ออกมาให้อัตโนมัติ ✅
3. ต่อ Arduino UNO R4 WiFi เข้ากับ Hotspot ใหม่นี้
    * ในโค้ด ใส่:
        * const char WIFI_SSID[] = "ArduinoLab";
        * const char WIFI_PASSWORD[] = "12345678"; 
    * Upload โค้ด แล้วดู Serial Monitor 
ถ้าขึ้น “WiFi connected!” → ต่อสำเร็จ 🎉
ตอนนี้ Arduino → ต่อ Wi-Fi จากคอม (2.4 GHz) ส่วนคอม → ได้อินเทอร์เน็ตจาก iPhone Hotspot (5 GHz) ทุกอย่างเชื่อมกันครบ ✅
