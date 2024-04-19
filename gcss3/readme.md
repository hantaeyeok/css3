# CSS 란?

- CSS(Cascading Style Sheet) 라고도 하며, 줄여서 스타일(Style)이라고도 한다.
- Cascading(계단식) Style(모양) Sheet(기록패널) 이라는 뜻으로 스타일 지정시 선택자를 범위를 큰 것에서 부터 작은 순으로 지정을 계단식으로 한다고 해서 붙여진 이름입니다.

------------------------------------------------------------------------

<br><br>

## 1. CSS 적용 방법과 기본 문법

### 1-1. 외부 스타일(External Style)

- 별도의 css 파일을 생성하여 여러 HTML 문서에서 link 요소로 적용하는 방법
```html
    <link rel="stylesheet" href="서식파일이름.css">
```

<br><br>

### 1-2. 내부 스타일(Internal Style)

- 현재 문서에 있는 요소(Element)에만 스타일을 적용하는 방법
- 현재 문서 내 style 요소의 안에 스타일 내용을 기재하는 방법
```html
    <style>
    /* 내부 스타일 */    
    </style>
```
<br><br>

### 1-3. 인라인 스타일(Inline Style)

- 해당 요소에 직접 스타일을 적용하는 방법
- 해당 요소에 style 속성(attribute)에 직접 지정하는 방법으로서 재사용성이 가장 좋지 않지만, 다른 스타일 지정 방식보다는 우선 순위가 가장 빠르다.

```html
    <h3 style="color:red">제목</h3>
```

------------------------------------------------------------------------

<br><br>

### 1-4. CSS 기본 문법

![CSS기본문법](style_rule.png)

<br>

------------------------------------------------------------------------

<br><hr><br>

## 2. CSS 선택자


