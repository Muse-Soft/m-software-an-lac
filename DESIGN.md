# DESIGN.md — Landing page nhà hàng chay An Lạc (MSR-39)

> Tài liệu thiết kế chốt cho sprint TEC-304. Dev (task Dev của sprint) dựng đúng tài liệu này, không tự thêm màu, font hay khối ngoài danh sách. QA đối chiếu bản dựng với tài liệu này, kèm kiểm tra đa dạng theo OPERATIONS.md mục 16.5.

## 0. Khác biệt so với các project gần nhất (bắt buộc theo mục 16.5 — đã đọc thật ngày 2026-10-25)

Thứ tự project mới nhất lấy từ https://msoft.genalpha.dev/api/office (đối chiếu với mục "Khác biệt" trong DESIGN.md của Lửa Ấm). Đã đọc trực tiếp DESIGN.md của cả 3 project gần nhất trên GitHub:

1. **Lửa Ấm** (m-software-lua-am, TEC-297) — archetype ghi rõ trong file: **A5 Theo chương** (7 chương đánh số khổng lồ + mục lục chương ở hero); cặp font: **Fraunces + Be Vietnam Pro**; nhiệt màu: **tối-ấm** (nền nâu sẫm, chữ kem).
2. **Lá Xanh** (m-software-la-xanh, TEC-290) — archetype suy ra từ bố cục mô tả (file viết trước luật 16.5 nên không ghi mã): **A1 Editorial dọc** (hero toàn màn hình, các khối xếp dọc đều, ảnh lớn + khoảng trắng, lệch trục nhẹ); cặp font: **Playfair Display + Be Vietnam Pro**; nhiệt màu: **sáng-ấm** (nền kem ấm, chữ xanh rừng, nhấn đất nung).
3. **Tĩnh Trà** (m-software-tinh-tra, TEC-277) — archetype suy ra từ bố cục mô tả (file viết trước luật 16.5 nên không ghi mã): **A1 Editorial dọc** (hero rót trà toàn màn hình, 6 khối xếp dọc, lưới lệch editorial trong khối bộ sưu tập); cặp font: **Cormorant Garamond + Be Vietnam Pro**; nhiệt màu: **sáng-ấm** (nền giấy ấm, nhấn xanh trà đậm).

Lựa chọn cho An Lạc (đối chiếu trực tiếp với 3 project trên):

