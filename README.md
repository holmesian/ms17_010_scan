# ms17_010_scan
ms17_010的批量扫描工具

因为Fuzzbunch的运行环境是Python2.6，所以[站在巨人的肩膀][1]上改了一个Python2.6的支持批量扫描ms17_010工具。

## 用法 ##


 - 扫单个IP

    python2 ms17_010_scan.py [single_ip]



>     $ python ms17_010_scan.py 192.168.206.152
>     [+] [192.168.206.152] is likely VULNERABLE to MS17-010! (Windows 7 Ultimate 7600)


 - 扫IP段



    python2 ms17_010_scan.py [start_ip] [end_ip]



>     $ python2 ms17_010_scan.py 192.168.206.1 192.168.206.254
>     [+] [192.168.206.152] is likely VULNERABLE to MS17-010! (Windows 7 Ultimate 7600)
>     [+] [192.168.206.153] is likely VULNERABLE to MS17-010! (Windows 7 Ultimate 7600)
>     [+] [192.168.206.154] is likely VULNERABLE to MS17-010! (Windows 7 Ultimate 7600)
>     ...


----------


另附一个FB上的现成的ms17010scan-h-n-amd64-1.exe工具

 - 扫单个IP

    ms17010scan-h-n-amd64-1.exe -h 192.168.1.1

 - 扫IP段

    ms17010scan-h-n-amd64-1.exe -n 192.168.1.0/24


  [1]: https://github.com/nixawk/labs/blob/master/MS17_010/smb_exploit.py
