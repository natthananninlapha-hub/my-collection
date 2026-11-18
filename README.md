# My Collection: ขึ้น Vercel

## 1) ตั้ง Firebase (ฟรี ~5 นาที)
1. console.firebase.google.com > Add project
2. Build > Authentication > Get started > เปิด **Google**
3. Build > Firestore Database > Create (โหมด production) แล้วไปแท็บ Rules วางเนื้อหาจาก `firestore.rules` > Publish
4. Project settings > Your apps > `</>` Web > ลงทะเบียนแอป แล้วคัดลอก config
5. เปิดไฟล์ `firebase-config.js` วางค่าที่คัดลอกมาแทนที่

## 2) ขึ้น Vercel
- ทางง่าย: อัปโหลดโฟลเดอร์นี้ขึ้น GitHub > vercel.com > Add New Project > เลือก repo
  (Framework Preset = **Other**, ไม่ต้องใส่ Build Command)
- หรือใช้ CLI: `npx vercel` ในโฟลเดอร์นี้

## 3) อนุญาตโดเมน (สำคัญ ไม่งั้นล็อกอิน Google ไม่ได้)
Firebase > Authentication > Settings > Authorized domains > เพิ่มโดเมน `xxx.vercel.app` และโดเมนของคุณ

## หมายเหตุ
- รูปถูกบีบเป็น 800x1000 JPEG แล้วเก็บใน Firestore (ไม่ต้องใช้ Storage จึงไม่ต้องผูกบัตร)
- ข้อมูลแยกตามบัญชี Google ตามกฎใน firestore.rules
