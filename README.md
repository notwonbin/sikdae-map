# 식권대장 가맹점 찾기

카카오맵에 저장해 둔 식권대장 가맹점(음식점 356 · 카페 114 · 편의점 72)을 사진과 함께 검색하는 정적 웹페이지입니다.

- 메뉴·가게 이름·카테고리 검색 (예: `고기`, `국수`, `텐동`, `스타벅스`)
- 지역(가장 가까운 역) · 카테고리 필터, 가까운순 정렬
- 랜덤 추천
- 주소 해시로 탭 바로가기: `/#food`, `/#cafe`, `/#cvs`

## 구조

```
index.html   화면 (HTML/CSS/JS 한 파일)
data.js      장소 데이터 (window.PLACES)
thumbs/      썸네일 이미지 (카카오맵 장소 ID.webp)
vercel.json  썸네일 캐시 설정
```

빌드 과정이 없는 정적 사이트입니다.

## 로컬에서 보기

```bash
npm install
npm run dev
```

브라우저에서 http://localhost:3000 을 엽니다.

## 배포 (Vercel)

1. 이 폴더를 GitHub 저장소로 올립니다.
2. Vercel에서 **Add New → Project**로 저장소를 가져옵니다.
3. Framework Preset은 **Other**, Build Command와 Output Directory는 비워 둔 채 **Deploy**를 누릅니다.

## 데이터 출처

장소 정보, 사진, 카테고리, 도보 시간은 카카오맵 기준입니다(2026년 11월 수집).
