---
layout: post
title:  "Sử dụng tên miền tuỳ chỉnh cho blog Jekyll"
categories: 
  - jekyll
  - blog
tags:
  - jekyll
  - domain
img: Adding Custom Domain.png
---

Ở bài trước mình có hướng dẫn về cách tạo 1 blog sử dụng Jekyll

Nhưng tên miền mặc định của trang blog bạn sẽ là: `<username>.github.io`. Trong bài viết này, mình sẽ hướng dẫn cách tuỳ chỉnh tên miền riêng của bạn.

**Yêu cầu:**

-   1\. Trang web tĩnh đang host trên github.
-   2\. Tên miền riêng của bạn đã mua từ trước.

1\. Tạo file CNAME
------------------

Đầu tiên bạn hãy vào repository của chính blog/website bạn đã tạo, click vào Create new file.

![Sử dụng tên miền tuỳ chỉnh cho blog Jekyll](https://caodem.com/wp-content/uploads/image-11-1024x279.png)

Bạn hãy đặt tên file là CNAME.

![Sử dụng tên miền tuỳ chỉnh cho blog Jekyll](https://caodem.com/wp-content/uploads/image-12.png)

Nội dung trong file sẽ là tên miền tuỳ chỉnh của bạn.

![Sử dụng tên miền tuỳ chỉnh cho blog Jekyll](https://caodem.com/wp-content/uploads/image-13.png)

Save & commit lại file luôn nhé. Ở đây là coi như xong bước đầu tiên.

2\. Trỏ tên miền về Github.
---------------------------

Các bạn vào trang quản lý tên miền mà các bạn đã mua của nhà cung cấp dịch vụ.

Để bắt đầu, chúng ta hãy truy cập DNS và tạo 2 bản ghi A như thế này:

```
Host: @
Points to: 192.30.252.153
```

```
Host: @
Points to: 192.30.252.154
```

Sau khi tạo xong record thì bạn hãy chờ DNS cập nhật. Có thể mất tầm 5 -- 10 phút. Hãy kiên nhẫn nhé.

3\. Cấu hình tên miền Jekyll
----------------------------

Sau khi đã trỏ xong tên miền về Github, bạn hãy vào lại repository của bạn.

Vào file `_config.yml` tìm đến dòng: `url:<yourdomain>.com`

Sửa `<yourdomain>` thành tên miền riêng của bạn ban đầu lúc add vào CNAME.

Truy cập tên miền của bạn và sẽ thấy sự thay đổi.

Bonus: Kích hoạt SSL
--------------------

Đối với tên miền ở bên ngoài, Github sẽ không hỗ trợ SSL. Nếu như bạn muốn sử dụng SSL cho tên miền riêng, thì hãy [trỏ tên miền về CloudFlare ](https://canhme.com/kinh-nghiem/huong-dan-su-dung-cloudflare/). Rồi vào phần DNS để tuỳ chỉnh lại bản ghi như trên.

![Sử dụng tên miền tuỳ chỉnh cho blog Jekyll](https://caodem.com/wp-content/uploads/image-14.png)

![Sử dụng tên miền tuỳ chỉnh cho blog Jekyll](https://caodem.com/wp-content/uploads/image-15-1024x246.png)

Tạm kết
-------

Trỏ tên miền riêng về Github về cơ bản là dễ. Hy vọng qua bài viết này, các bạn có thể tìm thấy sự hứng thú của Jekyll và những bài viết của mình. Tks for reading.