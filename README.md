# exp5-蘇敬甯-3180100157 library使用說明#
<br>
##編譯說明注意事項:##
----------
作業目錄名稱為：exp5\_蘇敬甯\_3180100157

>可能因含有<font color="red">中文名字</font>，在編譯時可能因<font color="red">語系不同</font>造成路徑<font color="red">error</font>無法編譯，若遇此問題,可以將目錄名稱改為exp5_3180100157，並將library\_1目錄下的<font color="red">.project檔</font>以notepad開啟後，改為exp5\_3180100157，再Import即可順利進行編譯。


----------
##編譯環境建置：##

----------

####依下列步驟建置database及開發環境####

1.在mysql建置database及table，其sql語法為：
   <ul>
   <li>create database exp5_library;
   <li>create table book(bno char(10),category	varchar(10),title varchar(20),press	varchar(20),year int,author varchar(10),price decimal(7,2),total int,stock int,primary key(bno));
   <br>create table card(cno char(7),name varchar(10),department varchar(40),type char(1),primary key(cno),check(type in('T','S')));
   <li>create table borrow(cno char(7),bno char(8),borrow_date int,return_date int,primary key(cno,bno),foreign key (cno) references card(cno),foreign key (bno) references book(bno));
  </ul>

2.安裝Eclipse IDE 時選擇Eclipse IDE for Java Developers進行安裝
 <div align=center><img src="image/1.png" width="500"></div>

3.Eclipse 之window下選擇Eclipse Marketplace 找到window builder開發工具進行安裝

  <div align=center><img src="image/2.png" width="450"></div>

4.本環境建置時使用C:\Program Files (x86)\MySQL\Connector J 8.0\mysql-connector-java-8.0.19.jar连接数据库；
 <br>本次使用JDBC及mysql-connector-java-8.0.19.jar作為database的連接,在代碼中需將Class.forName("com.mysql.jdbc.Driver")改為Class.forName("com.mysql.cj.jdbc.Driver")。

5.代碼內容在 src/library1/HomePage.java

----------
##編譯運行的流程##
----------
####依下列步驟建置database及開發環境####
1.Import檔案

> 開啟Eclipse 選擇file->Import->general->existing projects into workspace->選擇exp5_蘇敬甯_3180100157 點擊Import檔案到Eclipse編譯器

2.設定數據庫連線

> Import檔案完成後,選擇src/library/HomePage.java 在75-77行設定連接mysql的數據庫名稱dbname,使用者dbuser,以及密碼dbpass。

3.window設計界面

> 若要以window builder進行設計,可以選擇src/library/HomePage.java後按mouse右鍵選擇open with WindowBuilder Editor進行設計

3.產生可執行的jar檔

> 編譯無誤後，點擊File->export->選擇java->選擇Runnable Jar file->輸出jar檔。

4.下載
[launch4j-3.12-win32](https://osdn.net/projects/sfnet_launch4j/downloads/launch4j-3/3.12/launch4j-3.12-win32.exe/)製成exe檔
> 下載檔案解壓縮後，執行launch4j.exe<br>
> 設定Output file <br>
> 選擇上一步驟產的的Jar檔 <br>
> 選擇Icon圖(可不選)<br>
> 切換上方功能至JRE，輸入Min JRE version <br>
> 選擇![](image\wheel.png) 即可產生exe檔
> 

## ##

**MarkdownPad** is a full-featured Markdown editor for Windows.2312

### Built exclusively for Markdown ###

Enjoy first-class Markdown support with easy access to  Markdown synasdtax sadsaand convenient keyboard shortcuts.

Give them a try:

- **Bold** (`Ctrl+B`) and *Italic* (`Ctrl+I`)
- Quotes (`Ctrl+Q`)
- Code blocks (`Ctrl+K`)
- Headings 1, 2, 3 (`Ctrl+1`, `Ctrl+2`, `Ctrl+3`)
- Lists (`Ctrl+U` and `Ctrl+Shift+O`)

### See your changes instantly with LivePreview ###

Don't guess if your [hyperlink syntax](http://markdownpad.com) is correct; LivePreview will show you exactly what your document looks like every time you press a key.

### Make it your own ###

Fonts, color schemes, layouts and stylesheets are all 100% customizable so you can turn MarkdownPad into your perfect editor.

### A robust editor for advanced Markdown users ###

MarkdownPad supports multiple Markdown processing engines, including standard Markdown, Markdown Extra (with Table support) and GitHub Flavored Markdown.

With a tabbed document interface, PDF export, a built-in image uploader, session management, spell check, auto-save, syntax highlighting and a built-in CSS management interface, there's no limit to what you can do with MarkdownPad.
