# 📘 Báo cáo Bài Tập Lớn  
## Thuật toán Bầy ong nhân tạo (ABC) và các biến thể  
**Môn học:** Nhập môn Kỹ thuật Truyền thông  
**Học kỳ:** 2024 – 2025  
---

## 👥 Thành viên nhóm thực hiện

| STT | Họ và tên          | MSSV     |
|----|---------------------|----------|
| 1  | Nguyễn Minh Xuân    | 20235882 | 
| 2  | Nguyễn Đức Hiếu     | 20235712 |

---

## 📖 Giới thiệu (Overview)

Dự án này tập trung nghiên cứu, cài đặt và đánh giá hiệu năng của thuật toán **Bầy ong nhân tạo (Artificial Bee Colony – ABC)** cùng với hai biến thể cải tiến nổi bật là **GABC** và **qABC**.

**Mục tiêu chính** là so sánh khả năng tối ưu hóa (tốc độ hội tụ, độ chính xác, khả năng thoát cực trị địa phương) của các thuật toán này trên các hàm mục tiêu chuẩn (Benchmark Functions) với không gian tìm kiếm đa chiều.

### Các thuật toán được triển khai:

- **Classic ABC:** Thuật toán gốc mô phỏng hành vi tìm kiếm nguồn thức ăn của bầy ong.  
- **GABC (Gbest-guided ABC):** Biến thể tích hợp thông tin nghiệm tốt nhất toàn cục (*gbest*) vào phương trình tìm kiếm để tăng tốc độ hội tụ.  
- **qABC (Quick ABC):** Tăng cường hành vi của ong quan sát, giới hạn vùng tìm kiếm trong bán kính lân cận (*r*) và học hỏi từ hàng xóm tốt nhất.

---

## 🧪 Môi trường thực nghiệm & Hàm mục tiêu

Dự án sử dụng Python trên nền tảng **Jupyter Notebook** / **Google Colab**.  
Các thuật toán được kiểm chứng trên hai hàm mục tiêu đại diện cho hai loại địa hình:

### 1. **Hàm Sphere (Unimodal)**

- Đặc điểm: Hàm lồi, trơn, chỉ có 1 cực trị toàn cục.  
- Mục đích: Đánh giá khả năng *Exploitation* và tốc độ hội tụ.  
- Số chiều (D): 20  
- Global Min: **0**

### 2. **Hàm Shifted Rastrigin (Multimodal)**

- Đặc điểm: Phi tuyến, có rất nhiều cực trị địa phương.  
- Mục đích: Đánh giá khả năng *Exploration* và thoát bẫy.  
- Số chiều (D): 20  
- Global Min: **0**

---

## 🚀 Hướng dẫn cài đặt và Chạy code

### Yêu cầu hệ thống
*   Python 3.7+
*   Thư viện: `numpy`, `matplotlib`

### Các bước thực hiện
1.  **Download file (.ipynb)**
    
2.  **Mở Notebook:**
    *   Chạy file `ABC_Algorithm.ipynb` bằng Jupyter Notebook hoặc VS Code.
    *   Hoặc mở trực tiếp trên Google Colab.
---

## 📊 Kết quả thực nghiệm (Highlights)

*(Bạn có thể chèn ảnh biểu đồ so sánh từ notebook vào đây để Github trông sinh động hơn)*

Dưới đây là tóm tắt kết quả so sánh hiệu năng trung bình sau **30 lần chạy độc lập**:

| Hàm mục tiêu | Thuật toán tốt nhất | Nhận xét |
|:---|:---:|:---|
| **Sphere** | **GABC** | GABC hội tụ cực nhanh về 0 nhờ cơ chế dẫn hướng toàn cục. qABC cũng cho kết quả tốt hơn ABC gốc. |
| **Rastrigin** | **qABC / GABC** | Các biến thể cải tiến giúp giảm đáng kể lỗi so với ABC gốc, chứng tỏ khả năng thoát bẫy tốt hơn trên không gian phức tạp. |

---

## 📂 Cấu trúc thư mục

```text
├── ABC_Algorithm.ipynb    # Source code chính (Notebook)
├── Report.pdf             # File báo cáo chi tiết
└── README.md              # Tài liệu hướng dẫn này
```
## 🔗 Tham khảo
1. Karaboga, D. (2005). *An idea based on honey bee swarm for numerical optimization*.
2. Zhu, G., & Kwong, S. (2010). *Gbest-guided artificial bee colony algorithm*.
3. Karaboga, D., & Gorkemli, B. (2014). *A quick artificial bee colony (qABC) algorithm*.
