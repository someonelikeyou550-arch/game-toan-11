GAME ONLINE TOÁN 11 – HƯỚNG DẪN TRIỂN KHAI

Gói này là ứng dụng web có lưu kết quả học sinh vào SQLite. Nó chưa tự có địa chỉ Internet công khai; muốn học sinh ở nhà/trên điện thoại truy cập được, cần triển khai lên một dịch vụ host Node.js (ví dụ Render, Railway hoặc máy chủ của trường).

1) Tải và giải nén toàn bộ ZIP.
2) Tạo dịch vụ web Node.js từ thư mục này; lệnh cài đặt: npm install; lệnh chạy: npm start.
3) Cấu hình biến môi trường:
   TEACHER_PASSWORD = mật khẩu riêng do giáo viên đặt
   SESSION_SECRET = chuỗi bí mật dài, ngẫu nhiên
   NODE_ENV = production
4) Dịch vụ phải hỗ trợ lưu đĩa bền vững cho file quiz.db (persistent disk/volume), nếu không kết quả có thể mất khi máy chủ khởi động lại.
5) Mở https://TEN-MIEN-CUA-BAN/teacher, đăng nhập bằng mật khẩu đã đặt.
6) Chọn đáp án đúng cho từng câu ở phần Thiết lập đáp án rồi nhấn Lưu đáp án.
7) Bấm Tạo mã QR, tải ảnh QR và chiếu cho học sinh quét.
8) Học sinh nhập họ tên, lớp, làm bài. Giáo viên làm mới danh sách hoặc tải CSV để mở bằng Excel.

LƯU Ý QUAN TRỌNG
- QR chỉ được tạo ra với địa chỉ thật sau khi ứng dụng đã triển khai lên Internet. Không thể tạo QR truy cập online hợp lệ trước khi có URL công khai.
- Một số ký hiệu/công thức trong file Word gốc bị mất khi trích xuất. Bộ câu hỏi trong bản mẫu được chuẩn hóa lại một phần và có câu củng cố cùng chủ đề. Giáo viên cần rà soát nội dung và tự thiết lập đáp án trong trang quản trị trước khi giao bài.
- Không dùng mật khẩu mặc định. Không nhập thông tin nhạy cảm của học sinh.
