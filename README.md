# ⚙️ 1. Yêu cầu hệ thống

* Python **3.10 (BẮT BUỘC)**
* Windows (khuyến nghị)
* Webcam (để nhận diện realtime)

---

# 📦 2. Tạo môi trường

## Model

Model không được include trong repo.

Khi chạy lần đầu:
- Model sẽ tự động được train
- Sau đó lưu thành file `model.h5`

## Bước 1: Tạo virtual environment

```bash
python -m venv venv310
```

Kích hoạt:

```bash
venv310\Scripts\activate
```

---

## Bước 2: Nâng cấp pip

```bash
pip install --upgrade pip
```

---

# 📥 3. Cách chạy


```bash
pip install -r requirements.txt
```

## ⚠️ Cài MediaPipe (RẤT QUAN TRỌNG)

```bash
pip install mediapipe==0.10.5 --no-deps
```

```bash
python app.py
```

Mở trình duyệt:

```
http://127.0.0.1:5000
```

---

# ⚠️ LƯU Ý QUAN TRỌNG

* ❌ KHÔNG nâng cấp numpy
* ❌ KHÔNG cài lại mediapipe nếu không có `--no-deps`
* ❌ KHÔNG dùng Python 3.11+

---

---

# 🧠 4. Cách hoạt động

## Trường hợp 1: Chưa có model

Bạn sẽ thấy:

```
⚡ Model not found, starting training...
```

Hệ thống sẽ:

* Load dataset
* Train model (20 epochs)
* Lưu model (`model.h5`)

---

## Trường hợp 2: Đã có model

* Bỏ qua bước train
* Load model
* Chạy server Flask




