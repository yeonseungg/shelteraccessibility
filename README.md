# 🔍 네트워크 분석을 통한 서울시 대피 취약지 발굴: 송파구의 민방위 대피소를 중심으로

---

## 📌 개요

본 프로젝트에서는 서울시 송파구를 대상으로, 행정기관 관할의 민방위 대피소 범위 내에서 가장 중요한 문제인 **가능한 주민 대피 전략과 그 대피소의 최적 지정** 문제를 다루고자 했다.

- 최근 사례에서는 **민방위 대피소가 수용 기준을 충족하지 못하고**,
- 연속적인 케이스에서 복잡한 주변 인구를 대상으로는 고령자에 대한 고려가 부족한 경우가 많았다.

---

## 🗓️ 프로젝트 개요

- **진행 기간**: 2023.06 ~ 2023.08  
- **참여 형태**: 서울시 빅데이터 캠퍼스 멘토링
- **역할**: 생활인구 데이터 수집 및 전처리, QGIS 기반 시각화 수행

---

## 📊 사용 데이터

| 구분 | 출처 | 설명 |
|------|------|------|
| 행정구 경계 | 통계청 (KOSIS) | 공간 단위 기준 설정 |
| 민방위 대피소 | 행정안전부 국가재난정보센터 | 대피소 위치, 수용 인원, 면적 |
| 서울시 생활인구 | 서울열린데이터광장 | 시간대/요일별 유동인구 |
| 도로망 | OpenStreetMap (OSM) | 네트워크 분석용 도로 데이터 |
| 행정동-집계구 매칭 | 자체 수기 매칭 | 생활인구와 공간 단위 간 정렬용 데이터 |

---

## 🛠 기술 스택 및 도구

- **GIS 소프트웨어**: QGIS
- **데이터 전처리**: Python, Excel
- **시각화**: QGIS (가이드 트리, 서비스 수준 지도, 접근성 공간 구현)
- **네트워크 분석**: OpenStreetMap 데이터, Dijkstra 알고리즘
- **보고서 작성**: PowerPoint

---

## 🔍 구현 기능/분석 목록

1. 도로망 기반 대피소 최단 거리 산출  
2. 거리 기반 가중치 함수(W_{ij}) 적용  
3. 서비스 품질 지수 Rj 계산  
4. 2SFCA 기법을 활용한 집계구 접근성 지수 Ak 산출  
5. 생활인구 기반 기대 수요 vs 서비스 수준 비교  
6. QGIS 기반 접근성 분석 지도 제작

---

## ✅ 결과 및 시사점

- 송파구 내의 일부 집계구는 대피소의 접근성이 낮고 서비스 품질이 떨어지는 것으로 분석되었다.
- 기존 수용량으로는 인구 밀집 시간대나 고위험 지역에서의 수요를 감당하기 어려운 경우가 확인되었다.
- 생활인구 기준 분석 결과, 특정 지역에서는 수용능력 부족이 명확히 드러났으며, 이는 실제 위기 상황 시 혼잡 및 대피 실패로 이어질 가능성이 크다.
- **정책적 활용 가능성**:
  - 대피소 신규 입지 선정 또는 시설 보완에 활용 가능
  - 고령자 및 취약계층 중심의 맞춤형 대피 계획 수립 가능
  - 공간 데이터 기반 실질적인 방재 전략 수립의 기초 자료로 활용 가능
