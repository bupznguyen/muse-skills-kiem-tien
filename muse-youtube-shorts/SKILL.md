---
name: muse-youtube-shorts
description: Bộ skill vận hành kênh YouTube Shorts bằng Muse — lên kế hoạch kênh và lịch tuần, viết kịch bản Shorts theo hook 3 lớp và khung escalation, thiết kế vòng lặp, viết prompt tạo video AI từng cảnh khóa chặt nhân vật, đóng gói SEO 3 bề mặt (Feed/kệ trang chủ/Tìm kiếm), cầu nối Shorts → video dài, đọc Analytics theo VVSA và đường retention để chẩn đoán. Kèm điều kiện YPP hiện tại và mốc đổi chuẩn 01/02/2027. Dùng khi xây hoặc vận hành kênh Shorts.
version: 1.1.0
language: vi
---

# Muse × YouTube Shorts

Nguyên tắc lõi: Muse là trợ lý đứng sau — lo kế hoạch, kịch bản, prompt, đóng gói và phân tích. Người dùng giữ tài khoản, render video, kiểm tra và đăng. Không bao giờ xin mật khẩu hay mã xác minh của người dùng.

Thuật toán Shorts chạy làn riêng, tách khỏi video dài; cỡ kênh gần như không quyết định — mỗi Short tự chịu trách nhiệm về số phận của mình. Chỉ số cổng đầu phễu là **VVSA (Viewed vs Swiped Away — tỉ lệ xem tiếp so với vuốt qua)**, không phải CTR như video dài.

## Workflow 7 bước

### 1. Chốt ngách, định vị và chế độ vận hành (làm một lần khi mở kênh)
Xuất: ngách hẹp làm được lâu dài · 1 câu định vị · khán giả mục tiêu · phong cách nhân vật/hình ảnh/giọng kể thống nhất.
Mỗi Short phải thuộc đúng MỘT chế độ — trộn hai chế độ trên cùng một video là hỏng cả hai:
- **Chế độ Reach**: tối ưu VVSA + vòng lặp, độ dài thường 15–45 giây, nhạc trend chấp nhận được.
- **Chế độ Kiếm tiền/nuôi kênh**: âm thanh gốc, 30–60 giây, có cầu nối sang video dài rõ ràng (bước 6).
Kênh nhỏ nên ưu tiên âm thanh gốc: vừa giữ trọn doanh thu, vừa là tín hiệu nội dung riêng.

### 2. Lịch nội dung tuần
Dựa trên ngách + số liệu tuần trước, lên danh sách video cả tuần: mỗi video đúng một câu chuyện riêng, tránh lặp ý tưởng đã dùng. Giữ tab Shorts nhất quán chủ đề theo từng đợt — đừng đăng một Short lạc đề ngay sau một Short đang nóng. Xuất dạng bảng: ngày · chủ đề · chế độ · hook dự kiến · trạng thái.

### 3. Kịch bản Shorts — hook 3 lớp và khung escalation
**Viết 3 giây đầu TRƯỚC toàn bộ phần còn lại.** Hook gồm 3 lớp chạy song song ngay từ frame 1:
1. **Hình**: frame đầu tự nó phải "kiếm" được giây tiếp theo — hiện payoff/xung đột/kết quả, soạn như khung hình vừa pause giữa hành động (click-to-unpause). Không logo, không intro động, không "welcome back".
2. **Lời**: câu thoại đầu đáp đất trong ~1,5 giây (quá 2 giây là bị vuốt), dẫn bằng payoff hoặc stake cụ thể, nói một lần, không warm-up.
3. **Chữ trên màn hình**: 3–5 từ, to, tương phản cao, nằm vùng an toàn giữa khung (trên ~20% và dưới ~25% khung hình bị giao diện che) — nhiệm vụ là nén/sắc lại câu nói, không lặp nguyên văn. Chữ xuất hiện ngay frame 1 và phải đọc hiểu được khi tắt tiếng.

