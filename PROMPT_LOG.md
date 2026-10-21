NHẬT KÝ PROMPT ENGINEERING (PROMPT LOG)

Dự án: Thiết kế Website Quán Ăn Vặt "Ăn Cùng Chú Mập"

Thành viên thực hiện: Học viên / Sinh viên : Đặng Duy Nhật

Công cụ AI hỗ trợ: Gemini

Tệp tài liệu: PROMPT_LOG.md

🎯 1. TỔNG QUAN TƯ DUY TINH CHỈNH (ITERATION PROCESS)

Quá trình làm việc với AI được chia thành các giai đoạn rõ ràng:

Khởi tạo (Initialization): Định hình ý tưởng, giao diện Vintage/Retro cho quán ăn vặt tại Biên Hòa.

Phát hiện lỗi & Tinh chỉnh (Bug Detection & Refinement): AI bị lệch thông tin giữa tiêu đề món ăn, mô tả và hình ảnh minh họa.

Mở rộng tính năng (Feature Expansion): Yêu cầu bổ sung món ăn mới, viết lại toàn bộ CSS với các hiệu ứng tương tác hiện đại (Zoom image, hover animation, badge, custom scrollbar).

Kiểm soát & Chuẩn hóa (Quality Control): Bắt lỗi AI khi liên kết hình ảnh Unsplash không chính xác với món ăn Việt Nam, yêu cầu sửa đổi triệt để.

📝 2. CHI TIẾT CÁC BƯỚC HỎI - ĐÁP & CHỈ ĐẠO AI

Bước 1: Phát hiện lỗi lệch khớp giữa Tên món & Nội dung

Prompt (Người dùng):

"hiện tại code của bạn đang làm tên món và món ăn không trùng nhau làm lại đi"

Mục tiêu: Phát hiện và yêu cầu AI khắc phục lỗi hiển thị không đồng bộ dữ liệu món ăn trong thẻ HTML.

Tư duy kỹ thuật: Chỉ ra lỗi trực tiếp để AI tập trung vào cấu trúc HTML thẻ bài (.menu-card) và gán đúng tên, mô tả, giá tiền, gọi hàm addToCart() tương ứng.

Kết quả AI: AI đã cập nhật lại 4 món ăn chuẩn dữ liệu (Bánh Tráng Trộn, Chân Gà Sả Tắc, Trà Sữa Trân Châu, Xoài Dầm).

Bước 2: Yêu cầu mở rộng tính năng Menu & Bổ sung CSS

Prompt (Người dùng):

"thêm món và thêm code css nữa"

Mục tiêu: Mở rộng quy mô thực đơn lên 8 món ăn vặt phổ biến và yêu cầu thêm CSS để giao diện thêm bắt mắt.

Tư duy kỹ thuật: Bổ sung các UI Element mới như Huy hiệu (.badge.hot, .badge.new) để tăng tính trải nghiệm người dùng (UX) và tạo nút tùy chỉnh trong giỏ hàng.

Kết quả AI: AI bổ sung thêm 4 món mới (Cút lết xào me, Khoai tây chiên phô mai, Bắp xào bơ, Nem chua rán) và cung cấp đoạn code CSS mở rộng cùng file HTML hoàn chỉnh.

Bước 3: Đòi hỏi tối ưu hóa toàn bộ CSS (Toàn diện)

Prompt (Người dùng):

"code css từ đầu tới đuôi đi cho tôi dễ copy"

Mục tiêu: Nhận toàn bộ file stylesheet thống nhất (style.css), tránh việc nối đoạn code nhỏ lẻ gây rối file.

Tư duy kỹ thuật: Quản lý mã nguồn sạch (Clean Code), gom nhóm CSS Selector theo thứ tự hệ thống:

CSS Variables & Reset

Header & Glassmorphism Navigation

Hero Banner

About Section

Menu Grid & Product Cards

Modal Cart & Animations

Responsive Breakpoints

Kết quả AI: AI đã tổng hợp đầy đủ mã CSS hoàn chỉnh từ đầu đến cuối.

Bước 4: Sửa lỗi AI khi hình ảnh không khớp thực tế (Critical Bug Fix)

Prompt (Người dùng + Ảnh chụp màn hình):

"bạn đùa tôi hả tên món là món ăn không giống nhau nè sai tùm tum tôi hết kiên nhẫn rồi đấy"

Lỗi phát hiện qua Screenshots:

Bánh Tráng Trộn hiển thị ảnh Fastfood/Burger.

Chân Gà Sả Tắc hiển thị ảnh Gà rán chiên xù.

Xoài Keo Dầm hiển thị ảnh Ly Ice-blended.

Cút Lết Xào Me hiển thị ảnh Bánh Tacos.

Bắp Xào Bơ hiển thị ảnh Thịt nướng BBQ.

Nem Chua Rán hiển thị ảnh Bít tết bò.

Tư duy chỉ đạo (Prompt Engineering Direction):

Ép AI nhận diện đúng vấn đề từ việc tìm kiếm từ khóa ảnh ngẫu nhiên trên Unsplash.

Đòi hỏi AI thay thế chính xác URL ảnh hoặc hướng dẫn dùng ảnh cục bộ (assets/images/) chuẩn hóa cho ẩm thực Việt Nam.

Kết quả AI: AI đã xin lỗi, giải thích rõ nguyên nhân và thay lại toàn bộ danh sách đường link ảnh chuẩn xác cho món ăn Việt Nam, đồng thời cấp lại bộ mã CSS chuẩn.

Bước 5: Yêu cầu chốt mã nguồn CSS cuối cùng

Prompt (Người dùng):

"code css ddau"

Mục tiêu: Yêu cầu xuất lại file CSS đồng bộ 100% với file HTML mới chỉnh sửa.

Kết quả AI: Cung cấp lại file style.css đầy đủ cấu trúc, tích hợp đầy đủ variable, hiệu ứng hover, shadow, animation pulse badge và responsive.

🛠️ 3. ĐÁNH GIÁ KẾT QUẢ VÀ BÀI HỌC KINH NGHIỆM

Hiểu rõ giới hạn của LLM: AI khi sinh code HTML có thể dùng các đường link ảnh minh họa ngẫu nhiên (placeholder/Unsplash query) dẫn đến sai lệch ngữ cảnh món ăn Việt Nam. Người lập trình cần kiểm tra trực quan (Visual QA) và yêu cầu AI điều chỉnh.

Kỹ năng Prompting phân tầng: Khi làm việc với ứng dụng Web, cần chỉ đạo theo từng block riêng (HTML Grid structure -> CSS styling -> JS Logic) rồi mới tổng hợp lại toàn bộ file.

Quản lý cấu trúc mã: Việc sử dụng các biến CSS (:root) giúp dễ dàng quản lý tông màu Vintage (--primary-color: #3b271a, --accent-color: #d06f36), đảm bảo tính nhất quán trên toàn bộ trang web.
