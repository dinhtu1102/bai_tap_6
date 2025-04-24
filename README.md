
Bài tập 6: Hệ quản trị CSDL
Chủ đề: Câu lệnh Select
Yêu cầu bài tập: 
Cho file sv_tnut.sql (1.6MB)
1. Hãy nêu các bước để import được dữ liệu trong sv_tnut.sql vào sql server của em
2. dữ liệu đầu vào là tên của sv; sđt; ngày, tháng, năm sinh của sinh viên (của sv đang làm bài tập này)
3. nhập sql để tìm xem có những sv nào trùng hoàn toàn ngày/tháng/năm với em?
4. nhập sql để tìm xem có những sv nào trùng ngày và tháng sinh với em?
5. nhập sql để tìm xem có những sv nào trùng tháng và năm sinh với em?
6. nhập sql để tìm xem có những sv nào trùng tên với em?
7. nhập sql để tìm xem có những sv nào trùng họ và tên đệm với em.
8. nhập sql để tìm xem có những sv nào có sđt sai khác chỉ 1 số so với sđt của em.
9. BẢNG SV CÓ HƠN 9000 ROWS, HÃY LIỆT KÊ TẤT CẢ CÁC SV NGÀNH KMT, SẮP XẾP THEO TÊN VÀ HỌ ĐỆM, KIỂU TIẾNG  VIỆT, GIẢI THÍCH.
10. HÃY NHẬP SQL ĐỂ LIỆT KÊ CÁC SV NỮ NGÀNH KMT CÓ TRONG BẢNG SV (TRÌNH BÀY QUÁ TRÌNH SUY NGHĨ VÀ GIẢI NHỮNG VỨNG MẮC)

DEADLINE: 23H59:59 NGÀY 25/4/2025

Ghi chú: Giải thích tại sao lại có SQL như vậy.

Bài làm:

1.IM pọt file sv_tnut.sql mà thầy giáo đã cho để đưa vào sql server của em

![image](https://github.com/user-attachments/assets/dcdbf0ec-91d9-4450-81b2-a8f0e0e06ae2)

b1 : Connect vào sql server của em, tạo một database mới => chọn New querry

![image](https://github.com/user-attachments/assets/dab40bb9-4f77-40bb-bb0f-b46146585979)

b2 : Chọn file -> open ->file... sv_tnut.sql

![image](https://github.com/user-attachments/assets/7771c153-0d2f-41cd-bba8-ae2156716c20)

b3 : Chọn file sv_tnut.sql ở mục đã down về rồi nhấn chọn

![image](https://github.com/user-attachments/assets/ed2e4ebe-6fda-44a3-8d77-120ae061fc09)

b4 : Ấn Excute để chạy file thành công ở database sv_tnut trong server của em

2. dữ liệu đầu vào là tên của sv; sđt; ngày, tháng, năm sinh của sinh viên (của sv đang làm bài tập này)
   
Đưa thông tin cá nhan của em vào db

![image](https://github.com/user-attachments/assets/2798793d-2b87-4036-b6fe-814c360676a9)

![image](https://github.com/user-attachments/assets/d77c0692-4ab3-4fbb-85f1-eea5cea1f435)

=> Đã có thông tin của em rồi 

3. nhập sql để tìm xem có những sv nào trùng hoàn toàn ngày/tháng/năm với em?

![image](https://github.com/user-attachments/assets/4e6ec37c-08db-4d05-abf4-57568218bcf1)

=> Kết quả in ra có 3 người trừng ngày sinh với em

4. nhập sql để tìm xem có những sv nào trùng ngày và tháng sinh với em?

![image](https://github.com/user-attachments/assets/9136465a-3020-4e4b-b624-606e041c42d3)

=> kết quả in ra tổng cộng có 25 sinh viên cùng ngày tháng sinh cảu em

5. nhập sql để tìm xem có những sv nào trùng tháng và năm sinh với em?

![image](https://github.com/user-attachments/assets/3865d38b-0e90-4704-a737-8ecde4ec4dd8)

=> kết quả in ra tổng cộng có 129 sinh viên cùng tháng và năm sinh của em

6. nhập sql để tìm xem có những sv nào trùng tên với em?

![image](https://github.com/user-attachments/assets/a1e53874-75c4-4189-9624-a603ff4d5dfa)

=> kết quả trả về có 134 sinh viên có cùng tên là " Tú "

7. nhập sql để tìm xem có những sv nào trùng họ và tên đệm với em.

![image](https://github.com/user-attachments/assets/0f119ca9-9f99-4bbe-bbc1-a4b437a195e2)

=> kết quả trả về có 71 sinh viên có cùng họ và tên đêm giống em
   
8. nhập sql để tìm xem có những sv nào có sđt sai khác chỉ 1 số so với sđt của em.

![image](https://github.com/user-attachments/assets/68146278-50bf-411d-8916-8352f404ce24)

=> sau khi test em ko thấy có số điện thoại nào trùng và khác 1 số với e cả 

  do sim độc lâp số điện thoại em là số chính chủ .

9. BẢNG SV CÓ HƠN 9000 ROWS, HÃY LIỆT KÊ TẤT CẢ CÁC SV NGÀNH KMT, SẮP XẾP THEO TÊN VÀ HỌ ĐỆM, KIỂU TIẾNG  VIỆT, GIẢI THÍCH.

![image](https://github.com/user-attachments/assets/3366ccd3-4b33-4346-b310-cf5317654681)

- WHERE lop LIKE 'K%KMT%'	Chọn các sinh viên có lớp thuộc ngành Kỹ thuật máy tính (KMT). Giả định rằng tên lớp chứa KMT (ví dụ: K58KMT.01)
  
- ORDER BY ten, hodem	Sắp xếp theo ten trước (ví dụ: An, Bình, Cường...), sau đó đến hodem nếu tên trùng nhau
  
- COLLATE Vietnamese_CI_AS	Sắp xếp đúng chuẩn tiếng Việt có dấu. Ví dụ: Ánh trước Bình, Đức sau Duy, không theo bảng mã ASCII
  
10. HÃY NHẬP SQL ĐỂ LIỆT KÊ CÁC SV NỮ NGÀNH KMT CÓ TRONG BẢNG SV (TRÌNH BÀY QUÁ TRÌNH SUY NGHĨ VÀ GIẢI NHỮNG VỨNG MẮC)

CÁCH 1: 
 
- em thấy dữ liệu của các trường của bảng SV được tạo , ko có trường phân biệt NAM Nữ
  
- Em nghĩ mình nên thêm một trường giới tính nữa vào bảng SV ( nam / nữ )

CÁCH 2

- nếu ko có giới tính chỉ có cách là nêu những tên con gái ra như Hiền, mai , thảo , hương, giang , linh, phương, trang , my , mi , thơ... để truy vấn ra danh schs nữ

- chỉ ra các họ đệm như thị ,ngọc, mai , thùy ,diễm ,thanh...

=> cách này khá mất thời gian và ko đảm bảo đủ danh sách 

![image](https://github.com/user-attachments/assets/e76eb7ab-6e6b-4634-abfe-3858da84cfa1)

=> kết quả truy vấn tuy ra đanh sách nữ nhưng mà ko đủ và khá mất thời gian .em nghĩ cách tốt nhất vẫn phải thêm trường nam/nữ  để phân biệt
