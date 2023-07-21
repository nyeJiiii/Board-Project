# 🔥 패스트캠퍼스 : 백엔드 개발 부트캠프 5기 과제 Spring 토이프로젝트 3


## 🗓️프로젝트 일정 : 7월 10일 (월) ~ 7월 21일 (금)

## 팀 구성

| Name | Github Link                           |
|------|---------------------------------------|
| 송태형  | [github](https://github.com/Ussu1112) |
| 오형석  | [github](https://github.com/brotherstone97) |
| 한혜지  | [github](https://github.com/bornin23) |
| 김주원  | [github](https://github.com/dali186)

## 프로젝트 환경

메인 서버 : `JDK11` `SpringBoot` `JPA` `SpringSecurity`   

관리자 서버: `MyBatis`

관리자 서버 레포 : [github](https://github.com/Ussu1112/KDTBE5_Spring_ToyProject3_admin)


## 프로젝트 요구사항

### 📄 유저 기능

1. 회원가입
    - [X]  [회원가입 페이지] 회원가입 구현 (id, username, password, email, nickName, role, createdAt, updatedAt) - role은 새싹 회원과 우수회원으로 구분 (디폴트 : 새싹회원, 게시글 수 10 개 이상 우수 회원)
2. 로그인
    - [X]  [로그인 페이지] 로그인 구현 (username, password)
3. 유저네임 중복체크
    - [X]  [회원가입 페이지] 동일 username 중복체크하기
4. 회원정보보기
    - [X]  [회원정보 페이지] username, email, role, createdAt 확인
5. 회원정보 수정하기
    - [X]  [회원정보 수정페이지] email, nickName 변경가능
6. 비밀번호 수정하기
    - [X]  [비밀번호 수정 페이지] 비밀번호 수정 구현

### 📄 게시판 기능 명세서

1. 게시글 카테고리
    - [X]  새싹회원 게시판, 우수회원 게시판 구현 (게시판은 2개이지만 하나의 화면을 공유해서 사용하고 카테고리로 구분함)
2. 게시글 쓰기
    - [X]  [게시글 쓰기 페이지] - 권한(새싹, 우수)에 따라 다른 게시판에 글이 적어짐 (썸머노트 적용)
3. 게시글 목록보기
    - [X]  [게시글 목록보기 페이지] 게시글 목록보기 (id, title, content, thumbnail, user의 nickName 화면에 보여야 함, content내용을 화면에 2줄이 넘어가면 Ellipsis(...)으로 스타일 변경, 정렬은 id순 Desc
4. 게시글 페이징
    - [X]  [게시글 목록보기 페이지] 페이지당 6개 게시글 보여야 함, 게시글은 Grid 형식으로 3개씩 카드(Card) 배치
5. 게시글 검색
    - [X]  [게시글 목록보기 페이지] 작성자(nickName), 제목(title), 내용(content)로 검색가능해야 함.
6. 게시글 상세보기
    - [X]  [게시글 상세보기 페이지] id, title, content, nickName, 댓글의 comment 리스트(id, comment, 댓글의 작성자 nickName) 이 화면에 보여야 함. 게시글 삭제버튼과 수정버
      튼 보여야 함(본인이 적은 글에 대해서만), 댓글 삭제버튼이 보여야함(본인이 적은 댓글에 대해서만)
7. 게시글 삭제하기
    - [X]  [게시글 상세보기 페이지] 본인이 적은 게시글만 삭제가능
8. 게시글 수정하기
    - [X]  [게시글 수정하기 페이지] title, content 수정 가능
9. 게시글 신고
    - [X]  [게시글 상세보기 페이지] 게시글 신고가능 (형태 : 욕설, 음란, 비방)
10. 댓글 쓰기
    - [X]  [게시글 상세보기 페이지] 댓글 쓰기 50자이내! , 댓글에 댓글을 작성할 수 있음. 대댓글 기능 구현 (depth 1까지)
11. 댓글 삭제
    - [X]  [게시글 상세보기 페이지] 댓글 삭제가능 (댓글은 수정은 없음)
12. 스케쥴러 등록
    - [X]  @Schedule 을 사용하여, 1분에 한번씩 게시글 수가 10개인데, 우수회원이 아닌 새싹회원 등급 자동 변경

### 📄 관리자 기능 명세서

1. 관리자 회원 권한 관리
    - [X]  회원의 role 변경 가능해야 함
2. 관리자 회원 Email 전송 관리
    - [X]  회원에게 email 전송 가능해야 함
3. 관리자 게시글 CRUD 관리
    - [X]  게시글 목록보기, 삭제하기, 숨기기/보이기, 블랙리스트(욕설) 등록 가능해야 함 (수정,
      상세보기는 구현할 필요 없음)
4. 관리자 게시글 통계 관리
    - [X]  유저의 게시글 수, 댓글 수를 볼 수 있고, 댓글수가 많은 유저 순, 게시글 수가 많은 유저
      순으로 정렬가능해야 함
5. 관리자 블랙리스트 고객 등록/해제
    - [X]  게시글 신고목록 페이지 구현, 해당 페이지에서 블랙리스트 고객 등록 및 해제 가능
