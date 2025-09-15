## 2. API tính phí và miễn phí

| Nhóm API | Ví dụ endpoint | Tính phí |
|----------|----------------|----------|
| **Chat & Completions** | `chat.completions.create` | ✅ Có (tính theo token) |
| **Embeddings** | `embeddings.create` | ✅ Có (tính theo số token input) |
| **Images** | `images.generate`, `images.edit` | ✅ Có (tính theo số ảnh, kích thước) |
| **Audio** | `audio.transcriptions.create` (Whisper), `audio.speech.create` (TTS) | ✅ Có |
| **Fine-tuning** | `fine_tuning.jobs.create` | ✅ Có |
| **Vector Stores / Assistants** | Khi tạo embeddings, gọi model trả lời | ✅ Có |
| **Models / Files (quản lý)** | `models.list`, `models.retrieve`, `files.list`, `files.retrieve` | ❌ Miễn phí |
| **Moderation** | `moderations.create` | ❌ Miễn phí (OpenAI hỗ trợ free) |

---

## 3. Lưu ý
- **Chỉ các lệnh `create` liên quan đến model sinh dữ liệu** (text, hình, audio, embeddings, …) mới trừ tiền.  
- Các thao tác **`list`, `retrieve`, `delete`** chỉ quản lý tài nguyên → **không tính phí**.  
- Có thể kiểm tra chi tiết chi tiêu tại:  
  [OpenAI Usage Dashboard](https://platform.openai.com/usage)