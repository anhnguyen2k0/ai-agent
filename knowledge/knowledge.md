# 📚 KNOWLEDGE — PRODUCTION & SUPPLY CHAIN RULES

---

## 📌 Rule 1: Sản xuất theo nhu cầu thị trường

- Không sản xuất theo cảm tính
- Luôn dựa trên:
  - Tốc độ bán (3d, 7d, 14d)
  - Tồn kho
  - WIP (đang làm + chờ nhập)

👉 Mục tiêu:
- Sản xuất đúng cái thị trường cần

---

## 📌 Rule 2: Tính nhu cầu ngắn hạn

Nhu cầu sản phẩm = max(
  (Bán 7 ngày / 7) × 3 ngày,
  Bán 3 ngày gần nhất
)

👉 Dùng để:
- Dự đoán nhu cầu 3 ngày tới

---

## 📌 Rule 3: Xác định thiếu hàng

Thiếu = Nhu cầu - (Tồn kho + Chờ nhập + Đang làm)

IF:
- Thiếu > 0

THEN:
- 🔴 Bắt buộc sản xuất

---

## 📌 Rule 4: Phân loại sản phẩm theo ưu tiên

### 🔴 Ưu tiên cao
- Thiếu hàng
- Bán nhanh (7d, 14d cao)

### 🟡 Trung bình
- Đủ hàng
- Bán ổn định

### ⚪ Thấp
- Tồn cao
- Bán chậm

---

## 📌 Rule 5: Tránh thiếu hàng (critical)

IF:
- Tồn + WIP < nhu cầu 3 ngày

THEN:
- 🔴 Nguy cơ hết hàng
- Ưu tiên sản xuất ngay

---

## 📌 Rule 6: Tránh tồn kho cao (overstock)

IF:
- Tồn > nhu cầu 14 ngày

THEN:
- ⚠️ Không sản xuất thêm
- Ưu tiên giảm tồn

---

## 📌 Rule 7: Sử dụng GTSX (Giá trị sản xuất)

Mỗi sản phẩm có:
- GTSX = giá trị sản xuất / đơn vị

---

### Công thức:

Giá trị sản xuất = Số lượng × GTSX

---

### Mục tiêu:

Tổng giá trị sản xuất ≈ Target

---

## 📌 Rule 8: Lập kế hoạch theo target

INPUT:
- Target (giá trị cần đạt)

OUTPUT:
- Danh sách sản phẩm + số lượng

---

### Cách làm:

1. Ưu tiên sản phẩm 🔴
2. Sau đó 🟡
3. Bỏ qua ⚪ (nếu không cần)

---

### Constraint:

- Tổng giá trị ≈ Target
- Không bỏ sót sản phẩm thiếu hàng

---

## 📌 Rule 9: Ưu tiên sản phẩm hiệu quả cao

IF:
- Bán nhanh + GTSX cao

THEN:
- 🔴 Ưu tiên sản xuất

---

## 📌 Rule 10: Cân bằng sản xuất vs bán

Không để xảy ra:

❌ Sản xuất nhiều nhưng không bán được  
❌ Bán tốt nhưng không có hàng  

---

## 📌 Rule 11: Phát hiện bottleneck

IF:
- Một nhân sự làm nhiều WIP

THEN:
- ⚠️ Bottleneck
- Cần phân bổ lại

---

## 📌 Rule 12: Phát hiện lệch sản xuất

IF:
- Sản phẩm tồn cao + bán chậm
- Nhưng vẫn đang sản xuất

THEN:
- ⚠️ Sai định hướng sản xuất

---

## 📌 Rule 13: Cross-analysis bắt buộc

- QC ↑ + Output ↓ → vấn đề chất lượng
- Lệnh trễ ↑ → vấn đề planning
- Tồn thấp + bán cao → thiếu hàng
- Tồn cao + bán thấp → overstock

---

## 📌 Rule 14: Validate kế hoạch

Sau khi lập kế hoạch:

Phải đảm bảo:

- Tổng giá trị ≈ Target
- Không có sản phẩm:
  - thiếu hàng mà không sản xuất
  - tồn cao mà vẫn sản xuất

---

## 📌 Rule 15: Ưu tiên hệ thống, không tối ưu cục bộ

- Không tối ưu 1 sản phẩm
- Tối ưu toàn bộ:
  - sản xuất
  - tồn kho
  - bán hàng

---

## 📌 Rule 16: Quyết định dựa trên dữ liệu

- Không đoán
- Không cảm tính
- Luôn có:
  - số liệu
  - logic