| 선택자 이름 | 선택자 문법 | 설명 | 예시 |
|--------------|----------------|------------------------------------------------------------------------------------------|-------------------------|
| 전체 선택자 | * { } | 모든 요소(Element)를 스타일을 부여할 대상으로 선택 | * { margin:0; padding:0; } | 
| 태그 선택자 | tagname { }  | 특정 요소(Element)를 스타일 부여 대상으로 선택 | h3 { color:blue } | 
| 클래스 선택자 | .클래스명 { } | 특정 클래스가 있는 요소(Element)를 스타일 부여 대상으로 선택 | .dp1 { text-align:center; } | 
| 아이디 선택자 | #아이디명 { } | 특정 아이디가 지정된 요소(Element)를 스타일 부여 대상으로 선택 | #hd { width:1200px; } | 
| 복수 선택자 | 선택자1, 선택자2 { } | 여러 요소를 한 번에 스타일을 부여할 대상으로 선택 | h1,h2,h3 { font-size:14px; } | 
| 속성 선택자 | [속성명] { } | 해당 속성(태그속성)이 존재하는 요소를 스타일 부여할 대상으로 선택 | [href] { text-decoration:none; } | 
| 속성 일치 선택자 | [속성명="값"] { } | 해당 속성(태그속성)의 값이 지정한 값과 일치하는 요소를 스타일 부여할 대상으로 선택 | [target="_blank"] { text-decoration:none; } | 
| 속성 접두 선택자 | [속성명^="값"] { } | 해당 속성(태그속성)의 값이 지정한 값으로 시작하는 요소를 스타일 부여할 대상으로 선택 | img[src^="kim"] { border:3px; } | 
| 속성 접미 선택자 | [속성명$="값"] { } | 해당 속성(태그속성)의 값이 지정한 값으로 끝나는 요소를 스타일 부여할 대상으로 선택 | [src$=".jpg"] { border:5px solid red; } | 
| 속성 포함 선택자 | [속성명*="값"] { }<br> | 해당 속성(태그속성)의 값이 지정한 값을 포함하는 요소를 스타일 부여할 대상으로 선택 | [src*="dall"] { border:5px solid red; } | 
| 부모자식 선택자 | elem1 > elem2 { }<br> | elem1의 안에 있는 elem2 자식 요소를 스타일 부여할 대상으로 선택 | #lst > li {  } | 
| 조상후손 선택자 | elem1 elem2 { }<br> | elem1의 안에 있는 elem2 후손 요소를 스타일 부여할 대상으로 선택 | #lst li {  } | 
| 동생(next) 선택자 | elem1 + elem2 { }<br> | elem1의 바로 다음에 나오는 elem2 동생 요소 하나만을 스타일 부여할 대상으로 선택 | .first + li { } | 
| 동생들(nextAll) 선택자 | elem1 ~ elem2 { }<br> | elem1의 다음에 나오는 elem2 동생들 요소를 스타일 부여할 대상으로 선택 | .first ~ li { } | 
| 자기 자신 선택자 | elem1elem2 { }<br> | elem1과 elem2가 모두 만족하는 요소를 스타일 부여할 대상으로 선택 | .sub.mid { } | 
| 링크 선택자 | :link { }<br> | href 속성이 있는 요소를 스타일 부여할 대상으로 선택 | a:link { } | 
| 방문 했던 요소 선택자 | :visited { }<br> | href 속성의 값이 방문했던 적이 있는 주소이면 스타일 부여할 대상으로 선택 | a:visited { } | 
| 롤오버 선택자 | :hover { }<br> | 해당 요소에 마우스 포인터를 올리면 그 요소를 스타일 부여할 대상으로 선택 | .box:hover { } | 
| 셀렉트 선택자 | :active { }<br> | 해당 요소에 마우스 포인터를 올리고 클릭하고 있으면, 그 요소를 스타일 부여할 대상으로 선택 | .box:active { } | 
| 커서 선택자 | :focus { }<br> | 해당 요소에 커서가 옮겨지면, 그 요소를 스타일 부여할 대상으로 선택 | input:focus { } | 
| 체크 선택자 | :checked { }<br> | 해당 체크박스나 라디오 버튼 요소에 체크를 하면, 그 요소를 스타일 부여할 대상으로 선택 | input:checked { } | 
| 폼 유효성 선택자 | :invalid { }<br> | 해당 폼 요소의 유효성 검사시 유효하지 않은 데이터 입력시에 그 요소를 스타일 부여할 대상으로 선택 | input:invalid { } | 
| 사용 가능한 폼 요소 선택자 | :enabled { }<br> | 해당 폼 요소 중에서 사용이 가능한 요소를 스타일 부여할 대상으로 선택 | input:enabled { } | 
| 사용 불가능한 폼 요소 선택자 | :disabled { }<br> | 해당 폼 요소 중에서 사용이 불가능한 요소를 스타일 부여할 대상으로 선택 | input:disabled { } | 
| 첫째 선택자 | elem:first-child { }<br> | 해당 요소 중에서 첫 번째 요소를 스타일 부여할 대상으로 선택 | li:first-child { } | 
| 첫째 요소 선택자 | elem:first-of-type { }<br> | 첫 번째 요소 중에서 해당 요소를 스타일 부여할 대상으로 선택 | li:first-of-type { } | 
| 마지막 선택자 | elem:last-child { }<br> | 해당 요소 중에서 마지막 번째 요소를 스타일 부여할 대상으로 선택 | li:last-child { } | 
| 마지막 요소 선택자 | elem:last-of-type { }<br> | 마지막 번째 요소 중에서 해당 요소를 스타일 부여할 대상으로 선택 | li:last-of-type { } | 
| 특정 번째 선택자 | elem:nth-child(위치숫자) { }<br> | 해당 요소 중에서 특정 번째 요소를 스타일 부여할 대상으로 선택 | li:nth-child(2) { }<br>li:nth-child(2n)<br>li:nth-child(even)<br>li:nth-child(2n+1)<br>li:nth-child(odd) | 
| 특정 번째 요소 선택자 | elem:nth-of-type(위치숫자) { }<br> | 특정 번째 요소 중에서 해당 요소를 스타일 부여할 대상으로 선택 | li:nth-of-type(2) { } | 
| 하나 뿐인 요소 선택자 | elem:only-child { }<br> | 특정 요소가 하나만 존재하는 요소를 스타일 부여할 대상으로 선택 | li:only-child { } | 
| 자식이 없는 요소 선택자 | elem:empty { }<br> | 해당 요소 중에서 비어 있는 요소를 스타일 부여할 대상으로 선택 | li:empty { } | 
| 이전 영역 선택자 | elem:before { }<br> | 해당 요소의 안쪽에서 그 앞을 스타일 부여할 대상으로 선택 | li:before { content:"앞 "; } | 
| 다음 영역 선택자 | elem:after { }<br> | 해당 요소의 안쪽에서 그 뒤를 스타일 부여할 대상으로 선택 | li:after { content:"뒤 "; } | 
| 첫 줄 선택자 | elem::first-line { }<br> | 해당 요소의 첫 번째 줄을 스타일 부여할 대상으로 선택 | .wrap p::first-line { color:red; } | 
| 첫 글자 선택자 | elem::first-letter { }<br> | 해당 요소의 첫 글자를 스타일 부여할 대상으로 선택 | .wrap p::first-letter { font-size:60px; } | 
| 글자/문단 범위 선택자 | elem::selection { }<br> | 해당 요소의 글자의 범위를 선택하면, 그 범위 안에 있는 글자를 스타일을 부여할 대상으로 선택 | .wrap p::selection { background-color:yellow; } | 
| 부정 선택자 | elem:not(조건) { }<br> | 해당 요소의 주어진 조건이 만족되지 않는 요소를 스타일을 부여할 대상으로 선택 | .ck:not(:checked) + label { font-size:14px; color:red; } | 


