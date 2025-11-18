# Mercury Pactum Demo - VPBank Hackathon 2025


**Tự động hóa quy trình thế chấp BĐS với AI: OCR sổ đỏ, trích xuất dữ liệu, sinh hợp đồng.**

## Giới thiệu
Mercury Pactum là giải pháp serverless AWS để tự động hóa quy trình thế chấp BĐS cho VPBank. 
- Front-end: Figma prototype (upload, track progress).
- Demo OCR: Client-side JSQR cho quét QR CCCD (file HTML).
- Backend concept: S3 trigger → Lambda (Textract, Comprehend, Rekognition, Generate Draft) → SES notify.
- SLA: <2 phút/hồ sơ, accuracy >85%.

## Demo Front-End
- **Link Figma:** [Figma Prototype](https://dimly-love-31263713.figma.site/)
- **Screenshot:**  
![FE_UI02](https://github.com/user-attachments/assets/e68ede78-7600-482e-bfa2-4b8faa1d4a1d)


Tính năng: Upload file, view progress dashboard, download draft.

## Demo OCR CCCD
- **Mô tả:** Client-side (không server), upload ảnh CCCD → Quét QR → Trích xuất ID, tên, DOB, địa chỉ.
- **Chạy demo:** Mở file `QR_CCCD.html` trong browser (Google Chrome).
- **Screenshot:**  
 ![Screenshot_error](https://github.com/user-attachments/assets/f373dd46-2195-40a4-84a1-208f94fab89a)

![OCR_Screen_Right](https://github.com/user-attachments/assets/33f917fa-42f9-4286-a1ef-7d54b1f5d758)

Hướng dẫn: Upload ảnh CCCD → Quét QR → Kết quả hiển thị ngay (ví dụ: ID: 001123456789, Tên: Nguyễn Văn A).

## Architecture Concept
- S3 upload trigger.
- Step Functions orchestrate Lambda:
  - Textract OCR.
  - Comprehend Extract.
  - Rekognition Verify.
  - Generate Draft.
- SES notify.
- **Diagram:**  
 

## Team Mercury Pactum
| Tên | Vai trò | Email |
|-----|--------|-------|
| Trần Trọng Hoàng | Leader / SA | hoang89210@gmail.com |
| Phạm Minh Quang | PM | (email) |
| Phạm Trung Hiếu | DS | (email) |
| Hoàng Hữu Hướng | DE | (email) |
| La Linh | Front-end | (email) |

## Installation & Usage
1. Clone repo: `git clone https://github.com/hoang89210/mercury-pactum-demo.git`
2. Mở `QR_CCCD.html` trong browser để demo OCR.
3. Figma: Truy cập link để view prototype.

## License
MIT – Miễn phí sử dụng.

**Chúc VPBank thành công với giải pháp này!**
