# 국공립 재위탁 연간 서류 분석기

AI 기반 보육 문서 자동 분석 시스템

## 배포 방법 (Vercel)

### 1단계: GitHub에 올리기
1. GitHub에서 새 저장소(Repository) 만들기
2. 이 폴더의 파일들을 모두 업로드
   - `api/analyze.js`
   - `public/index.html`
   - `vercel.json`
   - `README.md`

### 2단계: Vercel 연결
1. [vercel.com](https://vercel.com) 접속
2. GitHub 계정으로 로그인
3. "Add New Project" 클릭
4. GitHub 저장소 선택
5. "Deploy" 클릭

### 3단계: API 키 환경변수 설정 (중요!)
1. Vercel 대시보드 → 프로젝트 선택
2. Settings → Environment Variables
3. 아래 변수 추가:
   - **Name**: `ANTHROPIC_API_KEY`
   - **Value**: `sk-ant-api03-...` (발급받은 API 키)
4. "Save" 클릭
5. Deployments → "Redeploy" 클릭

### 완료!
배포된 URL을 공유하면 누구나 API 키 없이 사용 가능합니다.

## 주의사항
- API 사용 비용은 환경변수에 설정한 API 키 계정으로 청구됩니다
- 불특정 다수에게 공개할 경우 Anthropic 콘솔에서 사용량 한도를 설정하세요
- console.anthropic.com → Settings → Limits에서 월 최대 사용량 설정 가능
