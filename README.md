<div align="center">
  <img src="https://socialify.git.ci/your-username/topviec/image?description=1&font=Inter&language=1&name=1&owner=1&pattern=Solid&theme=Auto" alt="TopViec" width="640" height="320" />
</div>

<h1 align="center">🚀 TopViec - Nền Tảng Tuyển Dụng & Việc Làm Toàn Diện</h1>

<p align="center">
  <strong>Một nền tảng tìm kiếm việc làm và tuyển dụng hiện đại, dễ dàng mở rộng, được xây dựng với Spring Boot và Vue.js.</strong>
</p>

<p align="center">
  <a href="#tính-năng">Tính Năng</a> •
  <a href="#kiến-trúc">Kiến Trúc</a> •
  <a href="#công-nghệ-sử-dụng">Công Nghệ Sử Dụng</a> •
  <a href="#hướng-dẫn-cài-đặt">Hướng Dẫn Cài Đặt</a> •
  <a href="#cấu-trúc-dự-án">Cấu Trúc Dự Án</a>
</p>

---

## ✨ Tổng Quan

TopViec là một cổng thông tin việc làm toàn diện được thiết kế nhằm thu hẹp khoảng cách giữa các ứng viên tài năng và các nhà tuyển dụng hàng đầu. Nền tảng mang đến trải nghiệm mượt mà cho người tìm việc trong việc xây dựng hồ sơ, tạo CV chuyên nghiệp và ứng tuyển. Đồng thời cung cấp cho nhà tuyển dụng các công cụ mạnh mẽ để quản lý tin tuyển dụng, theo dõi hồ sơ ứng viên và cộng tác trong đội ngũ của họ.

## 🌟 Tính Năng Nổi Bật

### Dành Cho Ứng Viên 🎓
- **Tìm Kiếm Việc Làm Nâng Cao:** Lọc theo địa điểm, mức lương, ngành nghề và loại hình công việc.
- **Tạo CV Trực Tuyến:** Xây dựng CV chuẩn ATS một cách chuyên nghiệp sử dụng các mẫu có sẵn và có thể xuất ra file PDF.
- **Theo Dõi Ứng Tuyển:** Xem trạng thái của các hồ sơ đã ứng tuyển theo thời gian thực.
- **Quản Lý Hồ Sơ:** Cập nhật kỹ năng, kinh nghiệm và học vấn để thu hút nhà tuyển dụng.

### Dành Cho Nhà Tuyển Dụng 🏢
- **Dashboard Phân Quyền:** Giao diện chuyên biệt cho Owner (Chủ sở hữu), Manager (Quản lý), Recruiter (Người tuyển dụng) và Viewer (Người xem) với các quyền hạn cụ thể.
- **Quản Lý Tin Tuyển Dụng:** Tạo, chỉnh sửa và quản lý các bài đăng tuyển dụng một cách hiệu quả.
- **Hệ Thống Quản Lý Ứng Viên (ATS):** Xem xét hồ sơ ứng viên, thay đổi trạng thái ứng tuyển và lên lịch phỏng vấn.
- **Dịch Vụ Bổ Sung (Add-ons):** Mua và quản lý các dịch vụ cao cấp (ví dụ: làm nổi bật công việc, lượt xem CV) tích hợp thanh toán VNPay.

### Dành Cho Quản Trị Viên (Admin) 🛡️
- **Bảng Điều Khiển Đa Vai Trò:** Các dashboard chuyên biệt dành cho Super Admin, Content Moderator, Support Admin, và Finance Admin.
- **Giám Sát Hệ Thống:** Thống kê tổng quan, quản lý người dùng và phân tích dữ liệu nền tảng.
- **Quản Lý Tài Chính:** Quản lý thanh toán, hoàn tiền và báo cáo doanh thu.

## 🏗️ Kiến Trúc Dự Án

Dự án được xây dựng theo mô hình monorepo hiện đại, phân tách rõ ràng giữa frontend và backend thành các dịch vụ độc lập nhằm tăng khả năng bảo trì và mở rộng.

- **Backend (`topviec-be`):** Cung cấp các API RESTful bảo mật, xử lý logic nghiệp vụ, giao dịch cơ sở dữ liệu, lưu trữ file và tích hợp bên thứ ba (VNPay).
- **Frontend (`topviec-fe`):** Ứng dụng Single-Page Application (SPA) phản hồi nhanh, mang lại giao diện người dùng trực quan cho ứng viên, nhà tuyển dụng và admin.

## 💻 Công Nghệ Sử Dụng

### Frontend (`topviec-fe`)
- **Framework:** Vue 3 (Composition API)
- **Ngôn Ngữ:** TypeScript
- **Quản Lý Trạng Thái:** Pinia
- **Build Tool:** Vite
- **Styling:** Tailwind CSS / Custom CSS

### Backend (`topviec-be`)
- **Framework:** Spring Boot (Java)
- **Bảo Mật:** Spring Security & JWT
- **Cơ Sở Dữ Liệu:** MySQL / PostgreSQL (JPA/Hibernate)
- **Cổng Thanh Toán:** VNPay
- **Lưu Trữ File:** Lưu trữ máy chủ cục bộ (Đã chuyển đổi từ Cloudinary)

## 🚀 Hướng Dẫn Cài Đặt

Thực hiện các bước sau để thiết lập dự án trên môi trường local.

### Yêu Cầu Hệ Thống
- Node.js (v16+)
- Java Development Kit (JDK 17+)
- Maven
- MySQL hoặc PostgreSQL server

### 1. Cài Đặt Backend
```bash
cd topviec-be
# Cấu hình file application.yml với thông tin database của bạn
mvn clean install
mvn spring-boot:run
```

### 2. Cài Đặt Frontend
```bash
cd topviec-fe
npm install
npm run dev
```

Frontend sẽ chạy tại địa chỉ `http://localhost:5173` và Backend API tại `http://localhost:8080`.

## 📂 Cấu Trúc Thư Mục

```text
TopViec/
├── topviec-be/          # Dịch vụ Backend Spring Boot
│   ├── src/main/java    # Mã nguồn Java (Controllers, Services, Repositories)
│   ├── src/main/resources # File cấu hình (application.yml)
│   └── pom.xml          # Dependencies của Maven
│
└── topviec-fe/          # Ứng dụng Frontend Vue 3
    ├── src/             # Vue components, views, stores, và assets
    ├── public/          # Static assets
    ├── package.json     # Node dependencies và scripts
    └── vite.config.ts   # Cấu hình Vite
```

## 📄 Bản Quyền
Dự án này là tài sản độc quyền và bảo mật.
