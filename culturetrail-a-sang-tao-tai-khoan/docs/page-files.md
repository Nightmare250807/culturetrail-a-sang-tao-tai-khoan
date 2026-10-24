# Bộ ba tệp theo trang (HTML + CSS + JS)

Mỗi trang là một bộ ba **độc lập**, một sinh viên có thể sở hữu trọn vẹn:

```
<tên>.html            cấu trúc & nội dung (ngữ nghĩa)
css/pages/<tên>.css   CSS riêng của trang (tải sau cùng, ghi đè được lớp dùng chung)
js/pages/<tên>.js     logic riêng của trang
```

## Lớp dùng chung (không sửa trong phần việc của một trang; sửa thì báo cả nhóm)

| Lớp | Tệp | Nội dung |
|---|---|---|
| CSS nền | `css/base.css` | token màu/chữ/khoảng cách, reset, kiểu chữ |
| CSS khung | `css/layout.css` | header, thanh bên theo vai trò, chân trang |
| CSS thành phần | `css/components.css` | nút, thẻ, biểu mẫu, bảng, hộp thoại, trạng thái, sơ đồ, điểm dừng… |
| CSS responsive | `css/responsive.css` | tablet ≤1100px, di động ≤720px cho phần dùng chung |
| Dữ liệu | `js/api.js`, `assets/data/seed.js` | LocalStorage, phiên đăng nhập, “API” giả lập |
| Khung trang | `js/main.js` | header/sidebar/footer, phân quyền 401/403 |
| Thành phần JS | `js/modules/ui.js`, `ai.js`, `creator.js` | toast, hộp thoại, kiểm tra biểu mẫu, AI, kiểm tra điều kiện gửi duyệt |

**Thứ tự tải CSS** (mọi trang): `base → layout → components → responsive → pages/<tên>`.
**Thứ tự tải JS**: `seed → api → ui → ai → [creator] → main → pages/<tên>`.

Quy ước **lớp `pg-N`** trong `css/pages/*.css` (và `u-N` trong `components.css`): style trước đây viết trực tiếp trong thuộc tính `style=""`, nay được chuyển thành lớp, viết dạng `.pg-N.pg-N` để có độ ưu tiên ngang style inline cũ. Khi sửa giao diện, nên đổi tên lớp cho có nghĩa (ví dụ `.pg-3` → `.hero-actions`) ở cả HTML/JS và CSS cùng lúc.

## Phân công 9 – 9 – 9 (cân bằng số trang và khối lượng)

| Thành viên | Phụ trách | Số trang | Khối lượng (HTML+CSS+JS) | % |
|---|---|---|---|---|
| **A** | Sáng tạo & Tài khoản | 9 | 83,303 ký tự | 32.1% |
| **B** | Duyệt nội dung & Quản trị | 9 | 86,766 ký tự | 33.4% |
| **C** | Khám phá & Bộ sưu tập | 9 | 89,412 ký tự | 34.5% |

Cách chia khác nhãn SV1–SV3 trong bảng kiểm kê của đề (SV1 = 12 trang, SV2 = 5, SV3 = 8) vì nhóm cần chia đều số trang. Các trang đi kèm gói để chạy riêng được (`login`, `403`, `404`) giống hệt nhau ở cả 3 gói, chỉ chủ sở hữu sửa.

## Danh sách bộ ba theo thành viên

