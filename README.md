# BTL_ATBMTT
🎮 Game “Hệ thống mã hóa ngân hàng”
🏦 Nhóm đề tài: Phát triển game giáo dục – mô phỏng bảo mật
🔒 Đề tài 23: Game “Hệ thống mã hóa ngân hàng”
📜 Mô tả trò chơi
Trò chơi mô phỏng quy trình bảo mật giao dịch ngân hàng, cho phép người chơi hóa thân thành quản trị viên bảo mật của một tổ chức tài chính. Mỗi ngày, hàng loạt giao dịch (chuyển khoản, rút – nạp tiền…) được gửi đến. Nhiệm vụ của người chơi là:

🔐 Mã hóa dữ liệu giao dịch
🛡️ Xác thực nguồn gốc giao dịch
📑 Kiểm tra tính toàn vẹn của thông điệp
🔑 Các thuật toán bảo mật chính
AES (Advanced Encryption Standard)
Mã hóa nội dung giao dịch (số tài khoản, số tiền, thông tin người nhận…) để đảm bảo tính bảo mật.
RSA (Rivest–Shamir–Adleman)
Ký số và xác thực giao dịch, bảo vệ chống giả mạo.
SHA (Secure Hash Algorithm)
Sinh giá trị hash để kiểm tra xem dữ liệu có bị thay đổi trong quá trình truyền tải hay không.
📖 Cốt truyện & Cách thức chơi
Bối cảnh

Người chơi là Quản trị viên Bảo mật của Ngân hàng.
Mỗi “ngày” ảo, ngân hàng nhận hàng loạt giao dịch với độ phức tạp tăng dần.
Hacker “ảo” liên tục thử tấn công, yêu cầu người chơi nâng cấp bảo mật.
Luồng xử lý giao dịch

Bước 1 – Mã hóa (AES): Chọn khóa 128/192/256-bit để mã hóa thông tin giao dịch.
Bước 2 – Xác thực (RSA): Khách hàng ký giao dịch bằng khóa riêng; hệ thống kiểm tra chữ ký bằng khóa công khai.
Bước 3 – Kiểm tra tính toàn vẹn (SHA): So sánh giá trị hash trước và sau truyền tải.
Cách thức chơi

Khi có giao dịch đến, người chơi lần lượt thực hiện ba bước bảo mật trên.
Hệ thống cung cấp phản hồi ngay lập tức sau mỗi bước:
✅ “Mã hóa AES thành công”
✅ “Xác thực RSA hợp lệ”
✅ “Tính toàn vẹn giao dịch được đảm bảo”
Các cấp độ thử thách

🔰 Cấp độ 1: Giao dịch đơn giản, khối lượng nhỏ, khóa ngắn.
⚡ Cấp độ 2: Tăng số lượng giao dịch, yêu cầu chọn khóa dài hơn, xử lý nhanh.
🚀 Cấp độ 3: Giao dịch phức tạp, nhiều thông tin, hacker gia tăng tần suất tấn công.
🎯 Điểm số và phản hồi

Nhận điểm dựa trên độ chính xác và tốc độ hoàn thành từng bước bảo mật.
Phản hồi chi tiết (toast/pop-up) hướng dẫn nếu thao tác sai hoặc thiếu bước.
🔨 Quy trình phát triển game
Xây dựng thuật toán bảo mật

AES: cài đặt hàm mã hóa/giải mã, quản lý khóa.
RSA: tạo cặp khóa, ký/xác minh chữ ký số.
SHA: sinh và so sánh giá trị hash.
Thiết kế giao diện người chơi

🖥️ Màn hình Giao dịch: Liệt kê giao dịch cần xử lý, thông tin chi tiết.
🎛️ Màn hình Thực hiện: Nhập lựa chọn khóa, các nút “Mã hóa”, “Xác thực”, “Kiểm tra”.
📈 Màn hình Kết quả: Hiển thị trạng thái từng bước và tổng điểm.
Lập trình logic xử lý

Quản lý luồng từ nhận giao dịch đến hoàn tất ba bước bảo mật.
Kiểm soát thời gian và độ bảo mật tương ứng.
Xử lý lỗi: khóa sai, chữ ký không hợp lệ, hash không khớp.
Tối ưu và mở rộng

Cân bằng giữa bảo mật (độ dài khóa, số vòng thuật toán) và hiệu năng.
Thêm thử thách mới: tấn công “man-in-the-middle”, giao dịch đa chữ ký, v.v.
