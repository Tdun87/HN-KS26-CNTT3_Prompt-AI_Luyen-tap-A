# BÀI LÀM PHA 2 (ĐỀ LUYỆN TẬP CHỦ ĐỀ CHẠY AFFILIATE)

- **Họ tên:**Nguyễn Thế Huy
- **Lớp:**CNTT3
- **Link repository Pha2:**https://github.com/mrwe08/test_promting_final
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):**gemini

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đăng ký gói Affiliate ra JSON

**KET QUA AI**

```text
[
  {
    "ma_goi": "TT",
    "ngay_bat_dau": "2026-12-20",
    "creator_chinh": 2,
    "thuc_tap_sinh": 1,
    "hang_tai_khoan": "thuong",
    "ghi_chu": null
  },
  {
    "ma_goi": "SP",
    "ngay_bat_dau": "2027-01-08",
    "creator_chinh": 3,
    "thuc_tap_sinh": 0,
    "hang_tai_khoan": "thuong",
    "ghi_chu": "Có một bạn đang bó bột chân cần ngồi bàn gần cửa ra vào"
  },
  {
    "ma_goi": "PRO",
    "ngay_bat_dau": null,
    "creator_chinh": 4,
    "thuc_tap_sinh": 0,
    "hang_tai_khoan": "vip",
    "ghi_chu": "cần mượn thêm đèn trợ sáng và phông xanh để quay mẫu"
  }
]
```

**Link trò chuyện:**https://share.gemini.google/PTJCzyi3Z2mj

## 4.3. Báo giá gói Affiliate bằng Chain-of-Thought

**KET QUA AI**

```text
Tiền Creator chính: 4 × 1.500.000 = 6.000.000 đồng

Tiền thực tập sinh: (2 × 1.500.000 × 60%) + (1 × 0) = 1.800.000 đồng

Tổng tiền gói: 6.000.000 + 1.800.000 = 7.800.000 đồng

Giảm giá team: 7.800.000 × 10% = 780.000 đồng (còn 7.800.000 - 780.000 = 7.020.000 đồng)

Phụ thu thuê mic: 2 × 250.000 = 500.000 đồng

Tổng tiền: 7.020.000 + 500.000 = 7.520.000 đồng

[RESULT: 7.520.000 đồng]
```

**Link trò chuyện:**https://share.gemini.google/4ga74qeM2VBU

### b) Kiểm tra kết quả AI

đúng

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
  "loai_su_co": "sai_phong",
  "so_khach": 3,
  "so_ca_bi_anh_huong": 2,
  "tom_tat": "Nhóm 3 khách hàng (gói TT đợt thực chiến Mega Sale ngày 11/11/2026) bị xếp nhầm sang phòng học thường thiếu đèn livestream và vách cách âm như cam kết trong 2 ca thực hành đầu. Mức đền bù theo chính sách: hoàn 300.000 đồng/khách/ca x 3 khách x 2 ca = 1.800.000 đồng. Vì tổng mức đền bù trên 1.500.000 đồng, cần trình Trưởng bộ phận Chăm sóc Publisher duyệt trước khi phản hồi khách hàng."
}
```

**Link trò chuyện:**https://share.gemini.google/5nt5tF2oogLH

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
| :--- | :--- | :--- | :--- |
| **Đúng thông tin (50%)** | 0 / 5,0 | **Lỗi sai & Nguyên do:** Sai lệch hoàn toàn so với thông tin chuẩn của trung tâm do không đối chiếu dữ liệu quy định.<br>1. **Giá gói:** Báo *"1.200.000đ/người"* (thông tin chuẩn là **1.500.000 đồng/Creator chính**).<br>2. **Chính sách huỷ:** Báo huỷ trước 5 ngày được *"hoàn lại đủ 100% tiền"* (thông tin chuẩn quy định huỷ trước từ 3 đến 6 ngày chỉ được **hoàn 50%**). | Cung cấp lại đúng dữ liệu chuẩn:<br>- **Giá gói TT:** 1.500.000 đồng/Creator chính.<br>- **Chính sách huỷ:** Huỷ trước ngày bắt đầu 5 ngày (nằm trong mốc từ 3 đến 6 ngày) sẽ được **hoàn lại 50% tiền** (mất 50% phí đăng ký). |
| **Đầy đủ (30%)** | 2,0 / 3,0 | - **Đạt:** Đã giải đáp đủ 2 câu hỏi của khách hàng (mức giá và điều kiện hoàn tiền khi huỷ trước 5 ngày).<br>- **Lỗi sai & Nguyên do:** Bỏ sót bước khai thác thông tin chốt đơn theo quy trình; chưa mời khách hàng cung cấp **ngày đợt thực chiến** và **số lượng suất muốn đăng ký**. | Giữ nội dung trả lời 2 ý hỏi và bổ sung câu mời thông tin ở cuối: *"Bạn vui lòng cho mình xin thông tin về ngày đợt thực chiến dự kiến tham gia và số lượng suất muốn đăng ký để trung tâm hỗ trợ giữ chỗ nhé."* |
| **Giọng điệu (20%)** | 0 / 2,0 | **Lỗi sai & Nguyên do:** Sử dụng văn phong thiếu chuẩn mực trong tư vấn dịch vụ và đưa ra lời hứa hẹn sai thực tế.<br>1. **Từ ngữ suồng sã:** *"hello bạn nha"*, *"chốt lẹ kẻo hết slot nè"*.<br>2. **Cam kết doanh thu/hoa hồng ảo:** *"đăng ký xong gắn link là nổ đơn hoa hồng trăm triệu luôn ạ"*. | Thay thế bằng ngôn ngữ lịch sự, chuyên nghiệp, loại bỏ toàn bộ từ lóng và cam kết thu nhập không có căn cứ. Sửa thành: *"Chào bạn, trung tâm Vietaffiliate xin gửi đến bạn thông tin chi tiết về gói TikTok Affiliate (TT) như sau..."* |
| **Tổng điểm** | **2,0 / 10** | | |
```

**Link trò chuyện:** https://share.gemini.google/kpjtudtVAull
