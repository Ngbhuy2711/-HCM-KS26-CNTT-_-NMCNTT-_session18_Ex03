# ***Báo cáo phân tích (IPO)***
## Xác định Input (Dấu hiệu nhiễm), Process (Các bước xử lý), Output (Hệ thống sạch).
- Input : tài khoản facebook, gmail tự động đăng xuất hoặc xuất hiện thông báo thay đổi mật khẩu khôi phục mà bạn không thực hiện
-process :
 + B1 : ngắt kết nối mạng
 + B2 : Đổi mật khẩu và đăng xuất toàn bộ
 + B3 : thu hồi token và quyền ứng dụng . Xóa toàn bộ API key đang liên kết với các tài khoản quan trọng
 + B4 : xóa sạch dữ liệu và cài lại hệ điều hành
-Output :
 - ổ cứng đc định dạng sạch sẽ , loại bỏ hoàn toàn mã độc nội bộ
 - Toàn bộ tài khoản trực tuyến được bảo vệ bằng mật khẩu mới
## Mô tả chi tiết cách thực hiện "Đổi mật khẩu từ thiết bị khác" và "Revoke Token" trên GitHub
 -Đổi mật khẩu từ thiết bị khác :
  + sử dụng điện thoại hoặc thiết bị an toàn , đăng nhập vào acc google hoặc face của bạn
  + truy cập vào cài đặt tài khoản rồi chọn mục bảo mật
  + Tìm đến mục thiết bị của bạn hoặc nơi bạn đã đăng nhập
  + Tiến hành đổi mật khẩu mới và bật xác thực 2 bước
 -Revoke token ( thu hồi token )
  + ấn vào setting
  + tại menu trái nhấn vào mục developer settings
  + thu hồi OAuth Apps
    * chọn oauth app từ menu con
    * tìm các ứng dụng lạ hoặc không rõ nguồn gốc mà bạn từng cấp quyền
    * nhấp vào ứng dụng đó và chọn nút revoke access
  + Thu hồi personal access tokens
    * Chọn personal access
    * rà soát danh sách các token đag hoạt động , nếu phát hiện token nào do kẻ tấn công tự tạo hãy nhấn vào token đó
    * nhấp vào nút delete hoặc revoke để vô hiệu hóa vĩnh viễn
