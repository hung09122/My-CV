# Nguyễn Lê Hưng - Portfolio CV

## Tên dự án

**Portfolio CV cá nhân của Nguyễn Lê Hưng**

## Mô tả

Website CV/portfolio tĩnh giới thiệu Nguyễn Lê Hưng, định hướng Frontend Developer. Trang trình bày thông tin giới thiệu, kỹ năng, các dự án tiêu biểu và cách liên hệ; giao diện được thiết kế responsive để sử dụng trên điện thoại, máy tính bảng và máy tính.

## Chức năng

- Điều hướng nhanh đến các phần Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Hiển thị thông tin cá nhân, định hướng nghề nghiệp và kỹ năng.
- Trình bày danh sách dự án cùng mô tả và công nghệ sử dụng.
- Cung cấp liên kết email và hồ sơ mạng xã hội.
- Tương thích với nhiều kích thước màn hình và có hiệu ứng tương tác khi rê chuột.

## Công nghệ

- HTML5: cấu trúc nội dung và các vùng điều hướng.
- CSS3: giao diện, Flexbox, CSS Grid, responsive và hiệu ứng.
- Không sử dụng framework, thư viện JavaScript hay quy trình build.
- Nginx (tùy chọn): phục vụ website khi chạy bằng Docker.

## Yêu cầu môi trường

- Trình duyệt hiện đại như Chrome, Edge, Firefox hoặc Safari.
- Git nếu muốn lấy mã nguồn bằng lệnh `git clone`.
- Python 3 (tùy chọn) nếu muốn chạy máy chủ web tĩnh trên máy.
- Docker Desktop trên Windows hoặc Docker Engine trên macOS/Linux nếu muốn chạy bằng Docker.

Ứng dụng không cần cài Node.js, không cần cơ sở dữ liệu và không cần biến môi trường.

## Cài đặt

Tải hoặc giải nén mã nguồn vào máy, sau đó mở thư mục `My-CV`. Nếu đã có URL Git của kho mã nguồn, thay `URL_REPOSITORY` bằng URL đó:

```bash
git clone URL_REPOSITORY
cd My-CV
```

Nếu tải mã nguồn dưới dạng tệp ZIP, hãy giải nén và mở thư mục `My-CV` trực tiếp. Cấu trúc cần giữ nguyên:

```text
My-CV/
├── index.html
├── README.md
└── assets/
	├── css/
	│   └── styles.css
	└── img/
```

## Cấu hình và tùy chỉnh

Không cần tạo tệp cấu hình để chạy trang. Để cá nhân hóa nội dung:

1. Chỉnh tiêu đề, mô tả, kỹ năng, dự án và thông tin liên hệ trong `index.html`.
2. Thay ảnh trong `assets/img/` và cập nhật đúng đường dẫn tương đối trong thuộc tính `src` của các thẻ ảnh. Tên tệp có phân biệt chữ hoa/chữ thường trên Linux.
3. Cập nhật các liên kết hồ sơ. Email hiện có trong trang là `nguyenleh839@gmail.com`; liên kết GitHub và LinkedIn đang là đường dẫn mẫu (`#`) và cần được thay bằng URL thật.
4. Chỉnh màu sắc, bố cục và kiểu chữ trong `assets/css/styles.css`.

Sau khi chỉnh sửa, tải lại trang trong trình duyệt để kiểm tra.

## Chạy thử

### Windows

Mở PowerShell tại thư mục `My-CV`.

Có thể mở trực tiếp tệp HTML:

```powershell
Start-Process .\index.html
```

Hoặc chạy máy chủ web tĩnh nếu Python 3 đã được cài:

```powershell
py -m http.server 8000
```

Mở <http://localhost:8000> trong trình duyệt. Dừng máy chủ bằng `Ctrl+C`.

### macOS

Mở Terminal, chuyển đến thư mục `My-CV`, rồi chạy:

```bash
open index.html
```

Hoặc, nếu đã cài Python 3, chạy máy chủ web tĩnh:

```bash
python3 -m http.server 8000
```

Mở <http://localhost:8000> trong trình duyệt. Dừng máy chủ bằng `Ctrl+C`.

### Linux

Mở Terminal, chuyển đến thư mục `My-CV`. Mở trực tiếp bằng trình duyệt mặc định:

```bash
xdg-open index.html
```

Hoặc chạy máy chủ web tĩnh bằng Python 3:

```bash
python3 -m http.server 8000
```

Mở <http://localhost:8000> trong trình duyệt. Dừng máy chủ bằng `Ctrl+C`.

### Docker

Cần cài và khởi động Docker trước. Chạy lệnh tại thư mục `My-CV`; lần chạy đầu tiên Docker sẽ tải image `nginx:alpine` nếu máy chưa có image đó.

**Windows PowerShell:**

```powershell
docker run --rm -d --name my-cv -p 8080:80 --mount "type=bind,source=$((Get-Location).Path),target=/usr/share/nginx/html,readonly" nginx:alpine
```

**macOS/Linux:**

```bash
docker run --rm -d --name my-cv -p 8080:80 -v "$(pwd):/usr/share/nginx/html:ro" nginx:alpine
```

Mở <http://localhost:8080> để xem trang. Các thay đổi trong tệp HTML/CSS/ảnh sẽ được phục vụ trực tiếp từ thư mục dự án. Dừng container bằng:

```bash
docker stop my-cv
```

## Kiểm tra

- Mở trang và xác nhận CSS, ảnh, nội dung cùng các mục điều hướng đều hiển thị.
- Kiểm tra giao diện ở cả màn hình nhỏ và màn hình lớn.
- Thử các liên kết email, dự án và hồ sơ sau khi đã cập nhật URL.

## Thông tin liên hệ

- **Tên:** Nguyễn Lê Hưng
- **Email:** [nguyenleh839@gmail.com](mailto:nguyenleh839@gmail.com)
- **GitHub:** `github.com/hung09122` (cần cập nhật liên kết thật trong `index.html`)
- **LinkedIn:** `linkedin.com/in/nguyenlehung` (cần cập nhật liên kết thật trong `index.html`)
