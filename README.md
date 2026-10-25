# Train Interior Display Simulator / จำลองหน้าจอภายในรถไฟฟ้า

[English](#english) · [ภาษาไทย](#ภาษาไทย)

---

## English

A single-file web app (`train-display.html`, with CSS and JavaScript inline) that simulates the passenger information screen inside an electric train. No build step, no dependencies. Open the file in a browser.

### Screen layout

| Position | Content |
|---|---|
| Top left | Lines you can transfer to at the next station (or this station) |
| Top center | Whether the doors open on this side |
| Top right | Date and time |
| Center | Next / current station name (Thai and English) and station code. While approaching, blinking arrowheads on both sides point toward the front of the train, then fade out when the train stops |
| Bottom left | Line name, in the line's color |
| Bottom right | Destination station |
| Bottom strip | Scrolling announcement text |

The screen can be set to **16:9** or **21:9** (for wide screens), and can go fullscreen.

### Settings

- **Stations**: add, delete and reorder. Each station has a code, Thai and English names, a door side (left, right or both) and any number of interchange lines, each with a name and color.
- **Line**: Thai and English name, line color, which side of the train the screen is mounted on, and which side of the screen is the front of the train (the direction the arrows point).
- **Date and time**: real time or a simulated time; the simulated clock can keep ticking; Buddhist Era (BE) or Common Era (CE) year.
- **Announcements**: one line per message, scrolling speed, on/off.
- **Simulation**: automatic mode with adjustable approach and stop durations, or step manually with Previous / Next; switch direction; jump to any station.
- **Backup**: export, import and reset the configuration as JSON. Settings are also remembered in the browser (localStorage).

### Notes

- Door sides are defined relative to the **outbound direction**. On the return direction the app flips left/right automatically.
- The doors show "open on this side" when the station's door side matches the side the screen is mounted on, or when the station opens both sides.
- The arrow direction does not change on the return trip, because the front of the train stays the same.
- The sample data (a Blue Line with 9 stations and some interchange lines) is only an example. Edit it freely.
- The Noto Sans Thai font is loaded from Google Fonts. Offline, the system Thai font is used instead.

### Usage

1. Open `train-display.html` in a modern browser.
2. Use the buttons under the screen to run or step the simulation.
3. Edit the cards below to change the line, stations, time and announcements.

---

## ภาษาไทย

เว็บแอปไฟล์เดียว (`train-display.html` รวม CSS และ JavaScript ไว้ในไฟล์) สำหรับจำลองหน้าจอแสดงข้อมูลผู้โดยสารภายในรถไฟฟ้า ไม่ต้องติดตั้งหรือสร้างโปรเจกต์ เปิดไฟล์ด้วยเบราว์เซอร์ได้ทันที

### ส่วนประกอบของหน้าจอ

| ตำแหน่ง | เนื้อหา |
|---|---|
| มุมซ้ายบน | สายที่เปลี่ยนได้ที่สถานีถัดไปหรือสถานีนี้ |
| ตรงกลางด้านบน | ประตูเปิดฝั่งนี้หรือไม่ |
| มุมขวาบน | วันและเวลา |
| กลางจอ | ชื่อสถานีถัดไปหรือสถานีปัจจุบัน (ไทยและอังกฤษ) พร้อมรหัสสถานี ตอนรถกำลังเข้าสถานี หัวลูกศรที่กะพริบทั้งสองข้างจะชี้ไปทางด้านหน้าของรถ แล้วหายไปเมื่อรถจอด |
| มุมซ้ายล่าง | ชื่อสาย ในสีของสายนั้น |
| มุมขวาล่าง | สถานีปลายทาง |
| แถบล่างสุด | ข้อความประกาศเลื่อนวน |

เลือกขนาดหน้าจอได้ทั้ง **16:9** และ **21:9** (จอยาว) และดูแบบเต็มจอได้

### การตั้งค่า

- **สถานี**: เพิ่ม ลบ และเรียงลำดับได้ แต่ละสถานีมีรหัส ชื่อไทย ชื่ออังกฤษ ฝั่งประตู (ซ้าย ขวา หรือทั้งสองฝั่ง) และสายเชื่อมต่อได้หลายสาย โดยตั้งชื่อและสีของแต่ละสายได้
- **สายรถไฟฟ้า**: ชื่อสายไทยและอังกฤษ สีของสาย จอติดตั้งอยู่ฝั่งใดของตัวรถ และด้านหน้าของรถอยู่ทางใดของหน้าจอ (ทิศที่ลูกศรชี้)
- **วันและเวลา**: ใช้เวลาจริงหรือเวลาสมมุติ ให้เวลาสมมุติเดินต่อได้ และเลือกปี พ.ศ. หรือ ค.ศ.
- **ข้อความประกาศ**: หนึ่งบรรทัดต่อหนึ่งประกาศ ปรับความเร็วเลื่อนและเปิดปิดได้
- **การจำลอง**: โหมดอัตโนมัติ ปรับเวลาช่วงเข้าสถานีและช่วงจอดได้ หรือกด ย้อนกลับ/ถัดไป เอง สลับทิศทาง และเลือกไปยังสถานีใดก็ได้
- **สำรองข้อมูล**: ส่งออก นำเข้า และคืนค่าเริ่มต้นเป็น JSON นอกจากนี้ค่าที่ตั้งจะถูกจำไว้ในเบราว์เซอร์ (localStorage)

### ข้อควรรู้

- ฝั่งประตูของแต่ละสถานีนับตาม**ทิศทางขาไป** ตอนรถวิ่งขากลับ ระบบจะสลับซ้าย/ขวาให้อัตโนมัติ
- จะแสดง “ประตูเปิดฝั่งนี้” เมื่อฝั่งประตูของสถานีตรงกับฝั่งที่ติดตั้งจอ หรือสถานีนั้นเปิดทั้งสองฝั่ง
- ทิศของลูกศรไม่เปลี่ยนตอนขากลับ เพราะด้านหน้าของรถยังเป็นด้านเดิม
- ข้อมูลเริ่มต้น (สายสีน้ำเงิน 9 สถานี พร้อมสายเชื่อมต่อบางส่วน) เป็นเพียงตัวอย่าง แก้ไขได้ตามต้องการ
- ฟอนต์ Noto Sans Thai โหลดจาก Google Fonts หากออฟไลน์จะใช้ฟอนต์ไทยของเครื่องแทน

### วิธีใช้

1. เปิด `train-display.html` ด้วยเบราว์เซอร์รุ่นใหม่
2. ใช้ปุ่มใต้หน้าจอเพื่อเล่นอัตโนมัติหรือกดเปลี่ยนสถานะเอง
3. แก้ไขการ์ดด้านล่างเพื่อเปลี่ยนสาย สถานี วันเวลา และข้อความประกาศ
