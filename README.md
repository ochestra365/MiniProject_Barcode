# Barcode_Scan
회사에서 내려준 개인 프로젝트(2021.7.24)

-------------
<br>
##SUMMARY<br>
+ 이강산 과장님의 지시로 Barcode_Scan 프로젝트를 하게되었다.<br>
+ Flow Chart<br>
+ WBS<br>
<br>
고객사인 LG의 LQC공정에서 FixScanner 및 작업자가 GUN Scanner를 가지고 데이터를 취합한다.<br>
업무 프로세스를 습득을 위해 과제형으로 프로젝트를 내주셨다.<br>
목차
---------------<br>
1. TODO<br>
2. DOING<br>
3. DONE<br>
<br><br>

##1. TODO
-------------
1. 라즈베리파이 4 사기<br>
2. GUN Scanner 구매 혹은 동료 직원에게 협조 받기(TCP/Serial통신 방식으로 구현하기) or 포트 연결해서 읽기<br>
3. GIT-PRO 학습 및 GIT-Extension 학습하기(DEV_TEST 브랜치 만들기)<br>
4. 선보고 후조치(안하면 사유서 써야 함)<br>
5. 이전 전임자 GIT 연결 끊고, 내 GIT 연동하기.<br>

##2. DOING
-------------
1. DB 공부 및 프로시저 활용법 학습(DELETE랑 DROP은 1년간 쓰지 말 것.)<br>
2. SISMA 클래스 정의서 작성하기<br>
3. 신입사원 메뉴얼 VERSION_UP하기<br>

##3. DONE
-------------
<br>
1. 신입사원 메뉴얼 VERSION-1 작성(이강산과장님 지시)<br>
2. 회사 정보자산 보안<br>
3. XML 입출력 데이터생성 가능(개발자용 오픈소스 클로닝함)-->라이센스 명세화할 것.<br>



# barcodelib ![Barcode CI](https://github.com/barnhill/barcodelib/workflows/Barcode%20CI/badge.svg) [![NuGet](https://img.shields.io/nuget/v/BarcodeLib.svg)](https://www.nuget.org/packages/BarcodeLib)

### Overview ###
 
This library was designed to give an easy class for developers to use when they need to generate barcode images from a string of data.

|   Supported   |  Symbology    | List  |
| :------------- | :------------- | :-----|
| Code 128      | Code 93       | Code 39 (Extended / Full ASCII) |
| Code11        | EAN-8         | FIM (Facing Identification Mark) |
| UPC-A         | UPC-E         | Pharmacode   |
| MSI           | PostNet       | Standard 2 of 5 |
| ISBN          | Codabar       | Interleaved 2 of 5 |
| ITF-14        | Telepen       | UPC Supplemental 2 |
| JAN-13        | EAN-13        | UPC Supplemental 5 |

### Usage ###

The library contains a class called BarcodeLib with three constructors:
```csharp
Barcode();
Barcode(string);
Barcode(string, BarcodeLib.TYPE);
```

If you decide to create an instance with parameters, the parameters are as follows: the string is the data to be encoded into the barcode, and BarcodeLib.TYPE is the symbology to encode the data with. If you do not choose to specify the data and type at the time the instance is created, you may specify them through the appropriate property later on (but before you encode).

### Example ###
```csharp
BarcodeLib.Barcode b = new BarcodeLib.Barcode();
Image img = b.Encode(BarcodeLib.TYPE.UPCA, "038000356216", Color.Black, Color.White, 290, 120);
```

![Alt text](BarcodeStandard/examples/upca.jpg?raw=true "UPC-A")

### Support ###
If you find this or any of my software useful and decide its worth supporting.  You can do so here:  [![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=QKT9PSYTDNSXS)

### Copyright and license ###

Copyright 2007-2020 Brad Barnhill. Code released under the [Apache License, Version 2.0](https://github.com/bbarnhill/barcodelib/blob/master/LICENSE).
