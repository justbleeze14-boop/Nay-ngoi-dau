# Đi cà phê — Hanoi Coffee Shuffle

Bản xuất ngày 11/09/2026, chạy trực tiếp trên GitHub Pages. Không cần cài thư viện, chạy build, API key hay tài khoản ChatGPT.

## Đăng website bằng giao diện GitHub

1. Giải nén gói ZIP trên máy tính.
2. Tạo repository mới trên GitHub, đặt tên ví dụ `hanoi-coffee-shuffle`, chọn Public.
3. Chọn Add file → Upload files. Tải các file BÊN TRONG thư mục đã giải nén lên repository, rồi Commit changes. Không tải nguyên file ZIP lên.
4. Đảm bảo `index.html`, `app.js`, `style.css`, `cafes.json`, `coffee.jpg` nằm ngay ở thư mục gốc repository, không nằm trong thư mục con.
5. Vào Settings → Pages. Trong Build and deployment, chọn Source: Deploy from a branch.
6. Chọn Branch: main và thư mục /(root), rồi Save. Nếu repository dùng tên nhánh khác, chọn nhánh đang chứa các file vừa tải lên.
7. Khi GitHub hoàn tất, lấy đường dẫn website ở Settings → Pages và mở trên điện thoại hoặc chia sẻ cho bạn bè.

Link thường có dạng: https://TEN-GITHUB.github.io/TEN-REPOSITORY/

File `.nojekyll` là file rỗng để tắt xử lý Jekyll. Nếu giao diện tải lên không hiển thị file này, có thể tạo bằng Add file → Create new file, đặt tên `.nojekyll`.

Hướng dẫn chính thức: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## Tính năng

- 50 địa điểm Hà Nội từ danh sách đã chọn.
- Quay chọn quán và món uống, không lặp quán liên tiếp.
- Đổi riêng món uống và lọc cà phê / không cà phê.
- Giao diện sáng/tối, lưu tùy chọn trên thiết bị.
- Bố cục điện thoại và máy tính; hỗ trợ giảm chuyển động.
- Mở tìm kiếm tên quán trên Google Maps.

## Cập nhật sau này

- Danh sách quán: sửa mảng `places` trong `cafes.json`. Danh sách Maps không tự đồng bộ. Nếu thay số lượng, sửa các nhãn 50 quán trong `index.html`.
- Món uống và logic quay: `app.js`.
- Màu sắc, bố cục: `style.css`.
- Nội dung trang: `index.html`.
- Sau khi commit thay đổi lên nhánh đã chọn, GitHub Pages sẽ xuất bản lại.

Món uống là gợi ý chung, chưa xác minh trên menu quán. Ảnh cà phê là ảnh minh họa; ghi nguồn ở ATTRIBUTION.md. Google Fonts và Maps cần kết nối Internet. Cần phục vụ qua HTTP/HTTPS, không mở index.html bằng file:// vì trình duyệt có thể chặn tải cafes.json.
