# week1
## 웹과 HTTP
- 웹 : 여러 컴퓨터가 서로 연결되어 정보를 공유하는 공간
    - 클라이언트 - 서버 패러다임.
    - 클라이언트 - 요청 -> 서버 / 서버 - 응답 -> 클라이언트
    - 요청을 보내면 클라이언트 / 요청을 받으면 서버. 상대대적임

- 프로토콜과 HTTP : 데이터 전송 방법을 명시해야함. 규칙이 필요함(프로토콜)
    - 웹에서는 HTTP라는 프로토콜(즉, 규칙)을 사용함
    - HTTP Method : 데이터를 다루는 방법/ URL : 다룰 데이터의 위치 (받는 주소)
    - GET : 조회 / POST : 생성 / PUT : 있으면 교체, 없으면 생성 / PATCH : 수정 / DELETE : 삭제
    - URL 구조 : 프로토콜 :// 서버 주소(도메인) / 서버 내 데이터 위치 ? query string
    
    - HTTP 헤더 : 통신 자체에 대한 정보 / HTTP 바디 : 주고 받으려는 데이터
    - 상태코드 : 200 (ok) 2XX (성공) / 4XX (client 오류) / 500 (서버 에러)

## 프론트엔드와 백엔드
- 프론트엔드 : 데이터를 백엔드에 요청
- 백엔드 : DB에서 가져온 컨텐츠 데이터를 프론트에게 응답

## REST API
- ***API(Application Programming Interface) : 어플리케이션에서 원하는 기능을 수행하기 위해 어플리케이션과 소통하는 방법을 정의한 것***
- REST API : REST 아키텍쳐를 따르도록 설계한 API
    - URL : 조작할 데이터 (명사) / HTTP Method : 데이터에 대한 행위 (동사)


# API 설계하기
1. 회원가입하기     POST /join
2. 로그인하기   POST /login
3. 할 일 생성하기   POST /todo
4. 할 일 조회하기   GET /todo/list
5. 할 일 수정하기   PATCH /todo/{todo}
6. 할 일 삭제하기   DELETE /todo/{todo}
7. 할 일 체크하기   POST /todo/{todo}/check
8. 할 일 체크 해제하기  POST /todo/{todo}/uncheck
9. 친구 찾기    GET /search/friend
10. 친구 팔로우하기     POST /friend_list/{friend}/follow
11. 친구 언팔로우하기   POST /friend_list/{friend}unfollow
12. 나의 친구 리스트 조회하기   GET /friend_list
13. 특정 친구의 할 일 조회하기      GET /friend_list/{friend}/list