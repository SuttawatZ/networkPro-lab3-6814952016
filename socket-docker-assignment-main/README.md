# รายงานแบบฝึกหัด Socket API & Docker (Assignment 1 & 2)

**ข้อมูลผู้จัดทำ**
* ชื่อ-นามสกุล: นายสุทธวัฒน์ ยะสุนทร
* รหัสนักศึกษา: 6814952016
* กลุ่ม/เซคชั่น: 2

---

## 🛠️ แบบฝึกหัดที่ 1: ระบบ Chat ด้วย Docker (2 Clients & 1 Server)

### คำอธิบายการทำงาน
ระบบแชทนี้ประยุกต์ใช้ Socket API แบบ TCP ในการส่งข้อมูลระหว่าง Client 2 ตัว ผ่าน Server กลาง โดยรันอยู่ในรูปแบบของ Docker Multi-container

### ขั้นตอนการเริ่มทำงาน (How to run)
1. เปิด Terminal และเข้าไปที่โฟลเดอร์แบบฝึกหัดที่ 1:
   ```bash
   cd exercise-1
   ```
2. สั่งรันคอนเทนเนอร์ทั้งหมดผ่าน Docker Compose:
   ```bash
   docker-compose up --build
   ```
3. การเข้าใช้งาน Client:
   * เปิด Terminal ใหม่เพื่อเข้าคอนเทนเนอร์ Client 1:
```bash
docker exec -it chat_client1 python client.py
```
   * เปิด Terminal ใหม่เพื่อเข้าคอนเทนเนอร์ Client 2:
```bash
docker exec -it chat_client2 python client.py
```
4. หยุดการทำงานของคอนเทนเนอร์:
   ```bash
   docker-compose down
   ```

exercise-1
<img width="1920" height="1080" alt="สกรีนช็อต 2026-11-26 110825" src="https://github.com/user-attachments/assets/6d8d579f-b245-4b93-8169-08e3f11880c3" />
<img width="1920" height="1080" alt="สกรีนช็อต 2026-11-26 110830" src="https://github.com/user-attachments/assets/434cd2e4-9070-418b-be00-bc4d6a3f69c4" />
<img width="1920" height="1080" alt="สกรีนช็อต 2026-11-26 111047" src="https://github.com/user-attachments/assets/abb9231a-0131-43d0-aeba-e8d4f9119b2d" />

---

## 🌐 แบบฝึกหัดที่ 2: Web Application เชื่อมต่อ Socket Server

### คำอธิบายการทำงาน
เว็บแอปพลิเคชันสร้างด้วย Python (Flask) รับข้อความจากฟอร์มหน้าเว็บผ่าน POST method แล้วส่งต่อไปยัง Socket Server เพื่อรับค่าตอบกลับแบบ Echo แสดงผลบนหน้าเว็บ

### ขั้นตอนการเริ่มทำงาน (How to run)
1. เปิด Terminal และเข้าไปที่โฟลเดอร์แบบฝึกหัดที่ 2:
   ```bash
   cd exercise-2
   ```
2. สั่งรันคอนเทนเนอร์ทั้งหมดผ่าน Docker Compose:
   ```bash
   docker-compose up --build
   ```
3. ทดสอบการใช้งานผ่านเบราว์เซอร์:
   * เปิดเว็บเบราว์เซอร์แล้วเข้าไปที่ `http://localhost:5000`
   * กรอกข้อความลงในฟอร์มและกดปุ่ม **Send** เพื่อดูผลลัพธ์การตอบกลับจาก Socket Server
4. หยุดการทำงานของคอนเทนเนอร์:
   ```bash
   docker-compose down
   ```

   exercise-2
  <img width="1920" height="1080" alt="สกรีนช็อต 2026-11-26 111705" src="https://github.com/user-attachments/assets/47d7e9b2-db09-45e6-9d03-62700b66a208" />
  <img width="1920" height="1080" alt="สกรีนช็อต 2026-11-26 111650" src="https://github.com/user-attachments/assets/27e9d2a1-8bfa-43a2-ba6f-321f48f688ac" />

   
