Dự án này được thiết kế để tự động hóa quy trình nhận hình ảnh từ Telegram, gửi qua API AI để chỉnh sửa theo yêu cầu và lưu trữ kết quả trực tiếp lên Google Drive với tên file được tùy biến.

## 🚀 Tính năng chính
- **Nhận dữ liệu:** Tự động lắng nghe ảnh và caption (yêu cầu) từ Telegram Bot.
- **Xử lý AI:** Kết nối với API (Stability AI) để chỉnh sửa ảnh dựa trên mô tả của người dùng.
- **Logic thông minh:** Sử dụng JavaScript để xử lý tên file tự động dựa trên "đoạn đề xuất" của người dùng.
- **Lưu trữ:** Đồng bộ hóa kết quả cuối cùng lên Google Drive.

## 🛠 Cấu trúc Workflow
Hệ thống bao gồm các Node chính:
1. **Telegram Trigger:** Tiếp nhận sự kiện tin nhắn mới.
2. **Get a file:** Tải file ảnh thực tế từ server Telegram.
3. **HTTP Request:** Gọi API AI để thực hiện chỉnh sửa hình ảnh.
4. **Code Node:** Xử lý dữ liệu nhị phân (Binary) và đổi tên file theo Caption.
5. **Google Drive Node:** Upload file hoàn thiện lên thư mục đám mây.

## 📂 Cách sử dụng dự án
1. Tải file `.json` đính kèm trong Repository này.
2. Tại giao diện n8n, chọn **Import from file** và tải file lên.
3. Cấu hình Credentials cá nhân cho Telegram, Google Drive và API Key của AI.
4. Nhấn **Execute Workflow** và gửi ảnh qua Bot để kiểm tra.
