# ✨ 한강파 JS기초 스터디 2주차 요약본

# 1차 스터디

## 🚩 스터디 내용: 2주차 이론 및 실습 복습, 자기소개 페이지 중간 점검

- 미팅 날짜: 2022년 9월 25일 오후 2:00
- 스터디 기간: 2022년 9월 19일 → 2022년 9월 24일
- 온/오프라인: 오프라인

> **14:00 ~ 18:30 @스벅 강남2**

구두로 진행하여 기록한 내용이 없음

# 1.5차 스터디

## 🚩 스터디 내용: 1차 스터디 보충, 자기소개 페이지 중간 점검

- 미팅 날짜: 2022년 9월 28일 오후 5:00
- 스터디 기간: 2022년 9월 26일 → 2022년 9월 28일
- 온/오프라인: 온라인

> **17:00 ~ 19:00 @엘리스 강의실(온라인)**

## `readline` 구조 조사

### 0. readline?

- `Readable Stream`에서 한번에 한줄씩 데이터를 읽기 위한 인터페이스를 제공하는 모듈

→ 입출력을 한줄씩 처리하는 모듈

### 1. `readline` 모듈 불러오기

```jsx
const readline = require("readline");
```

### 2. `readline` 모듈 內 입출력 인터페이스 객체(`rl` 변수) 생성하기

```jsx
const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout,
});
```

### 3. `rl` 변수 활용하여 입출력 control하기

```jsx
rl.on("line", (line) => {
  // 한 줄씩 입력받은 후 실행할 코드
  // 입력된 값은 line에 저장된다.

  rl.close(); // 필수!! close가 없으면 입력을 무한히 받는다.
});
rl.on("close", () => {
  // 입력이 끝난 후 실행할 코드
  process.exit();
});
```

- .on() 메서드는 연결해서 사용 가능

  ```jsx
  rl.on("line", (line) => {
    /*입력받는 값을 처리하는 코드*/
    rl.close();
  }).on("close", () => {
    /*입력이 끝나고 실행할 코드*/
    process.exit();
  });
  ```

### 참고할만한 사이트s

