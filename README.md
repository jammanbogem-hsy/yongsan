# 용산구청 신나는AI교실

용산구청 2026년 신나는AI교실 랜딩페이지입니다. Starbucks 디자인 시스템에서 영감을 받은
크림 캔버스 + 4-tier 그린 팔레트, 50px 풀 필 버튼, 12px 카드 라운드, 위스퍼 셰도우를
한국어 컨텍스트(Pretendard)에 맞춰 적용했습니다.

## 프로그램

| 트랙 | 링크 |
|---|---|
| 마인크래프트 속 용산 메타버스 | [수업설계서](https://docs.google.com/presentation/d/1IrSxHu8HOaKNf2NSjY3iYrXYQHycAGWVT-IP9JOkRRk/edit?usp=sharing) |
| 용산 스마트 시티 보안관 제작하기 | [수업설계서](https://docs.google.com/presentation/d/1Rz1BoFat8g54cPGC-t5FvxLBirCaB70SM5QPvdB2f8s/edit?usp=sharing) |

## 구조

순수 정적 사이트입니다. 빌드 단계가 없으므로 Vercel은 루트 디렉토리만 그대로
서빙하면 됩니다.

```
yongsan/
├── index.html      # 페이지 마크업
├── styles.css      # Starbucks-스타일 디자인 시스템 토큰 + 컴포넌트
├── vercel.json     # Vercel 라우팅 (선택)
└── README.md
```

## 로컬 미리보기

```bash
# 어떤 정적 서버라도 OK
python3 -m http.server 5500
# 또는
npx serve .
```

브라우저에서 `http://localhost:5500` 열기.

## Vercel 배포

1. https://vercel.com 에 GitHub로 로그인
2. **Add New → Project** → `jammanbogem-hsy/yongsan` 임포트
3. Framework Preset: **Other** (정적 사이트로 자동 감지됨)
4. Build Command/Output Directory는 비워둠 (루트에서 정적 서빙)
5. **Deploy**

빌드 단계가 없어 30초 내로 첫 배포가 완료됩니다.
