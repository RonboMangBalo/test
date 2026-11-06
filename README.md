# 🥖 Bánh Mì Ngôn Ngữ — Học Ngoại Ngữ Mỗi Ngày, Không Áp Lực

> **Học phần:** Tư duy thiết kế và đổi mới sáng tạo (Design Thinking & Innovation)  
> **Đơn vị:** Vietnam MIT University  
> **Nhóm thực hiện:** Nhóm 7 — Quyết Chiến  
> **Chủ đề:** CAMPUS AND STUDENT LIFE — Hỗ trợ sinh viên gặp khó khăn trong việc học ngôn ngữ  
> **Persona nghiên cứu:** Lê Văn Trọng (18 tuổi, Sinh viên năm nhất)

---

## 🌟 1. Vấn đề & Giải pháp (Design Thinking)

### 📌 Thấu cảm (Empathize) & Xác định vấn đề (Define)
- **Persona:** Lê Văn Trọng (18 tuổi), tân sinh viên muốn đạt chuẩn đầu ra đại học và giao tiếp tự tin, nhưng bị **mất gốc**, sợ sai, tự ti khi nói, và áp lực khi bài giảng trên lớp quá nhanh.
- **Nỗi đau (Pain points):** Bỏ ngang Duolingo vì streak tạo áp lực như "nhiệm vụ bắt buộc"; học trước quên sau vì thiếu ôn tập ngắt quãng; không dám mở miệng nói vì sợ bị người khác soi xét, đánh giá.
- **HMW (How Might We):** *Làm thế nào chúng ta có thể hỗ trợ sinh viên mất gốc ôn luyện kiến thức một cách hiệu quả với lưu lượng hợp lý?*

### 💡 Khởi tạo ý tưởng (Ideate) & Tính năng cốt lõi
1. **Lặp lại ngắt quãng (Spaced Repetition):** Sổ thẻ 3D lật mặt (Hộp 1 đến 5), tự động tính toán thời gian sắp quên để nhắc ôn tập đúng thời điểm.
2. **Phương pháp Feynman ("Dạy lại cho Bắp"):** Sau mỗi bài học, sinh viên đóng vai người hướng dẫn để giảng lại kiến thức cho mascot **Bắp** (học sinh mới) bằng từ ngữ bình dân, đơn giản nhất.
3. **Đồng hồ Pomodoro 25/5 & Quy tắc 70/30:** 25 phút tập trung cao độ, 5 phút nghỉ ngơi; trong đó **70% thời gian** dành cho củng cố thẻ nhớ, **30% thời gian** luyện bài tập phản xạ.
4. **Bạn AI luyện nói không phán xét (Voice AI Buddy):** Trò chuyện bằng giọng nói qua micro (Speech-to-Text), AI hồi đáp bằng giọng bản ngữ (Text-to-Speech) và chấm điểm độ chuẩn xác từng từ (xanh/đỏ) để tăng phản xạ mà không lo bị chê cười.
5. **Thông điệp mỗi ngày (Daily Quote):** Mỗi ngày một câu châm ngôn truyền cảm hứng bằng ngoại ngữ đang học kèm phiên âm và audio.
6. **Kiểm tra đột xuất (Pop Quiz):** 3 câu hỏi nhanh bất kỳ lúc nào để kích hoạt khả năng truy xuất trí nhớ chủ động (active recall).

---

## 🚀 2. Cách Chạy Ứng Dụng (Không Cần Bỏ Tiền Ra Zip, Miễn Phí 100%)

Ứng dụng được viết theo chuẩn **Web Công nghệ Hiện đại (HTML5, Vanilla JS, CSS3, PWA)**:
- **Không cần cài đặt Node.js hay npm**: Chạy được ngay lập tức trên mọi máy tính và điện thoại.
- **Dữ liệu lưu trữ LocalStorage**: Toàn bộ tiến độ học, sổ thẻ nhớ và streak được lưu thẳng trên máy bạn, hoạt động offline mượt mà không tốn tiền server.