[Node.js v0.8.20 Manual & Documentation](https://nodejs.sideeffect.kr/docs/v0.8.20/api/readline.html)

[[Node.js] 자바스크립트 콘솔에서 입력 받는 방법](https://lakelouise.tistory.com/140)

[[Node.js / readline] 값 입력받기](https://intrepidgeeks.com/tutorial/accept-node-jsreadline-value-input)

[readline 모듈 사용하기](https://velog.io/@leenzy/readline-%EB%AA%A8%EB%93%88-%EC%82%AC%EC%9A%A9%ED%95%98%EA%B8%B0)

## `process.exit()` 활용 예 조사

[Exit Process When all Readline on('line') Callbacks Complete](https://stackoverflow.com/questions/55045812/exit-process-when-all-readline-online-callbacks-complete)

> 모든 비동기 작업이 완료되면(그리고 미해결 핸들러가 없는 경우) nodeJS는 저절로 중지됩니다. 명시적으로 `process.exit()`를 호출할 필요가 없습니다. 이는 조기 종료(또는 특정 오류 코드로 종료)하는 경우에만 유용합니다. 프로세스가 종료되지 않는 이유를 조사해야 합니다.

### fileReader 관련 링크 (심화 공부하실 분들)

[정리함, 수납공간, 서랍 등 : 네이버 블로그](https://blog.naver.com/diddnjs02/222235800988)

[[Javascript] FileReader 객체로 파일 읽기](https://developer-syubrofo.tistory.com/102)

[FileReader - Web API | MDN](https://developer.mozilla.org/ko/docs/Web/API/FileReader)

[[JavaScript]파일 입출력 - FileReader 객체](https://developer-talk.tistory.com/331)

### IndexedDB 관련 링크 (심화 공부하실 분들)

[IndexedDB 사용하기 - Web API | MDN](https://developer.mozilla.org/ko/docs/Web/API/IndexedDB_API/Using_IndexedDB)

[IndexedDB API - Web API | MDN](https://developer.mozilla.org/ko/docs/Web/API/IndexedDB_API)

[IndexedDB 사용법 정리](https://lcs1245.tistory.com/entry/IndexedDB-%EC%82%AC%EC%9A%A9%EB%B2%95-%EC%A0%95%EB%A6%AC)

[IndexedDB](https://ko.javascript.info/indexeddb)

[indexedDB에 대해 알아보자!](https://mong-blog.tistory.com/entry/indexedDB%EC%97%90-%EB%8C%80%ED%95%B4-%EC%95%8C%EC%95%84%EB%B3%B4%EC%9E%90)

[Working with IndexedDB](https://web.dev/indexeddb/)

[IndexedDB 간단 정리하기](https://pks2974.medium.com/indexeddb-%EA%B0%84%EB%8B%A8-%EC%A0%95%EB%A6%AC%ED%95%98%EA%B8%B0-ca9be4add614)

[](https://velog.io/@xcv3549/IndexedDB%EC%97%90-%EB%8C%80%ED%95%B4-%EC%95%8C%EC%95%84%EB%B3%B4%EC%9E%90)

## 앞으로 일정 정리

### 1주차 (26 ~ 10/2)

- 자기소개페이지: 10/3(월)까지 완성

### 2주차 (10/3 ~ 10/9)

- 온(10/7 금 시간 14:00 - 16:00)
- 알고리즘 문제 풀기 & 해설 공유
- 해당 주차 문제 & 개념 풀이 공유

### 3주차 (10/10 ~ 10/13)

- 온 or 오프 (온 이 별로면 오프)
- 알고리즘
- 해당 주차 문제 & 개념 풀이 공유

### 발표: 10/14(금)

## 자기소개페이지 중간점검

- 0928 - 전원 배포 완료
- 진행상태 체크
  - 문제 발생 시 문제 내용 기재
- 완성 후 페이지 링크 기재

[자소페 멤버별 현황](https://www.notion.so/4192ebc339a44b7ba75b6d1ee2754568)

### 참고할만한 사이트s

[웹 퍼블리셔를 위한 웹 레퍼런스 사이트](https://webzz.tistory.com/)

[Material Symbols and Icons - Google Fonts](https://fonts.google.com/icons)

---

# 2차 스터디

## 🚩 스터디 내용: [자바스크립트 문제집 Ⅰ](https://swtrack.elice.io/courses/30256/lectures/226289/) JS로 풀어온 뒤 해설 발표

※ 사다리게임으로 해설자 랜덤 선정

- 미팅 날짜: 2022년 10월 7일 오후 2:00
- 스터디 기간: 2022년 9월 29일 → 2022년 10월 6일
- 온/오프라인: 온라인

> **14:00 ~ 15:30 @엘리스 강의실(온라인)**

<br>

# 1️⃣ 좋아하는 카드의 개수

## 🏁 발표자(윤동주 레이서)의 풀이

| 입력               | 첫줄 : 엘리스가 가지고 있는 카드의 수<br>둘째줄 : 카드에 적힌 숫자<br>셋째줄 : 엘리스가 좋아하는 숫자                 |
| ------------------ | --------------------------------------------------------------------------------------------------------------------- |
| 출력               | 첫째 줄에 엘리스가 가지고 있는 N개의 카드 중에서 엘리스가 좋아하는 숫자가 적힌 카드의 수                              |
| 발표자의 접근 방식 | 카드 숫자 문자열을 배열로 변환<br>⇒ for of 로 순환<br>⇒ 좋아하는 숫자 favNum 와 일치하면<br>⇒ res의 숫자를 1씩 더하기 |

```jsx
// 1. 좋아하는 카드의 개수
const readline = require("readline");

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout,
});

let N = 0; // 카드 개수
let input = [];
let cards = [];
let count = 0; // 입력받는 줄 수 카운터
let res = 0; // 좋아하는 숫자 개수

rl.on("line", function (x) {
  if (count === 0) {
    N = parseInt(x); //  카드 수
  } else {
    input.push(x); // 카드들 & 좋아하는 숫자
  }
  count += 1;

  // 3줄만 입력 받기
  if (count === 3) {
    rl.close();
  }
}).on("close", function () {
  const favNum = input[1];
  cards = input[0].split(" ");
  for (const x of cards) {
    if (x === favNum) {
      res += 1;
    }
  }
  console.log(res);
  process.exit();
});
```

## ✅ 사용 메서드 및 포인트

- `parseInt(변환하고자 하는 변수)` 문자열을 숫자로 변환
- `배열.push(추가하려는 요소)` 배열에 추가
- `문자열.split(’ ‘)` 문자열을 배열로 변환
- `for of` 으로 배열 원소에 접근

## 💡다른 레이서의 풀이 보기

### ☑️ 다른 풀이(김채현 레이서) : `filter()` 사용

```jsx
const readline = require("readline");

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout,
});

let arr = [];
rl.on("line", function (x) {
  arr.push(x);

  if (arr.length >= 3) {
    rl.close();
  }
}).on("close", function () {
  arr[1] = arr[1].split(" ");

  let result = arr[1].filter((item) => item === arr[2]);
  console.log(result.length);
  process.exit();
});
```

### ☑️ 다른 풀이(홍화낙 레이서) : 구조분해 할당 사용

```jsx
const readline = require("readline");

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout,
});

let count = 0;
let data = [];
let cardcount = 0;

rl.on("line", function (x) {
  count++;
  data.push(x);

  if (count === 3) {
    const [N, card, M] = data;
    const cardArray = card.split(" ");
    for (let i = 0; i < Number(N); i++) {
      if (String(cardArray[i]) === String(M)) {
        cardcount++;
      }
    }
    rl.close();
  }
}).on("close", function () {
  console.log(String(cardcount));
  process.exit();
});
```

# 2️⃣ 토끼굴 탈출

## 🏁 발표자(이도연 레이서)의 풀이

| 입력               | 첫줄 : 문자열의 길이<br>둘째줄 : 문자열                                                                              |
| ------------------ | -------------------------------------------------------------------------------------------------------------------- |
| 출력               | 문자열의 대문자 소문자 숫자의 갯수                                                                                   |
| 발표자의 접근 방식 | 문자열을 배열로 만들어서 <br>⇒ forEach로 순회<br>⇒ 숫자, 대문자, 소문자를 각 배열에 push <br>⇒ 각 배열의 길이를 출력 |

```jsx
const readline = require("readline");

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout,
});

let N = 0;
let count = 0;
let input = [];
let upperCase = [];
let lowerCase = [];
let num = [];

rl.on("line", function (x) {
  if (count === 0) {
    N = parseInt(x);
  } else {
    input = x.split("");
  }
  count += 1;

  if (count > 1) {
    rl.close();
  }
});

rl.on("close", function () {
  input.forEach((char) => {
    if (!isNaN(char)) {
      num.push(char);
    } else if (char === char.toUpperCase()) {
      upperCase.push(char);
    } else if (char === char.toLowerCase()) {
      lowerCase.push(char);
    }
  });
  console.log(`${upperCase.length} ${lowerCase.length} ${num.length}`);

  process.exit();
});
```

## ✅ 사용 메서드 및 포인트

- `forEach()` 로 순회
- `isNaN(변수)` 변수가 숫자가 아니면 true 숫자면 false
- `문자열.toUpperCase()` 문자열의 모두 대문자로 만듦
- `문자열.toLowerCase()` 문자열의 모두 소문자로 만듦
- `문자열 === 문자열.toUpperCase()` 문자열이 대문자인지 아닌지 판별 가능

## 💡다른 레이서의 풀이 보기

### ☑️ 다른 풀이(홍화낙 레이서) : 유니코드 사용

```jsx
const readline = require("readline");

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout,
});

let Upper = 0;
let lower = 0;
let num = 0;
let count = 0;

rl.on("line", function (x) {
  if (count === 1) {
    x.split("").forEach((char) => {
      const code = char.charCodeAt();
      if (65 <= code && code <= 90) Upper += 1; //대문자
      if (97 <= code && code <= 122) lower += 1; //소문자
      if (48 <= code && code <= 57) num += 1; //숫자
    });
    rl.close();
  }
  count++;
}).on("close", function () {
  console.log(Upper, lower, num);
  process.exit();
});
```

### ☑️ 다른 풀이(윤동주 레이서)

```jsx
// 2. 토끼굴 탈출
const readline = require("readline");

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout,
});

let cnt = 0;
let str = "";
let bigCnt = 0;
let smallCnt = 0;
let numCnt = 0;

rl.on("line", function (x) {
  if (cnt > 0) {
    str += x;
  }
  cnt += 1;
  if (cnt == 2) {
    rl.close();
  }
}).on("close", function () {
  for (const x of str) {
    if (!isNaN(x)) {
      numCnt += 1;
    } else {
      if (x === x.toUpperCase()) {
        bigCnt += 1;
      } else if (x === x.toLowerCase()) {
        smallCnt += 1;
      }
    }
  }
  console.log(`${bigCnt} ${smallCnt} ${numCnt}`);
  process.exit();
});
```

### ☑️ 다른 풀이(김채현 레이서)

```jsx
//토끼굴 탈출
//대소문자 구분하는 법
// 숫자 구분하는 법
// 문자열 => 배열
const readline = require("readline");

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout,
});
let arr = [];
rl.on("line", function (x) {
  arr.push(x);
  if (arr.length >= 2) rl.close();
}).on("close", function () {
  let strarr = arr[1].split(""); //문자열을 배열로
  let num = 0;
  let upper = 0;
  let lower = 0;
  strarr.map((item) => {
    if (!isNaN(Number(item))) num++; //숫자인것
    else item === item.toUpperCase() ? upper++ : lower++;
  });
  console.log(`${upper} ${lower} ${num}`);

  process.exit();
});
```

# 3️⃣ 파일명 새로 저장하기

## 🏁 발표자(이도연 레이서)의 풀이

| 입력               | 첫줄 : 파일의 개수<br>둘째줄~ : 문자열                                   |
| ------------------ | ------------------------------------------------------------------------ |
| 출력               | 문자열의 첫글자는 대문자 나머지는 소문자로                               |
| 발표자의 접근 방식 | 문자열의 첫을자는 대문자, slice로 나머지는 소문자로 + 를 사용하여 합치기 |

```jsx
// 3. 파일명 새로 저장하기
const readline = require("readline");

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout,
});

let N = 0;
let count = 0;
let input = [];
let res = [];
let newStr = "";

rl.on("line", function (x) {
  if (count === 0) {
    N = parseInt(x);
  } else {
    input.push(x);
  }
  count += 1;

  if (count > N) {
    rl.close();
  }
});

rl.on("close", function () {
  res = input.map(
    // map으로 하나하나 형변환 시켜주기
    (el) => {
      newStr = el[0].toUpperCase() + el.slice(1, el.length).toLowerCase();
      console.log(newStr);
    }
    // 요소의 첫번째를 대문자로  + 요소의 나머지 부분을 소문자로
  );
  // console.log(res.join('\n'));
  // => join을 이용하면 14번, 15번 테스트 케이스 통과 못함 :(

  process.exit();
});
```

## ✅ 사용 메서드 및 포인트

- `map()` 로 배열 순회
- `slice(시작 인덱스, 끝 인덱스)` 원소들을 가지고 새로운 배열을 만들어 반환
- `배열.join('')` 배열을 문자열로

## 💡다른 레이서의 풀이 보기

### ☑️ 다른 풀이(홍화낙 레이서) : `splice()` 사용

```jsx
const readline = require("readline");

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout,
});

let count = 0;
let data = [];

rl.on("line", function (x) {
  count++;
  data.push(x);
  if (count === parseInt(data[0]) + 1) {
    rl.close();
  }
}).on("close", function () {
  let [line] = data;
  data.splice(0, 1);
  for (let i = 0; i < line; i++) {
    let result = data[i][0].toUpperCase() + data[i].toLowerCase().slice(1);
    console.log(result);
  }
  process.exit();
});
```

### ☑️ 다른 풀이(윤동주 레이서) : `slice()` 사용

```jsx
// 3. 파일명 새로 저장하기
const readline = require("readline");

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout,
});

let N = 0; // 파일 개수
let input = []; // S 담긴 배열
let count = 0;
let newStr = "";
let res = [];

rl.on("line", function (x) {
  if (count === 0) {
    N = parseInt(x);
  } else {
    input.push(x);
  }

  count += 1;

  if (count > N) {
    rl.close();
  }
}).on("close", function () {
  for (let x of input) {
    let firstChar = x.charAt(0);
    let others = x.slice(1);
    newStr = firstChar.toUpperCase() + others.toLowerCase();
    console.log(newStr);
    // res.push(newStr);
  }
  // console.log(res.join('\n'));
  process.exit();
});

// join 쓰면 14, 15번 테케가 틀렸다고 뜨는 듯?
```

### ☑️ 다른 풀이(김채현 레이서) : `replace()` 사용

```jsx
//파일명 새로 저장하기
//[0] 제거하는 방법 [-1] 제거하는 방법 그리고 각 메서드의 반환
//첫번째 입력에 따라 달라지는 입력의 길이를 컨트롤 하는 방법

const readline = require("readline");

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout,
});
let arr = []; //[3 abc helloWORLD qWeRtY]
rl.on("line", function (x) {
  arr.push(x);
  if (arr.length > arr[0]) {
    rl.close();
  }
}).on("close", function () {
  arr.shift(); //숫자 제거 [abc helloWORLD qWeRtY]
  arr.map((item) => {
    item = item.toLowerCase(); //다 소문자로 바꾸고
    item = item.replace(item[0], item[0].toUpperCase()); //맨대문자 하나만 바꿈
    console.log(item);
  });

  process.exit();
});
```

# 4️⃣ 받아쓰기

## 🏁 발표자(김채현 레이서)의 풀이

| 입력               | 첫줄 : 문자열 A의 길이 문자열 B의 길이<br>둘째줄 : 문자열 A<br>셋째줄 : 문자열 B |
| ------------------ | -------------------------------------------------------------------------------- |
| 출력               | A가 B의 부분 문자열이라면 1 아니면 0                                             |
| 발표자의 접근 방식 | includes 사용하여 ⇒ 있으면 1 없으면 0                                            |

```jsx
//받아쓰기
const readline = require("readline");

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout,
});
let arr = [];

rl.on("line", function (x) {
  arr.push(x);
  if (arr.length > 2) rl.close();
}).on("close", function () {
  arr[2].includes(arr[1]) ? console.log(1) : console.log(0);
  process.exit();
});
```

## ✅ 사용 메서드 및 포인트

- `if (arr.length > 2) rl.close();` 입력 줄 수 고정
- `대상문자열.includes(검사문자열)` true false 반환
- 삼항 연산자

## 💡다른 레이서의 풀이 보기

### ☑️ 다른 풀이(홍화낙 레이서) : `indexOf()` 사용

```jsx
const readline = require("readline");

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout,
});

let count = 0;
let data = [];

rl.on("line", function (x) {
  count++;
  data.push(x);
  if (count == 3) {
    rl.close();
  }
}).on("close", function () {
  data[2].indexOf(data[1]) >= 0 ? console.log(1) : console.log(0);
  process.exit();
});
```

### ☑️ 다른 풀이(윤동주 레이서) : `includes()` 사용

```jsx
// 4. 받아쓰기
const readline = require("readline");

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout,
});

// let N = 0; // 사실상 받아올 필요가 없
// let M = 0; // 사실상 받아올 필요가 없
let cnt = 0;
let A = "";
let B = "";
let str = [];

rl.on("line", function (x) {
  // if (cnt === 0) {
  // [N, M] = x.split(' ');
  if (cnt > 0) {
    str.push(x);
  }
  cnt += 1;

  if (cnt > 2) {
    rl.close();
  }
}).on("close", function () {
  A = str[0];
  B = str[1];

  if (B.includes(A)) console.log(1);
  else console.log(0);
  process.exit();
});
```

# 5️⃣ 명단 정리

## 🏁 발표자(김채현 레이서)의 풀이

| 입력               | 첫줄 : 명단의 개수<br>둘째줄~ : 성과 이름으로 이루어진 명단                                                                                                      |
| ------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 출력               | 이름 명단                                                                                                                                                        |
| 발표자의 접근 방식 | 명단을 배열로 받아서 map 으로 순회<br>⇒ 명단 문자열을 배열로 변환 split<br>⇒ 성의 대문자 제거<br>⇒ 성의 소문자 제거<br>⇒ 이름의 대문자 나오면 나머지를 join 으로 |

```jsx
//명단정리
//slice splice split 이름이 다 비슷해
// 순회하면서 직접 삭제하고 이럴때는 깊은 복사로 해서 삭제 할 것
const readline = require("readline");

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout,
});
let arr = [];
rl.on("line", function (x) {
  arr.push(x);
  if (arr.length > arr[0]) rl.close();
}).on("close", function () {
  arr.shift(); // n 제거 [ WhiteRabbit EliceAlgo]      R abbit
  arr.map((item) => {
    item = item.split(""); // 문자열로 만든 후 성의 대문자 제거 WhiteRabbit
    item.shift(); //WhiteRabbit
    item2 = [...item]; //깊은 복사 / 깊은 복사를 해조야함..!
    item2.map((i) => {
      i === i.toUpperCase() ? console.log(item.join("")) : item.shift();
    });
  });
  process.exit();
});
```

## ✅ 사용 메서드 및 포인트

- `map` 으로 순회
- `shift()` 로 `배열[0]` 제거 `pop()` 은 `배열[-1]` 제거
- 순회하면서 제거가 들어가기 때문에 깊은 복사를 한번 해줘야함 `[…배열]`

## 💡다른 레이서의 풀이 보기

### ☑️ 다른 풀이(홍화낙 레이서) : 이중 `for`문 사용

```jsx
const readline = require("readline");

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout,
});
let data = [];
let count = 0;

rl.on("line", function (x) {
  count++;
  data.push(x);
  if (count == parseInt(data[0]) + 1) {
    rl.close();
  }
}).on("close", function () {
  const [N, ...name] = data;
  let name1 = name.map((el) => el.slice(1));

  for (let i = 0; i < name1.length; i++) {
    for (let j = 0; j < name1[i].length; j++) {
      let code = name1[i][j].charCodeAt();
      if (65 <= code && code <= 90) {
        //대문자
        console.log(name1[i].slice(j));
      }
    }
  }
  process.exit();
});
```

### ☑️ 다른 풀이(윤동주 레이서) : `indexOf()`와 `slice()` 사용

```jsx
// 5. 명단 정리
const readline = require("readline");

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout,
});

let N = 0;
let cnt = 0;
let input = []; // 이름 명단
let res = "";
let resArr = [];

rl.on("line", function (x) {
  if (cnt === 0) {
    N = x;
  } else {
    input.push(x);
  }
  cnt += 1;
  if (cnt > N) {
    rl.close();
  }
}).on("close", function () {
  for (let str of input) {
    let firstChar = str[0];
    let others = str.slice(1);
    str = firstChar.toLowerCase() + others;
    for (const x of str) {
      if (x === x.toUpperCase()) {
        let idx = str.indexOf(x);
        res = str.slice(idx);
        resArr.push(res);
      }
    }
  }
  console.log(resArr.join("\n"));
  process.exit();
});
```

### ☑️ 다른 풀이(이도연 레이서) : `forEach()`와 `slice()` 사용

```jsx
// 5. 명단정리
const readline = require("readline");

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout,
});

let count = 0; // 줄을 세어나갈 count
let N = 0; // 첫번째 줄 숫자 (밑에 줄 갯수) 넣어주기
let arr = [];
let result = ""; // 정답 문자열 넣기

rl.on("line", (x) => {
  if (count === 0) {
    N = parseInt(x);
  } else {
    arr.push(x);
  }
  count += 1;

  if (count > N) {
    rl.close();
  }
});

rl.on("close", () => {
  arr.forEach((el) => {
    // forEach를 이용해서 문자 하나하나에 접근
    let first = el[0].toLowerCase();
    // 첫번째 문자 대문자를 소문자로 변경
    let restAlphabet = el.slice(1, el.length);
    // 남은 알파벳
    let all = first + restAlphabet;
    // 바뀐 첫번째 문자를 나머지와 더해줌
    for (let i = 0; i < all.length; i++) {
      // for문을 이용해 all 부분의 문자하나하나에 접근
      if (all[i] === all[i].toUpperCase()) {
        // 대문자인지 판별
        // true이면 슬라이스 (뽑아내고 싶은 첫번째 문자의 인덱스, 문자열 길이)
        result = all.slice(i, all.length);
      }
    }
    console.log(result);
  });

  process.exit();
});
```

---

## 🗣 스터디원들의 주차별 회고

### - 김선은 레이서

- 1주차 <br>
  2주차 학습의 문제풀이를 다시 짚어보는 시간이 너무 유익했다. 메소드 활용과 문제ㄴ풀이에 너무 익숙치 못해서 문제를 대체로 풀지를 못했기에 풀이방식을 같이 공유하지 못한 점이 아쉬웠으나 다양한 접근 방식을 직접 들을 수 있어서 주차 학습에도 도움되었다. 추가로 자기소개서 페이지를 만들며 기초적인 CSS 활용을 하면서도 특정 요소들을 변경하면 어떻게 될지 싶은 궁금증이 많이 들었고 아직은 레이아웃을 잡는 연습부터 많이 해야겠음을 느꼈다.

- 2주차 <br>
  스터디용 자바스크립트 문제풀이를 제대로 접근하지 못해서 다른 팀원들의 다양한 풀이방식을 듣는 시간이었다. 모두의 코드를 공유하면서 생각지도 못한 방법으로 풀이를 들은 내용도 있었고, 아직 잘 못다루는 메소드들의 이용 방식을 볼 수 있었다.

### - 김채현 레이서

- 1주차 <br>
  어려운 개념이 많았는데 스터디를 하면서 다시 복습하니 이해가 훨씬 잘되었다. 각자 꾸민 자기소개서 페이지가 흥미로웠다
- 2주차 <br>
  풀이를 공유하는 시간이 재미있었고 모두 조금씩 다른 풀이를 가지고 있어 신기했다. 개인적으로 다른 레이서들의 풀이를 복습하는 시간을 가져야겠다.

### - 백소라 레이서

- 1주차 <br>
  그동안 배웠던 것들을 다시 한번 복습하면서 정리할 수 있었고 막막했던 문제들을 다양한 각도에서 푸는 법을 배울 수 있었다.
- 2주차 <br>
  readline을 이용하는 법을 배울 수 있었고 어떻게 readline으로 문제를 푸는지 여러 메소드들을 이용하는 해설을 들었다.

### - 윤동주 레이서

- 1주차 <br>
  첫 스터디장을 맡게 되어 진행이 서툴렀지만 오프라인 미팅이었음에도 팀원 분들이 빠짐없이 성실하게 참여해 주셔서 감사했다. 풀었던 문제들을 말로 설명하며 개념을 복기하고 코딩하는 사고 흐름을 완성시킬 수 있어서 유익했다. 다음 오프라인 스터디 땐 손님이 적은 카페에서 스터디를 진행해야 될 것 같다.
- 2주차 <br>
  역시 혼자 공부하는 것보다 다른 분들의 코드를 통해 새로운 발상과 관점을 엿보는 것이 훨씬 도움이 많이 된다. 아직 코테를 C++로 볼지 JS로 볼지 확정하지 못했지만 JS로 알고리즘 문제들을 푸는 것이 생각보다 간편해서 고민 중이다. 보다 효율적인 방식과 편리한 메소드들을 이번 기회에 잘 익혀두어야겠다.

### - 이도연 레이서

- 1주차 <br>
  2주차에 배운 문제들을 다같이 풀어보며 자기소개 페이지를 만들고 공유하는 시간을 가졌다. 놓쳤던 개념이나 부분들을 되짚어보는 시간이어서 의미있었고, 자기소개 페이지는 같은 지시사항을 가지고 만들었음에도 불구하고 각자의 개성이 가득 담겨있어 놀랐고 재밌었다.
- 2주차 <br>
  자바스크립트 문제집 1을 풀고 각자의 풀이과정을 공유하는 시간을 가졌다. 스터디원 모두 조금씩 다른 방법을 가지고 풀었다는게 신기했으며, 그 방법들을 모두 알 수 있어서 상당히 의미있는 시간이었다. 또, 이러한 방법을 적용해서 다시 문제를 풀어봐야겠다는 생각을 했다.

### - 홍화낙 레이서

- 1주차 <br>
  🎈 CSS에 대해서 & DOM 요소에 대해서 더 깊이 알게 됨. Grid , flex에 대해서 더 자세히 알게 됐고 CSS 레이아웃에 대해서 더 공부해야겠다. DOM 요소를 사용해본 경험이 없는데 자기소개 페이지에 적용하면서 조금씩 이해를 했다. DOM 요소와 CSS 레이아웃에 대해서 더 경험해 보고 연습해야겠다.

- 2주차 <br>
  알고리즘 문제를 풀면서 직접적으로 웹페이지를 만들 때 유용하게 사용 할 수 있는 Method에 대해서 자세히 알게 됐고, 각자 문제를 푸는 방식이 다른 것을 보고 여러가지 풀이 방식을 배우면서 “더 열심히 해야겠다” 느꼈다. 문제를 풀 수 있는 방법을 많은 관점으로 생각해 봐야겠다.
