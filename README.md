# My favorite Tips & Tricks (Cheat Sheet)

## Table of Contents
- [My favorite Tips \& Tricks (Cheat Sheet)](#my-favorite-tips--tricks-cheat-sheet)
  - [Table of Contents](#table-of-contents)
      - [Chạy engine cờ tướng Pikafish trên Cloud](#chạy-engine-cờ-tướng-pikafish-trên-cloud)


#### Chạy engine cờ tướng Pikafish trên Cloud

1. Vào <https://shell.segfault.net> và làm theo hướng dẫn.
2. Chạy lệnh `info` trong Terminal để lấy khóa (private key) và cấu hình config kết nối SSH.
3. Lưu tệp khóa SSH vào thư mục `~/.ssh/` trên máy **Windows**.
4. Sao chép cấu hình kết nối SSH vào tệp `~/.ssh/config` trên máy **Windows**.
5. Mở Terminal trên **Windows**, kết nối SSH tới **Server**:
    ```cmd
    ssh giga
    ```

6. Cài đặt engine Pikafish trên **Server** bằng lệnh sau:
    ```bash
    cd
    wget -O pika https://github.com/vinhgiga/assets/releases/download/xiangqi-engine/pikafish-vnni512
    wget -O pikafish.nnue https://github.com/vinhgiga/assets/releases/download/xiangqi-engine/pikafish.nnue
    chmod +x pika
    ```

7. (Tùy chọn) Kiểm tra xem engine đã hoạt động chưa:
    ```bash
    ./pika
    ``` 

8. Tạo tệp `cloud.bat` trên máy **Windows** với nội dung sau:
    ```bat
    @echo off
    ssh giga "cd; ./pika"
    ```
  
9. Nạp tệp `cloud.bat` vào GUI Pengfei hoặc [chuyển đổi sang exe](https://bat-to-exe-converter-x64.en.softonic.com/download). Thưởng thức 🫖