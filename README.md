# Embedded Learning Website - Project Roadmap

## 1. Mục tiêu dự án

Xây dựng website dạy học Embedded theo hướng project thực tế, cho phép học viên:

- Xem danh sách khóa học và bài học.
- Tạo tài khoản, đăng nhập và đăng xuất.
- Truy cập nội dung theo quyền được cấp.
- Tải source code và tài liệu học tập.
- Theo dõi tiến độ học.

Admin có thể thêm, sửa và xóa khóa học hoặc bài học mà không cần sửa trực tiếp source code.

---

## 2. Công nghệ dự kiến

| Thành phần | Công nghệ |
|---|---|
| Trình soạn thảo | VS Code |
| Frontend | Next.js |
| Giao diện | Tailwind CSS |
| Ngôn ngữ ban đầu | JavaScript |
| Database | PostgreSQL |
| Backend, Auth, Storage | Supabase |
| Quản lý source code | GitHub |
| Hosting | Vercel |
| Domain | Mua sau khi website ổn định |

---

## 3. Lộ trình thực hiện

### Chặng 1 - Website chạy trên máy

**Target:** Website chạy được tại `http://localhost:3000`.

- [ ] Cài Node.js.
- [ ] Cài VS Code.
- [ ] Tạo project Next.js.
- [ ] Chạy project bằng `npm run dev`.
- [ ] Mở website tại `http://localhost:3000`.
- [ ] Sửa được tiêu đề và nội dung trang chủ.

**Hoàn thành khi:** Trang web hiển thị được nội dung do mình tự sửa.

---

### Chặng 2 - Giao diện cơ bản

**Target:** Có trang chủ rõ ràng và danh sách khóa học mẫu.

- [ ] Tạo Header.
- [ ] Tạo phần giới thiệu website.
- [ ] Tạo Course Card.
- [ ] Hiển thị khóa học STM32 cơ bản.
- [ ] Hiển thị khóa học ESP32 IoT.
- [ ] Tạo Footer.
- [ ] Kiểm tra giao diện trên máy tính và điện thoại.

**Hoàn thành khi:** Trang chủ có giao diện cơ bản, dễ nhìn và responsive.

---

### Chặng 3 - Các trang và điều hướng

**Target:** Người dùng bấm được từ khóa học sang danh sách bài học.

- [ ] Tạo trang `/courses`.
- [ ] Tạo trang `/courses/stm32`.
- [ ] Tạo trang `/courses/esp32`.
- [ ] Tạo trang bài học mẫu.
- [ ] Thêm nút quay lại và chuyển bài.
- [ ] Kiểm tra các đường dẫn không bị lỗi.

**Hoàn thành khi:** Có thể đi theo luồng `Trang chủ → Khóa học → Bài học`.

---

### Chặng 4 - Đưa website lên Internet

**Target:** Người khác có thể mở website mà laptop không cần chạy liên tục.

- [ ] Tạo tài khoản GitHub.
- [ ] Đưa source code lên GitHub repository.
- [ ] Tạo tài khoản Vercel.
- [ ] Kết nối Vercel với GitHub.
- [ ] Deploy website.
- [ ] Gửi URL public cho một người khác kiểm tra.

**Hoàn thành khi:** Điện thoại hoặc máy khác ngoài project mở được website bằng URL public.

---

### Chặng 5 - Kết nối database

**Target:** Khóa học và bài học được đọc từ database thay vì viết cứng trong code.

- [ ] Tạo project Supabase.
- [ ] Tạo bảng `courses`.
- [ ] Tạo bảng `lessons`.
- [ ] Thêm dữ liệu khóa học mẫu.
- [ ] Kết nối Next.js với Supabase.
- [ ] Đọc danh sách khóa học từ database.
- [ ] Đọc danh sách bài học theo khóa học.

**Hoàn thành khi:** Thêm dữ liệu trong Supabase thì website hiển thị dữ liệu mới.

---

### Chặng 6 - Tài khoản học viên

**Target:** Học viên tự đăng ký và đăng nhập được.

- [ ] Tạo trang Register.
- [ ] Tạo trang Login.
- [ ] Tạo chức năng Logout.
- [ ] Hiển thị thông tin người đang đăng nhập.
- [ ] Bảo vệ trang Dashboard.
- [ ] Thêm chức năng quên mật khẩu.
- [ ] Thêm Google Login sau khi Email/Password chạy ổn định.

