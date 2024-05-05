# Android Debug Bridge *version 1.0.39*

Android Debug Bridge (ADB) là một công cụ mạnh mẽ được cung cấp bởi Google cho phép tương tác giữa máy tính và thiết bị Android thông qua kết nối USB hoặc Wi-Fi. ADB được sử dụng rộng rãi trong phát triển ứng dụng Android, cho phép các nhà phát triển thực hiện các nhiệm vụ như:

- Cài đặt và gỡ cài đặt ứng dụng trên thiết bị Android.
- Gửi tệp tin giữa máy tính và thiết bị Android.
- Chạy các lệnh shell trực tiếp trên thiết bị Android.
- Gỡ lỗi và kiểm tra hiệu suất của ứng dụng trên thiết bị thực tế.

ADB cũng cung cấp một loạt các tính năng như truy cập vào trình quản lý gói (package manager), quản lý thiết bị từ xa, chụp ảnh màn hình và nhiều hơn nữa.

## Cài đặt

ADB đi kèm với Android SDK, bạn có thể tải và cài đặt SDK từ trang chính thức của Android Developers: [Android Developers](https://developer.android.com/studio/releases/platform-tools)
Bạn cũng có thể clone về từ đây

## Sử dụng

Sau khi cài đặt, bạn có thể sử dụng ADB từ dòng lệnh hoặc tích hợp vào các công cụ phát triển ứng dụng Android như Android Studio.

### Ví dụ
Dưới đây là một số lệnh ADB phổ biến mà bạn có thể sử dụng để tương tác với thiết bị Android của mình:

1. **Liệt kê tất cả các thiết bị đã kết nối:**
   ```
   adb devices
   ```
2. **Cài đặt một ứng dụng trên thiết bị:**
   ```
   adb install path/to/app.apk
   ```
3. **Gỡ cài đặt một ứng dụng từ thiết bị:**
   ```
   adb uninstall package.name
   ```
4. **Chụp ảnh màn hình của thiết bị và lưu lại:**
   ```
   adb shell screencap -p /sdcard/screenshot.png
   adb pull /sdcard/screenshot.png .
   ```
5. **Lấy thông tin về các ứng dụng đã cài đặt trên thiết bị:**
   ```
   adb shell pm list packages
   ```
6. **Mở một ứng dụng trên thiết bị:**
   ```
   adb shell am start -n package.name/activity.name
   ```
7. **Lấy thông tin về thiết bị, bao gồm model, hệ điều hành và nhiều hơn nữa:**
   ```
   adb shell getprop
   ```
8. **Lấy thông tin về pin của thiết bị:**
   ```
   adb shell dumpsys battery
   ```
9. **Chạy lệnh shell trực tiếp trên thiết bị:**
   ```
   adb shell <command>
   # Chạm vào điểm 300 400
   adb shell input tap 300 400
   # Nhập vào văn bản
   adb shell input text "Hello"
   ...
   ```

Đây chỉ là một số ví dụ cơ bản, bạn có thể tìm hiểu thêm về các lệnh ADB khác trong [tài liệu chính thức của Android Debug Bridge](https://developer.android.com/studio/command-line/adb) và [ADB Command Reference](https://developer.android.com/studio/command-line/adb#command-summary)
