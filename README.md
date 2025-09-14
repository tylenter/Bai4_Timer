CÁC BƯỚC THỰC HIỆN:
1. Cấu hình GPIO:
   -PA5: Output push-pull (kết nối LED).
<img width="563" height="170" alt="image" src="https://github.com/user-attachments/assets/c7a7d1b5-86ef-4d50-b46e-47b5b5fcbb86" />

2. Cấu hình Timer 2:
   - Prescaler = 71 → mỗi 1 µs đếm tăng 1.
   - ARR = 0xFFFF → dùng cho delay.
   - Bật Timer2 để làm bộ đếm thời gian.
<img width="654" height="180" alt="image" src="https://github.com/user-attachments/assets/00ef2b9d-90a6-4200-8608-6f8ff14ff8af" />

3. Hàm delay
   - Tạo delay theo đơn vị ms bằng cách reset CNT và chờ đủ 1000 µs cho mỗi 1 ms.
<img width="654" height="201" alt="image" src="https://github.com/user-attachments/assets/d10b38cc-88f6-4b7e-b52d-76abcb8dcec3" />

4. Chương trình chính:
   - LED tại PA5 sẽ nhấp nháy với chu kỳ 1 Hz (500 ms ON, 500 ms OFF).
<img width="710" height="298" alt="image" src="https://github.com/user-attachments/assets/313c5235-dc3a-463e-84ab-5220e81e5273" />

5. Kết quả:
   - LED tại PA5: Nhấp nháy tần số 1 Hz (chu kỳ 1 giây).
