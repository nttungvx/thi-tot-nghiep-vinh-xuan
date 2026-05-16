# Hệ Thống Thi Trắc Nghiệm THPT (Chuẩn định dạng 2026)

Nền tảng Thi Tốt nghiệp THPT trực tuyến. Đây là hệ thống thi tốt nghiệp mô phỏng chính xác cấu trúc đề thi và cách tính điểm mới nhất của Bộ GD&ĐT áp dụng từ năm 2026.
Lưu ý: Web được thiết kể để học sinh tự làm bài & luyện tập (không có lưu lại điểm số)

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/72cfbbe2-b966-4fbe-8405-a735dd544b1f" />

## Hướng dẫn sử dụng cho Học Sinh

1. Truy cập vào đường link trang web [(Trang GitHub)](https://nttungvx.github.io/thi-tot-nghiep-vinh-xuan/).
2. Tại màn hình chính, bấm **CHỌN ĐỀ TỪ THƯ VIỆN ONLINE**.

<img width="1763" height="844" alt="image" src="https://github.com/user-attachments/assets/ec6d1d15-78a7-430e-b44e-71c591a3ae93" />

3. Chọn môn học từ Menu thả xuống và click chọn đề thi bạn muốn làm.

<img width="1763" height="844" alt="image" src="https://github.com/user-attachments/assets/be34d3fd-4334-4f5e-89a1-e3eb456d8782" />

4. Tùy chỉnh cài đặt phòng thi (Thời gian, Đảo mã đề, Chế độ luyện tập...).

<img width="1763" height="844" alt="image" src="https://github.com/user-attachments/assets/c62f1ada-a599-4c80-8e41-532e45735e6a" />

5. Bấm **TẠO PHÒNG THI** và **BẮT ĐẦU LÀM BÀI**.

<img width="1763" height="844" alt="image" src="https://github.com/user-attachments/assets/c2e15b94-7e05-4004-a2ba-90db4cf476b4" />

---

## Tính năng nổi bật

- **Đúng chuẩn 2026:** Hỗ trợ đầy đủ 3 phần thi (Trắc nghiệm nhiều lựa chọn, Đúng/Sai, Trả lời ngắn) với thuật toán chấm điểm đúng với format của Bộ (Phần 2 chấm theo thang 0.1 - 0.25 - 0.5 - 1.0).
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/1f9d8d3c-62d0-4b95-a193-c8dbba91f937" />

- **Thư viện Online tự động:** Đọc dữ liệu trực tiếp từ GitHub, tự động phân loại theo môn học.
- **Tối ưu hóa đa thiết bị (Responsive):** Giao diện xịn sò, mượt mà trên cả Máy tính, Máy tính bảng và Điện thoại di động.
<img width="459" height="1020" alt="image" src="https://github.com/user-attachments/assets/ff3e06a5-3c85-4c96-8845-defe3259a588" />

- **Tính năng mở rộng:** Chế độ Luyện tập (chấm điểm ngay), Đảo mã đề ngẫu nhiên, Đồng hồ đếm ngược/đếm tiến, Chế độ Dark Mode OLED bảo vệ mắt.
- **Công cụ Đóng gói đề thi (Packager):** Tích hợp sẵn bộ công cụ kết hợp với AI (Gemini/ChatGPT) để số hóa đề thi file Word/PDF thành file JSON siêu tốc, hỗ trợ chèn ảnh trực tiếp bằng thao tác Copy-Paste (Ctrl+V).
<img width="1919" height="1020" alt="image" src="https://github.com/user-attachments/assets/6f36e44b-6211-474d-bc9c-004a73e03476" />

---

## Cấu trúc hệ thống

Dự án bao gồm 3 thành phần chính:

1. `index.html`: Web giao diện làm bài thi dành cho học sinh.
2. `packager.html`: Công cụ số hóa và đóng gói đề thi dành cho giáo viên/người ra đề.
3. Thư mục `/data`: Nơi chứa toàn bộ các file đề thi (định dạng `.json`). Hệ thống sẽ tự động quét thư mục này để hiển thị lên Thư viện.

---

## 🛠️ Hướng dẫn Số hóa Đề thi (Dành cho Giáo viên)

Để đưa một đề thi mới từ file Word/PDF lên hệ thống, bạn chỉ mất khoảng 3-5 phút với **Công cụ Đóng Gói (Packager)**.

### Bước 1: Nhờ AI trích xuất dữ liệu
- Mở trang **[MỞ BỘ ĐÓNG GÓI ĐỀ]** (`packager.html`).
- Tại phần **Bước 0**, bấm nút **COPY PROMPT** để lấy "Thần chú".
<img width="1763" height="844" alt="image" src="https://github.com/user-attachments/assets/02f56625-7e33-4761-bae1-a2b1c16e6486" />

- Mở ChatGPT hoặc Google Gemini, dán "Thần chú" này vào kèm theo file Word/PDF (hoặc ảnh chụp) đề thi của bạn. AI sẽ trả về cho bạn một đoạn mã JSON.

<img width="1763" height="844" alt="image" src="https://github.com/user-attachments/assets/7c70902e-1558-4357-a44d-f9959dab6cf1" />

### Bước 2: Nạp dữ liệu vào Packager
- Copy đoạn mã JSON mà AI vừa tạo.
- Quay lại trang Packager, dán đoạn mã đó vào ô **"Dán trực tiếp Code JSON"** ở Bước 1 và bấm **XỬ LÝ CODE JSON**.
<img width="1901" height="904" alt="image" src="https://github.com/user-attachments/assets/b9d93684-9a3b-4383-b258-6623ff2f8b81" />

### Bước 3: Chèn Hình Ảnh (Nếu có)
Nếu đề bài hoặc lời giải có hình ảnh/đồ thị, hệ thống sẽ tự động nhận diện và mở ra khu vực **Bước 2 (Quản lý Hình Ảnh)**.
- Dùng công cụ chụp màn hình (Snipping Tool / Lightshot) chụp ảnh đồ thị từ file gốc.
- Click chuột vào ô nét đứt tương ứng trên web và ấn **Ctrl + V** để dán ảnh vào.
- *Lưu ý: Nhãn màu xanh là ảnh của Câu hỏi, Nhãn màu tím là ảnh của Lời giải.*

<img width="1763" height="844" alt="image" src="https://github.com/user-attachments/assets/a5c2c1d1-3a4e-454e-886f-ed8b189199bb" />

### Bước 4: Sửa lỗi (Nếu cần)
- Nếu AI trích xuất sai một chữ nào đó, bạn mở **Trình sửa code** để sửa nhanh nội dung của từng câu hỏi một cách an toàn.
<img width="1889" height="900" alt="image" src="https://github.com/user-attachments/assets/675b0fe6-f0aa-4c08-ac74-e077751b271a" />

### Bước 5: Xuất file và Đăng tải
- Cuộn xuống cuối cùng, bấm **TẢI XUỐNG FILE .JSON**. Hệ thống sẽ tự động đặt tên file cực chuẩn (VD: `Toán _ Đề khảo sát lần 1.json`).
- Mở kho GitHub repository này, kéo thả file vừa tải về vào trong thư mục `data`. (up bởi admin/mn có thể tự lưu vào máy để tự up lên web làm)
- Chờ khoảng 1 phút, đề thi mới sẽ tự động xuất hiện trên Thư viện trực tuyến của web thi!

---


---
*Phát triển bởi Gemini (idea ý tưởng và tính năng: almay4024)*