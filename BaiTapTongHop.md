 Phần 1

### 1
#### 1.1. Mục tiêu
Xây dựng hệ thống quản lý thư viện, giúp quản lý sách và phiếu mượn.
#### 1.2. Đối tượng sử dụng
Thủ thư, sinh viên và quản trị viên.

### 2. Chức năng hệ thống
Hệ thống hỗ trợ quản lý mượn, trả sách và tra cứu thông tin sách. Người dùng có thể theo dõi tình trạng mượn sách.

#### 2.1. Quản lý mượn sách
##### 2.1.1. Luồng mượn sách qua thẻ sinh viên
Sinh viên xuất trình thẻ, thủ thư kiểm tra thông tin và tạo phiếu mượn.

#### 2.2. Quản lý trả sách
Ghi nhận ngày trả và cập nhật tình trạng sách.

### 3. Yêu cầu bảo mật
Hệ thống yêu cầu đăng nhập và phân quyền người dùng. Dữ liệu sinh viên phải được bảo vệ, tránh truy cập trái phép.

Mục lục được tạo tự động bằng Heading Styles và Auto TOC trong Word.

## Phần 2: Chuẩn hóa dữ liệu

### 1. Ba lỗi vi phạm

| Lỗi | Vị trí | Quy tắc vi phạm |
|---|---|---|
| Merge ô tiêu đề | Hàng 1 | Không gộp ô trong bảng dữ liệu |
| Hàng trống | Hàng 5 | Không để hàng trống |
| Dòng tổng cộng | Hàng 6 | Không đặt dòng tổng trong vùng dữ liệu |

### 2. sau khi sửa

| MSSV | Họ Tên | Mã Sách | Ngày Mượn | Tình Trạng |
|---|---|---|---|---|
| SV001 | Nguyễn Văn An | S001 | 01/10/2026 | Đang mượn |
| SV002 | Trần Thị Bình | S002 | 03/10/2026 | Quá hạn |
| SV003 | Lê Văn Cường | S003 | 10/10/2026 | Đã trả |
| SV004 | Phạm Thu Hà | S099 | 12/10/2026 | Đang mượn |

### 3

- Record: Một dòng dữ liệu của sinh viên, ví dụ SV001.
- Field: Một cột dữ liệu, ví dụ MSSV hoặc Tình Trạng.

### 4

Chọn bảng dữ liệu, nhấn Ctrl + Shift + L, mở bộ lọc ở cột Tình Trạng và chọn Quá hạn. Kết quả là SV002 - Trần Thị Bình.

Phần 3

Công thức lấy tên sách tại ô F2:

=VLOOKUP(C2,DanhMucSach!$A$2:$B$4,2,FALSE)

Mã S099 trả về lỗi #N/A vì không tồn tại trong danh mục sách

Công thức xử lý lỗi:

=IFERROR(VLOOKUP(C2,DanhMucSach!$A$2:$B$4,2,FALSE),"Không tìm thấy sách")

Kéo công thức xuống các dòng còn lại

 Phần 4

Tiêu đề: Dữ liệu phiếu mượn đã được chuẩn hóa và tự động tra cứu tên sách

Nội dung chính:
- 4 phiếu mượn đã được chuẩn hóa.
- 1 phiếu quá hạn.
- 3 mã sách hợp lệ, 1 mã sách chưa có trong danh mục.

Biểu đồ: Bar Chart, dùng để so sánh số phiếu theo tình trạng.

rule 10/20/30
- Slide này chiếm 1/10 tổng số slide.
- Thời gian trình bày dự kiến: 2 phút.
- Cỡ chữ tối thiểu: 30 pt.