### ※ 스타일 선택자 사용 주의 사항

- 선택자의 우선 순위는 아이디 > 클래스 > 태그 순이다.
- 단계적으로 선택자를 기입하되, 단순한 선택자 부터 기입하고, 복잡한 선택자를 아래에 배치한다.
- 범위가 크거나 부모의 선택부터 하고, 범위가 작거나 세밀한 선택을 하도록 해야 한다.
- 아이디는 한 문서 내에서 중복되어서는 안된다.
- 같은 서식이 부여되는 경우는 가급적 클래스를 활용하여 같은 서식을 부여하도록 한다.


------------------------------------------------------------------------

<br><br>


## 3. CSS 속성 - Background

| 속성명 | 도메인 | 설명 | 예시
|------------|--------------------------------------------------|------------------------------------|-----------------------------|
| background-color	 | transparent &#124; 컬러명 &#124; RGB HEX(3/6) &#124; RGB(0-255,0-255,0-255) &#124; HSL(Hue,Sturation%,Lightness%) | 배경색을 지정하는 속성 | background-color:#000<br>background-color:#000000<br>background-color:black<br>background-color:rgb(0,0,0)<br>background-color:rgba(0,0,0,1)<br>background-color:hsl(240,0%,0%)<br>background-color:hsla(240,0%,0%,1) |
| background-image | none &#124; url(이미지경로) | 배경 이미지를 지정하는 속성 | background-image:url(./images/ive.png), url(./images/jungle.jpg) |
| background-repeat | repeat &#124; repeat-x &#124; repeat-y &#124; no-repeat | 배경이미지의 반복 속성 | background-image:url(./images/ive.png), url(./images/jungle.jpg) |
| background-position | 가로위치 세로위치로 지정하되, 0 0 &#124; top &#124; bottom &#124; left &#124; right &#124; middle &#124; 숫자(+/-)px/% | 배경이미지 위치 지정 속성 | background-position:left bottom<br> background-position:-200px -100px |
| background-attachment | scroll &#124; fixed &#124; local | 배경이미지 고정 유무 지정 속성 | background-attachment:fixed |
| background-origin | padding-box &#124; border-box &#124; content-box	배경이미지의 원점 기준 지정 속성 | background-origin:content-box |
| background-size | auto &#124; 가로크기 세로크기 &#124; cover &#124; contain | 배경이미지의 크기 지정 속성 | background-size:100px 200px, 200px 400px |
| background-clip | padding-box &#124; border-box &#124; content-box | 배경이미지의 영역을 어디까지 표시할지 지정 속성 | background-clip:border-box |
| background | bg-color bg-image position/bg-size bg-repeat bg-origin bg-clip bg-attachment | 배경에 모든 세부속성을 한 꺼번에 지정하는 통합 속성 | background-clip:border-box |
| filter | blur(px) &#38;&#124; brightness(%) &#38;&#124; contrast(%) &#38;&#124; grayscale(%) &#38;&#124; invert(%) &#38;&#124; opcacity(%) &#38;&#124; saturate(%) &#38;&#124; sepia(%) &#38;&#124; drop-shadow(x y blur px) &#38;&#124; hue-rotate(deg) | 배경이나 이미지에 필터 효과를 적용하는 속성 | filter:blur(3px) hue-rotate(45deg) opacity(85%) |

