# cvechecker介绍

## 快速入门

```
Initalize the SQLite3 Database
# cvechecker -i


Load CVE and version matching rules
# pullcves pull

Generate List of Files to scan
$ find / -type f -perm -o+x > scanlist.txt
$ echo /proc/version >> scanlist.txt

Gather List of Installed Software/Versions
$ cvechecker -b scanlist.txt

Output Matching CVE Entries
$ cvechecker -r

More detailed installation information available via the installation docs.
```

## 更新历史

```
The changelog for the cvechecker tool is available through the git commit log.

Up to the 3.8 release a manual ChangeLog file was in use (alongside the git commit log since the use of Git). This one will not be maintained anymore and is kept for historical reference.

Release history:

2020/07/26 - cvechecker 4.0
2018/09/09 - cvechecker 3.9
2017/03/27 - cvechecker 3.8
2017/03/01 - cvechecker 3.7
2015/11/07 - cvechecker 3.6
2013/09/30 - cvechecker 3.5
2013/09/17 - cvechecker 3.4
2013/09/16 - cvechecker 3.3
2012/11/25 - cvechecker 3.2
2011/04/13 - cvechecker 3.1
2011/04/12 - cvechecker 3.0
2010/12/01 - cvechecker 2.0
2010/10/01 - cvechecker 1.0
2010/09/08 - cvechecker 0.6
2010/09/02 - cvechecker 0.5
2010/08/25 - cvechecker 0.4
2010/08/20 - cvechecker 0.3
2010/08/16 - cvechecker 0.2
2010/08/14 - cvechecker 0.1
```



## 代码统计

```
     103 text files.
      95 unique files.                              
      47 files ignored.

github.com/AlDanial/cloc v 1.90  T=0.14 s (421.5 files/s, 180991.6 lines/s)
--------------------------------------------------------------------------------
Language                      files          blank        comment           code
--------------------------------------------------------------------------------
Bourne Shell                      9            943           1163           6897
XML                              12            960             12           3678
HTML                              5            315              0           3606
C                                 7            556            603           3264
m4                                2            155            152           1258
C/C++ Header                      8            140            141            304
XSLT                              2             29              4            243
SQL                               1             15             24            117
Perl                              1             13             32             88
make                              6             13              1             66
Bourne Again Shell                1              4              0             40
CSS                               1              0              1             32
Markdown                          1              7              0             19
awk                               1              0              0              9
YAML                              1              0              0              1
--------------------------------------------------------------------------------
SUM:                             58           3150           2133          19622
--------------------------------------------------------------------------------
```


## rpm信息


```
[root@cvechecker-docker-fedora36 ~]# rpm -qi --changelog cvechecker
Name        : cvechecker
Version     : 4.0
Release     : 5.fc36
Architecture: x86_64
Install Date: Mon Dec 19 16:20:09 2022
Group       : Unspecified
Size        : 197842
License     : GPLv3
Signature   : RSA/SHA256, Thu Jan 20 09:32:59 2022, Key ID 999f7cbf38ab71f4
Source RPM  : cvechecker-4.0-5.fc36.src.rpm
Build Date  : Thu Jan 20 08:16:04 2022
Build Host  : buildvm-x86-17.iad2.fedoraproject.org
Packager    : Fedora Project
Vendor      : Fedora Project
URL         : https://github.com/sjvermeu/cvechecker
Bug URL     : https://bugz.fedoraproject.org/cvechecker
Summary     : Tool for compare packages installed in your system with CVE database
Description :
The goal of cvechecker is to report about possible vulnerabilities on your
system, by scanning a list of installed software and matching results with the
CVE database.
This is not a bullet-proof method and you will have many false positives
(i.e.: vulnerability is fixed with a revision-release, but the tool isn't able
to detect the revision itself).
* Thu Jan 20 2022 Fedora Release Engineering <releng@fedoraproject.org> - 4.0-5
- Rebuilt for https://fedoraproject.org/wiki/Fedora_36_Mass_Rebuild

* Wed Jul 21 2021 Fedora Release Engineering <releng@fedoraproject.org> - 4.0-4
- Rebuilt for https://fedoraproject.org/wiki/Fedora_35_Mass_Rebuild

* Tue Jan 26 2021 Fedora Release Engineering <releng@fedoraproject.org> - 4.0-3
- Rebuilt for https://fedoraproject.org/wiki/Fedora_34_Mass_Rebuild

* Tue Sep 29 2020 Zamir SUN <sztsian@gmail.com> - 4.0-2
- Add jq to requires

* Sat Sep 26 2020 Zamir SUN <sztsian@gmail.com> - 4.0-1
- Update to 4.0

* Mon Jul 27 2020 Fedora Release Engineering <releng@fedoraproject.org> - 3.8-9
- Rebuilt for https://fedoraproject.org/wiki/Fedora_33_Mass_Rebuild

* Tue Jan 28 2020 Fedora Release Engineering <releng@fedoraproject.org> - 3.8-8
- Rebuilt for https://fedoraproject.org/wiki/Fedora_32_Mass_Rebuild


```

```
[root@cvechecker-docker-fedora36 ~]# rpm -ql cvechecker
/etc/cvechecker.conf
/usr/bin/cvechecker
/usr/bin/cvegenversdat
/usr/bin/cvereport
/usr/bin/cverules
/usr/bin/pullcves
/usr/lib/.build-id
/usr/lib/.build-id/41
/usr/lib/.build-id/41/982c0d7fc6e47cd12d5635746004783aa158ae
/usr/share/cvechecker
/usr/share/cvechecker/csv2xml.awk
/usr/share/cvechecker/cvereport.xsl
/usr/share/cvechecker/mysql_cvechecker.sql
/usr/share/cvechecker/report.css
/usr/share/doc/cvechecker
/usr/share/doc/cvechecker/ChangeLog
/usr/share/doc/cvechecker/README.md
/usr/share/doc/cvechecker/acknowledgements.html
/usr/share/doc/cvechecker/userguide.html
/usr/share/man/man1/cvechecker.1.gz
/usr/share/man/man1/cvegenversdat.1.gz
/usr/share/man/man1/cvereport.1.gz
/usr/share/man/man1/cverules.1.gz
/usr/share/man/man1/pullcves.1.gz
/var/lib/cvechecker/cache
/var/lib/cvechecker/local
[root@cvechecker-docker-fedora36 ~]#
```








---
