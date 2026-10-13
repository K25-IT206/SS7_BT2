# Bài 2 - Phân tích và vá lỗi báo cáo Velocity và Burndown Chart của Sprint 4

## Phần 1 - Phân tích

| Nhận định | Đúng / Sai | Căn cứ trong dữ liệu | Hậu quả nếu giữ nguyên |
|---|---|---|---|
| BC1. Velocity Sprint 4 = 21 SP: 15 SP của các PBI Done cộng 6 SP cho PBI ví RikkeiPay đã làm khoảng 75%. | Sai | Velocity chỉ tính SP của PBI đạt DoD. Các PBI Done trong Sprint 4 là 5 + 5 + 3 + 2 = 15 SP; PBI ví RikkeiPay chưa đạt DoD nên tính 0 SP, dù đã làm khoảng 75%. | Báo cáo Velocity bị phóng đại, làm sai kế hoạch và đánh giá hiệu suất đội. |
| BC2. Ngày 1 sang ngày 2 đường nằm ngang, nên tại Daily Scrum đội hỏi nhau có Task nào quá lớn hoặc đang làm dở quá nhiều việc cùng lúc. | Đúng | Đường ngang là tín hiệu cần tìm nguyên nhân, không phải kết luận rằng đội làm chậm. Câu hỏi về task lớn hoặc multitasking là cách phù hợp để kiểm tra. | Nếu không rà soát, team sẽ bỏ qua rào cản thực tế như blocker, task quá lớn hoặc bị chia nhỏ không hợp lý. |
| BC3. Ngày 3 đường tăng từ 21 lên 24, chứng tỏ Developers làm việc chậm. | Sai | Dữ liệu cho thấy ngày 3 có thêm PBI mới “Hiển thị mã khuyến mãi trên hóa đơn” với 3 SP, nên đường tăng là do scope mới, không phải do năng suất giảm. | Team sẽ đánh giá sai mức độ sản xuất và làm mất niềm tin vào báo cáo. |
| BC4. Ngày 10, đội sửa số còn lại từ 11 về 0 để Actual Line chạm đúng điểm cuối của Ideal Line. | Sai | Nếu Sprint kết thúc với PBI ví RikkeiPay chưa Done và mã khuyến mãi chưa làm, thì SP còn lại thực tế vẫn là 11 SP (8 + 3). Không được “làm đẹp” số liệu để chạm ideal line. | Burndown Chart mất tính trung thực, dẫn đến đánh giá sai tiến độ và chất lượng dự báo sprint. |
| BC5. PBI ví RikkeiPay chỉ còn thiếu Integration Test, nên được tự động chuyển sang Sprint 5 với 2 SP còn lại. | Sai | PBI chưa Done phải quay lại Product Backlog để PO xem xét thứ tự; không có chuyển tự động “2 SP còn lại”. PBI này vẫn là 8 SP theo đầu bài, chưa đạt DoD. | Team sẽ bỏ qua nguyên tắc DoD và làm sai quản lý backlog, gây xáo trộn kế hoạch sprint tiếp theo. |

## Phần 2 - Vá lỗi

### 1) Tính lại Velocity Sprint 4
Velocity Sprint 4 = tổng SP của các PBI đạt DoD trong Sprint = 5 + 5 + 3 + 2 = 15 SP.

- Hủy chuyến trước khi tài xế nhận: 5 SP, Done
- Đánh giá tài xế sau chuyến đi: 5 SP, Done
- Lưu địa chỉ yêu thích: 3 SP, Done
- Đổi ảnh đại diện: 2 SP, Done
- Thanh toán bằng ví RikkeiPay: 8 SP, chưa đạt DoD → 0 SP
- Hiển thị mã khuyến mãi trên hóa đơn: 3 SP, chưa làm → 0 SP

=> Velocity Sprint 4 = 15 SP.

### 2) Số SP còn lại đúng của ngày 10
Số SP còn lại đúng của ngày 10 là 11 SP.

- PBI ví RikkeiPay chưa Done: 8 SP
- PBI “Hiển thị mã khuyến mãi trên hóa đơn” chưa làm: 3 SP

=> 8 + 3 = 11 SP

### 3) Cách xử lý PBI ví RikkeiPay
PBI ví RikkeiPay chưa đạt DoD nên phải quay lại Product Backlog để Product Owner và Developers rà soát lại mức độ ưu tiên, rủi ro tích hợp và điều kiện hoàn thành trước khi đưa vào Sprint 5. Nó không được coi là 2 SP còn lại, và cũng không được tự động chuyển nhầm vì đã làm gần xong; cần làm rõ phần thiếu sót (ví dụ Integration Test) và chốt lại kế hoạch theo đúng DoD.

---

### Kết luận ngắn
- Velocity phải phản ánh đúng công việc đã hoàn thành theo DoD, không cộng theo phần trăm.
- Burndown phải phản ánh real work remaining, không được chỉnh số liệu để “đẹp” hơn.
- PBI chưa Done phải trở lại Product Backlog để quyết định ưu tiên và kế hoạch tiếp theo.
