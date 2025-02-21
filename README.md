Do it! 공공데이터로 배우는 R데이터분석 with 샤이니 교재 내용을 토대로 작성한 코드이며 이해하기 쉽게끔 설명과 함께 작성한 것이다 (for me)


[오류 정리]

03. 자료수집: API 크롤러 만들기
- https와 http의 차이

HTTP는 데이터를 암호화하지 않고 HTTPS는 HTTP의 보안 버전이다.
HTTPS는 암호화해서 데이터를 보내는데 API에게 url을 보냈을 때 HTTPS였어서 데이터가 제대로 안받아들여졌음



[매커니즘]

●03. 자료수집: API 크롤러 만들기

크롤링: 웹사이트에서 자동으로 데이터를 수집하는 기술
1. 신청 url을 만든다
2. URL을 API에게 보낸다
3. 응답 내역을 XML 형태로 받는다


●04. 전처리: 데이터를 알맞게 다듬기
1. 불필요한 정보 지우기(결측값과 공백 제거하기)
2. 항목별 데이터 다듬기


●05. 카카오맵 API로 지오 코딩하기

지오코딩: 문자로 된 주소를 위도와 경도라는 숫자로 변환하지는 작업
1. 카카오 로컬 API 키 발급받기
2. 카카오 로컬 API를 이용해 주소를 얻고 좌표로 변환시킨다


●06. 지오 데이터프레임 만들기

sp: 좌표계 같은 정보를 저장할 수 있으며 공간 분석을 가능하게 한다 / 데이터 일부를 편집하거나 수정이 어렵다 / 데이터 전체의 기하학 정보를 처리할 때 유리

sf: 공간 데이터를 일반 프레임과 비슷하게 편집하거나 수정할 수 있게 sf의 업데이트 버전 / 하지만 공간 도형을 다루기에늰 sp가 빠르다는 평이 많음 / 부분적인 바이어리(0과 1) 정보 처리가 빠르다
1. 주소와 좌표 결합하기
2. 지오 데이터프레임 만들기

●07. 분석 주제를 지도로 시각화하기
- 어떤 지역이 제일 비쌀까?
1. 지역별 평균 가격 구하기
2. 평균 가격을 그리드와 결합하기
3. 지도 경계 그리기
4. 밀도 그래프 표시하기
5. 래스터 이미지로 변환하기(노이즈도 제거)
6. 경계선 외곽의 불필요한 부분을 자르기 -> 래스터 이미지 완성
7. 완성된 래스터 이미지를 지도 위에 올려놓기

- 요즘 뜨는 지역은 어디일까?
 1. 이전/이후 데이터 세트 만들기
 2. 가격이 오른 지역 찾기
 3. 지도 경계 그리기
 4. 밀도 그래프 표시하기
 5. 래스터 이미지로 변환하기(노이즈도 제거)
 6. 경계선 외곽의 불필요한 부분을 자르기 -> 래스터 이미지 완성
 7. 완성된 래스터 이미지를 지도 위에 올려놓기

- 우리 동네가 옆 동네보다 비쌀까?
 1. 마커 클러스트링 옵션 설정하기
 2. 마커 클러스트링 시각화하기(지도 위에 래스터 이미지와 개별 마커를 표시)

●08. 통계 분석과 시각화
- 서울에서 가장 비싼 지역 찾기
 1. 래스터 이미지+그리드에서 빨간 부분이 가장 비싼 지역임을 알 수 있음

- 확률 밀도 함수: 이 지역 아파트는 비싼 편일까?
 1. 전체 지역 평당 평균가 계산
 2. 관심 지역 평당 평균가 계산
 3. y축 최대값 구하기
 4. 확률 밀도 함수 구하기

- 회귀 분석: 이 지역은 일년에 얼마나 오를까?
 1. 회귀식을 구하기
 2. 회귀계수를 구하기
 3. 그래프 구하기

- 주성분 분석: 이 동네 단지별 특징은 무엇일까?
  1. 주성분 분석하기
  2. 그래프 그리기
