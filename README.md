# CryptoHelper
Simple jars to do some simple crypto stuff. Nothing but a homework of java 
Parameters format:
[1]UI(CryptoHelper.exe)
  #1 Rot13:input cipher/plaint text directly
  example: admin -> nqzva
  #2 Caser:number(key in Caesar)+text(to encode/decode)<br>
  example:<br> 
	13 admin -> nqzva<br>
  #3 Fence:number(key in Fence)+text(to encode/decode)<br>
  example:<br> 
	3 admin -> amndi<br>
  3 amndi -> admin<br>
  #4 Vigenere<br>
  encode/decode:words(key in Vigenere)+text(to encode/decode)<br>
  example: <br> admin admin -> agyqa <br>
           admin agyqa -> admin<br>
  break1: <br> Enumerate key to decode, using a dictionary to test whether the "plaint" is valid.<br>
          It takes a lot of time(1 minute?) for we don't use any optimization.<br>
          just input ciphertext directly.(short ciphertext recommended)<br>
  example: <br> qeglx wjrud ohrs ds namtq -> hello world this is earth <br>
  break2: <br> Using word frequency analysis which is difficult to explain here.<br>
          You can have an introduction at https://en.wikipedia.org/wiki/Vigen%C3%A8re_cipher<br>
          just input ciphertext directly just like break1.(long ciphertext recommended)<br>
          You can find long cipher in testcipher.txt.<br>
  #5 decode<br>
          just input ciphertext directly.<br>
          Moss cipher need interupt by "/"<br>
  example:<br>
          .-/-../--/../-./ -> admin<br>
          YWRtaW4= -> admin<br>
          61646D696E -> admin<br>
  #6 hill<br>
          3 letters to encode or decode only.<br>
          wow -> mym<br>
          mym -> wow<br>
  #7 Zip  identify whether a zip file is pseudo encrypted and repair it if so.<br>
          You're suppose to put the zip file in the same directory.<br>
[2]CMD<br>
  There isn't big difference from UI to CMD.<br>
  Some funtions just need an extra 0/1 at the beginning to specify encoding or decoding.<br>
  java -jar Caser.jar 1 13 admin  ->  nqzva<br>
  java -jar fence.jar 1 3 admin  ->  aidnm<br>
  java -jar hill.jar 1 wow  ->  mym<br>
  java -jar Rot13.jar 1 admin  ->  nqzva<br>
  java -jar vigenere.jar 0 admin admin  ->  agyqa<br>
  java -jar vigenere.jar 1 admin agyqa  ->  admin<br>
  java -jar ZipCenOp.jar -r flag.zip  ->  success 1 flag(s) found<br>
![image](https://github.com/RicardoNacanda/CryptoHelper/blob/master/runtime.png）
