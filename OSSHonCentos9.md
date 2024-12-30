# Cài OpenSSH
  `sudo dnf install openssh-server`
# Kiểm tra phiên bản
  `ssh -V`
# Khởi động dịch vụ SSH
  ` sudo systemctl start sshd`
# Bật dịch vụ tự động khởi động cùng hệ thống
  `sudo systemctl enable sshd`
# Kiểm tra trạng thái 
  `sudo systemctl status sshd`
## Error: Access Denied khi SSH bằng Pass
Fix: Thay đổi cấu hình SSH trong đừng dẫn `/etc/ssh/sshd_config`
Tìm và sửa dòng PasswordAuthentication thành Yes hoặc có dấu # thì xóa nó đi
và sửa dòng PermitRootLogin thành YES 
Cuối cùng thì restart lại hệ thống sshd 
# Test kiểm tra lại xem ssh dc chưa
