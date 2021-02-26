# Techcombank 2021 mã hóa 

**Api Techcombank kiểu đéo thể đọc được nhưng cam đoan an toàn do mai mình đi nvqs :)))**

0. **Mặc định server chạy trên port 6789. Tiến hành mở port**
```sh
sudo iptables -I INPUT -p tcp --dport 6789 -j ACCEPT
```

**Cách cài đặt**

1. **Cài đặt MongoDB**
2. **Cài đặt Nodejs**
3. **Cài đặt PM2**

9. **Khởi chạy server**
```sh
cd /tcb2021
sudo pm2 start node.js
```

> Để kiểm tra log thì dùng lệnh: sudo pm2 logs

12. **Kết thúc**

Bây giờ có thể sử dụng server ở địa chỉ: http://IP.Server.XXX:6789

# Các API
Copy curl này vào POSTMAN hoặc một phần mềm tương tự để test
1. **Kiểm tra lịch sử giao dịch**
```curl
curl --location --request POST 'IP:6789/api/techcombank/getTransactions' \
--header 'Content-Type: application/json' \
--data-raw '{
    "username": "tk",
    "password": "mk",
    "begin": "28/12/2020",
    "end": "26/02/2021"
}'
```

- **Giải thích thông số POST**
```json
{
    "begin": "DD/MM/YYYY",
    "end": "DD/MM/YYYY",
    "username": "ten_dang_nhap_TCB",
    "password": "mat_khau_TCB"
}
```
