# ![RealWorld Example Applications](media/realworld.png)

[![Travis](https://img.shields.io/travis/gothinkster/realworld.svg)](https://travis-ci.org/gothinkster/realworld) [![Gitter](https://img.shields.io/gitter/room/realworld-dev/main.svg)](https://gitter.im/realworld-dev/main) [![Twitter](https://img.shields.io/twitter/follow/gothinkster.svg?style=social&label=Follow)](https://twitter.com/gothinkster)

<p align="center">
<img src="media/stacks_hr.gif"  />
</p>

<a href="https://demo.realworld.io/"><img src="media/conduit_l.png" align="right" width="250px" /></a>

### See how *the exact same* Medium.com clone (called [Conduit](https://demo.realworld.io)) is built using any of our supported [frontends](#frontends) and  [backends](#backends). Yes, you can mix and match them, because **they all adhere to the same [API spec](spec/)** 😮😎

 대부분의 "todo" 데모는 프레임워크의 기능을 아주 잘 보여 주지만, 통상적인 실제 응용 프로그램을 빌드하는 데 필요한 지식과 관점을 전달하지는 않습니다 .

RealWorld는 어떤 프론트 엔드 (React, Angular 2, & More)와 백엔드 (Node, Django, & More)를 선택하고 " Conduit " 이라는 아름답게 디자인 된 풀 스택 응용 프로그램을 실세계에 어떻게 적용 할 수 있는지 살펴봄으로써 이를 해결합니다 .



# 프로젝트 개요

"도관 (Conduit)"은 소셜 블로깅 사이트 (예 : Medium.com 클론)입니다. 인증을 포함하여 모든 요청에 대해 사용자 정의 API를 사용합니다. [https://demo.realworld.io](https://demo.realworld.io/) 에서 라이브 데모를 볼 수 있습니다. 

**일반적인 기능 :**

- JWT를 통한 User 인증 (설정 페이지의 로그인 / 가입 페이지 + 로그아웃 버튼)

- CRU * User (가입 및 설정 페이지 - 삭제 필요 없음)

- CRUD Article

- CR * D Article에 대한 의견 (업데이트 필요 없음)

- 페이징된 Article 목록 GET, display

- Article 즐겨찾기

- 다른 User 팔로우

  

## 더 알아보기

- ["RealWorld 소개 🙌"](https://medium.com/@ericsimons/introducing-realworld-6016654d36b5) 에릭 시몬스

- 모든 자습서는 모든 프론트 엔드 및 백엔드의 모듈성을 보장하기 위해 동일한 [API 사양에 따라 작성](https://github.com/gothinkster/realworld/blob/master/api) 되었습니다.

- 모든 프론트 엔드는 동일한 UI / UX에 대해 동일한 핸드 메이드 [부트 스트랩 4 테마](https://github.com/gothinkster/conduit-bootstrap-template) 를 사용합니다.

  

## 프론트엔드 Spec

### 호스팅 된 API 사용

 `https://conduit.productionready.io/api`!

### 라우팅 지침

- 홈페이지 (URL : /#/)

  - 태그 목록
  - 피드, 글로벌 또는 태그 중 하나에서 가져온 Article 목록
  - Article 목록의 페이지네이션

- 로그인 / 가입 페이지  (URL: /#/login, /#/register)

  - JWT를 사용 (localStorage에 토큰 저장).
  - 세션 / 쿠키 기반 인증으로 쉽게 인증 전환 가능

- 설정 페이지 (URL : /#/settings)

- Article 작성 / 편집을 위한 에디터 페이지 (URL : /#/editor, /#/editor/article-slug-here)

- Article 페이지 (URL : /#/article/article-slug-here)

  - Article 삭제 버튼 (Article 작성자에게만 표시)
  - 서버 클라이언트 측에서 마크 다운 렌더링
  - 페이지 하단의 댓글 섹션
  - 댓글 삭제 버튼 (댓글 작성자에게만 표시됨)

- 프로필 페이지 (URL : /#/profile/:username, /#/profile/:username/favorites)

  - 기본 사용자 정보 표시

  - 작성자가 만든 Article 또는 작성자가 즐겨찾기한 Article 목록

    

## 백엔드 Spec

모든 백엔드 구현은 [API Spec](https://github.com/gothinkster/realworld/tree/master/api) 을 준수해야합니다.

편의를 위해 앱을 빌드 할 때 API 엔드포인트를 테스트하는 데 사용할 수 있는 [postman 컬렉션](https://github.com/gothinkster/realworld/blob/master/api/Conduit.postman_collection.json) 이 있습니다.


# License
All of the codebases are **MIT licensed** unless otherwise specified.

<br />

[![Brought to you by Thinkster](media/end.png)](https://thinkster.io)
