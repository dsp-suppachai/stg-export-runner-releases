# STG Export Runner — ไฟล์ติดตั้ง

## ⬇ [ดาวน์โหลดตัวติดตั้ง (STGExportRunner-Setup.exe)](https://github.com/dsp-suppachai/stg-export-runner-releases/releases/latest/download/STGExportRunner-Setup.exe)

หรือ [ไฟล์โปรแกรมอย่างเดียว (STGExportRunner.exe)](https://github.com/dsp-suppachai/stg-export-runner-releases/releases/latest/download/STGExportRunner.exe) — ไม่ต้องติดตั้ง

ลิงก์นี้ชี้ไปที่เวอร์ชันล่าสุดเสมอ · ดูประวัติทุกเวอร์ชันที่ [Releases](https://github.com/dsp-suppachai/stg-export-runner-releases/releases)

repo นี้เก็บเฉพาะไฟล์โปรแกรม (`STGExportRunner.exe`) ของแต่ละเวอร์ชัน
โปรแกรมที่ติดตั้งแล้วจะตรวจและดาวน์โหลดเวอร์ชันใหม่จากที่นี่เอง (⚙ ตั้งค่า → เวอร์ชันโปรแกรม)

แต่ละ release มี:
- `STGExportRunner-Setup.exe` — ตัวติดตั้ง (Start Menu, ไอคอน Desktop, เปิดอัตโนมัติตอนเข้า Windows, ถอนได้จาก Settings → Apps)
- `STGExportRunner.exe` — ตัวโปรแกรม (ไฟล์เดียว ไม่ต้องติดตั้ง)
- `STGExportRunner.exe.sha256` — ค่าตรวจสอบไฟล์ (โปรแกรมตรวจก่อนติดตั้งทุกครั้ง ไม่ตรง = ไม่ติดตั้ง)
- `latest.json` — เวอร์ชันล่าสุด + รายการเปลี่ยนแปลง

## ติดตั้งบนเครื่องใหม่
1. ดาวน์โหลด `STGExportRunner-Setup.exe` จาก Release ล่าสุด แล้วเปิด — ไฟล์ไม่ได้ sign ถ้า Windows ขึ้น "Windows protected your PC" ให้กด **More info → Run anyway**
2. กด Next ไปตามขั้นตอน (ไม่ต้องใช้สิทธิ์ admin) — ถ้าเครื่องนี้ใช้ตั้งเวลารัน ให้ติ๊ก **เปิดโปรแกรมอัตโนมัติเมื่อเข้า Windows**
   (หรือใช้ `STGExportRunner.exe` ตัวเดียวแบบไม่ติดตั้ง วางไว้ในโฟลเดอร์ที่ต้องการก็ได้)
3. กด **Sign in with Microsoft** (บัญชีเดียวกับ ESS) — ครั้งต่อไปโปรแกรมจำบัญชีไว้ เข้าได้เลย
4. ไปที่ **⚙ ตั้งค่า** แล้วตั้งค่าต่อเครื่อง:
   - **เครื่องนี้ใน DSP** — ชื่อเครื่องตาม Settings › PC ของ DSP Console
   - **รหัสผ่าน SurveyToGo** (เข้ารหัสเก็บเฉพาะเครื่องนี้)
   - **SurveyToGo Studio** — โปรแกรมสแกนหาเวอร์ชันให้เอง (เลือก “ล่าสุดอัตโนมัติ”)
   - **Google Sheet** — เลือกไฟล์ key ของ Service Account (ขอจากผู้ดูแล)
   - กด 💾 บันทึก

ข้อมูลของแต่ละเครื่อง (ตั้งค่า, log, ประวัติตั้งเวลา) อยู่ที่ `%APPDATA%\STGExportRunner` — อัปเดตโปรแกรมแล้วไม่หาย
