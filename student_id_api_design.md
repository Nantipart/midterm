| HTTP Method | Endpoint         | Description                 | Request Body                                      | Response (Success)              | Status Code |
| ----------- | ---------------- | --------------------------- | ------------------------------------------------- | ------------------------------- | ----------- |
| GET         | `/api/rooms`     | ดึงรายการห้องทั้งหมด        | -                                                 | `[{ room_id, name, capacity }]` | 200         |
| GET         | `/api/rooms/:id` | ดึงข้อมูลห้องเดียว          | -                                                 | `{ room_id, name, capacity }`   | 200         |
| POST        | `/api/rooms`     | เพิ่มห้องใหม่ (เจ้าหน้าที่) | `{ name, building, floor, capacity, facilities }` | `{ room_id, ... }`              | 201         |
| PUT         | `/api/rooms/:id` | แก้ไขข้อมูลห้อง             | `{ name, capacity }`                              | `{ updated_room }`              | 200         |
| DELETE      | `/api/rooms/:id` | ลบห้อง                      | -                                                 | `{ message: "deleted" }`        | 200         |


{
  "room_id": 101,
  "booking_date": "2026-01-15",
  "start_time": "09:00",
  "end_time": "12:00",
  "purpose": "ประชุมโครงงาน"
}
