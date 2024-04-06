# Style-note

## 반응형 웹

### viewport 
meta 태그로 사용할 수 있음.
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
device-width: 화면 너비 기준
initial-scale: 1.0 배율

### em
상위 부모 요소의 사이즈

- padding, margin의 em은 부모가 아닌 자신의 font-size를 기준으로 정해진다.


### rem 
루트(html)의 사이즈 

### vw, vh
'viewport' 크기 기준으로 값을 계산하여 크기를 결정하는 가변 단위
```css
.class {
    /* 뷰포트 기준 너비의 100분의 1 */
    width: 1vw;     
    /* 뷰포트 기준 높이의 100분의 1 */
    height: 1vh; 
    /* 뷰포트 높이와 너비 중 작은 쪽의 100분의 1 */
    font-size: 1vmin; 
    /* 뷰포트 높이와 너비 중 큰 쪽의 100분의 1 */
    font-size: 1vmin; 
}
```

### %
% 단위는 백분율 값을 나타낸다.
보통 부모의 요소와 상대적 크기를 지정할 때 사용.
너비와 높이, 여백 뿐 아니라 글자 크기에도 사용할 수 있다.
```css
.child{
    /* 부모 요소의 글자 크기 기준 퍼센트 */
    font-size: 50%;
    /* 부모 요소의 너비 기준 */
    width: 50%;
    margin: 10%;
    padding: 10%;
}
```


### calc
계산식의 결과를 속성값으로 지정할 수 있다.
calc() 함수는 괄호 안에 표현식 하나를 받고, 표현식의 결과가 최종 값이 된다.
표현식은 단순 계산식이면 무엇이든 가능하다.


### @media
미디어 쿼리는 미디어 타입을 인식하고, 콘텐츠를 읽어들이는 방식 기기나 브라우저의 물리적 속성을 감지할 수 있는 유용한 장치(기능)
모든 미디어 쿼리는 다음 두 가지 구성 요소를 지니고 있다.
- 미디어 타입
- 조건에 대한 물음(query)

```css
@media 미디어_타입 and (조건에_대한_물음)
 {
    /* 
    미디어 타입과 조건을
    모두 만족할 때 덮어씌울
    스타일 선언문
     */
 }

 @media screen and (max-width: 768px)
 {
    /* 
    화면 (screen)의 
    너비가 768px 이하일 경우에 
    여기에 정의된 스타일 선언문을
    추가 적용할 것이다.
     */
 }
 ```

```html
<link rel="stylesheet" href="style.css" media="screen and (max-width: 768px)">
```

```javascript
@import url("style.css") screen and (max-width: 768px);
```

---


## 인터렉션 