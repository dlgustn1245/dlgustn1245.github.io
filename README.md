# lhsdev.info

Unity 콘텐츠 개발자 이현수의 포트폴리오 사이트입니다.

**사이트: [lhsdev.info](https://lhsdev.info)**

## 구성

빌드 과정이 없는 정적 사이트입니다. 화면, 스타일, 스크립트가 모두 `index.html` 한 파일에 들어 있습니다.

| 파일 | 역할 |
|---|---|
| `index.html` | 사이트 전체 (HTML, CSS, JavaScript) |
| `CNAME` | GitHub Pages 커스텀 도메인 (`lhsdev.info`) |

외부 서비스

- 이미지·영상: Cloudinary
- 문의 폼 전송: Formspree
- 글꼴: Noto Serif KR (Google Fonts), Pretendard

## 프로젝트 추가·수정

작업 목록과 상세 화면은 `index.html` 안의 `projects` 배열로 만들어집니다. 배열 순서가 곧 화면 순서(번호)입니다.

| 필드 | 설명 |
|---|---|
| `name`, `type`, `summary` | 카드 제목, 분류, 소개 문장 |
| `role`, `org`, `period` | 상세 화면의 역할, 소속, 기간 |
| `imgSrc` | 썸네일 이미지 |
| `imgFit` | 비우면 칸을 꽉 채움 / `'contain'` 로고처럼 여백을 두고 가운데 / `'fit'` 가로로 긴 화면 캡처를 자르지 않고 표시 |
| `pixel` | `true`면 픽셀아트 썸네일을 번지지 않게 표시 |
| `bg` | 썸네일 뒤 배경색 |
| `gallery` | 상세 화면 이미지·영상 주소 목록 (Cloudinary `video/upload` 주소는 영상으로 표시) |
| `desc` | 주요 구현 항목. `UL(LI('제목', '내용'), ...)` 형식 |
| `stack` | 기술 태그 |
| `link`, `linkLabel`, `repo` | 관련 링크, 링크 이름, GitHub 저장소 |

## 로컬에서 보기

`index.html`을 브라우저로 바로 열면 됩니다. 로컬 서버로 보려면 저장소 폴더에서 아래 명령을 실행합니다.

```bash
python -m http.server 5500
```

브라우저에서 `http://localhost:5500`을 엽니다.

## 배포

`main` 브랜치에 푸시하면 GitHub Pages로 자동 배포됩니다.