<br><hr><br>

## 4. CSS 속성 - 글자/문단 속성

| 속성명 | 도메인 | 설명 | 예시 |
|------------|--------------------------------------------------|------------------------------------|-----------------------------|
| @font-face | @font-face { font-family:"폰트별칭"; src:url(폰트파일이름을포함한웹폰트의경로); }	| 웹페이지에서 적용할 폰트를 규정하는 규칙 | @font-face { font-family:"ntg"; url(./font/notosans.woff); } |
| font-famliy | font-family:"폰트별칭"[, 대체폰트1, 기본웹폰트]; | 폰트 규칙(@font-face) 에서 규정한 폰트를 적용하는 속성. <br> 기본웹폰트에는 serif(명조), sans-serif(고딕), cursive(궁서), fantasy(장식), monospace(장평같음) | .con { font-family:"ntg", sans-serif; } |
| color | color:색상명 &#124; HEX(3/6) &#124; rgb() &#124; rgba() &#124; hsl() &#124; hsla() | 글자색을 지정하는 속성으로 16진수 HEX code와 여러 색 함수를 활용할 수 있음. | .con { color:deepskyblue; } <br>.con strong { color:#333; } |
| font-size | font-size: initial &#124; xx-small &#124; x-small &#124; small &#124; medium &#124; large &#124; x-large &#124; xx-large &#124; px, cm, em, %, rem 단위 | 글자크기를 지정하는 속성으로 크기를 나타내는 키워드 또는 크기단위로 지정할 수 있음. | .con { font-size:14px; } <br>.con strong { font-size:1.5em; } |
| font-weight | font-weight: normal &#124; bold &#124; bolder &#124; lighter &#124; 100 &#124; 200 &#124; 300 &#124; 400 &#124; 500 &#124; 600 &#124; 700 &#124; 800 &#124; 900 | 글자 두께를 지정하는 속성으로 크기를 100부터 900까지 100단위로 지정할 수 있으며,<br> 해당 키워드도 가능함. | .con { font-size:14px; }<br> .con strong { font-size:1.5em; } |
| font-style | font-style: normal &#124; italic &#124; oblique | 기울임꼴을 지정하는 속성 | .con { font-style:italic; } <br> .con strong { font-style:normal; } |
| font-variant | font-variant: normal &#124; small-caps | 대소문자가 있는 알파벳 계열에서 대소문자의 크기가 서로 달라서 대문자를 소문자 크기로 변경하기 위한 속성 | .con { font-variant:small-caps; }<br> .con strong { font-variant:normal; } |
| font-stretch | font-stretch: normal &#124; ultra-condensed &#124; extra-condensed &#124; condensed &#124; semi-condensed &#124; semi-expanded &#124; expanded &#124; extra-expanded &#124; ultra-expanded	| 글자의 장평(높이와 폭의 비율) 지정하기 위한 속성 | .con { font-stretch:condensed; }<br>.con strong { font-stretch:expanded; } |
| line-height | line-height: normal &#124; 숫자 &#124; px, % 단위 | 한 행의 높이를 지정하기 위한 속성으로 블록요소에 지정 | .con { line-height:2; } <br> .con strong { line-height:30px; } |
| word-spacing | word-spacing: normal &#124; px,pt,cm,em 단위 | 어간(단어와 단어 사이의 간격)을 지정하기 위한 속성 | .con { word-spacing:10px; }<br> .con strong { word-spacing:normal; } |
| letter-spacing | letter-spacing: normal &#124; px,pt,cm,em 단위 | 자간(글자와 글자 사이의 간격)을 지정하기 위한 속성 | .con { letter-spacing:10px; } <br> .con strong { letter-spacing:-2px; } |
| text-align | text-align: left &#124; right &#124; center &#124; justify | 글자 정렬을 의미하며, 블록요소에 지정하는 속성 | .con { text-align:center; } <br> .con strong { text-align:left; } |
| text-decoration | text-decoration: none &#124; underline &#124; overline &#124; line-through | 글자나 특정 단어에 줄을 적용할 때 지정하는 속성 | .con { text-decoration:none; }<br> .con strong { text-decoration:underline; } |
| text-indent | text-indent: %, px, pt, cm, em 단위 | 들여쓰기(+)/내어쓰기(-)를 지정하는 속성 | .con1 { text-indent:20px; }<br> .con2 { text-indent:-20px; } |
| text-transform | text-transform: none &#124; uppercase &#124; lowercase &#124; capitalize | 영문계열의 문자를 대/소문자로 변환해주는 속성 | .con1 { text-transform:uppercase; }<br> .con2 { text-transform:capitalize; } |
| text-orientation | text-orientation: mixed &#124; upright &#124; sideways &#124; sideways-right &#124; use-glyph-orientation | 문단의 글자 읽는 진행방향을 설정해주는 속성 | .con1 { text-orientation:upright; }<br> .con2 { text-orientation:sideways; } |
| direction | direction: ltr &#124; rtl | 글자의 진행 방향을 지정하는 속성 | .con1 { direction: rtl; } |
| writing-mode | writing-mode: horizontal-tb &#124; sideways-lr &#124; sideways-rl &#124; vertical-rl &#124; vertical-lr | 글자의 표시 방향을 지정하는 속성 | .con1 { writing-mode: sideways-rl; } |
| word-break | word-break: normal &#124; break-all &#124; keep-all &#124; break-word | 줄 끝에 도달했을 때 단어가 어떻게 끊어져야 하는지를 지정하는 속성 | .con1 { word-break:break-all; }<br> .con2 { word-break:keep-all; } |
| word-wrap | word-wrap: normal &#124; break-word | 긴 단어를 나누어 다음 줄로 넘길 수 있도록 지정하는 속성 | .con1 { word-break:break-word; } <br> .con2 { word-break:normal; } |
| white-space | white-space: normal &#124; nowrap &#124; pre &#124; pre-line &#124; pre-wrap | 요소 내부의 공백을 처리하는 방법을 지정하는 속성 | .con1 { white-space:nowrap; }<br> .con2 { white-space:pre; } |
| text-overflow | text-overflow: clip &#124; ellipsis &#124; string | 영역의 크기에 비해 흘러 넘치는 텍스트를 어떻게 처리할지 지정하는 속성 | .con1 { text-overflow:clip; }<br> .con2 { text-overflow:ellipsis; } |
| text-shadow | text-shadow: none &#124; h-shadow v-shadow blur-radius color | 텍스트에 그림자를 지정하는 속성 | .con1 { text-shadow:2px 2px 8px #ff0000; }<br> .con2 { text-shadow:-3px -3px 4px #00ff00; } |

※ font-variant, text-transform 속성의 경우 알파벳과 같이 대소문자가 있는 경우만 지원하는 속성이며, 적용되는 폰트에 따라 지원하지 않거나 적용되지 않는 속성이 있음을 주의하시기 바랍니다.

<br><hr><br>

