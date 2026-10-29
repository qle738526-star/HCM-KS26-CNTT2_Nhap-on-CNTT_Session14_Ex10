**Phần 1: Phân tích & Đề xuất**

1. Phân tích bài toán:

* Đầu vào: Nhu cầu trao đổi đa nền tảng của 5 sinh viên (gửi code, file, phân công việc) trong bối cảnh chạy deadline và giao tiếp ngoại bộ.
* Đầu ra: Một nền tảng lưu trữ vĩnh viễn, chống trôi tin nhắn, hỗ trợ giao tiếp bất đồng bộ và quản lý tiến độ.

2. Ưu nhược điểm:

* Giải pháp A (Zalo): Quen thuộc, dễ kết nối đối tác. Nhược điểm là trôi tin nhắn, mất file sau vài tháng, không có chức năng quản lý công việc.
* Giải pháp B (Lark): Phân luồng tốt, lưu trữ vĩnh viễn, tích hợp công việc. Nhược điểm là tốn thời gian học cách dùng ban đầu.

**Phần 2: So sánh & Lựa chọn**

3. Bảng so sánh 5 tiêu chí:

| Tiêu chí | Giải pháp A (Zalo) | Giải pháp B (Lark Suite) |
| --- | --- | --- |
| 1. Ngăn chặn tin nhắn trôi | Kém | Tốt |
| 2. Quản lý công việc (Task) | Kém | Tốt |
| 3. Độ miễn phí & dễ cài đặt | Tốt | Trung bình |
| 4. Tìm kiếm lịch sử (Lưu trữ) | Kém | Tốt |
| 5. Giao tiếp bất đồng bộ | Trung bình | Tốt |

4. Chốt lựa chọn & Xử lý bẫy:
Đề xuất dùng Mô hình Lai: Lark dùng cho nội bộ, Zalo dùng để giao dịch với đối tác.

* Bẫy 1 (Chỉ có điện thoại): Lark có app mobile đầy đủ tính năng nên Ban KD vẫn dùng bình thường.
* Bẫy 2 (Sát deadline): Giai đoạn này chỉ cần áp dụng Chat chia kênh và Docs trong Lark để làm quen nhanh trong 30 phút, khoan dùng các tính năng phức tạp.
* Bẫy 3 (Đối tác dùng Zalo): Giao tiếp qua Zalo bình thường, sau đó người phụ trách chụp màn hình hoặc tóm tắt ý chính đẩy sang Lark để lưu trữ.

**Phần 3: Thiết kế & Triển khai**

5. Cấu trúc 5 Channel cho CampusPay:

* #01-thong-bao: Kênh một chiều, chỉ Trưởng nhóm đăng thông báo quan trọng và deadline.
* #02-dev: Ban Kỹ thuật và Trưởng nhóm thảo luận code, API.
* #03-design: Ban Design và Trưởng nhóm duyệt UI/UX, slide.
* #04-kinh-doanh: Ban Kinh doanh báo cáo tiến độ thị trường.
* #05-giai-tri: Nơi tán gẫu, không bàn công việc.

6. Quy tắc chống Spam:

* Cấm @all bừa bãi: Chỉ cấp quyền dùng @all cho Trưởng nhóm tại kênh #01-thong-bao.
* Tag đích danh: Yêu cầu ai làm gì thì chỉ @Tên người đó kèm hạn chót.
* Bắt buộc dùng Thread: Mọi phản hồi phải nhắn vào bên trong Thread của tin gốc, tuyệt đối không nhắn ra luồng chính của Kênh.
