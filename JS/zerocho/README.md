# ZeroCho 님과 함께 하는 자바스크립트 웹 게임 개발
- 구름에듀 무료 강좌
- zerocho.com / 유튜브
- 10분 내외의 유튜브 영상 114개로 이루어져 있음
- 22/5/11 에 수강 시작
- 스파르타코딩의 내일배움단 웹개발 강의와 함께, 생애 첫 접하는 프로그래밍 공부이다.
- 자바스크립트를 비롯한 프로그래밍의 기초적인 부분을 이해할 수 있을 것 같아 수강함.
- 강의를 들으면서 처음엔 원노트에 배운 것을 정리하려고 했지만 비효율적인 것 같아 개발 일지 플랫폼을 비교하다가 비교적 간결하고 bash 명령어로 로컬 스토리지와 동기화가 간편한 깃헙을 이용하기로 결정하였다.

----------
## 강좌 챕터 구성 (114강)
1. 자바스크립트 기초와 끝말잇기 (14)
2. 객체 기본과 구구단 게임
3. 웹 화면 구현
4. 숫자야구
5. 틱택토
6. 로또 추첨기
7. 가위바위보
8. 지뢰찾기
9. 반응속도 테스트
10. 틱택토 심화
11. 카드 짝맞추기 게임
12. 자스스톤
13. 2048
14. 테트리스

--------


## 01 자바스크립트 기초와 끝말잇기

    "자바스크립트로 테트리스 정도 만들면 신입으로 어떤 회사든 거의 취직을 할 수 있어요. 테트리스가 정말 어려웠거든요"

> 정말일까?  
하지만 그렇지 않다고 하더라도,  
이런 게임 개발은 내가 너무 하고 싶은 그림과 프로그래밍을 동시에 충족시켜주고,  
지루하지 않게 프로그래밍에 입문할 수 있을 것 같다.  

> 배운 것들을 정리하려고 한다.  
그런데 어짜피 vs code에서 현재 md를 작성하는데 크롬F12 대신 여기서 바로 자바스크립트 콘솔을 실행하는 게 편할 것 같아 방법을 찾아보았다.  
-터미널에서 node 입력
-clear 용도로 F1> keybindings.json  

```
    #자바콘솔에서 clear ctrl+k 단축키 설정 방법
    #F1> keybindings.json 열고
    {
        "key": "ctrl+k",
        "command": "workbench.action.terminal.clear",
        "when": "terminalFocus"
    }
    저장
```
```js
    > 5>=5
    true
    > '5'>"5"
    false
    > 5 === 5
    true
    > 5 == '5'
    true
    > 5 === '5'
    false
```
```js
    > var f = '제로초'
    undefined
    > f
    '제로초'
    > var d = 3*5
    undefined
    > d
    15
    > d === 15
    true
```
>다음 코드는 vs code 터미널에서 prompt 가 실행이 안되어서 크롬 F12에서 진행하였다.

```js
var 답 = prompt('답?')
'5'
답
'5'
Number(답)
5

if (1*5===Number(답)) {
    '딩동댕'
} else {
    '땡'
}
'딩동댕'

//다음과 동일하다.
if (true) {
    '딩동댕'
} else {
    '땡'
}
'딩동댕'
```
>위 코드를 다음과 같이 압축 가능하다. 브라우저 개발자 콘솔에서 강제 개행은 Shift+Enter

```js
var 답 = prompt('답?')
if (3*8 === Number(답)) {
    '딩동댕'
} else {
    '땡'
}

'딩동댕'
```
```js
var 값 = 0
while (값<100) {
  console.log(값)
	값 = 값 + 1
}

>0~100
```
```js
var dateChecker = function() {
  var date = new date();
	alert(date);
}
dateChecker
```
>다음에서 zero 를 객체, {}안의 것을 속성, firstName과 lastName 을 키라고 한다.
```js
var zero = {
  firstName: 'Zero',
    lastName: 'Cho'
};

zero
Object { firstName: "Zero", lastName: "Cho" }

zero['firstName'];
"Zero"
zero.firstName
"Zero" 

zero.lastName = 'Lee';
zero.lastName
"Lee"
```
```js
var zero = {
  body: {
    height: 173,
    weight: 66
  },
    name: {
        firstName: 'Zero',
        lastName: 'Cho'
  }
};
undefined
zero
Object { body: {…}, name: {…} }

zero.body.weight
66
zero.name.firstName
"Zero" 
```
>배열(Array). 여기서 0과 1가 객체에서의 키에 해당한다.

```js
var zero = ['Zero', 'Cho']
undefined

>
zero
Array [ "Zero", "Cho" ]
zero[0]
"Zero"
zero[1]
"Cho" 
```
>위 배열은 다음 객체랑 비슷하다.
```js
va
