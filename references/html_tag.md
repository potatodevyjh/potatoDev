# <HTML TAG 정리>


## 기본 태그
    <!DOCTYPE html>
    웹 문서의 유형 지정

    <html>
    웹 페이지의 시작과 끝

    <head>
    웹 페이지의 정보, 문서에서 사용할 외부 파일들을 링크할 때 사용
    <title>, <meta>, <link>

    <body>
    브라우저에 실제 표시되는 내용

    <title>
    문서 제목

    <meta>
    문자 인코딩 및 문서 키워드, 요약 정보
    <meta charset="utf-8">

    <script>
    코드 삽입

## 문서 구조
    <header>
    헤더 영역

    <main>
    메인 영역

    <section>
    콘텐츠 영역

    <aside>
    사이드 바

    <footer>
    푸터 영역

    <nav>
    내비게이션 영역
    문서 내 다른 위치, 다른 문서로 연결

    <article>
    독립적인 콘텐츠 사용

    <div>
    묶는 폴더(의미 X)
    줄바꿈 O

    <span>
    묶는 폴더(의미 X)
    줄바꿈 X

    <link>
    외부 파일 연결
    <link href"외부css파일 경로" rel = "stylesheet" type = "text/css">
    css 사용 시 link 와 style의 차이
        link는 외부 css 설정할 때, style은 css 설정을 같은 웹페이지에서 할 때

## 텍스트 입력
    <h1>, <h2>
    제목

    <p>
    단락

    <br>
    줄바꿈(닫기 태그 없음)

    <blockquote>
    인용문, 들여쓰기 적용됨

    <strong>
    텍스트 굵게, 주로 중요한 내용

    <b>
    텍스트 굵게, 단순히 굵게만 표시

    <em>
    텍스트 기울임(강조)

    <i>
    텍스트 기울임(단순 기울여)

    <u>
    텍스트 밑줄

    <s>
    텍스트 취소

    <abbr>
    줄임말
    
    <cite>
    참고 내용

    <code>
    소스 코드

    <small>
    작은 텍스트

    <sub>
    아래 첨자

    <sup>
    위 첨자

    <ins>
    공동작업문서에 새로운 내용 삽입

    <del>
    공동작업문서에 기존 내용 삭제

## 목록 입력
    <ol>
    순서가 있는 목록
    type = 
    "1"    "a"    "A"   "i"  "I"

    <ul>
    순서가 없는 목록

## 설명 목록 태그
    <dl>
    <dt>
    설명할 용어
    <dd>
    설명할 내용

## 표입력
    <table>
    테이블 만들기

    1) <caption>
    표제목

    2) <tr>
    행 삽입
        <td> 셀 삽입
        <th> 셀 삽입(진하게 표시)

    3) <thead>
    표 중 제목, 여러 페이지에 걸쳐서 고정 가능

    4) <tbody>
    표 중 본문

    5) <tfoot>
    표 중 요약, 여러 페이지에 걸쳐 고정 가능

    rowspan = "2"   2개의 행 합치기
    colspan = "2"   2개의 열 합치기
    합쳐진 셀들은 태그를 적지 않는다.

    <colgroup>
        1) <col style="~">	첫번째 열 스타일 지정
        2) <col>	두번째 열은 스타일 지정 안함
        3) <col style="~">	세번째 열 스타일 지정
        4) <col style="~">	네번째 열 스타일 지정
    5) <col span="2">	동일한 스타일로 다섯, 여섯번째 스타일 지

## 이미지 삽입
    <img>
    이미지 삽입
    <img src = "이미지 경로" alt = "대체용 텍스트>
    1) width
        너비
    2) height
        높이
    3) alt
        대체용 텍스트
    4) width = , height = 
        가로 세로 크기 조절
        % 브라우저 창의 크기 단위
        px 픽셀 단위

# 오디오, 비디오 등 멀티미디어 파일 삽입
    <object width="너비" height="높이" data="파일"></object>
    <embed src="파일 경로" width="너비" height="높이">
    <audio src="오디오 파일 경로"></audio>
    <video src="비디오 파일 경로"></video>
    1) controls=	    컨트롤 바 표시
    2) autoplay=    	자동 재생
    3) loop=	        반복 재생
    4) muted=	        음소거
    5) preload=	        로딩방법, 사용할 수 있는 값은
            auto(기본값), metadata, none
    6) width=, height=	    비디오 플레이어의 너비, 높이 지정
    7) poster="파일 이름"     비디오 플레이어의 재생 전 포스터

    크롬 브라우저에서 비디오 자동 재생을 하려면
    muted를 넣어야 한다. (muted autoplay loop)

