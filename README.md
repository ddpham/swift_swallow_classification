# SWIFT VS SWALLOW
> Đây là bài viết khá đơn giản về phân loại hình ảnh nhằm hỗ trợ việc thực hành khóa học `Practical Deep Learning for Coders` do Jeremy Howard (người đồng sáng lập ra fast.ai) và các đồng nghiệp. Thông tin chi tiết của khóa học có thể xem tại [đây](https://course.fast.ai/). Với chủ đề về hình ảnh, tôi chọn chim yến (swift) và chim én (swallow) để làm chủ đề phân loại hình ảnh. Lý do khá đơn giản vì tôi thích 2 loài chim này.

## Yêu cầu
Bài viết được viết lại trên Jupyter Notebook và sử dụng ngôn ngữ Python. Nên hy vọng các bạn đều đã làm quen với hai công cụ này.
Ngoài ra, để thực hiện được các code trong notebook, bạn cần cái các gói trong file requiremens.txt, về cơ bản, chúng ta chỉ cần fastai để chạy được hầu hết các code của bài viết này.

## Tạo tập dữ liệu
Tập dữ liệu được sử dụng cho dự án này là thông qua dữ liệu của công cụ tìm kiếm duckduckgo.com là chính, một vài ảnh tôi có nhặt nhạnh thêm được từ google.com và bing.com. Trong khóa học của Jeremy, tôi có để ý về cách sử dụng dịch vụ của bing search để thu thập dữ liệu. Tuy nhiên, do việc setup và xin tài khoản miễn phí khá phức tạp nên tôi đã quyết định lựa chọn việc thu thập dữ liệu bằng tay. Việc này nghe có vẻ rất ...`tay to`, nhưng thực sự mà nói, tôi khá vui vẻ làm công việc này vì nó giúp tôi nhìn thêm được nhiều điểm thú vị của chim yến và chim én mà trước nay mình không hề biết. Ngoài ra, bạn có thể sử dụng 2 cách khác khá đơn giản và nhanh gọn để lấy dữ liệu (tuy nhiên hình ảnh sẽ có kích cỡ nhỏ và không được chất lượng như ý)

1. Sử dụng lại code đã được hướng dẫn trong khóa học cũ: chi tiết xem file nbs/download.ipynb.
2. Tải toàn bộ tập tin html của công cụ search:
- sử dụng firefox hoặc google chrome.
- chọn google search image rồi search : "swallow bird" -"swift bird" cho chim én/ "swift bird" -"swallow bird" cho chim yến (lưu ý chỉ có 1 dấu cách giữa cụm tự đầu tiên và dấu trừ `-`, còn dấu `-` sẽ viết liền với cụm từ sau. Bạn sẽ thấy kết quả khá khác biệt khi có dấu cách giữa `-` và 2 cụm từ).
- kéo chuột xuống dưới và chọn `Show more results` cho đến khi không thể nữa.
- Sau đó bạn chỉ cần đơn giản ấn phím tắt: `Ctrl` + `s` và ấn vào nút save.
- Bạn sẽ có 2 folder của chim yến và chim én, trong folder sẽ có các file hình ảnh dạng `.jpeg` hoặc `.png`, bạn có thể chọn loại `.jpeg` là đủ. bạn tạo folder data/swift và data/swallow nơi bạn dùng để lưu hình ảnh và code của bạn. 
