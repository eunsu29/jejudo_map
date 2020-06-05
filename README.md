### 리뷰 감성 분석(긍/부정 판단)
업체별 총 리뷰 50개 이상, 부정 리뷰 20% 이상인 업체 리스트 작성(음식점 기준)<br>
해당 업체들 부정 리뷰 내용 분석 및 요약<br><br>

#### 내용 요약 (selenium,  konlpy, nltk, keras, folium 패키지 사용)
selenium패키지를 통한 웹스크래핑(리뷰 수집) 후 데이터 전처리 후 csv파일로 저장<br>(https://store.naver.com/restaurants/list?bounds=121.0849205%3B34.184039%3B135.1364342%3B40.9669969&query=%EB%A7%9B%EC%A7%91&sessionid=dErvWZ6KBTCFitPSlhnkhdDu&sortingOrder=reviewCount)<br>
konlpy패키지의 okt.pos()함수를 사용하여 리뷰 토큰화, ntlk로 빈도수 상위 10000개 토큰 선정<br>
keras패키지를 통한 모델 학습으로 긍정/부정 리뷰 판단(https://wikidocs.net/24559)<br>
folium패키지로 지도 위에 시각화<br><br>

00.음식점 리뷰 감성 분석 데이터셋 수집.ipynb :<br>
   네이버 플레이스 기준 예약자 리뷰, 영수증 리뷰 데이터 수집<br>
   
01.음식점 리뷰 감성분석 Keras 학습.ipynb :<br>
   약 5만개 학습용 데이터셋으로 Keras 학습 모델 생성 및 검증용 데이터셋 긍/부정 판단<br>
   
02.음식점 리뷰 시각화.ipynb :<br>
   음식점, 카페, 숙소 카테고리별 긍정/부정 리뷰 워드클라우드<br>
   지도에 나타내기<br>
   
03.음식점 리뷰 html코드 작성.ipynb<br>
   항목별 리뷰 내용 요약<br>