Khung kịch bản mặc định cho Short 30–45 giây (sweet spot; Short dưới 15 giây dù xem hết 100% vẫn khó qua cổng vì tổng thời gian xem tuyệt đối quá thấp):
- 0–3s: hook 3 lớp.
- 3–8s: escalation 1 — rẽ ngoặt / nâng stakes / bơm chi tiết cụ thể.
- 8–25s: escalation 2, kèm một câu re-hook quanh giây 8–10 ("nhưng đây mới là phần không ai ngờ").
- ~25–38s: payoff — giao đúng thứ đã hứa, hiện kết quả chứ không nói suông.
Nối các beat bằng **"but / therefore"**, không dùng "and then" — beat nào nối bằng "and then" là beat thừa.

**Thiết kế vòng lặp (loop) chủ động** — ghi rõ kiểu loop vào kịch bản, chọn một: *visual* (frame cuối khớp frame đầu) · *audio* (câu cuối bắt nhịp sạch vào câu mở đầu) · *question* (câu kết khiến câu mở đầu nghe khác đi) · *cliff* (kết bằng tease, payoff nằm ở đầu vòng sau). Câu cuối bắt sạch vào câu đầu; không "cảm ơn đã xem".

Trước khi chốt kịch bản, chạy 4 pressure test cho hook: **muted test** (tắt tiếng còn hiểu không) · **eyes-away test** (chỉ nghe còn giữ được không) · **glance test** (nhìn 0,5 giây có nắm được ý) · **alignment test** (3 lớp có nói cùng một ý không).

### 4. Prompt tạo video AI
Biến mỗi cảnh thành một prompt render riêng (mỗi clip khoảng 3–15 giây, ghép lại sau):
- **Khóa chặt nhân vật**: mô tả ngoại hình, trang phục, bối cảnh và giọng nói của nhân vật chính viết nguyên văn giống hệt nhau trong mọi prompt — đây là khâu quyết định video trông thật hay ghép vụng.
- Mỗi clip chỉ một hành động chính; ghi rõ ý định âm thanh (tiếng động, nhạc nền, lời thoại).
- Tránh các cảnh dễ lỗi khi render (ví dụ hành động dưới nước/ngập nước thường thiếu thật) — ưu tiên bối cảnh mặt đất.
- Dựng dọc 9:16 thật (1080×1920): bố cục lại cho khung dọc (re-layout), không crop giữa, không letterbox thanh đen.

### 5. Đóng gói theo 3 bề mặt phân phối (chọn một bề mặt chính cho mỗi video)
- **Shorts Feed**: tối ưu VVSA + loop như bước 3.
- **Kệ Shorts trang chủ**: frame đầu phải đứng vững như một thumbnail tĩnh; nhất quán chủ đề cả tab.
- **Tìm kiếm**: tiêu đề viết như câu truy vấn người xem gõ; mô tả 2–3 câu chứa từ khóa; **nói từ khóa thành tiếng** trong video (bản transcript được index) và **cháy từ khóa lên chữ trên màn hình** (YouTube đọc được chữ trong video).
Tiêu đề luôn hứa đúng điều video giao. Soạn thêm bản tiếng Anh (tiêu đề + mô tả) nếu kênh nhắm khán giả quốc tế.

### 6. Cầu nối Shorts → video dài (khi kênh có video dài)
Tín hiệu giá trị nhất một Short kiếm được là lượt click sang video dài. Kích hoạt đồng thời:
- **Tính năng "Video liên quan" (Related video) của YouTube**: gắn link video dài vào Short ngay trong YouTube Studio — đây là cầu nối chính thức, ưu tiên dùng trước mọi cách khác.
- **5 giây cuối**: callout gọi TÊN CỤ THỂ một video dài cùng chủ đề + chữ trên màn hình đi kèm. CTA đúng là "xem bản đầy đủ", KHÔNG kêu subscribe (kêu subscribe kéo chân người xem đúng chỗ vòng lặp cần cháy, mà không tăng tỉ lệ đăng ký đo được).
- **Bình luận ghim**: link + "một thứ cụ thể chỉ bản dài mới có" — nói chung chung "bản dài hơn" thì không ai bấm.
Chưa có video dài cùng chủ đề thì hoặc làm video dài TRƯỚC rồi mới đăng Short, hoặc chấp nhận Short đó chỉ kiếm reach.

