![배너](https://i.postimg.cc/0NMmwBB9/moiza-Post.png)

# 소마고생 이력서 공유 서비스(모이자)

소프트웨어마이스터고생들의 이력서를 볼 수 없을까? 라는 아이디어에서 시작하여,<br>
소마고생들의 이력서를 열람할 수 있는 웹 서비스를 기획하였습니다. 

[운영중인 서비스 바로가기](https://www.moiza.kro.kr)  
[API 명세서 바로가기](https://assorted-color-425.notion.site/API-39f31b5d075c47129f84a5ae45bf4711)

## 세부 성과
2025.04 | 모이자 서비스 배포  
2025.04 | 서비스 가입자 100+명

## 기능

### 이력서
- 이력서 생성, 수정, 삭제 및 유저 상태별 조회, 페이징 처리
### 유저
- 소셜 로그인, 이력서 PDF 추출, 끌올 기능, 유저 정보 관리
### 좋아요
- 이력서 좋아요 등록 및 좋아요 리스트 조회 기능

## 시스템 아키텍처

### Querydsl 기반의 이력서 동적 필터링 시스템 설계  

**정렬, 기술 스택, 학교, 재직 여부를 가지고 이력서 동적 필터링**  
- 구현 - BooleanExpression을 사용하여 null에 대한 처리와 동적 필터링 구현
- 회고 - null-safe한 쿼리 작성과 가독성이 향상됨

<img src="https://i.postimg.cc/fLrM9MJb/image.png" width="50%" />  

<br>

**유저 상태를 enum으로 정의 후 상태에 따라 필터링된 결과를 제공**  
<i>ex ) NOT_LOGGED_IN(0), LOGGED_IN(1), PORTFOLIO_COMPLETED(2), PORTFOLIO_PUBLISHED(3)</i>
- 구현  
  - 유저 상태 level을 기반으로 비교 연산자로 조회  
  - 유저별로 상태를 지정하여 상태에 맞는 리스트를 반환  
- 회고 - 추후에 유저 상태가 추가되더라도 유연성과 일관성 있는 단계 비교

<img src="https://i.postimg.cc/qRPMFk05/screenshot-3.png" width="50%" />  

## ERD
![erd](https://i.postimg.cc/8cLWKX8L/2025-04-25-10-42-26.png)

## 화면 설계

|                                 메인 페이지                                 |                             이력서 상세 페이지                             |
|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
|    <img width="329" src="https://i.postimg.cc/gjbLZywj/image.png"/>    | <img width="329" src="https://i.postimg.cc/y8pJPCJw/image.png"/> |  
|                                 이력서 등록 페이지                                 |                             마이 페이지                             |  
| <img width="329" src="https://i.postimg.cc/FsD1rXx7/image.png"/> | <img width="329" src="https://i.postimg.cc/dtpPmWs5/image.png"/> |

## 팀원
|                             Backend                             |                               Backend                               |                               Frontend                               |                            Frontend                             |                            Designer                             |
|:---------------------------------------------------------------:|:--------------------------------------------------------------------:|:--------------------------------------------------------------------:|:---------------------------------------------------------------:|:---------------------------------------------------------------:|
| ![image](https://avatars.githubusercontent.com/u/127452485?v=4) | ![image](https://avatars.githubusercontent.com/u/129156398?v=4) | ![image](https://avatars.githubusercontent.com/u/128370710?v=4) | ![image](https://avatars.githubusercontent.com/u/107257423?v=4) | ![image](https://avatars.githubusercontent.com/u/128601631?v=4) |
|                [안예성](https://github.com/anys34)                 |                 [김명진](https://github.com/4mjeo)                  |                  [강민지](https://github.com/rkdalswl718)                  |               [육기준](https://github.com/six-standard)               |                [김수아](https://github.com/0ccssu)                |