### Cách 1: Chạy trên Máy tính (PC / Laptop)
1. Nhấp đúp vào tệp `start_app.bat` (hoặc nhấp đúp trực tiếp vào tệp `index.html`).
2. Ứng dụng sẽ tự động mở trên trình duyệt (Microsoft Edge, Google Chrome, Cốc Cốc, Brave, Safari).
3. **Mẹo xem giao diện Điện thoại (Mobile App):**
   - Trên trình duyệt, nhấn phím `F12` (hoặc chuột phải chọn *Kiểm tra / Inspect*).
   - Nhấn vào biểu tượng điện thoại `Ctrl + Shift + M` (Toggle device toolbar) để trải nghiệm giao diện di động vuốt chạm mượt mà.

### Cách 2: Cài đặt thành App trên Điện thoại (PWA)
1. Tải thư mục này lên GitHub Pages / Vercel / Netlify (hoặc mở trên mạng nội bộ).
2. Mở đường link trên Safari (iOS) hoặc Chrome (Android).
3. Nhấn **Chia sẻ / Menu ba chấm** ➔ Chọn **"Thêm vào màn hình chính" (Add to Home Screen)**.
4. Biểu tượng **Bánh Mì Ngôn Ngữ** sẽ xuất hiện trên màn hình điện thoại như một app native cài từ App Store / CH Play!

---

## 📂 3. Cấu Trúc Mã Nguồn

```
Ho tro hoc sinh hoc ngon ngu (App Bánh mì ngôn ngữ)/
├── index.html          # File giao diện chính SPA (Single Page Application)
├── manifest.json       # Cấu hình PWA để cài app lên điện thoại
├── sw.js               # Service Worker hỗ trợ chạy Offline
├── start_app.bat       # Phím tắt mở nhanh app bằng 1 cú nhấp chuột
├── README.md           # Hướng dẫn chi tiết đề tài
├── css/
│   └── styles.css      # Hệ thống màu bánh mì, card mềm, 3D flip card, dark mode
├── js/
│   ├── data.js         # 40 câu hỏi kiểm tra, 36 bài ngữ pháp, 100+ từ vựng, IPA, Quotes
│   ├── storage.js      # Bộ nhớ LocalStorage & Thuật toán lặp lại ngắt quãng (Leitner)
│   ├── speech.js       # Tích hợp Web Speech API (Text-to-Speech & Speech-to-Text)
│   └── app.js          # Controller điều hướng, bài học Feynman, Pomodoro, AI Chat
└── assets/
    └── logo.svg        # Biểu tượng linh vật ổ bánh mì nướng vàng giòn
```

---

## 👥 4. Thành Viên Nhóm 7 (Quyết Chiến)

| Họ và Tên | MSSV | Chức Vụ | Công Việc Đảm Nhận |
| :--- | :---: | :---: | :--- |
| **NGUYỄN THẾ HUY** | 1326110004 | **CEO** | Bàn giao việc, điều chỉnh nội dung và thiết kế Canva |
| **TRẦN HUỲNH MINH ĐĂNG** | 1326110015 | **CTO** | Xây dựng nội dung học & kiến trúc logic hệ thống |
| **ĐINH NGUYỄN PHÚC LỘC** | 1326110040 | **Thư ký** | Làm nội dung, kiểm tra chất lượng & thiết kế Canva |
| **NGUYỄN THIỆN PHÁT** | 1326110058 | **CPO** | Tìm kiếm tư liệu hình ảnh, xây dựng ý tưởng sản phẩm |
| **NGUYỄN HỮU LỘC** | 0026110118 | **CMO** | Thiết kế trực quan Canva & truyền thông |

---

*Chúc các bạn nhóm 7 thuyết trình môn Tư duy thiết kế và Đổi mới sáng tạo đạt điểm A+ xuất sắc!* 🥖🚀