| TV | Trang | HTML | CSS riêng | JS riêng |
|---|---|---|---|---|
| A | `creator-event-editor` | `creator-event-editor.html` | `css/pages/creator-event-editor.css` | `js/pages/creator-event-editor.js` |
| A | `creator-event-management` | `creator-event-management.html` | `css/pages/creator-event-management.css` | `js/pages/creator-event-management.js` |
| A | `creator-profile` | `creator-profile.html` | `css/pages/creator-profile.css` | `js/pages/creator-profile.js` |
| A | `creator-story-editor` | `creator-story-editor.html` | `css/pages/creator-story-editor.css` | `js/pages/creator-story-editor.js` |
| A | `creator-story-management` | `creator-story-management.html` | `css/pages/creator-story-management.css` | `js/pages/creator-story-management.js` |
| A | `forgot-password` | `forgot-password.html` | `css/pages/forgot-password.css` | `js/pages/forgot-password.js` |
| A | `index` | `index.html` | `css/pages/index.css` | `js/pages/index.js` |
| A | `login` | `login.html` | `css/pages/login.css` | `js/pages/login.js` |
| A | `register` | `register.html` | `css/pages/register.css` | `js/pages/register.js` |
| B | `403` | `403.html` | `css/pages/403.css` | — |
| B | `404` | `404.html` | `css/pages/404.css` | — |
| B | `admin-culture-dashboard` | `admin-culture-dashboard.html` | `css/pages/admin-culture-dashboard.css` | `js/pages/admin-culture-dashboard.js` |
| B | `admin-tag-management` | `admin-tag-management.html` | `css/pages/admin-tag-management.css` | `js/pages/admin-tag-management.js` |
| B | `admin-user-management` | `admin-user-management.html` | `css/pages/admin-user-management.css` | `js/pages/admin-user-management.js` |
| B | `curator-content-map` | `curator-content-map.html` | `css/pages/curator-content-map.css` | `js/pages/curator-content-map.js` |
| B | `curator-content-review` | `curator-content-review.html` | `css/pages/curator-content-review.css` | `js/pages/curator-content-review.js` |
| B | `curator-review-detail` | `curator-review-detail.html` | `css/pages/curator-review-detail.css` | `js/pages/curator-review-detail.js` |
| B | `notifications` | `notifications.html` | `css/pages/notifications.css` | `js/pages/notifications.js` |
| C | `account-settings` | `account-settings.html` | `css/pages/account-settings.css` | `js/pages/account-settings.js` |
| C | `curator-collection-editor` | `curator-collection-editor.html` | `css/pages/curator-collection-editor.css` | `js/pages/curator-collection-editor.js` |
| C | `curator-collection-management` | `curator-collection-management.html` | `css/pages/curator-collection-management.css` | `js/pages/curator-collection-management.js` |
| C | `explorer-ai-trail-generator` | `explorer-ai-trail-generator.html` | `css/pages/explorer-ai-trail-generator.css` | `js/pages/explorer-ai-trail-generator.js` |
| C | `explorer-my-trail` | `explorer-my-trail.html` | `css/pages/explorer-my-trail.css` | `js/pages/explorer-my-trail.js` |
| C | `explorer-place-detail` | `explorer-place-detail.html` | `css/pages/explorer-place-detail.css` | `js/pages/explorer-place-detail.js` |
| C | `explorer-story-detail` | `explorer-story-detail.html` | `css/pages/explorer-story-detail.css` | `js/pages/explorer-story-detail.js` |
| C | `explorer-story-discovery` | `explorer-story-discovery.html` | `css/pages/explorer-story-discovery.css` | `js/pages/explorer-story-discovery.js` |
| C | `personal-profile` | `personal-profile.html` | `css/pages/personal-profile.css` | `js/pages/personal-profile.js` |

## Cách liên kết lại với nhau (khi ghép bài của 3 người)
1. Giữ nguyên tên tệp theo bảng trên; mỗi người chỉ thêm/sửa bộ ba của mình.
2. Muốn thêm style dùng chung → đề xuất vào `components.css` (báo nhóm), không tự sửa trong CSS trang.
3. Muốn thêm hàm dữ liệu → thêm vào `js/api.js` (lớp dữ liệu); trang chỉ gọi `CT.db` / `CT.api`.
4. Một người sửa `assets/data/seed.js` rồi cả nhóm kéo về (tránh xung đột Git).
5. Sau khi ghép: chạy `sh tests/run.sh smoke.py` và `flows.py` để kiểm tra không vỡ trang nào.
