# BÀI LÀM – HACKATHON 01

- **Mã đề:** 01
- **Họ tên: Nguyễn Ngọc Tuấn Anh** 
- **Lớp: CNTT04** 
- **Link repository:** 
- **Hệ điều hành (Windows/macOS): Windows** 

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```shell
●	Hiển thị đường dẫn tuyệt đối của thư mục hiện tại: pwd
●	Liệt kê nội dung, gồm cả file ẩn: ls -Force
●	Di chuyển các file yeu_cau.txt vào docs, các file logo vào media:
        +) mv .\yeu_cau.txt .\docs
        +) mv ".\Logo Nha Sach.PNG" .\media
●	Sao chép logo từ media vào backup: Copy-Item '.\media\Logo Nha Sach.PNG' .\backup
●	Xoá file .tmp tại thư mục gốc; không xoá file khác: Remove-Item .\temp_014.tmp
●	Dùng đường dẫn tương đối vào logs, liệt kê nội dung rồi quay lại thư mục gốc:
        +) cd .\logs
        +) ls
        +) cd ..

```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text
    Hiển thị đường dẫn tuyệt đối của thư mục hiện tại:
Path
----
C:\Users\ngoin\Documents\starter-kit\nha-sach-website\nha-sach-website
    Liệt kê nội dung, gồm cả file ẩn:

    Directory: C:\Users\ngoin\Documents\starter-kit\nha-sach-website\nha-sach-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/15/2026   8:15 AM                backup
d-----        10/15/2026   8:00 AM                data
d-----        10/15/2026   8:08 AM                docs
d-----        10/15/2026   8:00 AM                logs
d-----        10/15/2026   8:10 AM                media
------        10/12/2026   1:38 AM             72 .env
-a----        10/15/2026   8:15 AM           2831 bai_lam.md

```
    Dùng đường dẫn tương đối vào logs, liệt kê nội dung rồi quay lại thư mục gốc:


    Directory: C:\Users\ngoin\Documents\starter-kit\nha-sach-website\nha-sach-website\logs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/12/2026   1:38 AM           1057 store.log

## 4.3. Lọc log thủ công

### Lệnh đã chạy

```shell
●	Dùng các lệnh đọc file và lọc nội dung, tiến hành lọc các dòng chứa ERROR trong logs/store.log: Select-String "ERROR" .\logs\store.log
●	Ghi kết quả vào logs/daily_report.txt: Select-String "ERROR" .\logs\store.log > .\logs\daily_report.txt


```

### 2 dòng lỗi đầu tiên trong daily_report.txt

```text
Dùng các lệnh đọc file và lọc nội dung, tiến hành lọc các dòng chứa ERROR trong logs/store.log:

logs\store.log:4:2025-10-28 08:15:16 [ERROR] Thanh toan bi tu choi
logs\store.log:7:2025-10-28 08:24:16 [ERROR] Ket noi kho du lieu that bai
logs\store.log:9:2025-10-28 08:30:16 [ERROR] Thanh toan bi tu choi
logs\store.log:10:2025-10-28 08:33:16 [ERROR] Khong tim thay trang /sach-moi (404)
logs\store.log:14:2025-10-28 08:45:16 [ERROR] Khong tim thay trang /sach-moi (404)
logs\store.log:19:2025-10-28 09:00:16 [ERROR] Thanh toan bi tu choi


```

## 4.4. Thao tác với tài liệu Markdown (README.md)

> README.md được chấm trực tiếp trên file `README.md` ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [x] Heading 1: tên dự án
- [x] Mô tả ngắn có cả **in đậm** và *in nghiêng*
- [x] Bảng `Thư mục | Nội dung`, ít nhất 3 dòng dữ liệu
- [x] Code block chứa lệnh PowerShell/Terminal liệt kê nội dung dự án
- [x] Task list ít nhất 2 công việc, có ít nhất 1 mục đã hoàn thành
- [x] Blockquote nhắc không upload `.env`

## 4.5. Chạy script auto_report (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```shell
●	Script cần đọc file logs/store.log, lọc các dòng chứa ERROR và ghi vào file báo cáo mới logs/auto_report.txt: Get-content .\logs\store.log | Select-String "ERROR" >> logs/auto_report.txt
```

### Kết quả hiển thị

```text

```

## 4.6. Đếm số dòng lỗi

### Lệnh

```shell
(Select-String "ERROR" logs/store.log).Count

```

### Kết quả đếm (Windows: giá trị Count; macOS: con số in ra)

```text
6

```

## 4.7. Báo cáo tổng hợp

### Các lệnh đã chạy

```shell
"=== TONG HOP LOG ===" >> logs/tong_hop.txt

```

### Nội dung file logs/tong_hop.txt

```text
(Dán kết quả vào đây – xoá dòng này)

```

## 4.8. Excel

> Phần Excel được chấm trực tiếp trên file `data/hoa_don_thang_10.xlsx`, không cần ghi vào đây.
