# Xin chao GitHub
# ==============================================================================
# HƯỚNG DẪN SỬ DỤNG GIT & GITHUB CHI TIẾT
# Bạn có thể chạy các lệnh này trực tiếp trong Git Bash
# ==============================================================================

# ------------------------------------------------------------------------------
# BƯỚC 1: KHAI BÁO THÔNG TIN CÁ NHÂN (Chỉ cần làm 1 lần duy nhất khi cài Git)
# ------------------------------------------------------------------------------
# Giúp GitHub biết ai là người tạo ra các điểm lưu (commit)
git config --global user.name "tunglt1697"
git config --global user.email "thangtung0106997@gmail.com"

# Tùy chọn: Tự động xử lý ký tự xuống dòng giữa Windows và Linux/Mac để tránh warning
git config --global core.autocrlf true


# ------------------------------------------------------------------------------
# BƯỚC 2: QUY TRÌNH KẾT NỐI DỰ ÁN LẦN ĐẦU TIÊN (Initial Setup)
# ------------------------------------------------------------------------------
# 1. Khởi tạo Git trong thư mục hiện tại (tạo một kho chứa ẩn .git)
git init

# 2. Đưa file README.md vào khu vực chờ đóng gói (Staging Area)
# (Mẹo: Thay 'README.md' bằng dấu '.' để chọn TẤT CẢ các file có trong thư mục)
git add README.md

# 3. Chốt danh sách file và dán nhãn ghi chú cho lần lưu này
git commit -m "Tao file README va khoi tao du an"

# 4. Đổi tên nhánh mặc định từ 'master' sang 'main' (chuẩn của GitHub hiện tại)
git branch -M main

# 5. Liên kết thư mục máy tính với đường link kho chứa trên GitHub (đặt tên tắt là 'origin')
git remote add origin https://github.com/tunglt1697/Begin_with_Git.git

# 6. Đẩy toàn bộ dữ liệu lên GitHub lần đầu tiên (-u giúp ghi nhớ nhánh cho các lần sau)
git push -u origin main


# ------------------------------------------------------------------------------
# BƯỚC 3: QUY TRÌNH LÀM VIỆC HÀNG NGÀY (Daily Workflow)
# ------------------------------------------------------------------------------
# Mỗi khi bạn sửa code, thêm file mới hoặc xóa file, chỉ cần chạy 3 lệnh sau:

# Lệnh 1: Gom tất cả các file đã chỉnh sửa/tạo mới vào khu vực chờ
git add .

# Lệnh 2: Đóng gói và ghi rõ bạn vừa sửa/thêm tính năng gì
git commit -m "Cap nhat noi dung moi"

# Lệnh 3: Đẩy bản cập nhật mới nhất lên GitHub
git push