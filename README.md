NHẬN DIỆN KHUÔN MẶT TRONG THỜI GIAN THỰC

Hướng dẫn thực hiện xây dựng và khảo sát mô hình nhận diện khuôn mặt trong thời gian thực

*Chương trình sử dụng cơ sở dữ liệu tự tạo. Yêu cầu môi trường Python IDLE 3.9 và ứng dụng DB Browser (SQLite).
#LINK TẢI: PYTHON 3.9: https://www.python.org/downloads/release/python-390/
                    hoặc tại cửa sổ command prompt chạy lệnh: python --version
                    hướng dẫn tại: https://www.geeksforgeeks.org/how-to-install-opencv-for-python-in-windows/
          ứng dụng SQLite    : https://sqlitebrowser.org/
          
Cài đặt và tạo CSDL bằng SQLite có thể tham khảo tại đây: https://www.dotplays.com/android-co-ban-su-dung-sqlite-bang-phan-mem-db-browser-for-sqlite/
Cài đặt các thư viện cần thiết cho ứng dụng Python bằng lệnh pip install trong cửa sổ Command Prompt.
Một số thư viện cần thiết:
Cú pháp: pip install PACKAGE_NAME
      Đối với opencv, PACKAGE_NAME có thể là:
                    opencv-python (chỉ chứa các mô-đun chính)
                    opencv-contrib-python (chứa cả mô-đun chính và mô-đun đóng góp)
                    opencv-python-headless(giống như opencv-pythonnhưng không có chức năng GUI)
                    opencv-contrib-python-headless(giống như opencv-contrib-pythonnhưng không có chức năng GUI)
                    
      Đối với sqlite (python v3):  pip install pysqlite3 
      
      Thư viện để load mô hình file đuôi .h5: pip install h5py
     
      
Link tải SQLite Browser: https://sqlitebrowser.org/ tạo Database như hướng dẫn ở mục 2.2.2 của chương 2.


CSDL sau khi tạo được tách riêng theo từng danh mục hoàn toàn thủ công. Dựa trên id và user đã đặt trong code "thu thap CSDL".

Các bước thực hiện:
1)	Khởi chạy code thu thập cơ sở dữ liệu để thu thập dữ liệu khuôn mặt.
2)	Tách, phân loại và đặt tên các danh mục cho dữ liệu lấy từ CSDL vừa thu thập được trong tệp “DataSet” vừa tạo tại code thu thập.
3)	Chạy code đào tạo. Sau khi đào tạo hoàn tất và lưu mô hình vào file .h5.
4)	Chạy code nhận diện để kiểm tra mô hình.

Link tải các tệp thuật toán Haar Cascade sử dụng trong mô hình: https://github.com/opencv/opencv/tree/master/data/haarcascades
 sử dụng trong chương trình này là f.xml đính kèm tương ứng với file "haarcascade_frontalface_default.xml" trong đường dẫn trên.
 
 
 
 
 
 contact: utplutoa1@gmail.com
