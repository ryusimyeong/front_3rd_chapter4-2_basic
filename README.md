# 바닐라 JS 프로젝트 성능 개선(항해플러스 FE 3기 7팀 류시명)

- url: https://d1qyek1wa6r1nl.cloudfront.net/

## 성능 개선 보고서

| 개선 항목          | 개선 이유             | 개선 방법          | 개선 지표     |
| ------------------ | --------------------- | ------------------ | ---------------- |
| head 내 스크립트 async, defer 사용 | head 내 스크립트 실행으로 FCP 속도 저하 | script tag의 async defer 속성 사용 | FCP 1.9 초 -> 0.9 초 |
| 이미지 형식 webp로 변경 | jpg 대신 데이터 효율이 좋은 webp를 사용하여 성능 개선 | jpg 파일을 webp로 converting | 2,156KiB 절감 |
| 히어로 이미지 해상도에 맞게 렌더링 | 초기 렌더링 속도 지연 | picture tag를 활용하여 해상도에 맞는 이미지 렌더링 | 성능 37점 -> 58점 |
| 로컬 폰트 사용 | head tag 내 웹폰트 다운로드 항목 때문에 FCP 속도 저하 | 로컬 폰트 사용 | FCP 2.4 초 -> 1.9 초 |
| 이미지 레이지로딩 | 뷰포트 바깥 이미지 로딩 지연으로 초기 렌더링 최적화 | img 태그 loading 속성 사용 | FCP 2.7초 -> 2.4 초 |