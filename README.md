# 🎙️ 1-Minute English Monologue (1분 영어 혼잣말 첨삭 & 단어장)

> **바쁜 직장인을 위한 1분 영어 스피킹 루틴**  
> 매일 1분 동안 랜덤 주제로 혼잣말을 녹음하면, 브라우저가 실시간으로 인식(STT)하고, AI가 의도를 파악해 **원어민스러운 2단계 표현(Casual/Business)**으로 교정해주며, **플래시카드 단어장과 마크다운 노트**로 자동 축적해줍니다.

---

## ⚡ 빠른 실행 방법 (Zero Setup)

별도의 Node.js 설치나 복잡한 빌드 과정 없이, 브라우저에서 즉시 실행할 수 있습니다:

1. **`run_app.bat`** 파일을 더블 클릭하여 실행하거나,
2. **`index.html`** (또는 `1-minute-monologue.html`) 파일을 크롬/엣지 브라우저로 열기만 하면 즉시 작동합니다.

> 💡 **로컬 개발 서버로 띄우고 싶을 때:**  
> 터미널에서 `python -m http.server 3000` 실행 후 브라우저에서 `http://localhost:3000/1-minute-monologue/` 접속

---

## 🌟 주요 기능 및 워크플로우

### 1. 오늘의 랜덤 주제 뽑기 (Topic Generator)
- **카테고리 필터**: `전체`, `직장생활 & 비즈니스`, `일상 & 취미`, `재테크 & 트렌드`, `오픽(OPIc) 돌발 주제`
- 직장인이 실제 겪는 딜레마와 흥미로운 질문 40여 종 수록
- '🎲 랜덤 뽑기' 또는 '직접 입력'으로 오늘 하고 싶은 말 선택

### 2. 1분 타이머 & 음성 녹음 (Speaking & STT)
- **60초 원형 카운트다운 타이머**와 시각적 마이크 파형(Web Audio API)
- 브라우저 내장 `Web Speech API`를 활용한 실시간 음성 인식
- **핵심 UX (한/영 혼용 에디터)**: 말문이 막혀 한국어로 얼버무렸거나 추가하고 싶은 단어/문맥을 녹음 후 에디터 박스에서 자유롭게 수정·보완 가능

### 3. AI 3단계 심층 첨삭 파이프라인
1. **💡 내가 말하려던 핵심 의도 요약**: 어설픈 발화에서도 원래 전하려던 요점을 한국어로 명확히 정리
2. **🗣️ 수준별 원어민 재구성**:
   - **Natural Casual**: 동료와 편하게 스몰토크할 때 쓰는 구어체
   - **Professional Business**: 회의, 프레젠테이션, 오픽 AL 타깃 논리적 표현
   - 🔊 원어민 TTS 발음 듣기 지원
3. **🔍 교정 포인트 & Diff 비교**:
   - `[ 취소선 콩글리시 ] ➔ [ 초록색 원어민 표현 ]` 인라인 배지
   - 왜 어색했는지 짚어주는 직관적인 **원포인트 코칭**
4. **📚 핵심 구동사 & 어휘 3~5개**:
   - 주제 맞춤형 표현, 한국어 의미, 실전 예문 제공
   - `[전체 단어장 자동 저장]` 또는 개별 `[+ 플래시카드 추가]`

### 4. 복습 플래시카드 & 인터랙티브 영작 퀴즈
- **🃏 3D 부드러운 카드 플립 모드**: 앞면(한국어 상황) ➔ 뒷면(원어민 표현 & 예문 + 발음 듣기)
- **✍️ 영작 / 빈칸 퀴즈 모드**: 한국어 상황을 보고 영어 표현을 직접 타이핑하여 정답 확인 & 초성 힌트 제공
- **📋 목록 뷰**: 전체 단어 검색 및 상태 관리 (`외웠어요` / `다시보기`)

### 5. 히스토리 & 연속 학습 스트릭 (통계)
- **🔥 연속 학습일 스트릭**: 매일 1분 스피킹 달성 시 불꽃 카운트 및 주간 잔디(출석체크)
- **일자별 세션 히스토리**: 과거 발화문, 첨삭 리포트 다시보기 및 TTS 청취
- **마크다운(Markdown) 원클릭 복사**: Logseq, Obsidian, Notion에 바로 붙여넣을 수 있는 계층형 불릿 포맷
- **JSON 백업/복원**: 브라우저 캐시 삭제에 대비한 원클릭 데이터 백업 및 복원 지원

---

## 🔑 AI 연동 설정

우측 상단 **[⚙️ AI 설정]** 버튼을 통해 언제든 변경 가능합니다:

1. **Google Gemini (권장)**: 무료 티어로 초고속 응답을 제공하는 `gemini-2.5-flash` 모델 연동 ([Google AI Studio](https://aistudio.google.com/app/apikey)에서 무료 키 발급 가능)
2. **OpenAI GPT**: `gpt-4o-mini` 모델 연동
3. **데모 모드 (키 없음)**: API Key 없이도 구조 확인용 실감 나는 Mock AI 첨삭 데이터를 무제한 무료 테스트 가능

*※ 입력하신 API Key는 외부 서버로 절대 전송되지 않으며, 사용자 브라우저의 `localStorage`에만 암호화 저장됩니다.*

---

## 🛠️ 기술 사양

| 항목 | 상세 사양 |
| :--- | :--- |
| **Frontend** | React 18, Tailwind CSS, Lucide Icons, Pretendard Font |
| **STT Engine** | Web Speech API (`SpeechRecognition` / `webkitSpeechRecognition`) |
| **TTS Engine** | Web Speech API (`SpeechSynthesisUtterance`) |
| **Audio Visualizer** | Web Audio API (`AudioContext`, `AnalyserNode`) |
| **AI LLM** | Google Gemini REST API & OpenAI REST API with JSON Mode |
| **Storage** | Browser `localStorage` (세션 히스토리, 플래시카드, 스트릭) |
