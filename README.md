# HIS-BVCHORAY-LECTURE5-6TESTING-N23DCPT091
HIS – Hospital Information System (Lab)

Sinh viên: Nguyễn Đỗ Tú Mai
MSSV: N23DCPT091

1) Mục tiêu

Thiết kế CSDL cho hệ thống HIS (đăng ký khám, EMR, xét nghiệm, kê đơn, thanh toán).

Cung cấp script tạo bảng, seed dữ liệu, trigger tự tính tổng tiền, view báo cáo.

Đính kèm “dấu vết” MSSV trong DB để xác thực người thực hiện.

2) Yêu cầu môi trường

MySQL Server 8.x, MySQL Workbench 8.x

Collation khuyến nghị: utf8mb4_0900_ai_ci

3) Cấu trúc thư mục
.
├─ his_schema_choray.sql                # Tạo database + bảng
├─ his_seed.sql                         # Seed dữ liệu mẫu + cập nhật tổng tiền
├─ his_triggers.sql                     # Trigger tự động cập nhật total_amount
├─ his_views.sql                        # View báo cáo
├─ his_NGUYEN DO TU MAI_meta_N23DCPT091.sql     
├─ his_checks.sql                       # Câu lệnh kiểm tra nhanh
├─ run_all_N23DCPT091.sql               # Chạy tất cả theo thứ tự
└─ (tùy chọn) ERD_HIS_from_SQL.png      # Ảnh ERD xuất từ Workbench

4) Cách chạy (MySQL Workbench)
Cách A – One click

File → Open SQL Script… → mở run_all_N23DCPT091.sql

Bấm Execute (tia sét).

Cách B – Từng bước

Mở & chạy his_schema_choray.sql

Mở & chạy his_seed.sql

(Tuỳ chọn) his_triggers.sql

(Tuỳ chọn) his_views.sql

his_NGUYEN DO TU MAI_meta_N23DCPT091.sql

his_checks.sql

Lưu ý: Script đã dùng câu UPDATE ... WHERE invoice_id IN (...) nên không cần tắt Safe Update Mode.

5) Kiểm tra nhanh (đối chiếu kết quả)

Chạy các câu sau để xác nhận cấu hình 2025
Bài thực hành môn Nhập môn Công nghệ Phần mềm – chủ đề Requirements & Analysis → HIS.
