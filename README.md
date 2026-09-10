# Content-Web-KD-img

Kho ảnh **công khai** cho các content block khuyến mãi của [kymdanshop.vn](https://kymdanshop.vn).

Repo này **chỉ chứa ảnh**. Phần mã nguồn HTML/CSS nằm ở repo riêng (private).

## Vì sao tách repo

Ảnh được phục vụ qua **jsDelivr**, mà jsDelivr chỉ đọc được repo **public**. Repo mã nguồn cần giữ private vì có những chiến dịch chưa tới ngày chạy. Nên tách làm hai.

## Cách lấy link

```
https://cdn.jsdelivr.net/gh/noeffortnomoney/Content-Web-KD-img@main/<chiến-dịch>/<tên-file>
```

Ví dụ:

```
https://cdn.jsdelivr.net/gh/noeffortnomoney/Content-Web-KD-img@main/ngay-hoi-trai-nghiem/banner-pc.webp
```

**Dùng `@main`**, đừng ghim mã commit — đổi ảnh thì chỉ cần push đè cùng tên file, link giữ nguyên. Đổi lại là jsDelivr nhớ tạm 12 tiếng; cần lan ngay thì mở link purge một lần:

```
https://purge.jsdelivr.net/gh/noeffortnomoney/Content-Web-KD-img@main/<đường-dẫn-file>
```

## Nội dung

| Thư mục | Chiến dịch | Ảnh |
|---|---|---|
| `ngay-hoi-trai-nghiem/` | Ngày Hội Trải Nghiệm — AEON MALL Huế, 19–27/09/2026 | 31 |
| `thang-vang-aeon-hue/` | Tháng Vàng Ưu Đãi — AEON MALL Huế, 09/2026 | 34 |
| `em-ai-ven-tron/` | Êm Ái Vẹn Tròn — quà cưới Diamond Place | 19 |

Mỗi thư mục có `manifest.md` ghi **vai trò ô ↔ tên file ↔ URL Cloudinary cũ**.

## Quy ước đặt tên

Tên file theo **vai trò của ô ảnh**, không theo tên file gốc:

- `banner-pc` · `banner-tablet` · `banner-mobile` — ảnh nền hero từng khổ màn hình
- hậu tố `-cut` — bản đã tách nền, **có kênh alpha**, đè lên lớp phủ hero
- hậu tố `-pc` / `-mb` — hai phiên bản của cùng một ô, đổi nhau bằng CSS

## Lưu ý

**9 ảnh banner là do Cloudinary dựng ra bằng AI (`b_gen_fill`), không có file gốc ở bất cứ đâu.** Chạy lại cùng một prompt sẽ ra bức tường khác. Đây là bản duy nhất — đừng xoá, đừng nén lại.

Ba file `*-cut` giữ **kênh alpha**. Chuyển sang `.jpg` là mất alpha và hero sẽ hiện ra một khối chữ nhật đặc.