**Hoàn thành khi:** Một người mới có thể đăng ký, đăng nhập, vào Dashboard và đăng xuất.

---

### Chặng 7 - Phân quyền Student và Admin

**Target:** Học viên và quản trị viên có quyền khác nhau.

- [ ] Tạo bảng profile người dùng.
- [ ] Thêm role `student`.
- [ ] Thêm role `admin`.
- [ ] Tạo trang `/admin`.
- [ ] Chặn Student truy cập trang Admin.
- [ ] Tạo form thêm khóa học.
- [ ] Tạo form thêm bài học.
- [ ] Thêm chức năng sửa và xóa nội dung.

**Hoàn thành khi:** Admin quản lý được nội dung, Student chỉ xem được nội dung cho phép.

---

### Chặng 8 - Khóa và mở nội dung

**Target:** Có bài miễn phí và bài chỉ dành cho học viên được cấp quyền.

- [ ] Đánh dấu bài học Free hoặc Locked.
- [ ] Tạo bảng `user_courses` hoặc `enrollments`.
- [ ] Kiểm tra quyền trước khi mở bài học.
- [ ] Hiển thị biểu tượng khóa cho nội dung chưa được cấp quyền.
- [ ] Tạo chức năng Admin cấp quyền khóa học cho học viên.

**Hoàn thành khi:** Hai tài khoản có quyền khác nhau sẽ nhìn thấy nội dung khác nhau.

---

### Chặng 9 - Theo dõi tiến độ

**Target:** Website ghi nhớ bài học mà học viên đã hoàn thành.

- [ ] Tạo bảng `lesson_progress`.
- [ ] Thêm nút “Đánh dấu hoàn thành”.
- [ ] Hiển thị trạng thái hoàn thành từng bài.
- [ ] Tính phần trăm hoàn thành khóa học.
- [ ] Hiển thị tiến độ trong Dashboard.

**Hoàn thành khi:** Đăng xuất rồi đăng nhập lại vẫn thấy đúng tiến độ đã lưu.

---

### Chặng 10 - Hoàn thiện website

**Target:** Website đủ ổn định để mời nhóm học viên đầu tiên sử dụng.

- [ ] Upload hình ảnh và tài liệu.
- [ ] Cho phép tải source code.
- [ ] Thêm tìm kiếm khóa học hoặc bài học.
- [ ] Tối ưu giao diện điện thoại.
- [ ] Thêm trang giới thiệu và liên hệ.
- [ ] Thêm chính sách quyền riêng tư và điều khoản sử dụng.
- [ ] Kiểm tra bảo mật và quyền truy cập database.
- [ ] Thiết lập backup dữ liệu.
- [ ] Gắn domain riêng khi cần.
- [ ] Kiểm thử với nhóm học viên nhỏ trước khi mở rộng.

**Có thể bổ sung sau:** Video, quiz, comment, chứng chỉ, thanh toán, email và analytics.

---

## 4. Thứ tự ưu tiên

```text
Website chạy local
    ↓
Giao diện cơ bản
    ↓
Điều hướng các trang
    ↓
Deploy lên Internet
    ↓
Database
    ↓
Register / Login
    ↓
Admin
    ↓
Khóa / mở nội dung
    ↓
Theo dõi tiến độ
    ↓
Hoàn thiện sản phẩm
```

---

## 5. Phạm vi phiên bản đầu tiên - MVP

Phiên bản đầu tiên chỉ cần:

- [ ] Một trang chủ.
- [ ] Một khóa học STM32 cơ bản.
- [ ] Ba bài học mẫu.
- [ ] Register, Login và Logout.
- [ ] Một Dashboard dành cho học viên.
- [ ] Một trang Admin để thêm bài học.
- [ ] Deploy công khai để người khác truy cập.

Không làm thanh toán, chứng chỉ, comment hoặc hệ thống video riêng trong phiên bản đầu tiên.

---

## 6. Trạng thái hiện tại

- **Chặng đang thực hiện:** Chặng 1 - Website chạy trên máy.
- **Việc tiếp theo:** Cài Node.js và tạo project Next.js đầu tiên.
- **Nguyên tắc:** Hoàn thành và kiểm tra từng chặng trước khi chuyển sang chặng tiếp theo.