### 7. Đọc Analytics và lặp lại — chẩn đoán theo đúng thứ tự
Người dùng gửi số liệu YouTube Studio. Đọc theo thứ tự, mỗi lần chỉ kết luận MỘT lỗi lớn nhất + MỘT thay đổi:
1. **VVSA trước tiên**: thấp (tham khảo kinh nghiệm cộng đồng: dưới ~60% thường flop, 70–90% thường breakout — đây là mốc kinh nghiệm, không phải ngưỡng YouTube công bố; kênh nhỏ mẫu số ít thì VVSA dao động mạnh, đừng kết luận từ vài trăm lượt xem) → lỗi ở 3 giây đầu → viết lại mở đầu và đăng như một Short MỚI.
2. **VVSA khỏe mà % xem trung bình thấp** → thân chảy máu. Đọc hình dạng đường retention: sụt ngay 3 giây đầu = mở đầu yếu · chảy đều ở giữa = thiếu escalation (thêm rẽ ngoặt ở mốc 5–8 giây) · sụt muộn ngay trước payoff = payoff bị chôn (đưa payoff lên sớm). Mục tiêu: đường cong phẳng và nằm trên dải "typical" của kênh.
3. **% xem trên 100% mà reach vẫn kẹt** → loop đã cháy, giới hạn nằm ở chủ đề/share, không phải kỹ thuật.
4. **Short chạy tốt mà không có click sang video dài** → thiếu cầu nối (bước 6), không phải lỗi video.
Mọi kết luận về doanh thu/YPP chỉ đọc **Engaged Views**, không đọc Views thô. Không xóa video yếu — Short có thể tìm được khán giả muộn. Khi xếp hạng video của kênh, xếp theo **bội số so với median của chính kênh** (video đạt ≥2× median là công thức đáng học), không xếp theo view thô.

## Bẫy bản quyền nhạc phải biết
- Short dài trên 60 giây mà đang có Content ID claim đang hoạt động (ví dụ cắt từ video dài dính nhạc bản quyền) sẽ bị chặn toàn cầu và không kiếm được tiền — kiểm tra Content ID trước khi coi một Short là đã sẵn sàng kiếm tiền.
- Dùng nhạc bản quyền thì một phần phân bổ doanh thu của Short đi vào pool bản quyền nhạc trước khi áp tỉ lệ chia 45% — âm thanh gốc giữ trọn phần của mình.

## Kiếm tiền trên YouTube (số liệu để tư vấn đúng)
- YouTube Partner Program hiện tại: 1.000 người đăng ký + 4.000 giờ xem công khai hợp lệ trong 12 tháng, HOẶC 10 triệu lượt xem Shorts hợp lệ (Engaged Views) trong 90 ngày. Đạt mốc mới được nộp đơn; YouTube còn xét duyệt kênh.
- **Từ 01/02/2027, hồ sơ mới cần gấp đôi: 8.000 giờ xem hoặc 20 triệu lượt xem Shorts/90 ngày** (vẫn 1.000 người đăng ký). Hồ sơ nộp trước mốc này được xét theo chuẩn cũ — kênh mới nên chạy sớm.
- Shorts: nhà sáng tạo giữ 45% doanh thu quảng cáo phân bổ từ Creator Pool. RPM Shorts thực tế thấp hơn video dài rất nhiều (tham khảo cộng đồng: khoảng $0,03–0,10/1.000 lượt xem hợp lệ, cao hơn ở ngách tài chính/tech và khán giả Mỹ) — đây là khoảng cách cấu trúc; Shorts mạnh ở khâu kéo khán giả và nuôi các đường tiền khác.
- Nội dung AI trông như thật (dựng sự kiện có vẻ đã xảy ra) phải khai báo khi đăng; chỉ dùng AI viết dàn ý/kịch bản thì thường không cần. Kênh phải đáp ứng chính sách nội dung nguyên gốc — không sản xuất hàng loạt nội dung na ná nhau, không đăng lại nội dung người khác.
- Đường tiền thứ hai: Amazon Influencer Program (Storefront) nếu được chấp thuận — luôn công bố khi dùng link hoa hồng.

## Việc Muse làm / việc người dùng làm
- Muse: kế hoạch, lịch tuần, kịch bản (hook 3 lớp + escalation + loop), prompt từng cảnh, đóng gói 3 bề mặt, cầu nối video dài, đọc Analytics theo VVSA/retention, nhắc mốc chính sách.
- Người dùng: tạo kênh, render video trên tài khoản công cụ của mình, kiểm tra video, đăng và khai báo AI trung thực, gắn Video liên quan trong Studio.
