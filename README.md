# b4x20220313
B4X實驗: 利用B4JPackager11打包Windows應用程序 (B4J)..Inno Setup 構建獨立安裝包

B4X實驗: 利用B4JPackager11打包Windows應用程序 (B4J)..Inno Setup 構建獨立安裝包
參考資料:
https://www.b4x.com/android/forum/threads/b4jpackager11-the-simplest-way-to-distribute-ui-apps.99835/
https://www.b4x.com/android/forum/threads/solved-win-10-64-bit-java-11-cannot-run-jar-file.105016/#content
https://www-b4x-com.translate.goog/android/forum/threads/integrated-b4jpackager11-the-simple-way-to-distribute-standalone-ui-apps.117880/?_x_tr_sl=auto&_x_tr_tl=zh-TW&_x_tr_hl=zh-TW

0.c:\java\jdk-11.0.1\bin\java.exe -jar gCodeSplit.jar
出現這個錯誤提示 Error: JavaFX runtime components are missing, and are required to run the application.

B4X openJDK 11
>>>Java 11 doesn't support executable jars (for UI apps). You need to use B4JPackager11 to create an package with an embedded Java.
>>>Java 11 無法執行jars(UI APP),請用b4jpackager11打包程式.打包後再去執行

參考: https://www.b4x.com/android/forum/threads/solved-win-10-64-bit-java-11-cannot-run-jar-file.105016/#content



1.執行打包的設定... 
You have two options:
a. Create a json file and run the tool from the command line.  

packager.json
{
  "InputJar": "d:/t61.jar"
}

執行打包...執行時會刪暫存目錄..指令/參數 都要加入路徑  
c:\java\jdk-11.0.1\bin\java -jar d:\B4JPackager11.jar d:\packager.json


b. Set the variable directly (Process_Globals):   專案 B4JPackager11
Private InputJar As String = "d:/t61.jar" 'change as needed


2.
請先準備一個新專案..並且編譯好jar...

執行打包...執行時會刪暫存目錄..指令/參數 都要加入路徑
c:\java\jdk-11.0.1\bin\java -jar d:\B4JPackager11.jar d:\packager.json




3.如何除錯
run_debug.bat

4.Inno Setup解說

5.安裝..執行看看



99.進階==>自己摸索了喔!!!

