## 뷰엑스(Vuex)

* 는 상태 관리 라이브러리.
* 상태 관리를 props 로 한다면 손이 많이감, 이벤트 버스의 경우 단방향이 아닌 많은 데이터 흐름의 문제
* 컨포넌트가 많아 관리가 어려운 복잡한 규모의 애플리케이션에서 필요.
* 애플리케이션에서 사용하는 모든 데이터를 중앙에서 관리하여 크기가 큰 애플리케이션의 데이터 관리를 효율적으로 하는것이 목표
* https://joshua1988.github.io/web-development/vuejs/vuex-start/
 
## Vue 반응성(reactivity)

* 뷰의 반응성은 데이터 변화를 감지하여 자동으로 화면을 갱신하는 특성.
* 프레임워크 내부적으로 화면을 그리는 방법, 가상 돔이 동작하는 방법, 브라우져에 부하를 주지 않고 돔을 추가,삭제하는 방법을 익힐 수 있다.
* 뷰 애플리케이션을 실행시 인스턴스 생성을 하며 생성시에 data에 정의된 모든 속성을 getter, setter 의 형태로 변환, data 속성 변화가 생길때 감지하기 위해 사용.
* 때문에 인스턴스 생성 이후 data 속성의 변경시 감지 하지 못함.
* watcher 에서 data 속성 변화 감지.
* https://vuejs.org/v2/guide/reactivity.html

## 서버 사이드 렌더링(Server Side Rendering)

* Client Side Rendering 은 다 그려져 있지 않은 HTML 페이지를 브라우져에서 받고 자바스크립트를 이용하여 나머지 부분을 그리는 것을 의미.
* SSR 은 완벽히 그려진 HTML 페이지를 브라우져에서 받는 것을 의미.
* SSR 은 검색엔진 최적화, 초기화면 렌더링 속도에 장점
* CSR 은 매끄러운 화면 전환과 사용자 경험의 향상에 장점
* 두 가지 방식을 적절하게 사용하는 것이 필요

## 웹팩(webpack)

* 최신 프론트엔드 프레임워크인 앵규러, 리액트, 뷰에서 모두 권하는 모듈 번들러
* '서로 연관이 있는 모듈 간의 관계를 해석하여 정적인 자원으로 변환해 주는 도구'
* '파일 간의 연관 관계를 파악하여 하나의 자바스크립트 파일로 변환해 주는 변환 도구'
* 애플리케이션 동작과 관련된 여러개의 파일(HTML, CSS, javascript, 이미지 등)을 1개의 자바 스크립트 파일 안에 다 넣어 동작하도록 함
* 왜? 정적 파일 다운 request 가 많아 질수록 웹 화면 로딩 속도가 길어 지기 때문
* 이전에는 걸프(Gulp), 그런트(Grunt) 같은 자동화 도구로 해결

### 웹팩 데브 서버

* 웹팩 데브 서버란 웹팩 설정 파일의 변화를 감지하여 웹팩을 빌드할 수 있도록 지원하는 유틸리티이자 Node.js 서버
* 웹팩 데브 서버는 웹팩 설정 파일의 내용이 변경되면 브라우져 화면을 자동으로 새로 고침하고, 바로 다시 웹팩으로 빌드하는 기능을 가지고 있다
* 웹팩으로 빠르게 제작하고자 할때 유용
* [웹팩 속성 참고](https://joshua1988.github.io/webpack-guide/concepts/overview.html)

```
// 웹팩 빌드 명령어
npm run build
// inmemory 기반 프로젝트 시작 명령어, 빌드 결과물 만들지 않음
npm run dev
```

## ES6

* ES6(ECMAScript 2015) 는 최신 자바스크립트 문법이자 스펙. 기존 자바스크립트를 ES5 라고 명명
* const와 let 예약어
* 블록의 유효 범위(호이스팅)
* 화살표 함수(Arrow Functions)
* Import 와 Export
  * 모듈화 관련 기능
  * 이전에는 프로그래밍 패턴(namespace), CommonJS, RequireJS 등 모듈화를 지원하는 라이브러리 사용

## NPM

* 전 세계 자바스크립트 라이브러리가 존재하는 공개 저장소

```
// 설치 명령어, npm 설정 파일에 설정된 라이브러리 목록을 다운로드
npm install
// dependencies 속성에 추가
npm install --save
// devDependencies 속성에 추가
npm install --save-dev
// 전역설치
npm install --global
// 또는 
npm install -g 
```