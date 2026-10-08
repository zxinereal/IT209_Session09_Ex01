# Bài 1 — Kiểm tra Docker Engine và Hello-World

Ngày thực hiện: 08/10/2026  
Hệ điều hành: Windows (Docker Desktop context: `desktop-linux`)

## 1. `docker version`

```text
Client:
 Version:           29.7.2
 API version:       1.55
 Go version:        go1.26.5
 Git commit:        a7dcaa6
 Built:             Wed Aug  5 18:31:33 2026
 OS/Arch:           windows/amd64
 Context:           desktop-linux
failed to connect to the docker API at npipe:////./pipe/dockerDesktopLinuxEngine; check if the path is correct and if the daemon is running: open //./pipe/dockerDesktopLinuxEngine: The system cannot find the file specified.
```

## 2. `docker info`

```text
Client:
 Version:    29.7.2
 Context:    desktop-linux
 Debug Mode: false

Server:
failed to connect to the docker API at npipe:////./pipe/dockerDesktopLinuxEngine; check if the path is correct and if the daemon is running: open //./pipe/dockerDesktopLinuxEngine: The system cannot find the file specified.
```

## 3. `docker run hello-world`

```text
failed to connect to the docker API at npipe:////./pipe/dockerDesktopLinuxEngine; check if the path is correct and if the daemon is running: open //./pipe/dockerDesktopLinuxEngine: The system cannot find the file specified.
```

## Kết luận

Docker CLI phiên bản `29.7.2` đã được cài đặt. Tại thời điểm kiểm tra, Docker Daemon chưa chạy nên chưa thể khởi động container `hello-world`.

Sau khi mở Docker Desktop và đợi trạng thái **Engine running**, chạy lại:

```bash
docker version
docker info
docker run hello-world
```

Kết quả thành công cần chứa dòng:

```text
Hello from Docker! This message shows that your installation appears to be working correctly.
```