- **Archetype: A2 Split (chia đôi)** — KHÁC A5 của project liền trước (Lửa Ấm) và KHÁC A1 của project liền trước nữa (Lá Xanh), thỏa luật "không dùng lại archetype của 2 project liền trước".
- **Cặp font: Lora + Be Vietnam Pro** — KHÁC nguyên cặp của project liền trước Lửa Ấm (Fraunces + Be Vietnam Pro): font tiêu đề đổi sang Lora; cũng khác cặp Playfair Display + Be Vietnam Pro của Lá Xanh và Cormorant Garamond + Be Vietnam Pro của Tĩnh Trà.
- **Nhiệt màu: sáng-ấm** — KHÔNG vi phạm "tránh 3 project liên tiếp cùng nhiệt màu": chuỗi sáng-ấm của Lá Xanh → Tĩnh Trà đã bị Lửa Ấm (tối-ấm) cắt đứt, nên An Lạc sáng-ấm chỉ đứng sau 1 project tối-ấm, không tạo chuỗi 3 sáng-ấm liên tiếp.
- **Điểm nhấn đặc sắc riêng:** khung ảnh vòm cổng vườn + nhãn mùa tròn vàng nghệ (mô tả cụ thể ở mục 7).
- **Không đổi so với công thức gợi ý trong yêu cầu:** bảng màu (nền #FBF8F1, chữ #23402E, nhấn #C08A2D), cặp font (Lora + Be Vietnam Pro) và không khí (vườn thiền Nhật Bản + ẩm thực chay Việt) đều giữ nguyên, vì không vi phạm luật chống trùng nào — chỉ mở rộng bảng màu từ 3 mã gợi ý thành 6 mã đủ vai trò (thêm nền khối phụ, chữ phụ, nhấn phụ).

## 1. Tổng quan và phong cách tham chiếu (duy nhất)

- Sản phẩm: landing page 1 trang cho nhà hàng chay An Lạc — ăn chay thanh tịnh trong không gian vườn thiền, thực đơn thay đổi theo mùa.
- Phong cách tham chiếu duy nhất: **vườn thiền Nhật Bản gặp ẩm thực chay Việt** — tĩnh lặng, mộc mạc, nhiều khoảng thở; ảnh món chay và vườn xanh làm chủ đạo; chữ serif ấm, không bóng bẩy kiểu thương mại.
- CẤM: template bán hàng (giỏ hàng, nút mua ngay, banner khuyến mãi), icon stock đủ màu, ảnh sáng phẳng ban ngày kiểu sàn thương mại điện tử, lưới thẻ đều tăm tắp không có nhịp chia đôi.

## 2. Bảng màu (chỉ dùng đúng 6 mã dưới đây, không dùng màu ngoài bảng)

| Mã | Vai trò |
|---|---|
| `#FBF8F1` | Nền chính toàn trang (kem giấy ấm, sáng-ấm) |
| `#EDE5D3` | Nền khối phụ, nền thẻ món, nền form |
| `#23402E` | Chữ chính (tiêu đề + nội dung), nền chân trang |
| `#6A7B6E` | Chữ phụ: mô tả, ghi chú, nhãn nhỏ, placeholder trong form |
| `#C08A2D` | Nhấn chính (vàng nghệ): nút CTA, giá món, nhãn mùa, gạch chân liên kết khi rê chuột |
| `#7D9B76` | Nhấn phụ (xanh lá non): viền khung vòm, nền nhãn nhóm món, nền khối ảnh khi ảnh lỗi/chưa tải |

Quy tắc dùng màu:

- Nền sáng chiếm đa số diện tích; chữ xanh đậm trên nền kem phải đọc rõ, không dùng chữ phụ cho đoạn văn chính.
- Nhấn chính chỉ dùng cho nút CTA, giá, nhãn mùa và điểm nhấn nhỏ — không làm nền khối lớn.
- Ảnh lỗi tải thì hiện nền nhấn phụ kèm tên món/không gian bằng chữ xanh đậm, không để khung ảnh trống vỡ.

## 3. Chữ (typography)

- Font tiêu đề: **Lora** (serif, dùng cho H1/H2/H3 và tên món nổi bật).
- Font nội dung: **Be Vietnam Pro** (dùng cho đoạn văn, nút, form, ghi chú).
- Trong bản dựng An Lạc chỉ dùng đúng 2 font trên; nạp font từ Google Fonts, khai báo `font-display: swap`.

Thang kích thước:

| Cấp | Desktop | Mobile (≤768px) | Ghi chú |
|---|---|---|---|
| H1 | 64px / dòng 1.1 | 40px / dòng 1.15 | Chỉ 1 H1 ở hero |
| H2 | 40px / dòng 1.2 | 30px / dòng 1.25 | Tiêu đề mỗi khối |
| H3 | 24px / dòng 1.3 | 20px / dòng 1.35 | Tên món, tên không gian |
| Nội dung | 17px / dòng 1.7 | 16px / dòng 1.7 | Đoạn văn chính |
| Nhỏ/ghi chú | 14px / dòng 1.5 | 14px / dòng 1.5 | Giá mẫu, nhãn, chân trang |

- Breakpoint duy nhất: **768px** (trên = desktop, dưới hoặc bằng = mobile, các nửa chia đôi xếp chồng 1 cột, ảnh lên trước chữ).
- Tiêu đề căn trái theo lưới 1200px; không căn giữa máy móc toàn trang.

## 4. Lưới, khoảng cách và cấu trúc chia đôi (archetype A2)

- Khung nội dung tối đa **1200px**, lề hai bên 24px (mobile 16px).
- Mọi khối nội dung (trừ hero) đều **chia đôi**: một nửa ảnh, một nửa chữ, tỉ lệ 50/50 trên desktop; các khối đảo chiều xen kẽ nhau (khối chẵn ảnh trái — chữ phải, khối lẻ ảnh phải — chữ trái) để mắt người xem đi theo nhịp ziczac, nhìn là biết ngay trang chia đôi chứ không phải trang xếp dọc đều kiểu A1 hay trang theo chương kiểu A5.
- Khoảng cách dọc giữa các khối: **96px desktop / 56px mobile**.
- Khoảng cách giữa tiêu đề khối và nội dung dưới nó: 32px desktop / 24px mobile.
- Bo góc: ảnh khung vòm theo mục 7 (bo tròn phía trên); thẻ và form bo **12px**; nút bo **999px** (dạng viên thuốc) — giữ đúng các con số này, không tự thêm kiểu bo khác.
- Hero (phần Mở đầu) là ngoại lệ duy nhất không chia đôi: hero toàn màn hình theo yêu cầu nội dung, đóng vai trò "mở mâm" trước khi các khối chia đôi bắt đầu.

## 5. Bố cục trang (Mở đầu + 5 khối, đúng thứ tự)

### Mở đầu — Hero mâm chay toàn màn hình

- Ảnh toàn màn hình (chiều cao 100vh, tối thiểu 640px): một mâm chay đầy đặn nhìn từ trên xuống, đặt giữa vườn xanh.
- Lớp phủ tối nhẹ bằng màu chữ chính để chữ kem nổi rõ, không làm ảnh bị sáng phẳng.
- Lớp chữ: nhãn nhỏ "Nhà hàng chay — [CẦN BỔ SUNG: khu vực/thành phố]", H1 "An Lạc", 1 câu ngắn về ăn chay thanh tịnh giữa vườn thiền, 1 nút CTA nhấn chính "Xem thực đơn theo mùa" trỏ xuống khối Thực đơn.
- Dòng địa chỉ + điện thoại dưới nút: để placeholder **[CẦN BỔ SUNG]**.

### Khối 1 — Triết lý ăn chay (chia đôi: chữ trái — ảnh phải)

- 2–3 đoạn ngắn về triết lý: ăn chay là ăn chậm, ăn đủ, ăn theo mùa; nguyên liệu tươi từ vườn, nêm nếm nhẹ để giữ vị gốc của rau củ.
- 1 ảnh khung vòm (tỉ lệ 4:5): góc vườn thiền có đá, rêu và cây xanh.
- Không nhắc giá ở khối này.

### Khối 2 — Thực đơn theo mùa (chia đôi đảo chiều, 3 nhóm món)

- Mở đầu khối bằng 1 câu: thực đơn đổi theo mùa, món dưới đây là thực đơn mùa hiện tại (mùa là mẫu, chưa phải thực đơn thật).
- 3 nhóm món, mỗi nhóm là 1 hàng chia đôi (ảnh món 1 bên, danh sách món 1 bên, đảo chiều xen kẽ):
  - **Khai vị:** 2–3 món, mỗi món: tên món (H3) + 1 dòng mô tả ngắn + giá ghi rõ **"Giá mẫu"**.
  - **Món chính:** 3–4 món, cùng cấu trúc; món chính là trung tâm của thực đơn nên hàng của nhóm này có ảnh lớn nhất khối.
  - **Tráng miệng:** 2 món, cùng cấu trúc.
- Giá mẫu tham khảo (chỉ là giá mẫu, chờ giá thật): khai vị 45.000–65.000đ · món chính 85.000–120.000đ · tráng miệng 35.000–55.000đ.
- Dưới khối ghi chú 1 câu: toàn bộ giá trên là giá mẫu, giá thật ghi ở đây sau khi có thông tin thật.
- Không có nút mua/giỏ hàng — chỉ 1 liên kết chữ "Đặt bàn để thưởng thức" trỏ xuống form khối 5.

### Khối 3 — Không gian vườn thiền (chia đôi: ảnh trái — chữ phải)

- 2–3 đoạn ngắn về không gian: sân vườn rêu đá, lối đi sỏi, phòng ăn nhìn ra vườn, chỗ ngồi thiền sau bữa ăn.
- 2 ảnh khung vòm (tỉ lệ 4:5): lối vườn và góc phòng ăn nhìn ra vườn.
- Khối này chủ yếu để ảnh nói thay chữ.

### Khối 4 — Cảm nhận khách hàng (không chia đôi ảnh — 3 trích dẫn)

- 3 trích dẫn ngắn, mỗi trích dẫn: dấu ngoặc kép lớn (font Lora, màu nhấn chính) + 1–2 câu cảm nhận + tên người nói để placeholder **[CẦN BỔ SUNG]** (không tự bịa tên khách thật).
- Khối này không dùng ảnh, chỉ chữ và dấu ngoặc kép lớn làm điểm nhấn — là nhịp thở giữa hai khối nhiều ảnh.

### Khối 5 — Form đặt bàn (CHỈ giao diện) + chân trang

- H2 "Đặt bàn" + 1 câu nói rõ form chỉ là giao diện mẫu.
- Trường: Họ tên · Số điện thoại · Ngày mong muốn · Số người · Ghi chú.
- Nút gửi nhấn chính; khi bấm chỉ hiện dòng cảm ơn tại chỗ (JavaScript `preventDefault`), KHÔNG gửi đi thật, không có backend, không thanh toán.
- Chân trang nền chữ chính, chữ kem: địa chỉ, điện thoại, giờ mở cửa, người phụ trách — tất cả để placeholder **[CẦN BỔ SUNG]**.

## 6. Quy tắc hình ảnh

- Ảnh là nội dung chính: tổng diện tích ảnh trên trang lớn hơn diện tích chữ ở hero và khối 3; các khối còn lại ảnh và chữ chia đôi đều nhau.
- Chất lượng: ảnh mẫu chất lượng cao (rộng tối thiểu 1600px cho hero, 900px cho ảnh khối), nét, không vỡ hạt; mọi ảnh đều khai báo là **ảnh mẫu** trong kết quả bàn giao của Dev.
- Tông ảnh: sáng-ấm, xanh vườn tự nhiên, ánh sáng ban ngày dịu qua tán lá, đồng tông với bảng màu. Cấm ảnh tông lạnh xanh dương, ảnh tối u ám, ảnh chụp flash gắt.
- Tỉ lệ khung chốt: hero **16:9** (cắt phủ toàn màn hình), ảnh khối chia đôi **4:5** (dọc, khung vòm theo mục 7), ảnh món trong khối thực đơn **4:3**. Đặt `object-fit: cover`, không méo ảnh.
- Mọi ảnh có dự phòng khi lỗi tải: hiện nền nhấn phụ kèm tên món/không gian bằng chữ xanh đậm — không để khung ảnh trống vỡ.

## 7. Điểm nhấn đặc sắc riêng (bắt buộc)

**Khung ảnh vòm cổng vườn + nhãn mùa tròn vàng nghệ:** mọi ảnh khối chia đôi đều đặt trong khung vòm — bo tròn phía trên thành hình bán nguyệt (border-radius phía trên bằng 50% chiều rộng khung, phía dưới vuông), gợi cổng vườn thiền và mái chùa cong; viền khung dày 3px màu nhấn phụ xanh lá non. Mỗi nhóm món trong khối thực đơn mở đầu bằng một nhãn mùa hình tròn (đường kính 72px desktop / 56px mobile, nền nhấn chính vàng nghệ, chữ xanh đậm): ghi tên mùa của thực đơn (ví dụ "Mùa Thu") + 1 biểu tượng lá nhỏ. Người xem nhìn khung vòm và nhãn mùa tròn là biết ngay đây là trang An Lạc, không lẫn với trang xếp dọc đều, trang chia đôi trơn hay trang theo chương. Đây là yếu tố nhận diện duy nhất và bắt buộc của trang này — Dev không được thay khung vòm bằng khung chữ nhật thường hay bỏ nhãn mùa tròn.

## 8. Dữ liệu mẫu và placeholder (bắt buộc giữ đúng)

- Giá món: luôn ghi kèm chữ **"Giá mẫu"**; giá thật chờ PO/khách cấp.
- Các mục **[CẦN BỔ SUNG]** (địa chỉ, điện thoại, giờ mở cửa, người phụ trách, khu vực ở hero, tên người nói ở khối 4) giữ nguyên dạng placeholder trên bản demo — Dev/QA không tự bịa số liệu thật.
- Toàn bộ ảnh trên trang là **ảnh mẫu** (chưa phải ảnh thật của nhà hàng); ghi rõ trong comment kết quả của Dev.
- Form khối 5 chỉ là giao diện: không nối backend, không thu thập dữ liệu thật.

## 9. Điều cấm

- Không dùng template bán hàng phổ thông, lưới thẻ đều tăm tắp không có nhịp chia đôi, icon stock.
- Không thêm màu, font hay khối ngoài danh sách ở mục 2, 3 và 5.
- Không có nút "mua ngay", giỏ hàng, thanh toán online, backend.
- Không dùng ảnh sáng phẳng kiểu sàn thương mại điện tử, không dùng ảnh AI méo mó món ăn/bàn tay.
- Không bịa địa chỉ thật, số điện thoại thật, giá thật, tên khách thật — mọi dữ liệu thật chưa có đều ghi [CẦN BỔ SUNG].

## 10. Nguồn

- Task: TEC-305 (Epic TEC-304, yêu cầu web MSR-39).
- Repo: https://github.com/Muse-Soft/m-software-an-lac
