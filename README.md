# arduinoRadio
Arduino Radio using by TEA5767

Reference : https://www.ardumotive.com/how-to-use-the-tea5767-fm-radio-module-en.html

## mBlock 확장 모듈 만들기 

http://download.makeblock.com/mblock/mblock_extension_guide.pdf

1. arduino용 C 소스 동작 확인
2. Demo Extension 설치 후 직접 해당 위치로 이동하여 파일수정 
* Mac : /Users/cnapman/Library/Application Support/com.makeblock.Scratch3.4.12/Local Store/mBlock/libraries
* Windows : 
3. 소스 수정 
* src : 블록 코딩에서 필요한 블록 작성 시 필요한 라이브러리의 cpp 소스 코드 
* js : 자바스크립트 소스로 스크래치에 바로 붙이는거 같긴 하지만 정확히 파악못함. 아두이노 업로드 형태로 사용할 경우는 필요없음. 
* *.s2e : 각 블록 마다 c 코드를 작성하여 블록 호출 시 마다 설정 할수 있는 함수 작성
4. 위 소스를 zip 파일로 압축 
5. mBlock Extension Center에 github 계정으로 로그인 
6. Drag and Drop 으로 4번에서 생성한 zip 파일 업로드 (동일한 파일이 있다면 버전 업데이트가 됨 )

## 예시 코드

* 9핀 입력 버튼을 누르면 상위 주파수를 SEEK 하고 
* 8핀 입력 버튼을 누르면 하위 주파수를 SEEK 한다. 
단, SEEK 기능은 주파수를 찾는 기능이기 때문에 난청 지역에서는 무한루프처럼 돌 수 있음. 

![tea5767_example](https://user-images.githubusercontent.com/8978613/68285637-fe666400-00c2-11ea-8ba8-253687213590.png)


