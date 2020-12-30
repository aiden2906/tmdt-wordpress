## Môn: Thương mại điện tử
Giáo viên hướng dẫn: **Trần Thị Quế Nguyệt**

Thành viên:
- **Đinh Hoàng Kim** - 1711872
- **Trần Thanh Quang** - 1712802
- **Nguyễn Văn Hoàng** - 1711400
- **Võ Quý Giang** - 1711130
- **Trần Đình Tấn** - 1713093

Công nghệ chúng em sử dụng khi làm bài tập lớn môn thương mại điện tử bao gồm:
- `Wordpress`: Một phần mềm mã nguồn mở giúp tạo một website nhanh chóng. Ngoài ra, việc quản lý nội dùng website cũng trở nên dễ dàng nhờ vào cms mà wordpress hỗ trợ cho người dùng amdin.
- `PostgresSQL`: Hệ quản trị cơ sở dữ liệu cho dự án
- `Docker`: Công cụ hỗ trợ đóng gói ứng dụng cùng môi trường để chạy ứng dụng, tạo ra một môi trường cô lập với bên ngoài, chạy ứng dụng một cách ổn định, tiết kiệm thời gian cho nhà phát triển.

Hiện tại, nhóm em chạy dự án thông qua các image như `wordpress`, `postgres`, .. được cộng đồng docker phát triển.

Để khởi chạy ứng dụng sẽ cần thực hiện các bước sau đây
- Mở terminal và di chuyển đến thư mục chứa `docker-compose.yml`
- Đảm bảo hệ thống đã được cài đặt `docker` và `docker-compose` và port 8000 sẳn sàng trên hệ thống.

```
# Nếu chưa cài đặt, hãy chạy lệnh sau để cài đặt
curl https://get.docker.com | bash -
curl -L "https://github.com/docker/compose/releases/download/1.25.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose && chmod +x /usr/local/bin/docker-compose && ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
sudo timedatectl set-timezone Asia/Ho_Chi_Minh
```

- Run command:

```
# chạy ở chế độ thường
docker-compose up 

# chạy ở chế độ detech
docker-compose up -d
```

- Hoàn tất, truy cập website tại `http://localhost:8000`
- Truy cập cms tại `http://localhost:8000/wp-admin`