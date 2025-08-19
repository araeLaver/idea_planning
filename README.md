# 아이디어 매니저 - 창의적 아이디어 관리 시스템

## 📝 프로젝트 소개

**아이디어 매니저**는 창의적인 아이디어를 체계적으로 관리하고 추적할 수 있는 개인용 웹 애플리케이션입니다. 
일상에서 떠오르는 아이디어들을 놓치지 않고 기록하고, 체계적으로 분류하여 발전시킬 수 있도록 도와줍니다.

## ✨ 주요 기능

### 🎯 대시보드
- **실시간 통계**: 아이디어 현황을 한눈에 파악
- **상태별 분포**: 파이 차트로 아이디어 진행 상황 시각화
- **우선순위별 분포**: 바 차트로 중요도별 아이디어 현황
- **최근 활동**: 최근 수정된 아이디어 목록
- **인기 카테고리 & 태그**: 자주 사용하는 분류 확인

### 💡 아이디어 관리
- **상세 정보 기록**: 제목, 설명, 카테고리, 태그, 우선순위 설정
- **상태 관리**: 초안 → 진행중 → 완료 → 보관됨 단계별 관리
- **검색 기능**: 제목, 내용, 태그로 빠른 검색
- **필터링**: 카테고리, 상태, 우선순위별 필터링

### 📋 칸반보드
- **시각적 관리**: 드래그 앤 드롭으로 상태 변경
- **직관적 인터페이스**: 아이디어 진행 상황을 한눈에 파악
- **실시간 업데이트**: 변경사항 즉시 반영

### 📅 일일메모 시스템
- **오늘의 메모**: 대시보드에서 바로 작성 가능
- **전체 메모 관리**: 날짜별 메모 기록 및 관리
- **편집/삭제**: 과거 메모 수정 및 삭제 기능
- **검색 가능**: 메모 내용으로 검색

### 🔍 고급 검색
- **통합 검색**: 모든 아이디어와 메모를 한 번에 검색
- **필터 조합**: 여러 조건을 조합한 정밀 검색
- **검색 히스토리**: 최근 검색 기록 저장

### 📊 기록 및 통계
- **활동 히스토리**: 모든 변경 사항 추적
- **통계 대시보드**: 생산성 지표 확인
- **진행률 추적**: 목표 대비 완성도 측정

## 🛠 기술 스택

### Frontend
- **React 18** - 사용자 인터페이스
- **TypeScript** - 타입 안전성
- **React Router** - 라우팅
- **Tailwind CSS** - 스타일링
- **Recharts** - 데이터 시각화
- **Lucide React** - 아이콘
- **date-fns** - 날짜 처리

### Build & Development
- **Vite** - 빌드 도구
- **ESLint** - 코드 품질
- **Prettier** - 코드 포매팅
- **Vitest** - 테스팅

### Storage
- **LocalStorage** - 브라우저 로컬 저장소
- **Firebase** (선택사항) - 클라우드 저장소

## 🚀 설치 및 실행

### 필수 요구사항
- Node.js 16+ 
- npm 또는 yarn

### 설치
```bash
# 저장소 클론
git clone https://github.com/araeLaver/idea_planning.git
cd idea_planning/idea-manager

# 의존성 설치
npm install

# 개발 서버 실행
npm run dev
```

### 빌드
```bash
# 프로덕션 빌드
npm run build

# 빌드 결과 미리보기
npm run preview
```

### 테스트
```bash
# 테스트 실행
npm test

# 테스트 커버리지
npm run test:coverage
```

## 📁 프로젝트 구조

```
idea-manager/
├── public/                    # 정적 파일
│   ├── idea-icon.svg         # 파비콘
│   └── manifest.json         # PWA 매니페스트
├── src/
│   ├── components/           # 공통 컴포넌트
│   │   ├── Layout.tsx       # 레이아웃
│   │   ├── AIAssistant.tsx  # AI 도우미
│   │   └── ...
│   ├── contexts/            # React Context
│   │   ├── DataContext.tsx  # 데이터 관리
│   │   └── ThemeContext.tsx # 테마 관리
│   ├── hooks/               # 커스텀 훅
│   ├── pages/               # 페이지 컴포넌트
│   │   ├── Dashboard.tsx    # 대시보드
│   │   ├── IdeaList.tsx    # 아이디어 목록
│   │   ├── KanbanBoard.tsx # 칸반보드
│   │   ├── DailyMemos.tsx  # 일일메모
│   │   └── ...
│   ├── services/            # 서비스 로직
│   │   ├── firebaseService.ts
│   │   └── aiService.ts
│   ├── utils/               # 유틸리티
│   ├── types/               # TypeScript 타입
│   └── styles/              # 스타일
├── .github/workflows/       # GitHub Actions
└── package.json
```

## 🎨 주요 특징

### 반응형 디자인
- 모바일, 태블릿, 데스크톱 모든 기기에서 최적화
- 다크모드/라이트모드 지원

### 오프라인 지원
- PWA(Progressive Web App) 구현
- 오프라인에서도 기본 기능 사용 가능

### 데이터 백업
- 로컬 스토리지 자동 백업
- 데이터 내보내기/가져오기 기능

### 접근성
- 키보드 내비게이션 지원
- 스크린 리더 호환
- ARIA 레이블 적용

## 🔧 환경 설정

### 환경 변수
```bash
# .env.local 파일 생성
VITE_FIREBASE_API_KEY=your_api_key
VITE_FIREBASE_AUTH_DOMAIN=your_domain
VITE_FIREBASE_PROJECT_ID=your_project_id
```

### Firebase 설정 (선택사항)
1. Firebase 프로젝트 생성
2. Firestore 데이터베이스 설정
3. 환경 변수 설정

## 📱 PWA 기능

이 애플리케이션은 PWA로 구현되어 있어 다음과 같은 기능을 제공합니다:

- **홈 화면에 추가**: 네이티브 앱처럼 사용
- **오프라인 캐싱**: 인터넷 없이도 기본 기능 사용
- **푸시 알림**: 중요한 업데이트 알림
- **자동 업데이트**: 새 버전 자동 감지 및 업데이트

## 🧪 테스트

```bash
# 단위 테스트
npm run test

# 통합 테스트
npm run test:integration

# E2E 테스트
npm run test:e2e

# 테스트 커버리지 확인
npm run test:coverage
```

## 🚀 배포

### GitHub Pages
```bash
npm run build
npm run deploy
```

### Vercel
```bash
# Vercel CLI 설치
npm i -g vercel

# 배포
vercel --prod
```

### Netlify
```bash
# Netlify CLI 설치
npm i -g netlify-cli

# 배포
netlify deploy --prod --dir=dist
```

## 🤝 기여하기

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 라이선스

이 프로젝트는 MIT 라이선스 하에 배포됩니다. 자세한 내용은 [LICENSE](LICENSE) 파일을 참조하세요.

## 🆕 업데이트 로그

### v1.0.0 (2024-08-19)
- 초기 버전 출시
- 기본 아이디어 관리 기능
- 대시보드 및 통계 기능
- 일일메모 시스템
- 칸반보드 구현
- PWA 지원

## 📞 연락처

프로젝트 링크: [https://github.com/araeLaver/idea_planning](https://github.com/araeLaver/idea_planning)

## 🙏 감사의 말

- [React](https://reactjs.org/)
- [Vite](https://vitejs.dev/)
- [Tailwind CSS](https://tailwindcss.com/)
- [Lucide Icons](https://lucide.dev/)
- [Recharts](https://recharts.org/)

---

⭐ 이 프로젝트가 유용하다면 Star를 눌러주세요!