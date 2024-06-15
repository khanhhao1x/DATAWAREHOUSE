# THIẾT KẾ DATAWAREHOUSE CHO CÔNG TY KINH DOANH XE ĐẠP

## GIỚI THIỆU TỔNG QUAN
Ngành công nghiệp xe đạp đang chứng kiến sự tăng trưởng mạnh mẽ trên toàn
cầu. Nhu cầu về phương tiện di chuyển xanh, lành mạnh và tiết kiệm chi phí ngày càng
gia tăng, thúc đẩy doanh số bán xe đạp tăng cao. Sự phát triển mạnh mẽ này dẫn đến
lượng dữ liệu khổng lồ được tạo ra từ nhiều nguồn khác nhau và điều này đặt một
thách thức to lớn trong việc phải quản lý lượng dữ liệu khổng lồ và đa dạng của doanh
nghiệp kinh doanh xe đạp. Với sự phát triển của thị trường xe đạp cũng như sự mở
rộng không ngừng về mặt quy mô, doanh nghiệp kinh doanh xe đạp xuất hiện nhu cầu
xây dựng một kho dữ liệu nhằm lưu trữ những dữ liệu quá khứ cũng như tiến hành
phân tích, đánh giá để đưa ra những chiến lược trong tương lai.
Trong kho dữ liệu của doanh nghiệp kinh doanh xe đạp, cần chứa đầy đủ các
thông tin về các sản phẩm, nhân viên, chi nhánh, các chiến dịch quảng bá sản phẩm,
thông tin chi tiết về khách hàng, giao dịch mua bán và dịch vụ hỗ trợ sau bán hàng.
Kho dữ liệu sẽ được cập nhật định kỳ từ các nguồn dữ liệu như hệ thống bán hàng,
website, các kênh truyền thông xã hội và các nguồn dữ liệu bên ngoài.

## BẢNG MÔ TẢ DỮ LIỆU
![image](https://github.com/khanhhao1x/DATAWAREHOUSE/assets/166882051/26402318-a850-47c7-bd19-57d981e6e957)
![image](https://github.com/khanhhao1x/DATAWAREHOUSE/assets/166882051/820265eb-4d32-466c-b4ba-48d29f14037b)
![image](https://github.com/khanhhao1x/DATAWAREHOUSE/assets/166882051/8b82a774-2fe8-4e79-afad-143d82af9eb2)
![image](https://github.com/khanhhao1x/DATAWAREHOUSE/assets/166882051/b937a2d9-ab4f-4b55-a015-e71ca55655bb)
![image](https://github.com/khanhhao1x/DATAWAREHOUSE/assets/166882051/91b6c485-e2b5-42ec-b0cd-dc07206c7e8a)

## SCHEMA
![image](https://github.com/khanhhao1x/DATAWAREHOUSE/assets/166882051/73806a89-ecb9-4685-9f42-8183e4406a58)

Đối với doanh nghiệp kinh doanh xe đạp, quy trình kinh doanh diễn ra xung
quanh 3 loại sự kiện chính, bao gồm: các giao dịch phát sinh từ hoạt động bán hàng,
các giao dịch từ các dịch vụ và các chiến dịch khuyến mãi. Từ đó, nhóm tiến hành xây
dựng 3 bảng Fact bao gồm: Fact_Order_Transaction, Fact_Service_Transaction và
Fact_Promotion_Tracking nhằm mục đích lưu trữ toàn bộ những sự kiện chính được
diễn ra trong doanh nghiệp.
Do đó trong quá trình xây dựng kho dữ liệu cho doanh nghiệp, nhằm đáp ứng đầy
đủ nhu cầu ghi nhận toàn bộ 3 sự kiện chính vừa kể trên, nhóm lựa chọn lược đồ
Constellation Schema (lược đồ chòm sao) bởi lược đồ này cho phép xây dựng nhiều
bảng Fact, mà trong đó các bảng Fact có thể cùng chia sẻ các dữ liệu từ các bảng
dimension khác nhau và điều này vô cùng hữu ích khi có thể giúp truy vấn dữ liệu với
các góc nhìn cũng như độ mịn của dữ liệu ở các mức độ khác nhau.

