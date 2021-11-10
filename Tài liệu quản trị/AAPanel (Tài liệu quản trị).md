**1. Giới thiệu**![](.//media/image1.png)


\- AAPanel là một phiên bản quốc tế hóa của BAOTA Panel. Một web hosting
control panel miễn phí rất tốt và nổi tiếng nhất của Trung Quốc phát
triển. Dù rằng AAPanel hiện tại ít tính năng hơn bản gốc BAOTA Panel
nhưng nó sẽ được cập nhật liên tục và sớm tích hợp các chức năng nổi bật
vào.

\- Đặc điểm nổi bật của AAPanel:

-   Rất nhẹ, chỉ yêu cầu VPS Linux 512MB RAM để sử dụng.

-   Dễ dàng sử dụng, cài đặt với cú click chuột.

-   Chỉnh sửa cấu hình PHP, Webserver trực tiếp trên giao diện.

-   Thư viện App Store giúp dễ dàng cài đặt Redis, Memcached, Google
    Drive,\... với một cú nhấp chuột.

-   Quản lý tập tin với File Manager giao diện đẹp, hỗ trợ code editor
    rất tiện lợi.

-   Cấu hình bảo mật VPS, Webserver với một cú nhấp chuột.

-   Hỗ trợ backup website lên Google Drive, Amazon S3, FTP,\...

-   Cộng đồng hoạt động sôi nổi

![](.//media/image2.png)


**2. Hướng dẫn cài đặt AAPanel**

\- Để cài đặt AAPanel, VPS/Server cần phải đáp ứng các điều kiện sau:

-   RAM >= 512MB, tuy nhiên tốt nhất từ 768MB để hoạt động ổn định nhất.

-   Hệ điều hành CentOS 7.1+, Ubuntu 16.04+, Debian 9.0+ chưa được cài
    bất kì phần mềm control panel hoặc webserver nào.

\- Để tiến hành cài đặt, ta chạy lệnh cài đặt sau (ở VD này là Ubuntu):

wget -O install.sh
http://www.aapanel.com/script/install-ubuntu_6.0_en.sh && sudo bash
install.sh

![](.//media/image3.png)


![](.//media/image4.png)

\- Tiếp tục quá trình cài đặt sẽ diễn ra, đợi đến khi việc cài đặt kết
thúc nó sẽ cung cấp thông tin đăng nhập vào AAPanel vừa cài đặt.

![](.//media/image5.png)


\- Ta hãy lưu lại thông tin đăng nhập trên, sau đó truy cập trên trình
duyệt với thông tin trên để bắt đầu cài đặt webserver.

![](.//media/image6.png)


\- Sau khi đăng nhập vào AAPanel lần đầu tiên, nó sẽ yêu cầu cài đặt
loại webserver, ở đây ta có thể chọn loại webserver sử dụng phù hợp.
AZDIGI khuyến nghị ta sử dụng bộ LNMP (Linux + NGINX + MySQL + PHP-FPM)
để hoạt động ổn định và tối ưu nhất.

\- Ta nên chọn LNMP với các phiên bản sau:

-   NGINX - TEngine 2.2

-   MySQL MariaDB 10.2

-   PHP 7.2 (có thể cài thêm sau)

-   Method: Fast

![](.//media/image7.png)
![](.//media/image8.png)


\- Sau khi ta ấn nút One-click Install thì giao diện cài đặt sẽ hiển thị
ra. Ta có thể giữ nguyên cửa sổ để xem tiến trình cài đặt. Thời gian cài
đặt có thể mất 20-40 phút tùy vào tình trạng mạng.

\- Ngay sau khi hoàn tất, ta có thể bắt đầu sử dụng AAPanel ngay.

![](.//media/image9.png)


**3. Thay đổi thông tin user/pass/port của AAPanel**

\- AAPanel có một vấn đề là sau khi cài đặt, thông tin truy cập control
panel mà aaPanel cung cấp tương đối khó nhớ và không được thuận mắt phần
đa người dùng. Vì thế ta sẽ thực hiện các bước sau để tiến hành thay đổi
thông tin truy cập aaPanel theo ý mình.

**Cách 1: Thực hiện qua cửa sổ Terminal**

\- Ta login vào trang quản trị aaPanel thông qua link/user/pass đã được
cung cấp trong quá trình cài đặt (như ở trên).

\- Tại giao diện quản trị, ta truy cập Terminal, để hiển thị các thông
tin liên quan đến aaPanel, ta gõ **bt**

![](.//media/image10.png)


\- Đổi thông tin user, ta nhấn phím 6 (Change Panel username) rồi bấm
Enter, ta nhập thông tin user mới vào và tiếp tục nhấn Enter.

![](.//media/image11.png)


\- Đổi thông tin password, ta nhấn phím 5 (Change panel password) rồi
nhấn Enter => Nhập password mới => và bấm Enter

![](.//media/image12.png)


**Cách 2: Thực hiện thông qua trang quản trị aaPanel**

\- Tại giao diện quản trị các bạn truy cập Settings, tại đây ta sẽ thấy
các thông tin của aaPanel. Để đổi thông tin user/pass/port thì ta click
chọn vào Modify tương ứng để điều chỉnh, chỉnh sửa xong ta nhấn Save.

![](.//media/image13.png)
![](.//media/image14.png)


**4. Thay đổi Link truy cập**

\- Việc bạn chọn Y ở phần enable panel ssl khi cài đặt thì mặc định khi
truy cập aaPanel sẽ sử dụng giao thức HTTPS, điều này khiến người dùng
gắp cảnh báo bảo mật khi truy cập trên các trình duyệt.

![](.//media/image15.png)


\- Để tắt tính năng truy cập thông qua HTTPS, tại giao diện quản trị
aaPanel, ta truy cập Settings => bỏ tick Panel SSL => Confirms.

![](.//media/image16.png)


\- Tiếp tục truy cập Terminal và dán dòng lệnh dưới vào là hoàn tất

**rm -f /www/server/panel/data/admin_path.pl**

![](.//media/image17.png)


Như vậy ta có thể truy cập theo link dạng http://192.168.17.141:8888

**Tài liệu tham khảo**

https://huongdan.azdigi.com/cai-dat-aapanel-cho-vps/

https://huongdan.azdigi.com/huong-dan-doi-thong-tin-quan-tri-aapanel/
