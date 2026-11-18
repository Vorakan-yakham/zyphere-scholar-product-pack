# Zyphere — เรียนรู้ไปพร้อมนักพัฒนา

ทุกการกระทำถูกบันทึกและสอนเข้า LocalBrain/DevBrain

จำนวนการกระทำ: 2

## Audit โค้ดก่อนพัฒนา (15:05)

- เครื่องมือ: subagent/explore
- รายละเอียด: ตรวจ 100 ไฟล์ app.py 5864 บรรทัด 278 endpoints พบ credential ฝังใน set_pw.py
- ผล: แก้เป็น env var แล้ว
- บทเรียน: ก่อนพัฒนาต้อง audit จริง ห้ามเชื่อตัวเลขที่ระบบรายงานเอง

## แก้ import order (15:05)

- เครื่องมือ: edit
- รายละเอียด: EBOOK/STORE import ก่อน MEDIA_DIR กำหนด ทำให้ endpoint 400 unavailable
- ผล: ย้าย import หลัง MEDIA_DIR
- บทเรียน: ตัวแปรต้องกำหนดก่อนโมดูลที่ใช้มันเสมอ
