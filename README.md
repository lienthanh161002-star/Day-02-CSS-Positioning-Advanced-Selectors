# Day-02-CSS-Positioning-Advanced-Selectors
🎯 Mục tiêu bài học
Làm chủ 4 kiểu định vị trong CSS: Static, Relative, Absolute, Fixed.

Hiểu sâu về cách kết hợp các bộ chọn (Combining Selectors) để viết CSS sạch và tối ưu.

🛠 Kỹ thuật trọng tâm: CSS Positioning
Hôm nay mình đã giải mã được câu hỏi: "Phần tử này đang nhảy theo ai?"

Static (Mặc định): Đứng im trong hàng ngũ, không bị ảnh hưởng bởi top/left.

Relative: Di chuyển so với chính nó. Dùng để làm "mỏ neo" cho con.

Absolute: Thoát ly khỏi hàng ngũ, tìm tổ tiên gần nhất có Relative để làm mốc.

Fixed: Dính chặt vào màn hình (Viewport), dùng cho Header hoặc nút Back-to-top.

🚩 Dự án thực hành: The Flag Project
Mình đã áp dụng mô hình Cha (Relative) - Con (Absolute) để vẽ lá cờ:

Tại sao? Khi di chuyển khung lá cờ (Cha), các chi tiết bên trong (Con) sẽ tự động chạy theo mà không bị lệch bố cục. Đây là tư duy "nhóm 3" - viết code bền vững.

⚠️ Những lỗi dễ "xoắn não" (Post-mortem)
Lỗi Selector: Dấu cách là ranh giới của cấp bậc.

li.done: Chọn chính thẻ li có class done.

li .done: Chọn phần tử bất kỳ có class done nằm bên trong li.

Lỗi Định vị: Quên đặt position: relative cho thẻ cha khiến thẻ con absolute bay ra tận mép màn hình.

💡 Bài học về UX & Developer Experience (DX)
UX: Header cố định (fixed) giúp người dùng không phải cuộn chuột ngược lên để tìm menu.

DX: Đặt tên class rõ ràng và dùng đúng Selector giúp code dễ bảo trì, tránh việc sửa chỗ này hỏng chỗ kia.
<style>
    .red-circle {
      width: 200px;
      height: 200px;
      background-color: red;
      border-radius: 50%;
      position: absolute;
      top: 150px;
      left: 250px;
    }
    
    .blue-box {
      background-color: blue;
      width: 500px;
      height: 300px;
      position: relative;
      top: 200px;
      left: 200px;
    }

  </style>
</head>

<body>
  <div class="blue-box">
    <div class="red-circle"></div>
  </div>
</body>
