# ML Model Selection Roadmap

สรุปบทเรียนแบบละเอียด สำหรับผู้เริ่มต้นที่อยากเข้าใจขั้นตอนการเลือกและประเมินโมเดล Machine Learning อย่างเป็นระบบ ตั้งแต่สำรวจข้อมูลไปจนถึงประเมินผลและวนกลับไปลองโมเดลตัวถัดไป

เขียนเป็นไฟล์ HTML เดี่ยว (single-file) ไม่มี dependency ภายนอกที่ต้องติดตั้ง เปิดดูได้ทันทีจากเบราว์เซอร์

## เนื้อหาในไฟล์

| หัวข้อ | เนื้อหา |
|---|---|
| 01 | EDA คือการสำรวจข้อมูลก่อนลงมือทำอะไร |
| 02 | การจัดการข้อมูลที่ขาดหาย (Missing Data) |
| 03 | สมมติฐานของแต่ละ Algorithm |
| 04 | Feature Encoding & Scaling |
| 05 | เลือก Algorithm ตัวแรกที่จะลอง |
| 06 | Train/Test Split เทียบกับ Cross-Validation |
| 07 | ประเมินผลและรู้ว่าเมื่อไหร่ควรลองโมเดลตัวถัดไป |

อ้างอิงจาก [scikit-learn 1.9.0 User Guide](https://scikit-learn.org/stable/user_guide.html) และเอกสารประกอบที่เกี่ยวข้อง

## วิธีเปิดดู

**แบบเร็วที่สุด** — ดับเบิลคลิกไฟล์ `ml-model-selection-roadmap.html` เปิดด้วยเบราว์เซอร์ได้เลย ไม่ต้องมีเซิร์ฟเวอร์หรือติดตั้งอะไรเพิ่ม

## วิธีแชร์เป็นเว็บไซต์

### วิธีที่ 1 — Netlify Drop (ง่ายสุด ไม่ต้องสมัคร)
1. เข้า https://app.netlify.com/drop
2. ลาก-วางไฟล์ HTML ลงไป (แนะนำเปลี่ยนชื่อเป็น `index.html` ก่อน)
3. ได้ลิงก์ทันที เช่น `random-name.netlify.app`

### วิธีที่ 2 — GitHub Pages
1. สร้าง repo ใหม่บน GitHub แล้วอัปโหลดไฟล์ (ตั้งชื่อเป็น `index.html`)
2. ไปที่ **Settings → Pages** เลือก branch `main` และโฟลเดอร์ `/root`
3. รอสักครู่ จะได้ลิงก์ `https://<username>.github.io/<repo>/`

### วิธีที่ 3 — Vercel
ลาก-วางไฟล์หรือเชื่อมกับ GitHub repo ได้เช่นกัน ได้ลิงก์แบบ `.vercel.app`

## โครงสร้างไฟล์

```
.
├── ml-model-selection-roadmap.html   # ไฟล์เว็บไซต์หลัก (self-contained)
└── README.md                          # ไฟล์นี้
```

## หมายเหตุ

- ฟอนต์และไอคอนโหลดจาก Google Fonts ผ่าน CDN จึงต้องมีอินเทอร์เน็ตตอนเปิดดูเพื่อให้ฟอนต์แสดงผลถูกต้อง (ถ้าไม่มีเน็ต จะ fallback ไปใช้ฟอนต์ระบบแทน ยังอ่านได้ปกติ)
- รูปแผนภาพ "Choosing the right estimator" โหลดจาก GitHub ของ scikit-learn โดยตรง
- รองรับทั้ง light mode และ dark mode ของเบราว์เซอร์/ระบบปฏิบัติการ
