# Youngble Metabus Blog

## description

- 나만의 메타버스 공간을 활용하는 블로그로 개인게시물, 미니게임, 채팅 등 다양한 컨텐츠 도입 및 개인 운영 서비스
- 홀로 운영하며 자유롭게 여러 Tech stack을 적용해보자는 취지와 나만의 게임 제작 및 1인개발 목표
- 성능최적화를 위한 여러가지 테스트
- 계획 설계 및 관리 업무

## architectures

서버
정의: 데브옵스 아키텍쳐, 도메인 설계 아키텍쳐 정의 추후 분리

- AWS EC2
- 추후 스펙 결정

---

웹
정의: 폴더의 구조, 컴포넌트 구조를 비즈니스 로직과 단순 컴포넌트를 어떤 패턴을 사용할지 정의.
해당 프로젝트의 특성상(여러가지 시도하려는 목적) 여러가지 패턴을 써볼려고함.

- Custom Hook Pattern
- Presentation / Container Component Pattern
- 다른 패턴 이해후 추후 추가(State Reducer Pattern, Props Getters Pattern 등)
- Apollo, axios 통신
- TDD 진행: scope는 unit Test & UI Component Test MVP로 진행 추후 통합/E2E 여부결정

---

앱
정의: 하이브리드앱으로 웹과앱 통신 전략, 모바일의 기능(Ex: 카메라)은 살리되 웹으로 서비스

- Webview 사용 Android/Ios 앱 배포 / 브릿지 사용 웹앱 통신

---

## Contents/Function

- 나의 경력 history 온보딩 페이지
- 블로그 게시물 페이지 (기존 tistory 글 이관) : 페이지네이션
- 프로젝트 구현/성과 기록 포스트잇 : 무한스크롤
- 채팅 페이지
- 미니게임 페이지
- 테스트 토스페이먼츠 결제 기능
- Todo 리스트 페이지
- 화상/영상 스트리밍 페이지
- 로그인 JWT/소셜
- 구글 Ads 광고
- 자신의 캐릭터 : 360회전, 숨쉬기애니메이션 / 랜덤 뽑기 아이템 장착
- 이미지/영상 upload & fetch display media
- 푸쉬알림 / 알림톡
- 브릿지 페이지 & 딥링(AirBridge.io) / Analytics
- 커뮤니티 게시판 / 페이지네이션

## as-is Tech Stack

웹

- next.js
- typescript
- css-module
- scss

---

앱(추후 추가)

- React Native

---

서버

- 자바
- 스프링/스프링부트
- 추후 추가

## to-be Tech Stack

(when I apply one of these stacks, I will move it up on 'as-is Tech Stack')

웹

- react-query \*MUST
- storybook for CDD (Component Driven Development) \*MUST
- jest for TDD (Test Driven Development)
- Three.js
- canvas
- websocket/socket.io
- webrtc
- graphQL
- recoil / context API
- view transitions API (페이지 이동간 에니메이션)
- web worker API 백그라운드 처리 

---

앱

---

서버

## Optimization

- 컴포넌트 재사용
- 사용자경험 개선 List : Intersection Observer를 사용 전 후

## Plan

- 애자일 스프린트
- Notion | Jira
- 개인 Todo 작성을 위한 Microsoft Todo앱

## Strategy

- MVP Minimum Viable Product로써 최소 스펙 및 기능으로 먼저 배포 후 phase 단계로 점차 진행
