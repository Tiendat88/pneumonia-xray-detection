Pneumonia Detection from Chest X-Ray using CNN
Giới thiệu
Dự án này sử dụng mạng nơ-ron tích chập (CNN) để phân loại ảnh X-quang ngực thành hai loại: Bình thường (Normal) và Viêm phổi (Pneumonia).
Quy trình bao gồm tiền xử lý ảnh, huấn luyện mô hình, đánh giá kết quả và dự đoán ảnh mới.

Mô hình sử dụng
Mạng CNN với 3 tầng Conv2D + MaxPooling

Lớp Dense với Dropout để giảm overfitting

Hàm kích hoạt: ReLU, Sigmoid

Loss function: binary_crossentropy

Optimizer: Adam

Cấu trúc thư mục
Sao chép
Chỉnh sửa
chest_xray_project/
├── chest_xray-ptdat.ipynb                # Notebook chính chứa toàn bộ quy trình
├── pneumonia_classification_model.h5     # Mô hình đã huấn luyện (không upload lên GitHub)
├── chest_xray_data/
│   ├── train/
│   └── test/
Cách chạy project
1. Cài đặt thư viện cần thiết:
bash
Sao chép
Chỉnh sửa
pip install tensorflow matplotlib scikit-learn
2. Chạy Notebook:
Mở file chest_xray-ptdat.ipynb trong Jupyter hoặc Google Colab và chạy từng ô code theo thứ tự.

3. Dự đoán ảnh mới:
Chạy đoạn code cuối cùng và nhập đường dẫn đến file ảnh khi được yêu cầu:

Sao chép
Chỉnh sửa
Nhập đường dẫn đến ảnh: /path/to/image.jpg
Kết quả mô hình
Accuracy cao trên tập kiểm tra

Hiển thị đồ thị loss và accuracy theo epoch

In ra confusion matrix và classification report

Tải mô hình .h5
File mô hình không được upload trực tiếp do giới hạn GitHub.
Bạn có thể tải mô hình tại đây:

Link tải mô hình: https://drive.google.com/file/d/1A9FktW6qJGSee2EsfPOkEzJAlqAZDpgo/view?usp=drive_link

Ghi chú
Dữ liệu phải được sắp xếp theo cấu trúc thư mục:

Sao chép
Chỉnh sửa
chest_xray_data/
├── train/
│   ├── NORMAL/
│   └── PNEUMONIA/
└── test/
    ├── NORMAL/
    └── PNEUMONIA/
Ảnh được resize về kích thước 150x150 trước khi đưa vào mô hình.