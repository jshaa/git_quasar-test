# git_quasar-test

Git 저장소 연동과 Quasar Framework(Vue 3) 프로젝트 구성을 연습하기 위해 만든 테스트 프로젝트입니다.
Quasar CLI로 생성한 기본 템플릿(로고 페이지 + 사이드 메뉴 레이아웃) 상태이며, 추가 기능은 구현되어 있지 않습니다.

> [git-test1](https://github.com/jshaa/git-test1) 저장소와 소스 코드가 동일합니다.

## 기술 스택

| 구분 | 사용 기술 |
|---|---|
| 프레임워크 | Quasar 2 (Vue 3), `@quasar/app-webpack` 3 |
| 라우팅 / 상태 관리 | Vue Router 4, Pinia 2 |
| HTTP | Axios (`src/boot/axios.js`, baseURL은 예제 값 `https://api.example.com`) |
| 요구 사항 | Node.js 12.22.1 이상, npm 6.13.4 이상 또는 Yarn 1.21.1 이상 |

## 프로젝트 구조

```
src/
  App.vue
  boot/axios.js          Axios 전역 등록
  layouts/MainLayout.vue 헤더 + 사이드 메뉴(Docs, GitHub 등 링크)
  pages/IndexPage.vue    메인(로고) 페이지
  pages/ErrorNotFound.vue 404 페이지
  router/                라우트 정의
  stores/                Pinia 스토어 예제
quasar.config.js         Quasar 빌드 설정
```

## 설치 및 실행

의존성 설치:
```bash
yarn
# 또는
npm install
```

개발 서버 실행(핫 리로드):
```bash
quasar dev
```

배포용 빌드(`dist/spa`에 생성):
```bash
quasar build
```

`quasar` 명령이 없으면 `npx quasar dev` 또는 `npm run dev` / `npm run build`로 실행합니다.

## 설정 변경

[Configuring quasar.config.js](https://v2.quasar.dev/quasar-cli-webpack/quasar-config-js) 참고.
