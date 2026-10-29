# 📖 HƯỚNG DẪN SỬ DỤNG GIAO DIỆN WEB

> **Lưu ý:** Repository này chứa mã nguồn giao diện Web (HTML/CSS) phục vụ cho bài Lab 4 môn Computer Networking của Nhóm 8. 
> Bên dưới là hướng dẫn chi tiết cách phân biệt 2 giao diện và cách đưa chúng vào phần mềm Cisco Packet Tracer để chạy mô phỏng.

---

# NHOM8_LAB4_Computer-Networking_UI_FOR_WEB

Dự án này chứa mã nguồn HTML/CSS cho hai trang web khác nhau, được sử dụng để cấu hình dịch vụ Web trên 2 Server trong bài thực hành mô phỏng mạng doanh nghiệp.

---

## 📂 Cấu trúc thư mục

Repository bao gồm 2 thư mục chính chứa mã nguồn:

### 1. Thư mục `html/` - Trang Web Nội Bộ
- **Dành cho:** `Server-NoiBo` (IP: `192.168.10.58`).
- **Tên miền truy cập:** `http://noibo.nhom8.local` (được phân giải bởi dịch vụ DNS nội bộ).
- **Mục đích:** Đây là trang Cổng thông tin nội bộ của Công ty TNHH TMĐT Nhóm 8. Trang web hiển thị **Sơ đồ Ban Lãnh Đạo**, bao gồm thông tin Giám đốc, 4 Trưởng phòng và các Thư ký.
- **Đặc điểm thiết kế:** Giao diện hiện đại, tông màu Tím/Xanh chủ đạo, sử dụng CSS Grid để bố cục Giám đốc ở giữa và Trưởng phòng ở 4 góc.

### 2. Thư mục `html2/` - Trang Web Internet
- **Dành cho:** `Internet-Server` (IP: `8.8.8.8`).
- **Tên miền truy cập:** `http://www.internet.com` (được phân giải bởi DNS nội bộ trỏ ra IP Public).
- **Mục đích:** Đây là trang Thương mại điện tử mô phỏng mạng Internet bên ngoài. Trang web hiển thị giao diện bán hàng, giỏ hàng và các sản phẩm (Tai nghe, Đồng hồ, Giày).
- **Đặc điểm thiết kế:** Đồng bộ tone màu Tím/Xanh với trang nội bộ nhưng mang phong cách thương mại điện tử (ShopVN.com).

---

## 🚀 HƯỚNG DẪN CÀI ĐẶT VÀO CISCO PACKET TRACER

Để đưa các giao diện này vào bài mô phỏng mạng, thực hiện theo các bước sau:

### Bước 1: Cấu hình Server Nội Bộ (Lấy code từ thư mục `html/`)
1. Mở `Server-NoiBo` -> chuyển sang tab **Services** -> chọn **HTTP**.
2. Bật HTTP: Chọn **On**.
3. Tìm file `index.html` trong danh sách, bấm vào chữ **`(edit)`**.
4. Mở file `index.html` trong thư mục `html/` của repository này, **Copy** toàn bộ mã nguồn và **Paste** vào cửa sổ của Packet Tracer.
5. Bấm **Save**.

### Bước 2: Cấu hình Server Internet (Lấy code từ thư mục `html2/`)
1. Mở `Internet-Server` -> chuyển sang tab **Services** -> chọn **HTTP**.
2. Bật HTTP: Chọn **On**.
3. Tìm file `index.html` trong danh sách, bấm vào chữ **`(edit)`**.
4. Mở file `index.html` trong thư mục `html2/` của repository này, **Copy** toàn bộ mã nguồn và **Paste** vào cửa sổ của Packet Tracer.
5. Bấm **Save**.

### Bước 3: Cấu hình DNS (Trên Server Nội Bộ)
1. Mở `Server-NoiBo` -> tab **Services** -> chọn **DNS**.
2. Bật DNS: Chọn **On**.
3. Thêm 2 bản ghi (A Record):
   - Name: `noibo.nhom8.local` -> Address: `192.168.10.58`
   - Name: `www.internet.com` -> Address: `8.8.8.8`

---

## 🧑‍💻 Công nghệ sử dụng
- HTML5 / CSS3 (Tĩnh, không cần JavaScript).
- FontAwesome (dùng CDN để lấy icon).
- CSS Grid & Flexbox để căn chỉnh bố cục.

---
*Lưu ý: Do đây là môi trường mô phỏng Packet Tracer, các hình ảnh thật (nếu dùng link ngoài) có thể không tải được. Giao diện được thiết kế ưu tiên sử dụng Icon Vector và CSS Gradient để đảm bảo hiển thị tốt nhất.*
