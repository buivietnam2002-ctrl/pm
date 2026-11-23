# CAD Survey 2D — Ứng dụng đo đạc công trình & vẽ CAD 2D (Flutter)

## Cách 1: Tự động xuất file `.apk` qua GitHub Actions (không cần cài Android Studio)
1. Giải nén tệp `cad_survey_2d_apk_ready.zip`.
2. Tạo một Repository mới trên GitHub, tải toàn bộ nội dung thư mục `cad_survey_2d` lên (nhớ giữ nguyên thư mục ẩn `.github/workflows/build_apk.yml`).
3. Vào tab **Actions** trên GitHub → chọn **Build Android APK** → bấm **Run workflow** (hoặc tự chạy khi vừa push code).
4. Sau 3–4 phút build xong, kéo xuống mục **Artifacts** và tải về **`cad-survey-2d-apk.zip`** chứa file **`app-release.apk`** để cài lên điện thoại/máy tính bảng Android.

## Cách 2: Chạy & build trực tiếp trên máy tính có Flutter SDK
```bash
flutter create --platforms=android .
flutter pub get
flutter test
flutter build apk --release
```
File cài đặt sẽ nằm tại `build/app/outputs/flutter-apk/app-release.apk`.
