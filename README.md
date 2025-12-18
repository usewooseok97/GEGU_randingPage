# 고양이 HODU 랜딩페이지

귀여운 고양이 HODU를 소개하는 반응형 랜딩페이지 프로젝트입니다.

## 프로젝트 구조

```
랜딩페이지/
├── index.html              # 메인 HTML 파일
├── css/
│   ├── recommendReset.css  # CSS 리셋 파일
│   ├── 랜딩페이지.css       # 데스크톱 스타일
│   └── 모바일랜딩페이지.css # 모바일 스타일 (570px 이하)
└── asset/
    └── 고양이/             # 이미지 리소스
        ├── logo.png
        ├── cat-boxhat.png
        ├── cat-onbed.png
        ├── cat-oncattower.png
        ├── cat-seewall.png
        ├── cat-seeme.png
        ├── cat-onlyhead.png
        └── icon-*.png      # SNS 아이콘들
```

## 주요 기능

### 1. 반응형 디자인
- **데스크톱**: 일반 네비게이션 메뉴
- **모바일** (570px 이하): 햄버거 메뉴 + 슬라이드 네비게이션

### 2. 헤더 (Header)
- 로고 이미지
- 네비게이션 메뉴: Home, About, Support, Download
- 햄버거 버튼 (모바일)
- 모바일 슬라이드 메뉴

### 3. 메인 콘텐츠 (Main)

#### Section 1
- 메인 타이틀과 설명
- 다운로드 버튼
- 고양이 이미지 (cat-boxhat.png)

#### Section 2
- 부제목과 설명
- 침대 위 고양이 이미지 (cat-onbed.png)

#### Section 3
- 갤러리 그리드 (3개 이미지)
- Learn More 버튼

#### Subscribe Section
- 뉴스레터 구독 폼
- 이메일 입력 필드
- Subscribe 버튼

### 4. 모달 (Modal)
- 구독 완료 시 표시되는 감사 메시지
- 고양이 이미지와 함께 표시
- "OK! I Love HODU" 버튼으로 닫기

### 5. 푸터 (Footer)
- 로고
- SNS 링크 (Instagram, Facebook, YouTube, Blog)
- 네비게이션 링크 (About, Support, Blog)

### 6. 맨 위로 가기 버튼
- 스크롤 시 표시되는 상단 이동 버튼

## JavaScript 기능

### 모달 제어
```javascript
// Subscribe 버튼 클릭 → 모달 열기
// OK 버튼 클릭 → 모달 닫기
// 모달 외부 클릭 → 모달 닫기
```

### 모바일 메뉴 제어
```javascript
// 햄버거 버튼 클릭 → 메뉴 열기
// 닫기 버튼 클릭 → 메뉴 닫기
// 메뉴 링크 클릭 → 메뉴 자동 닫기
```

## CSS 특징

### 주요 색상 변수
- `--button-color`: #d97652 (주황색)
- `--button-background`: #263140 (다크 블루)

### 반응형 중단점
- **데스크톱**: 기본 (570px 초과)
- **모바일**: 570px 이하

### 주요 스타일 클래스
- `.downloadbtn`: 다운로드/액션 버튼 스타일
- `.sr-only`: 스크린 리더 전용 텍스트
- `.shadows`: 이미지 그림자 효과
- `.bolds`: 굵은 제목 스타일
- `.regulars`: 일반 텍스트 스타일

## 접근성 (Accessibility)

- 시맨틱 HTML 태그 사용 (`header`, `main`, `section`, `footer`, `nav`)
- `sr-only` 클래스로 스크린 리더 지원
- `aria-label` 속성으로 버튼 설명 제공
- `aria-required` 속성으로 필수 입력 필드 표시
- `alt` 속성으로 모든 이미지에 대체 텍스트 제공

## SEO 최적화

- Open Graph 메타 태그 설정
- 적절한 `meta description` 작성
- 시맨틱 HTML 구조
- `lang="ko-KR"` 언어 설정

## 브라우저 호환성

- 모던 브라우저 지원 (Chrome, Firefox, Safari, Edge)
- CSS Grid 및 Flexbox 사용
- HTML5 `<dialog>` 요소 사용

## 사용 방법

1. 프로젝트 폴더에서 `index.html` 파일을 브라우저로 열기
2. 또는 로컬 서버 실행:
   ```bash
   # Python 3
   python -m http.server 8000

   # 브라우저에서 http://localhost:8000 접속
   ```

## 개발 참고사항

- 이미지 파일은 `./asset/고양이/` 경로에 위치
- CSS는 모듈화되어 데스크톱/모바일 분리
- 바닐라 JavaScript 사용 (외부 라이브러리 없음)
- 모바일 우선 접근 방식

## 향후 개선 가능 사항

- [ ] 폼 유효성 검사 강화
- [ ] 이미지 lazy loading
- [ ] 애니메이션 효과 추가
- [ ] 다국어 지원
- [ ] 백엔드 연동 (이메일 구독 기능)
