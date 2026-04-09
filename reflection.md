# Individual Reflection
##### Họ và tên: Nguyễn Quang Tùng
##### MSHV: 2A202600197

## 1. Role

Đóng góp chủ yếu: Frontend · UI/UX · SPEC · Eval metrics


[Xem repo sản phẩm tại đây](https://github.com/DangMinh21/Nhom09-E403-Day06)

## 2. Đóng góp cụ thể

- **AI Product Canvas + User Stories 4 paths**: Mình cùng nhóm xác định rõ user chính (hành khách Vietnam Airlines), pain point cốt lõi (phải mở nhiều trang để tra cứu), và chuyển thành 4 features × 4 paths (happy / low-confidence / failure / correction) để giảm rủi ro khi demo.
- **Prototype end-to-end**: Trong phạm vi role của mình, mình tham gia hoàn thiện luồng trải nghiệm từ UI đến backend integration, iterate system prompt nhiều vòng, và phối hợp để hệ thống gọi đúng bộ tools thay vì trả lời chung chung.


## 3. SPEC mạnh nhất / yếu nhất

- **Mạnh nhất**: Canvas và User Stories. Điểm mạnh là bám đúng pain point thực tế của người dùng, nên khi viết spec nhóm mình tránh được tình trạng làm feature "hay nhưng không cần".
- **Yếu nhất**: ROI. Ba kịch bản conservative / realistic / optimistic vẫn còn dùng assumption tương đối giống nhau. Nếu làm kỹ hơn, mình sẽ tách rõ phạm vi triển khai và chi phí vận hành cho từng kịch bản.

## 4. Đóng góp khác

- Tham gia iterate system prompt qua nhiều phiên bản; bản đầu còn hallucination, bản sau ổn định hơn nhờ ràng buộc phạm vi trả lời và ưu tiên gọi tool.
- Hỗ trợ review/debug các lỗi integration (đặc biệt ở mapping dữ liệu đầu vào), giúp giảm lỗi tool call khi test thủ công.
- Chủ động test nhiều kịch bản sử dụng (happy path, sai ngữ cảnh, thiếu dữ liệu) để phát hiện lỗi sớm trước khi demo.
- Tinh chỉnh UI/UX qua từng giai đoạn để cải thiện trải nghiệm người dùng, giúp luồng thao tác rõ ràng và dễ hiểu hơn.
- Gợi ý phát triển thêm các tính năng quan trọng sau phiên bản đầu, ưu tiên những tính năng tăng giá trị thực tế cho người dùng.

## 5. Điều học được

Điều mình học được rõ nhất là phải bắt đầu từ việc xác định đúng pain point, sau đó viết spec đủ cụ thể để cả team hiểu cùng một mục tiêu, rồi mới thiết kế hệ thống agent phù hợp với bối cảnh sử dụng thực tế. Bên cạnh đó, workflow phát triển cần được xây dựng đúng ngay từ đầu để có thể mở rộng và cải thiện dần theo từng vòng lặp, thay vì sửa chắp vá.

Mình cũng nhận ra sản phẩm AI muốn đi xa thì bắt buộc phải có độ đo và tiêu chí đánh giá cụ thể (độ chính xác, thời gian phản hồi, tỉ lệ xử lý đúng intent), đồng thời có chiến thuật xây dựng sản phẩm theo từng giai đoạn: validate nhanh, ổn định hệ thống, rồi mới mở rộng tính năng.

## 6. Nếu làm lại

Nếu làm lại, mình sẽ khóa quy trình theo thứ tự: **Pain point → Canvas → Danh sách tool cần thiết → Prompt + test thủ công → Build backend tools → Gắn UI → Polish**.

Lý do là khi prompt chưa ổn định mà đã đẩy nhanh UI, nhóm dễ bị sửa qua sửa lại nhiều vòng. Bài học lớn nhất của mình là ưu tiên nền tảng logic trước, rồi mới tối ưu trải nghiệm giao diện.

## 7. AI giúp gì / AI sai ở đâu

**AI giúp:**
- Giúp mình build giao diện nhanh hơn, đặc biệt ở phần layout và các thành phần UI cơ bản.
- Gợi ý cách trình bày thông tin rõ ràng hơn để người dùng dễ theo dõi khi chat với agent.
- Đề xuất các tính năng cần thiết trong scope, giúp nhóm chốt danh sách feature nhanh hơn.
- Hỗ trợ phân tích pain point và gợi ý core feature phù hợp với bài toán người dùng.

**AI sai / mislead:**
- Có xu hướng đề xuất thêm nhiều tính năng ngoài scope, dễ làm lệch trọng tâm nếu nhóm không kiểm soát.
- Code AI sinh ra có thể "trông đúng" nhưng vẫn chứa lỗi ngầm, nên bắt buộc phải test bằng dữ liệu thật.
- Một số gợi ý kiến trúc hơi over-engineering so với thời gian hackathon.

=> Với mình, AI là công cụ tăng tốc rất mạnh, nhưng chất lượng sản phẩm cuối cùng vẫn phụ thuộc vào con người ở 3 việc: chốt scope, review code, và kiểm thử thực tế.