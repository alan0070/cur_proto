# SK다이렉트 신차 큐레이션 프로토타입

셀프계약 전환율 제고를 위한 신차 큐레이션 기능 인터랙티브 프로토타입입니다.

## 기능 구성

- **5단계 질문 흐름**: 이용목적 → 이용스타일(상품분기) → 예산 → 연료방식 → 동승인원
- **3개 상품 분기**: 신차장기렌트 / 1년렌트 / 타고PAY플러스
- **결과 화면**: 추천 차량 카드 + 상품 선택 탭 + 조건 시각화 + 3개 상품 비교 테이블
- **타고PAY 전용**: 연 1만km 저마일리지 구조 시각화

## 로컬 실행

```bash
# 별도 설치 없이 바로 열기
open index.html

# 또는 간단한 서버로
npx serve .
python3 -m http.server 8080
```

## GitHub Pages 배포 방법

### 1. 저장소 생성 및 Push

```bash
# 프로젝트 폴더로 이동
cd curation-prototype

# git 초기화
git init
git add .
git commit -m "init: SK다이렉트 신차 큐레이션 프로토타입"

# GitHub에 새 저장소 생성 후 연결
git remote add origin https://github.com/<your-username>/sk-curation-prototype.git
git branch -M main
git push -u origin main
```

### 2. GitHub Pages 활성화

1. GitHub 저장소 → **Settings** 탭
2. 왼쪽 메뉴 → **Pages**
3. Source: **Deploy from a branch**
4. Branch: **main** / Folder: **/ (root)**
5. **Save** 클릭

### 3. 배포 확인

약 1~2분 후 아래 URL에서 접근 가능:
```
https://<your-username>.github.io/sk-curation-prototype/
```

## 파일 구조

```
curation-prototype/
├── index.html   # 메인 프로토타입 (단일 파일)
└── README.md    # 이 파일
```

## 향후 연동 포인트

| 기능 | 현재 (프로토타입) | 실 연동 시 |
|------|------|------|
| 차량 데이터 | 정적 JS 객체 | RMAS / RentOK API |
| 렌탈료 | 고정 표시값 | 실시간 가격 조회 |
| 셀프계약 CTA | alert() | 계약 페이지 파라미터 전달 |
| 세그 분석 | 없음 | GA4 이벤트 전송 |
