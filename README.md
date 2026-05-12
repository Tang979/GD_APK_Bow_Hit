# Bow Hit

## Video Gameplay
[Watch Gameplay](https://youtube.com/shorts/F9uFyXbLhtk)

## APK
[Download APK](https://github.com/Tang979/GDD_APK_Bow_Hit/releases)

## Source Code
[View Source Code](https://github.com/nguyenkhacnhat203-dev/BowGame2D)

---

## 1. Tổng quan
- **Tên game:** Bow Hit  
- **Thể loại:** Casual / Arcade  
- **Nền tảng:** Mobile (Android / iOS)  
- **Chế độ chơi:** Single-player  
- **Đối tượng người chơi:** Mọi lứa tuổi  

### Giới thiệu
Bow Hit là game casual bắn cung, người chơi cần bắn các mũi tên vào bàn gỗ đang xoay mà không được va chạm với các mũi tên đã ghim trước đó. Một số màn chơi yêu cầu người chơi bắn trúng táo để nhận thêm phần thưởng và hoàn thành điều kiện chiến thắng.

### Mục tiêu thiết kế
- Gameplay đơn giản, dễ tiếp cận  
- Có độ thử thách tăng dần theo level  
- Tạo trải nghiệm phản xạ nhanh và gây nghiện ngắn hạn  

---

## 2. Cấu trúc Scene

### Load Scene
- Hiển thị logo game  
- Khởi tạo dữ liệu game và loading  

### Home Scene
- Nút Play  
- Shop  
- Setting  
- Hiển thị số lượng đá quý  

### Gameplay Scene
- Bàn gỗ xoay  
- Hệ thống mũi tên  
- Táo xuất hiện trên bàn xoay  
- UI gameplay:
  - Số lượng mũi tên còn lại  
  - Số lượng táo cần bắn  
  - Pause button  

---

## 3. Core Gameplay Loop
1. Khởi tạo level và số lượng mũi tên  
2. Người chơi chạm màn hình để bắn tên  
3. Mũi tên ghim vào bàn gỗ đang xoay  
4. Tránh va chạm với các mũi tên đã ghim trước đó  
5. Bắn trúng táo để nhận thêm đá quý  
6. Hoàn thành đủ điều kiện để chiến thắng level  

---

## 4. Luật chơi
- Chạm màn hình để bắn tên  
- Nếu mũi tên va chạm với mũi tên đã ghim → thất bại  
- Một số level yêu cầu bắn trúng đủ số lượng táo  
- Bàn gỗ có thể:
  - Xoay đều  
  - Đổi hướng  
  - Tăng tốc trong một khoảng thời gian  

---

## 5. Điều kiện thắng
Người chơi chiến thắng khi:
- Ghim đủ số lượng mũi tên yêu cầu  
- Và hoàn thành đủ điều kiện táo của level  

---

## 6. Điều kiện thua
Game Over khi mũi tên bắn vào trúng mũi tên đã ghim trên bàn xoay.

---

## 7. Tính năng chính
- Gameplay bắn cung một chạm  
- Hệ thống bàn xoay thay đổi tốc độ  
- Hệ thống táo và đá quý  
- Level progression  
- Revive system  
- Shop skin và theme  

---

## 8. Công việc tôi thực hiện
- Đọc hiểu gameplay flow và codebase hiện tại  
- Phát triển thêm cơ chế xoay mới cho bàn xoay:
  - Tăng tốc đột ngột trong một khoảng thời gian  
- Setup level sử dụng cơ chế xoay mới nhằm tăng độ khó và đa dạng gameplay  
- Điều chỉnh thông số tốc độ và thời gian tăng tốc để đảm bảo trải nghiệm chơi hợp lý  

---

## 9. Technical Challenges
### 1. Đồng bộ tốc độ xoay động
- Thay đổi tốc độ xoay trong runtime nhưng vẫn đảm bảo:
  - Gameplay ổn định  
  - Collision chính xác  
  - Không ảnh hưởng tới timing bắn tên  

### 2. Cân bằng độ khó level
- Thiết kế mức tăng tốc phù hợp để:
  - Tạo thử thách mới  
  - Không khiến gameplay trở nên quá khó hoặc mất kiểm soát  

### 3. Tích hợp cơ chế mới vào hệ thống cũ
- Thêm kiểu xoay mới mà không ảnh hưởng các cơ chế xoay hiện có của game.

---

## 10. Tech Stack
- Unity  
- C#  
- PlayerPrefs  
- AdMob  
