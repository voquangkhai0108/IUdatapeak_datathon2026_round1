# IU DataPeak Datathon 2026 - Vòng 1

Repository này chứa toàn bộ mã nguồn, dữ liệu và báo cáo cho dự án dự báo doanh thu và tối ưu hóa tồn kho trong khuôn khổ cuộc thi IU DataPeak Datathon 2026.

## 📂 Cấu trúc Thư mục

Dưới đây là sơ đồ cấu trúc của repository dựa trên hệ thống file thực tế để hỗ trợ việc tra cứu và chạy lại kết quả:
```text
├── data/
│   ├── processed/          # Dữ liệu sau khi xử lý và file kết quả submission Kaggle
│   └── raw/                # Dữ liệu thô được cung cấp từ Ban tổ chức (BTC)
├── notebooks/
│   ├── catboost_info/      # Thư mục chứa log/cache tự động sinh ra khi chạy CatBoost
│   ├── MCQs.ipynb          # Câu trả lời MCQs cho phần 1
│   ├── data_cleaning.ipynb # Notebook hỗ trợ việc làm sạch dữ liệu
│   ├── exploratory_data_analysis.ipynb # EDA cho phần 2
│   └── model_training.ipynb# Model huấn luyện và dự báo cho phần 3
└── README.md               # Hướng dẫn và mô tả cấu trúc dự án
```

## 🛠 Hướng dẫn Chạy lại kết quả (Reproduce Results)

Để tái lập kết quả dự báo, vui lòng thực hiện theo các bước sau:

### 1. Chuẩn bị dữ liệu
- File dữ liệu gốc từ BTC trong thư mục `data/raw/`.
- File submission nộp trên hệ thống Kaggle sẽ được tạo ra và nằm trong `data/processed/`.

### 2. Chạy các Notebook
Mở thư mục `notebooks/` và chạy các file Jupyter Notebook (`.ipynb`) theo logic sau:
1. **`MCQs.ipynb`**: Xem các giải thích và đáp án cho phần 1.
2. **`data_cleaning.ipynb`**: Chạy bước làm sạch dữ liệu và xử lý ngoại lai ban đầu.
3. **`exploratory_data_analysis.ipynb`**: Xem các phân tích chẩn đoán, trực quan hóa rủi ro tồn kho (Phần 2).
4. **`model_training.ipynb`**: Chạy toàn bộ pipeline huấn luyện mô hình (Hybrid Model, XGBoost, Prophet...) và sinh ra file kết quả dự báo (Phần 3).

## 📝 Nội dung Dự án

- **Phần 1 (MCQs):** Trả lời và giải thích dựa trên việc truy vấn dữ liệu.
- **Phần 2 (EDA):** Trực quan hóa "Nghịch lý tồn kho", phân tích thực trạng Long-tail và rủi ro Stockout/Overstock.
- **Phần 3 (Modeling):**
    - Xây dựng hệ thống dự báo Doanh thu và Giá vốn.
    - Sử dụng kiến trúc Hybrid: **Prophet** (bắt xu hướng dài hạn) kết hợp với **Ensemble** (XGBoost, LightGBM, CatBoost) dự báo sai số.
    - Giải thích mô hình bằng giá trị **SHAP**.

---
**Thông tin nhóm:**
- Võ Quang Khải
- Nguyễn Huỳnh Anh Thư
- Hứa Thụy Hồng Ngọc
- Huỳnh Ngọc Thủy Tiên
- *Trường Đại học Quốc tế - ĐHQG TP.HCM (IU)*