## 하이퍼 링크 삽입
    <a>
    웹페이지나 외부 사이트 연결
    <a href="연결할 링크">내용</a>
    1) target
        _blank 새로운 탭 or 창
        _self 현재 탭 or 창
        _parent 현재 화면을 불러낸 부모탭 or 창, 없으면 현재 탭 or 창
        _top 최상위 탭 or 창, 없으면 현재 탭 or 창
    2) title
        커셔를 올렸을 때 나온느 설명
    3) id
        같은 페이지에서 이동할 때 사용
    
## 폼 입력
    <form>
    <form [속성="속성값"]>여러 폼 요소</form>
    1) method = 
        get 사용자 입력 내용이 드러나게 서버로 넘겨줌
        post 사용자 입력 내용이 드러나지 않게 서버로 넘겨줌
    2) name =
    자바스크립트로 폼 이름 지정
    3) action =
    서버 프로그램 지정
    4) target = 
    열어볼 파일 위치 지정
    5) autocomplete =
    자동 완성 기능 지정(기본값 on)
    6) <fieldset>
    폼 내부에서 구역을 나눔
        <legend> 구역 제목 붙이기

## 레이블 붙이기
    <label>레이블명<input></label>
    <label for="id명">레이블명<input id="id명"></label>

## input
    type =
    1) text
        한 줄 텍스트
    2) password
        비밀번호
    3) search
        검색
    4) url
        url
    5) email
        이메일 주소
    6) tel
        전화번호
    7) checkbox
        체크박스 (중복)
    8) radio
        라디오 버튼 (unique)
    9) number
        숫자 스핀 박스(버튼으로 조절)
    10) range
        숫자 슬라이드 막대
    11) date
    	local - 연, 월, 일
    12) month
    	local - 연, 월
    13) week
    	local - 연, 주
    14) time
    	local - 시, 분, 초, 분할 초
    15) datetime
    	UTC - 연, 월, 일, 시, 분, 초, 분할 초
    16) datetime-local
    	local - 연, 월, 일, 시, 분, 초, 분할 초
    17) submit
    	전송 버튼
    18) reset
    	리셋 버튼
    19) image
    	submit 버튼 이미지
    20) button
    	일반 버튼
    21) file
    	파일 첨부 버튼
    22) hidden
    	사용자에게 보이지 않는 값 필드

### text, password와 같이 쓰이는 속성들
    1) size=
        화면에 출력할 글자 수
    2) value=
        text 필드에 보여줄 내용, password에서 사용 안함
    3) maxlength=
        최대 입력 가능한 글자 수

### checkbox, radio랑 같이 쓰이는 속성들
    1) value=
    	서버에 전달될 값
    2) checked=
    	기본으로 선택하고 싶은 항목
    3) name=
    	radio 전용, 여러 옵션의 공통 이름

### submit, reset와 같이 쓰이는 속성들
    1) value=
        버틍에 표시할 내용

### image와 같이 쓰이는 속성들
    1) src=
    	이미지 경로
    2) alt=
    	대체 텍스트

### button와 같이 쓰이는 속성들
    1) value=
    	버튼에 표시할 내용
    2) onclick=
    	클릭 시 실행할 JS함수

### <input>의 다른 주요 속성들
    1) autofocus=
    	페이지를 불러오자마자 마우스 포인터가 표시
        예) autofocus
    2) placeholder=
    	힌트를 표시, 내용을 입력하면 사라짐
        예) 아이디를 입력하세요.
    3) readonly=
    	읽기 전용
        예) readonly="readonly"
            readonly="true"
    4) required=
    	필수 입력 필드
        예) required="required"
            required

## 이외 주요 태그들
    <textarea>
    여러 줄의 텍스트 입력 영역
        1) rows=	세로 줄 수, 길 경우 스크롤 막대가 생성됨
        2) cols=	가로 너비(문자 단위)

    <select>
    드롭다운 목록 생성
        1) size=	항목 개수
        2) multiple=	둘 이상의 항목을 선택
    <option>
    옵션
        1) value=	서버에 전달될 값
        2) selected=	기본 선택 항목
    <datalist>	
    미리 입력된 데이터 목록
    <option>	
        1) value=	서버에 전달될 값
    <button>	
    버튼
        1) type="submit"	폼을 서버로 전송
        2) type="reset"	폼 초기화
        3) type="button"	일반 버튼, <input type="button">과 같음


        