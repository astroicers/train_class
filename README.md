開始吧!
===
1. 首先希望大家都可以擁有自己的[GitHub](https://github.com/)和[Docker Hub](https://hub.docker.com/)，這樣以後共同開發會方便很多<br>
2. 下方資料部分參考下方所有連結
3. 一切教學皆為學術目的
---
目錄
* [網路攻擊](#網路攻擊)
    * [網路滲透作業系統(Kali Linux)](#一網路滲透作業系統kali-linux)
    * [搜尋引擎滲透(Google Hacking)](#二搜尋引擎滲透google-hacking)
    * [SQLMap使用攻略](#三sqlmap使用攻略)
* [程式開發](#程式開發)
    * [基礎程式語言(python)](#一基礎程式語言python)
* [虛擬化](#虛擬化)
    * [基礎虛擬化技術(Docker)](#一基礎虛擬化技術docker)
    * [基礎虛擬化技術(VMware)](#二基礎虛擬化技術vmware)
* [資料庫](#資料庫)
    * [基礎資料庫(Mongo)](#一基礎資料庫mongo)
    * [基礎資料庫(MySQL)](#二基礎資料庫mysql)
* [作業系統](#作業系統)
    * [Linux(Ubuntu)](#一linuxubuntu)
---
# 網路攻擊

## 一、網路滲透作業系統(Kali Linux)
* [Kali Linux 官方](https://www.kali.org/)
  - 下載Kali
* [Docker版 Kali Linux](https://hub.docker.com/r/kalilinux/kali-linux-docker/)
  - 如果常用Docker的人可以試試，但工具部分沒有其他版本那麼齊全
### 小問題
* 如何開啟Kail後自動登入桌面
  - 輸入 `vi /etc/gdm3/daemon.conf`
  - 將 `#AutomaticLoginEnable = True` 和 `#AutomaticLogin = root` 的 # 刪除
* 如何設定SSH遠端登入
  - 輸入 `vi /etc/rc.local`
  - 增加 `/etc/init.d/ssh start`
  - 輸入 `vi /etc/ssh/sshd_config`
  - 修改 `PermitRootLogin without-password` 為 `PermitRootLogin yes`
---
## 二、搜尋引擎滲透(Google Hacking)
* [宅學習 - Social Learning Space](https://sls.weco.net/node/12922)
  - 裏頭有非常多常用的手法可以應用在滲透上
* [GoogleHacking基礎](http://www.vixual.net/blog/archives/152)
  - 裏頭有非常多常用的手法可以應用在滲透上
* [exploit-db實戰範例](https://www.exploit-db.com/google-hacking-database/)
  - 裏頭有非常多常用的手法可以應用在滲透上
* [信息收集篇————Google Hacking](https://blog.csdn.net/Fly_hps/article/details/79404270)
  - 裏頭有非常多常用的手法可以應用在滲透上
* 基礎指令介紹
  - site: (搜尋特定網址)
  - inurl: (搜尋特定連結)
  - intext: (搜尋網頁內文字)
  - intitle: (搜尋網頁標題)
  - filetype  |  ext  : (搜尋特定檔案格式)
  - link: (搜尋互相連結的網頁)
  - cache: (顯示網頁在Google中的暫存資料)
  - info: (列出某網站在Google上存有哪些資訊)
* 常用指令集
  - inurl:admin
  - inurl:phpinfo.php
  - intitle:index of 學生證
---
## 三、SQLMap使用攻略
* [官方網站](http://sqlmap.org/)
* [GitHub SQLMap 下載地址](https://github.com/sqlmapproject/sqlmap/zipball/master)
* [執行範例](https://asciinema.org/a/46601)
* [教學](http://www.youtube.com/user/inquisb/videos)
* [SQL使用參數詳解](https://hk.saowen.com/a/07f782066171d02ac489ab396b666257d4a556a76fd94d40195a5fd8eafa5f1f)
* sqlmap簡介
  * sqlmap支持MySQL, Oracle,PostgreSQL, Microsoft SQL Server, Microsoft Access, IBM DB2, SQLite, Firebird,Sybase和SAP MaxDB等數據庫的各種     安全漏洞檢測。sqlmap支持五種不同的注入模式：
    - 基於布爾的盲注，即可以根據返回頁面判斷條件真假的注入；
    - 基於時間的盲注，即不能根據頁面返回內容判斷任何信息，用條件語句查看時間延遲語句是否執行（即頁面返回時間是否增加）來判斷；
    - 基於報錯注入，即頁面會返回錯誤信息，或者把注入的語句的結果直接返回在頁面中；
    - 聯合查詢注入，可以使用union的情況下的注入；
    - 堆查詢注入，可以同時執行多條語句的執行時的注入。
* 下載及安裝
  * linux下git直接安裝
    - 輸入指令 `gitclone –depth 1 https://github.com/sqlmapproject/sqlmap.git sqlmap-dev`
  * windows下安裝
    - windows下下載sqlmap的壓縮包，解壓後即可使用。但需要一些組件包的支持，需要有python2.7.x或者2.6.x環境支持。
  * kali及PentestBox默認安裝sqlmap
---
# 程式開發

## 一、基礎程式語言(python)
* [Python官方](https://www.python.org/)
  - 下載python
* [菜鳥教程](http://www.runoob.com/python/python-tutorial.html)
  - 不必看完，但要用的時候找的到
* [程式語言教學誌](http://kaiching.org/pydoing/python.html)
  - 不必看完，但要用的時候找的到
* [Python 基础入門教程](https://alleniverson.gitbooks.io/python2-course/content/)
  - 不必看完，但要用的時候找的到
* [《跟老齊學Python》（入門教程）](https://normanbb.gitbooks.io/test/content/)
  - 資料庫與EXCEL檔案的部份寫的很清楚，其他部份也相當完整
* [python 安全编程教程](https://wizardforcel.gitbooks.io/py-sec-tutorial/content/index.html)
  - 與滲透測試較有關係，算是較進階的部份
### 第三方函式庫

#### Flask
* [Flask官方](http://flask.pocoo.org/)
  - 裏頭有所有的函式和最詳細的資料。
* [Flask Web 開發入門](https://funhacks.gitbooks.io/head-first-flask/content/)
  - 快速簡單的學習用flask建立網頁。
* [Flask大型教程項目](http://flask-mega-tutorial.readthedocs.io/zh_CN/latest/index.html)
  - 詳細的講解關於flask的用法。
* []()
  - 

#### Selenium
* [Selenium官方](https://www.seleniumhq.org/)
  - 裏頭有所有的函式和最詳細的資料。
* [PYPI selenium](https://pypi.org/project/selenium/)
  - 含有此第三方函式庫的Doc與GitHub等連結
* [GitHub webdriver實用指南python版本](https://wangxiwei.gitbooks.io/webdriver-python/content/)
  - 裏頭有關於安裝環境、針對瀏覽器的控制與上傳和下載檔案
#### Paramiko
* [Paramiko官方](http://www.paramiko.org/)
  - 裏頭有所有的函式和最詳細的資料。
* [PYPI paramiko](https://pypi.org/project/paramiko/)
  - 含有此第三方函式庫的Doc與GitHub等連結
* [GitHub Paamiko](https://github.com/paramiko/paramiko)
  - 含所有的程式碼更新與原始碼。
* [GitBook python Paramiko(模仿SSH交互且執行指令)](http://python.jqlinux.com/pythonchang-yong-di-san-fang-3001-nei-zhi-mo-kuai/python-paramikomo-fang-ssh-deng-lu-zhi-xing-ming-4ee429.html)
  - 如標題，內容主要為SSH連線相關範例。
### 小問題
* pip安裝
  * windows
    - 下載[get-pip.py](https://bootstrap.pypa.io/get-pip.py)
    - 開啟cmd執行 `python get-pip.py`
    - 最後加入 `C:\Python27\Scripts` 到環境變數中
  * ubuntu 16.04 LTS
    - 輸入指令`sudo apt-get update && sudo apt-get -y upgrade`
    - 輸入指令`sudo apt-get install python-pip`
* pip Import Error:cannot import name main解决方案
  - [CSDN 代碼人生]https://blog.csdn.net/tintinetmilou/article/details/80091630
### 測驗
    請練習菜鳥教程-100例中第1、3、8、24、26、32、34、61、71、83、85、88、97和100題。
---
# 虛擬化

## 一、基礎虛擬化技術(Docker)
* [Docker —— 從入門到實踐](https://philipzheng.gitbooks.io/docker_practice/content/)
  - 請看完 Docker簡介、基本概念、安裝、映像檔、容器、倉庫和Dockerfile，其他不必看完，但要用的時候找的到
* [Docker Hub](https://hub.docker.com/)
  - 目前由Docker官方維護的公共倉庫 Docker Hub，且Docker Hub 中可直接下載他人或官方的映像檔來使用
* [docker docs-Get Docker CE for Ubuntu](https://docs.docker.com/install/linux/docker-ce/ubuntu/#install-docker-ce-1)
  - 目前docker更新到docker-ce的部份，docker.io和docker-engine皆為較舊之版本，安裝看這
* [Docker — 從入門到實踐-Docker Compose 项目](https://yeasy.gitbooks.io/docker_practice/content/compose/)
  - 學會單一容器的操作後，再來就是compose了，必學
* [docker docs-Install Docker Compose](https://docs.docker.com/compose/install/#install-compose)
  - 這是關於docker-compose的官方安裝說明文件，安裝看這
### 小問題
* 關於Docker下的alpine
  - alpine原本並沒有bash，所以要遠端登入時可使用sh來遠端登入
* docker-compose up leads to “client and server don't have same version” error but client and server have the same version
  - https://cutejaneii.wordpress.com/2017/06/19/docker-8-%E5%8D%87%E7%B4%9Adocker/
### 測驗
    請使用Docker建立一個FTP伺服器在Ubuntu中
---
## 二、基礎虛擬化技術(VMware)
* [VMware官方](https://www.vmware.com)
  - 下載VMware(有付費版及免費版)
* [虛擬機器VMware Workstation Pro 14下載與安裝](http://blog.xuite.net/yh96301/blog/63322621-%E8%99%9B%E6%93%AC%E6%A9%9F%E5%99%A8VMware+Workstation+Pro+14%E4%B8%8B%E8%BC%89%E8%88%87%E5%AE%89%E8%A3%9D)
  - 此篇Blog有關於下載與安裝的介紹等
### 小問題
* 於Ubuntu 中 VMtools 跳出錯誤訊息 VMware Tools installation cannot be started manually while Easy Install is in progress.
  - 開啟terminal執行 `sudo apt -y --reinstall install open-vm-tools-desktop fuse`
* 版本不相同而導致無法開啟
  - 只需用記事本打開虛擬機目錄下的 .vmx 文件，並將 virtualHW.version ="7" 中的數字改為虛擬機的版本即可。
---
# 資料庫

## 一、基礎資料庫(Mongo)
* [DockerHub mongo](https://hub.docker.com/_/mongo/)<br>
  - 裏頭有關於mongo與mongo-express的compose.yml，如果你已經學會docker，非常建議直接使用。
* [mongo 入門指南](https://jockchou.gitbooks.io/getting-started-with-mongodb/content/)
  - 簡單且完整教學，主要是如何操作mongo的基本指令，實用性非常高，必看也必會。
* [MongoDB 學習教程](https://piaosanlang.gitbooks.io/mongodb/content/)
  - 較為進階，有很多關於其他資料庫的比較，如果要深入mongodb，這個gitbook很值得參考。
### 小問題
* 跳出錯誤訊息 not authorized on admin to execute command { listDatabases: 1.0, $db: \"admin\" }
  - 輸入指令 `mongo`
  - 輸入指令 `use admin`
  - 輸入指令 `db.auth('root','example')`
---
## 二、基礎資料庫(MySQL)
* [MySQL 超新手入門（1）重新開始](http://www.codedata.com.tw/database/mysql-tutorial-getting-started)
  - 這是新手必看的Blog，整理的很完整了。
* [MySQL基礎筆記](https://cxiaodian.gitbooks.io/mysql/content/index.html)
  - 安裝、設定到基礎SQL語法都很完整。
* [mysql5.7官方文檔翻譯](https://404dream.gitbooks.io/mysql/content/)
  - 翻譯官方文件的第四和五章的部分，不想看英文的可以來看看。
### 小問題
* 跳出錯誤訊息 mysql ERROR 1130: Host '*****' is not allowed to connect to this MySQL server
  - [宇若彎彎-連接遠端MYSQL ERROR 1130解決辦法](http://s90304a123.pixnet.net/blog/post/39306139-mysql-error-1130)
---
# 作業系統

## 一、Linux(Ubuntu)

### 小問題
* 如何安裝中文輸入法
  - [軟體使用教學Ubuntu 16.0.4新增中文輸入法-新酷音輸入法](http://blog.xuite.net/yh96301/blog/342227672-Ubuntu+16.0.4%E6%96%B0%E5%A2%9E%E4%B8%AD%E6%96%87%E8%BC%B8%E5%85%A5%E6%B3%95-%E6%96%B0%E9%85%B7%E9%9F%B3%E8%BC%B8%E5%85%A5%E6%B3%95)
### 開發中...
