# Luyện viết chữ HP001 – Soạn văn bản vở ô ly

Công cụ chạy ngay trên trình duyệt, chuyển văn bản tiếng Việt sang **nét chữ nối HP001** trên **giấy vở 4 ô ly khổ A4**, rồi xuất **PDF** hoặc **DOCX** để in làm giấy tập viết / giấy thi viết chữ đẹp.

Toàn bộ công cụ là **một file HTML duy nhất**, không cần cài đặt, không cần máy chủ.

## Tính năng

- **Đổi chữ sang nét nối HP001:** gõ hoặc dán văn bản, kết quả hiện ngay trên trang vở. Font HP001 được nhúng sẵn trong file, máy in không cần cài font.
- **Quét chữ từ ảnh bằng Gemini:** chụp hoặc dán ảnh bài viết, công cụ nhận dạng chữ rồi đưa vào ô văn bản (cần Gemini API key của bạn).
- **Giấy vở ô ly A4:** ô lớn 10mm chia 4 ô ly, kẻ đậm đen, kẻ mảnh xám, có gạch đôi bên trái. Chữ đứng trên đường kẻ đậm.
- **3 mẫu giấy:**
  - Giấy thi (đủ tiêu đề: ngày tháng, họ tên, tuổi, lớp, trường, địa chỉ, đường cắt, điểm, số phách)
  - Giấy tập viết (tiêu đề gọn)
  - Chỉ lưới ô ly
- **Đặt chữ đúng ô theo quy định:**
  - Tiêu đề bài viết bắt đầu từ ô số N (mặc định ô 4)
  - Đầu mỗi đoạn bắt đầu từ ô số N (mặc định ô 2), các dòng sau quay về ô 1
  - Dấu cách gõ ở đầu đoạn cộng thêm để thụt lề
- **Kiểu chữ:** chữ thẳng hoặc chữ nghiêng.
- **Nét chữ:** thường, đậm, hoặc **mờ** (để học sinh tô theo).
- **Màu chữ:** 6 màu có sẵn và ô chọn màu tùy ý.
- **Dịch chữ ngang:** nút ◀ ▶, ô nhập số và thanh trượt để dịch chữ sang trái/phải theo px.
- **Tự sang trang:** văn bản dài tự chia thêm trang A4.
- **Xuất file:** PDF hoặc DOCX khổ A4, độ phân giải 300 dpi.
- Các lựa chọn (mẫu giấy, kiểu chữ, màu, vị trí ô, độ dịch) được **nhớ cho lần mở sau**.

## Cách dùng

1. Mở file `.html` bằng trình duyệt (Chrome, Edge, Firefox, Safari).
2. Gõ hoặc dán văn bản vào ô nhập. Nếu muốn quét từ ảnh, nhập Gemini API key ở phần cài đặt.
3. Chọn mẫu giấy, kiểu chữ, nét chữ, màu chữ ở dưới trang vở.
4. Chỉnh **Tiêu đề từ ô**, **Đầu đoạn từ ô** và **Dịch chữ ngang** nếu cần.
5. Bấm **Tải PDF** hoặc **Tải DOCX** rồi in ra giấy A4.

Gợi ý: nếu văn bản không có dòng tiêu đề riêng, bỏ tick **Dòng đầu là tiêu đề**.

## Lưu ý

- Hai nút **Tải PDF** và **Tải DOCX** cần Internet ở lần đầu để nạp thư viện từ CDN. Phần xem trước hoạt động không cần mạng.
- File PDF/DOCX là **ảnh** của trang giấy, nên chữ trong Word không sửa được. Muốn sửa thì sửa ở ô văn bản rồi xuất lại.
- Mỗi dấu cách giữa các từ rộng khoảng 1 ô ly nhỏ.
- Gemini API key được lưu trong trình duyệt của bạn (localStorage), không gửi đi đâu ngoài Google. Đừng đưa file đã nhập key lên nơi công khai.
- Tên model Gemini có thể thay đổi theo thời gian. Nếu báo model không tồn tại, đổi sang tên model mới hơn trong phần cài đặt.

## Công nghệ

- HTML, CSS, JavaScript thuần, vẽ trang giấy bằng `<canvas>`
- [jsPDF](https://github.com/parallax/jsPDF) để xuất PDF
- [docx](https://github.com/dolanmiu/docx) để xuất DOCX
- Google Gemini API để nhận dạng chữ từ ảnh

## Bản quyền font

Font HP001 là của tác giả font tương ứng. Hãy kiểm tra giấy phép sử dụng và phân phối của font trước khi đưa file có nhúng font lên GitHub công khai.

## Giấy phép

Chưa chọn giấy phép. Thêm file `LICENSE` (ví dụ MIT) nếu bạn muốn cho phép người khác dùng lại mã nguồn.
