# Tìm Hiểu Convolutional Neural Networks Cho Phân Loại Ảnh

## Giới Thiệu
Convolutional Neural Networks (CNN) là một trong những mô hình deep learning phổ biến nhất và có ảnh hưởng nhiều nhất trong cộng đồng Computer Vision. CNN được dùng trong trong nhiều bài toán như nhân dạng ảnh, phân tích video, ảnh MRI, hoặc cho bài các bài của lĩnh vự xử lý ngôn ngữ tự nhiên,và hầu hết đều giải quyết tốt các bài toán này. <br/><br/> CNN cũng có lịch sử khá lâu đời. Kiến trúc gốc của mô hình CNN được giới thiệu bởi một nhà khoa học máy tính người Nhật vào năm 1980. Sau đó, năm 1998, Yan LeCun lần đầu huấn luyện mô hình CNN với thuật toán backpropagation cho bài toán nhận dạng chữ viết tay. Tuy nhiên, mãi đến năm 2012, khi một nhà khoa học máy tính người Ukraine Alex Krizhevsky (đệ của Geoffrey Hinton) xây dựng mô hình CNN (AlexNet) và sử dụng GPU để tăng tốc quá trình huấn luyện deep nets để đạt được top 1 trong cuộc thi Computer Vision thường niên ImageNet với độ lỗi phân lớp top 5 giảm hơn 10% so với những mô hình truyền thống trước đó, đã tạo nên làn sóng mãnh mẽ sử dụng deep CNN với sự hỗ trợ của GPU để giải quyết càng nhiều các vấn đề trong Computer Vision. 

## Image Classification 
Trong bài blog này, mình giới thiệu kiến trúc cụ thể của mô hình CNN cho bài toán phân loại ảnh. Phân loại ảnh là một bài toán quan trọng bậc nhất trong lĩnh vực Computer Vision. Chúng ta đã có rất nhiều nghiên cứu để giải quyết bài toán này bằng cách rút trích các đặc trưng rất phổ biến như SIFT, HOG rồi cho máy tính học nhưng những cách này tỏ ra không thực sự hiểu quả. Nhưng ngược lại, đối với con người, chúng ta lại có bản năng tuyệt vời để phân loại được những đối tượng trong khung cảnh xung quanh một cách dễ làm.

Dữ liệu đầu vào của bài toán là một bức ảnh. Một ảnh được biểu ảnh bằng ma trận các giá trị. Mô hình phân lớp sẽ phải dự đoán được lớp của ảnh từ ma trận điểm ảnh này, ví dụ như ảnh đó là con mèo, chó, hay là chim. 

<div class="img-div" markdown="0">
    <img src="/images/cnn_input.png" />
</div>

Để biểu diễn một bức ảnh 256x256 pixel trong máy tính thì ta cần ma trận sẽ có kính thước 256x256 chiều, và tùy thuộc vào bức ảnh là có màu hay ảnh xám thì ma trận này sẽ có số kênh tương ứng, ví dụ với ảnh màu 256x256 RGB, chúng ta sẽ có ma trận 256x256x3 để biểu diễn ảnh này. 

## Mối liên kết giữ CNN và thị giác
CNN có mối liên kết chặt chẽ với sinh học, cụ thể là của võ não thị giác, nơi xử lý thông tin liên quan đến hình ảnh từ các tế bào cảm thụ ánh sánh nằm ở mắt người. Năm 1962, 2 nhà thần kinh học người Mỹ là Hubel and Wiesel đã thực hiện thí nghiệm khám phá cách tổ chức của các tế bào não để xử lý thông tin thị giác và các tổ chức này đảm nhận nhiệm vụ nào. Trong [video](https://www.youtube.com/watch?v=Cw5PKV9Rj3o) này, các bạn có thể nghe được âm thanh đại diện cho các tế nào não phản ứng lại với các hình ảnh, góc cạnh, hướng của các đường thẳng xuất hiện trong video theo một trật tự nhất định. Điều này có nghĩ là mỗi neuron được thiết lập để phản ứng lại một số đặc điểm cố định của neuron đó.  
<div class="img-div" markdown="0">
    <img src="/images/cnn_visual_cortex.jpg" />
</div>

Các bạn đọc tiếp tục tại [blog](https://pbcquoc.github.io/cnn/) của mình nhé

# Dataset
Các bạn có thể download tập dataset đã được xử lý tại [đây](https://drive.google.com/open?id=1ABhwNb5ioRzUEV9iLDpVSEIV_76yofNm) nhé

# Any Problems?

Nếu bạn có gặp bất kì vấn đề gì thì liên hệ với mình qua gmail pbcquoc@gmail.com.

