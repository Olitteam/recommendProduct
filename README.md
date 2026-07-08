# SLOOM 맞춤 추천 퀴즈

## 파일 구조
```
sloom-quiz/
├── index.html          ← 고객용 설문 페이지
├── api/
│   └── recommend.js    ← AI 추천 서버 함수 (수정 불필요)
├── vercel.json         ← Vercel 설정 (수정 불필요)
└── README.md
```

## 배포 방법

### 1단계 — GitHub에 올리기
1. github.com 접속 → 우측 상단 **+** → **New repository**
2. Repository name: `sloom-quiz`
3. **Create repository** 클릭
4. 이 폴더의 파일 전체를 업로드

### 2단계 — Vercel 연결
1. vercel.com 접속 → **Continue with GitHub** 로그인
2. **Add New Project** → `sloom-quiz` 저장소 선택
3. **Deploy** 클릭

### 3단계 — API 키 등록
1. Vercel 대시보드 → 해당 프로젝트 → **Settings** → **Environment Variables**
2. 추가:
   - Name: `ANTHROPIC_API_KEY`
   - Value: `sk-ant-xxxxxxxx` (Anthropic 콘솔에서 발급)
3. **Save** → **Redeploy**

완료! Vercel이 제공하는 URL로 접속하면 동작합니다.

## 내용 수정 방법
`index.html` 상단의 `CONFIG` 객체만 수정하세요.
- 질문/선택지 추가·삭제: `questions` 배열
- 제품 정보·링크 변경: `products` 배열
- 브랜드명·타이틀 변경: `brand`, `hero_title`, `hero_desc`
