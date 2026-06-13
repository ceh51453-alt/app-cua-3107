<div align="center">
  <img width="1200" height="400" alt="Tawa Worldbuilder Banner" src="https://files.catbox.moe/o82o4z.png" style="object-fit: cover; border-radius: 12px;" />
  
  # 🌸 Tawa Worldbuilder 2.0 🌸
  
  **Bộ Công Cụ Thiết Kế Bối Cảnh & Lorebook SillyTavern Tối Ưu Bằng AI**

  [![React](https://img.shields.io/badge/React-19-blue.svg?style=flat-square&logo=react)](https://react.dev/)
  [![Vite](https://img.shields.io/badge/Vite-6-purple.svg?style=flat-square&logo=vite)](https://vite.dev/)
  [![TypeScript](https://img.shields.io/badge/TypeScript-5-blue.svg?style=flat-square&logo=typescript)](https://www.typescriptlang.org/)
  [![License](https://img.shields.io/badge/License-MIT-green.svg?style=flat-square)](#)
  [![Version](https://img.shields.io/badge/Version-3.0_3107Ver-orange.svg?style=flat-square)](#)
</div>

---

## 📖 Giới Thiệu (Introduction)

**Tawa Worldbuilder** là ứng dụng chuyên nghiệp giúp tự động hóa và tối ưu hóa việc tạo lập thẻ Lorebook/Worldbook cho SillyTavern hoặc các trình giả lập RPG khác. Được trang bị giao diện hiện đại kết hợp với **Quy trình Trí Tuệ Nhân Tạo (Tawa AI Engine)**, ứng dụng hỗ trợ quét tài liệu thô hoặc cào trực tiếp Wiki Fandom để dệt nên các mục bối cảnh đồ sộ, có chiều sâu và cấu trúc hoàn chỉnh.

---

## ✨ Các Tính Năng Vượt Trội (Features)

1. **Giao Thức Ép Buộc Hoàn Thiện Tối Đa (Completeness Protocol)**: 
   - Đảm bảo AI trích xuất 100% tất cả thực thể (Thế giới quan, Hệ thống, Nhân vật, Địa điểm, Sự kiện...) từ nguồn thông tin mà không bỏ sót bất kỳ chi tiết canon nào.
2. **Chuẩn Hóa Cấu Trúc 6 Nhóm (OrderLorebook System)**:
   - Tự động phân phối và tối ưu hóa các mục Lorebook theo đúng logic sắp xếp chuyên sâu:
     - *Nhóm 1: Thế giới quan & Tổng cương (Before Char, Order 1, Constant)*
     - *Nhóm 2: Xem lướt nhân vật & thế lực (Before Char, Order 4, Constant)*
     - *Nhóm 3: Chi tiết nhân vật cốt lõi (After Char, Order 99, Selective)*
     - *Nhóm 4: Cảnh vật & Chi tiết sự kiện (After Char, Order 80, Selective)*
     - *Nhóm 5: Tài liệu NPC (After Char, Order 100, Selective)*
     - *Nhóm Đặc Biệt: Giải thích lần hai - D0 (Depth System, Depth 0, Selective)*
3. **Cào Dữ Liệu Tự Động (Auto Wiki Crawler)**:
   - Càn quét dữ liệu thông tin Wiki/Fandom qua API MediaWiki, tự động giải quyết các redirect, lọc rác bối cảnh (Behind-the-scenes, gameplay stats, ads, categories...) ở cấp độ nguồn.
4. **Bảo Toàn Bối Cảnh (Append-Only Guard)**:
   - Bảo vệ tuyệt đối cơ sở dữ liệu đã có. AI chỉ được phép thêm mới thông tin còn thiếu, cấm hoàn toàn hành vi ghi đè hoặc xóa bỏ thông tin cũ làm mất mát dữ liệu.
5. **Dịch Thuật Chuyên Sâu (Translation Engine)**:
   - Tự động chuyển đổi ngôn ngữ Lorebook cực kỳ chuẩn xác và mượt mà, hỗ trợ chế độ NSFW thô ráp chân thực cho các thẻ Erotica.

---

## 🛠️ Hướng Dẫn Cài Đặt & Chạy Ứng Dụng (Setup Guide)

Để clone và chạy ứng dụng này dưới local, hãy thực hiện theo các bước chi tiết sau:

### 1. Yêu Cầu Hệ Thống (Prerequisites)
- Đảm bảo máy tính đã cài đặt **Node.js** (Khuyên dùng phiên bản LTS mới nhất - Node 18+ hoặc 20+).
- Một trình quản lý gói như **npm** (đi kèm khi cài đặt Node.js).

### 2. Tải Mã Nguồn Về Máy (Clone Repository)

Mở Terminal (Command Prompt hoặc PowerShell trên Windows) và chạy lệnh:

```bash
# Clone bằng HTTPS
git clone https://github.com/ceh51453-alt/app-cua-3107.git

# Di chuyển vào thư mục dự án
cd app-cua-3107
```

### 3. Cài Đặt Các Gói Phụ Thuộc (Install Dependencies)

Chạy lệnh cài đặt các thư viện cần thiết:

```bash
npm install
```

### 4. Cấu Hình Khóa API (Configuration)

Bạn có hai cách để nạp API Key của mô hình ngôn ngữ (Gemini / OpenAI hoặc các Proxy trung gian):
- **Cách 1 (Khuyên dùng)**: Tạo file `.env.local` ở thư mục gốc của dự án và điền khóa API của bạn vào:
  ```env
  GEMINI_API_KEY=your_api_key_here
  ```
- **Cách 2**: Bạn có thể điền trực tiếp API Key và Base URL thông qua mục **Cài đặt (Settings - biểu tượng bánh răng)** ngay trên giao diện web của ứng dụng.

### 5. Chạy Dự Án (Start App)

Chạy môi trường phát triển (Local Development Server):

```bash
npm run dev
```

Sau khi khởi chạy thành công, Terminal sẽ hiển thị một đường dẫn cục bộ, thông thường là:
👉 [http://localhost:5173](http://localhost:5173)

Mở trình duyệt web của bạn và truy cập địa chỉ trên để bắt đầu trải nghiệm!

### 6. Biên Dịch Dự Án (Build for Production)

Nếu muốn đóng gói sản phẩm để deploy lên máy chủ hoặc chia sẻ, chạy lệnh:

```bash
npm run build
```
Sản phẩm được biên dịch tối ưu sẽ nằm trong thư mục `/dist`.

---

## 🌸 Hướng Dẫn Sử Dụng (Usage Guidelines)

1. **Chế Độ Editor (Biên Tập Thủ Công)**:
   - Giúp bạn quản lý danh sách các mục (entries), tùy chỉnh từ khóa kích hoạt, vị trí (`before_char`, `after_char`, `at_depth_system`), và thứ tự `order` bằng tay.
2. **Chế Độ Tawa Worldbuilding (Tự Động Hóa AI)**:
   - Chuyển sang thẻ *Tawa Worldbuilder* ở trên cùng.
   - Nhập đường dẫn Wiki hoặc tải lên file tài liệu bối cảnh `.txt`.
   - AI sẽ tự động phân tích và chia bước (Pipeline) để tạo lập Lorebook hoàn toàn tự động.
3. **Áp Dụng Sơ Đồ Tối Ưu**:
   - Nhấp vào nút **Sơ đồ tối ưu** ở thanh công cụ để AI tự động tối ưu hóa, dọn dẹp đệ quy, sửa chữa và phân loại lại toàn bộ Lorebook theo đúng chuẩn 6 Nhóm.

---

## 📄 Bản Quyền (License)

Dự án này được bảo hộ dưới bản quyền **MIT License**.
