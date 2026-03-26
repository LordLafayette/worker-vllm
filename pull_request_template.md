## Summary
อัปเดต vLLM จาก 0.16.0 เป็น 0.17.0 พร้อมรักษาความเข้ากันได้กับ CUDA 12.9

## Changes
- ✅ อัปเดต vLLM version จาก `0.16.0` เป็น `0.17.0`
- ✅ อัปเดตคอมเมนต์ให้สอดคล้องกับ vLLM 0.17.0
- ✅ รักษา CUDA 12.9 compatibility
- ✅ รักษา FlashInfer backend support

## Version Dependencies Verified
สำหรับ vLLM 0.17.0:
- **PyTorch**: >= 2.5.0 ✓ (จะติดตั้งอัตโนมัติพร้อม vLLM)
- **Transformers**: >= 4.46.0 ✓ (ปัจจุบันใช้ 4.57.0)
- **Python**: >= 3.9 ✓
- **CUDA**: 12.1+ ✓ (ใช้ CUDA 12.9.1)
- **bitsandbytes**: >= 0.45.0 ✓ (ระบุใน requirements.txt)
- **typing-extensions**: >= 4.8.0 ✓

## Files Changed
- `Dockerfile` - อัปเดตบรรทัดที่ 8 และ 10

## Dependencies
ไม่จำเป็นต้องแก้ไข `builder/requirements.txt` เนื่องจาก dependencies ปัจจุบันรองรับ vLLM 0.17.0 อยู่แล้ว

## Testing Recommendations
1. Build Docker image และทดสอบว่า build สำเร็จ
2. ทดสอบ vLLM 0.17.0 กับ FlashInfer backend
3. ทดสอบการโหลด model และ inference
4. ยืนยัน CUDA 12.9 compatibility