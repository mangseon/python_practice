# python 

- 6/9 

1차 강의에서 잘 이해 안되었던 것. 딕셔너리 개인공부 필요

-phone = ">경기 031 >강원 033 >충남 041 >충북 043 >경북 054 >경남 055 >전남 061 >전북 063"
phone.split() 결과값
['',
 '경기 031 ',
 '강원 033 ',
 '충남 041 ',
 '충북 043 ',
 '경북 054 ',
 '경남 055 ',
 '전남 061 ',
 '전북 063']

phone_dict = {}                                  # 빈 딕셔너리 생성
for x in phone.split(">"):                    # >를 기준으로 분리
if len(phone_split) > 0:                       #  공백이 있어서 제거용으로 사용        
key = x.split()[0]                                 # (경기 031)을 공란 기준으로 나누고 경기를 키값으로 설정
value = x.split()[1]                              # (경기 031)을 공란 기준으로 나누고 031을 밸류값으로 설정
phone_dict[key] = value                    # 딕셔너리 상 키값과 밸류값 매칭

- 6/13일 

파이썬 2차강의 재시청 ~시각화전까지
파이썬 2차 과제 풀이 - 모르는 부분이 꽤 있어서 보완 필요

구글링 통해 fillna()가 결측치 대체하는것알아냄

- 6/14일

df[""] 는 시리즈 출력
df[[""]]는 시리즈 결과를 데이터 출력
df[[""]] ([[]]안에 조건문) [""]하면 조건 내 뒷 컬럼 시리즈로 출력

판다스 다중 조건
df[(df["embarked"] == "C")  & (df["pclass"] == 3) ]
각 조건문은 ()로 감싸줘여한다.

boolean은 ""로 감싸지 말아라

- 6/15일
df.isnull() = df.isna()
frac = df의 전체 갯수 중 숫자만큼 갯수 가져온다.
.mead() * 100하면 비율이다.
데이터 불러온다음 확인할 정보들 = shape, head, tail, info, dtypes, describe, describe(include = "object")
.agg()는 보고싶은 정보 결합할 때 쓰인다.
regplot과 lmplot의 차이점 = lmplot은 reg플롯과 변수들을 결합하여 보여준다.
estimator in barplot = 원하는 집계
.unstack() = 재구조화

-6/30
drpona(axis = n) 하면 결측치가 하나라도 있는 것 삭제
dropna(axis = n, how ="all")은 모든 값이 결측치인것 삭제

-7/1
.append -> 리스트에 항목 추가
dropna()
df.dropna(thresh =2)는 nan값이 2개인 행 삭제
df.dropna(subset=['name', 'toy'])는 네임이랑 토이에 nan값 있는 행 삭제

![image](https://user-images.githubusercontent.com/85600255/124081429-819db000-da86-11eb-8990-21cea7832282.png)
