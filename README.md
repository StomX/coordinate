# Image coordinates generator?
일반적으로 프로모션 마크업 시, 이미지 속 링크 영역의 위치값을 지정하기 위해<br>
아래 사진과 같이 position:absolute 속성값을 주고 top, right, bottom, left 좌표값,
그리고 width, height 값을 적용하는데요.

*[예시] PC 프로모션*

![](http://thisisneverthat.dothome.co.kr/study/img/1.jpg)



이 때 필요한 좌표값을 구하기 위해,<br>
포토샵에서 링크 영역을 찾아서 계산기로 직접 구하거나<br>
별도 프로그램(예: Humming bird)을 사용하여 구하는 방법 등이 있지만<br>
구하는 과정에서, 적지 않은 시간이 할애되지요.

 
    +) 요한선임님께서 이전에 공유해주셨던 방법도 있습니다. (이미지맵 코드값 필요)
    https://home.worksmobile.com/main/article/206796030725
 


특히, 반응형 모바일 프로모션일 경우<br>
좌표값의 단위를 px(픽셀)이 아닌 %(퍼센트)로 지정해주어야 하기 때문에<br>
직접 변환을 하는 작업이 추가로 필요합니다. (아래 예시 참고)


- - -

**[예시] 반응형 모바일 프로모션 작업시, 좌표값 구하는 과정**
 
예를 들어, 아래와 같은 프로모션 이미지 속 '혜택 자세히 보기' 버튼의 링크영역을 잡을 경우<br>
버튼영역의 좌표값을 구하기위해 아래와 같은 계산이 필요합니다.

    - 이미지 전체 사이즈 : 750px(가로) x 1240px(세로)
    - 버튼영역 : 588px(가로) x 112px(세로)
 
width는 (588/750) * 100이 되고... height는 (112/1240) * 100..<br>
그외 top, right, bottom, left값도 계산이 필요하게되기 때문에 굉장히 비효율적이지요.

![](http://thisisneverthat.dothome.co.kr/study/img/2.jpg)

 
 
이와 같은 비효율적인 시간을 조금이라도 줄여보자는 생각으로<br>
최대한 간단하게! 좌표를 구할 수 있는 생성툴을 제작하게 되었습니다.
 
 
 
 
 
 
 
 
## How to use

    이미지 좌표 생성툴 ▼
    https://goo.gl/WpTHGK
 
 
1) 위의 URL을 브라우저로 연 후, (크롬, IE10+, Firefox) 

![](http://thisisneverthat.dothome.co.kr/study/img/3.png) 



2) 작업하는 프로모션이 PC 프로모션인지, 모바일 프로모션인지 선택합니다.<br>
모바일 선택 시, 생성될 좌표값의 소수점자리값을 지정할 수 있습니다.<br>
*예를 들어 “ 4 “ 입력시, 좌표값은 33.3333%이 출력됨.*

![](http://thisisneverthat.dothome.co.kr/study/img/4.gif) 






3) 원하는 프로모션 이미지를, 아래 사진과 같이 드래그 합니다.<br>
 *이미지 파일(jpg, png 등)의 형식이 아닌 파일을 드래그하면 오류창이 뜸.*

![](http://thisisneverthat.dothome.co.kr/study/img/5.gif) 






4) 링크영역의 **시작점**과 **끝점**을 각각 클릭합니다. (드래그 X)

* 클릭 방향은 자유롭게 가능함. ( ↘ ↗ ↖ ↙ )
* 시작점 클릭 후, ESC키를 눌러서 시작점을 재설정할 수 있음.

![](http://thisisneverthat.dothome.co.kr/study/img/6.gif) 





5) 지정한 영역의 좌표값이 순서대로 생성됩니다.

![](http://thisisneverthat.dothome.co.kr/study/img/7.gif) 
 
 

6) COPY 버튼을 클릭하여, 생성된 좌표값을 복사합니다.

![](http://thisisneverthat.dothome.co.kr/study/img/8.gif) 



7) 복사된 좌표값을, 버튼영역에 해당하는 클래스 CSS에 ‘붙여넣기’를 하면 끝!

![](http://thisisneverthat.dothome.co.kr/study/img/9.gif) 
 
 
 
이상입니다.


