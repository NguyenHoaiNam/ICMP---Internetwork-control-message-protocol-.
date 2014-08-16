###ICMP---Internetwork-control-message-protocol---
==============================================
**Nội dung về giao thức ICMP:**
* Khái niệm
* Cấu trúc gói tin ICPM
* Các kiểu mã code, trường

----

- **1. Khái niệm:** Giao thức ICMP là một giao thức hoạt động trên lớp 3 ( network) trong mô hình OSI, và nó là một giao thức điều khiển trong mô hình TCP/IP. Được dùng để trao đổi thông tin điều khiển giữa các thiết bị trong mạng bằng cách định ra các thông điệp hiện tại có thể truyền được gói tin hay không.

----

- **2. Cấu trúc gói tin ICMP:**

----------------
|Type|Code|Checksum|
|----|---|--------|
|ID|SEQ Number|
--------------

*Trong đó:* 

- Type: Sẽ cho chúng ta biết dạng của gói tin, có 8 bít dành cho TYPE ICMP vậy nếu tính tổng có khoảng 255 dạng ICMP nhưng chỉ có 8 dạng hay dùng và cần quan tâm nhất
- Code: Xem thông tin thông điệp
- Check sum : Ý nghĩa sử dụng để tính toán tổng cộng gói Header+data của gói ICMP
- ID: Thiết lập này có ý nghĩa cho dạng Echo Reply
- SEQ Number : ý nghĩa bao gồm các thông số cho quá trình trả lời Echo Reply

Một trong những protocols tại tầng Internet trong mô hình TCP/IP là ICMP. Nó có tác dụng cung cấp khả năng phân tích và đưa ra các lỗi logic. Gói tin ICMP có một dạng cơ bản. Byte đầu tiên trong gói ICMP Header sẽ cho chúng ta biết dạng của gói ICMP (ICMP Type). Các byte sau của một dạng ICMP sẽ là mã của gói ICMP (ICMP Code). Các dạng gói tin ICMP cho cúng ta biết các vấn đề khi phân tích kết nối, còn mã của gói tin cho chúng ta biết chính sác lỗi đó thuộc về vấn đề gì.

-----

- **3. Chi tiết các type và code trong bản tin ICMP**

Có tất cả tổng công có 255 dạng ICMP trong đó có 8 dạng cơ bản hay gặp sau đây:

<img class="image__pic js-image-pic" src="http://i.imgur.com/WcMTstL.png" alt="" id="screenshot-image">

