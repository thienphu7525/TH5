# TH5
2.1 Gán nhãn ảnh
•	Mục đích: Gán nhãn các vùng khác nhau trong ảnh (được phân ngưỡng bằng Otsu) và vẽ khung bao quanh từng đối tượng đã được phát hiện
•	Cách hoạt động:
  	Chuyển ảnh sang thang xám
  	Dùng ngưỡng Otsu để tách nền và đối tượng
  	Gán nhãn cho các vùng liên kết bằng hàm label
  	Lưu ảnh gán nhãn
  	Dùng regionprops để lấy thông tin từng vùng (bounding box)
  	Vẽ khung bao quanh từng đối tượng
2.2 Dò tìm cạnh theo chiều dọc
•	Mục đích: Phát hiện cạnh theo chiều dọc bằng cách lấy hiệu giá trị ảnh với ảnh bị dịch chuyển 1 pixel sang phải
•	Cách hoạt động:
  	Dịch chuyển ảnh gốc sang phải 1 pixel
  	Lấy hiệu trị tuyệt đối giữa ảnh gốc và ảnh dịch chuyển để phát hiện sự thay đổi cường độ (cạnh)
  	Hiển thị ảnh cạnh
2.3 Dò tìm cạnh với Sobel Filter
•	Mục đích: Phát hiện cạnh tổng hợp theo cả 2 hướng ngang và dọc bằng bộ lọc Sobel
•	Cách hoạt động:
  	Dùng Sobel để tính đạo hàm theo trục x (dọc) và y (ngang)
  	Tổng trị tuyệt đối của 2 đạo hàm này thể hiện cường độ cạnh
  	Hiển thị ảnh cạnh
2.4 Xác định góc của đối tượng
•	Mục đích: Tính toán điểm góc của ảnh bằng thuật toán Harris
•	Cách hoạt động:
  	Tính đạo hàm theo 2 chiều (Sobel)
  	Tính ma trận cấu trúc (matrix C) với Gaussian lọc để mượt.
  	Tính giá trị R của Harris theo công thức
  	Hiển thị ảnh điểm góc
2.5 Dò tìm hình dạng cụ thể với Hough Transform
•	Mục đích: Phát hiện đường thẳng trong ảnh bằng biến đổi Hough
•	Cách hoạt động:
  	Khởi tạo accumulator array (mảng tích lũy)
  	Với các điểm có giá trị lớn hơn ngưỡng gamma, cập nhật accumulator theo công thức Hough
  	Trả về accumulator và hiển thị
  2.5.2 Dò tìm đường tròn trong ảnh
•	Mục đích: Tìm các điểm góc trong ảnh "bird.png" để phát hiện các điểm đặc trưng, có thể dùng làm tiền đề cho phát hiện hình tròn
•	Cách hoạt động:
  	Chuyển ảnh sang ảnh xám
  	Dùng hàm “corner_harris” để phát hiện điểm góc
  	Hiển thị kết quả

