# Text-Based Story Game (C – Linux)

## 1. Giới thiệu
Text-Based Story Game là một trò chơi cốt truyện dạng văn bản (console-based) được viết bằng ngôn ngữ C và chạy trên hệ điều hành Linux.  
Người chơi sẽ đọc nội dung câu chuyện và đưa ra các lựa chọn khác nhau. Mỗi lựa chọn sẽ dẫn đến các nhánh truyện và các ending khác nhau.

Project được thực hiện nhằm đáp ứng yêu cầu của môn OSG (Operating System), tập trung vào việc sử dụng ngôn ngữ C, cấu trúc dữ liệu, quản lý file và tương tác người dùng trên môi trường Linux.

---

## 2. Môi trường và yêu cầu
- Hệ điều hành: Linux (Ubuntu / Debian / WSL Linux)
- Trình biên dịch: gcc
- Ngôn ngữ: C (C99)

---

## 3. Cấu trúc thư mục

StoryGame/
│
├── main.c        // Chương trình chính, menu và vòng lặp game
├── story.h       // Định nghĩa struct và prototype
├── story.c       // Xử lý scene, lựa chọn và ending
├── endings.txt   // Lưu các ending đã đạt được
├── Makefile      // Biên dịch chương trình
└── README.md     // Tài liệu mô tả project

---

## 4. Cách biên dịch và chạy chương trình

### 4.1 Biên dịch
Sử dụng Makefile:

make

### 4.2 Chạy chương trình

./storygame

### 4.3 Xóa file biên dịch

make clean

---

## 5. Chức năng chính
- Hiển thị menu game
- Bắt đầu game cốt truyện
- Người chơi đưa ra lựa chọn
- Điều hướng giữa các scene
- Kết thúc với nhiều ending khác nhau
- Lưu ending đã đạt được vào file endings.txt
- Xem lại các ending đã mở

---

## 6. System call và thư viện sử dụng

### 6.1 Thư viện C
- stdio.h – nhập xuất dữ liệu
- stdlib.h – quản lý bộ nhớ và tiện ích
- string.h – xử lý chuỗi

### 6.2 System call / thao tác hệ thống
- File I/O thông qua:
  - fopen()
  - fprintf()
  - fclose()

Chương trình không sử dụng fork/exec để đảm bảo độ khó phù hợp, nhưng vẫn chạy hoàn toàn trên Linux.

---

## 7. Lưu ý đạo đức và giả định
- Chương trình không thực hiện các hành vi nguy hiểm như chạy lệnh hệ thống độc hại.
- Không can thiệp vào file hệ thống ngoài thư mục project.
- Dữ liệu người dùng chỉ được lưu cục bộ trong file endings.txt.
- Nội dung câu chuyện mang tính giả lập, học tập.

---

## 8. Hướng mở rộng (nếu có)
- Thêm nhiều scene và ending hơn
- Thêm lưu trạng thái chơi
- Thêm tên người chơi
- Thống kê số ending đã đạt

---

## 9. Kết luận
Text-Based Story Game là một project C đơn giản nhưng đáp ứng đầy đủ yêu cầu của môn OSG, giúp nhóm hiểu rõ hơn về cách xây dựng chương trình C có cấu trúc và chạy trên Linux.
