# **W**ebtoon-related **R**esearch **I**n the **K**orean academic field (WRIK)

## Ⅰ. 소개
이 페이지는 한국 학술장 내 웹툰 관련 연구의 확장과 분화를 추적한 아래 논문의 데이터와 코드를 공유하기 위해 만들어졌습니다. 

(아직 100% 완성되진 않았으니 필요한 데이터 등이 있으실 경우 이메일로 문의주시기 바랍니다)

[한국 학술장 내 웹툰 관련 연구의 확장과 분화 : KCI 논문 서지 데이터 기반 구조적 토픽 모델링 분석, 2003∼2023(애니메이션연구 71호, 2024)](https://www.kci.go.kr/kciportal/ci/sereArticleSearch/ciSereArtiView.kci?sereArticleSearchBean.artiId=ART003123833)

논문을 확인하시면 지면의 한계로 '자세한 내용은 깃허브를 참조'하라는 내용이 일부 들어있습니다. 여기 README에서 관련 설명을 확인하신 후 데이터와 코드 파일을 확인하시면 됩니다.
수정과 보완, 추가에 대한 의견 항상 기다리고 있겠습니다. 웹툰 연구자들의 연구 외연(중 하나)인 '웹툰 관련 연구'들의 데이터를 분석하고 검토하는 작업에 많이 참여해주시면 감사하겠습니다.

### Ⅱ. 저자
- 이윤호(성균관대학교 비교문화협동과정 석사과정, dbsgh3838@g.skku.edu)
- 김병준(한국학중앙연구원 인문정보학 조교수, bjkim@byungjunkim.com)
---
## Ⅲ. 자료수집 및 정제(선별)
### 수집 범위 및 기준
[KCI 웹페이지](https://www.kci.go.kr/kciportal/main.kci)에서 검색되는 KCI 등록(등재, 등재후보) 학술지 탑재 논문 중 웹툰을 지칭하는 '주제어'가 제목, 키워드, 초록에 포함된 논문들의 서지 정보
  - 주제어 : 웹툰, webtoon, 웹만화, 디지털만화, 웹코믹스, 인터넷만화, 온라인만화 (오늘날 광의의 의미에서 '웹툰'이 포괄하는 단어들로 선정)
단, 
1) 제목 및 키워드에 주제어가 포함된 경우 '웹툰 연구'는 아니더라도 '웹툰 관련 연구'라고 볼 수 있으나
2) 초록에**만** 주제어가 포함된 경우 '웹툰 관련 연구'로 보기도 힘들 수 있으므로
데이터를 구분하여 수집하고, 각각에 대한 선별 과정을 거쳤음.

### 수집
웹페이지 [논문검색](https://www.kci.go.kr/kciportal/po/search/poArtiSear.kci)(상단메뉴)에서 '고급검색' 버튼을 눌러 **'쿼리'**를 입력하고, '검색 범위'를 조정
1. 쿼리 입력
  1) 제목 및 키워드에 주제어가 포함된 논문 584건
       > 쿼리 : TI:("웹툰") OR KW:("웹툰") OR TI:("webtoon") OR KW:("webtoon") OR TI:("웹만화") OR KW:("웹만화") OR TI:("디지털만화") OR KW:("디지털만화") OR TI:("웹코믹스") OR KW:("웹코믹스") OR TI:("인터넷만화") OR KW:("인터넷만화") OR TI:("온라인만화") OR KW:("온라인만화")
  2) 초록에**만** 주제어가 포함된 논문 279건
       > 쿼리 : AB:("웹툰") OR AB:("webtoon") OR AB:("웹만화") OR AB:("디지털만화") OR AB:("웹코믹스") OR AB:("인터넷만화") OR AB:("온라인만화") NOT TI:("웹툰") NOT KW:("웹툰") NOT TI:("webtoon") NOT KW:("webtoon") NOT TI:("웹만화") NOT KW:("웹만화") NOT TI:("디지털만화") NOT KW:("디지털만화") NOT TI:("웹코믹스") NOT KW:("웹코믹스") NOT TI:("인터넷만화") NOT KW:("인터넷만화") NOT TI:("온라인만화") NOT KW:("온라인만화")

2. '검색 범위' 설정
   1) 검색 간 범위 설정
     - 주제분류 : 대분류 / 전체
     - 재단등재구분 : '전체'에 체크(등재후보지 포함. 해당 사항을 체크하지 않을 시 학술대회 발표자료 포함)
     - 발행일자 : 2003년 1월 ~ 2023년 12월
   2) 검색 후 검색 범위 재조정 (좌측 체크리스트 활용)
     - 앞선 '재단등재구분'을 체크하여 학술대회 논문은 이미 제외(미체크 시 학술대회논문은 제외시켜야 함)
     - 철회논문, 비정규논문 제외
  
## 자료 정제(선별)
### 정제 기준
1. 제목 및 키워드에 포함된 경우 : 시스템 상 잘못 수집된 데이터 발견 후 유사 사례가 있을 경우 일괄 배제(논문 각주 24번 참조)
2. 초록에만 포함된 경우 : 초록 내용을 정성적으로 검토하여 웹툰 관련 주제어를 **단순 언급**한 경우 배제
  초록에만 키워드를 포함하는 경우 연구 배경 및 의의에 ‘웹툰’을 단순히 언급하였을 뿐 연구 내용 상으로는 웹툰과 관련이 없는 경우가 많았는데, 이를 본 연구의 취지와 연구방법론을 고려했을 때 데이터에 포함하는 것은 부적절하다고 판단하여 90건을 최종 선별
    > 선별된 논문들은 웹툰 산업 및 웹툰을 고려하고 계기로 삼아 진행된 공학적 정책적 연구, 웹툰 원작의 2차 저작물을 다루되 트랜스미디어적 성격에 주목하여 웹툰 원작과의 비교가 이루어진 연구, 혹은 핵심 '변인'으로 웹툰을 삼는 사회과학 연구 등임. 선별 전 데이터는 파일 참조(0.1. 초록에만 주제어를 포함한 논문 선별본.xls 참조)

    > A열 관련성 점수의 경우 '웹툰 연구'에 대해서는 0점, 나머지는 관련도를 기준으로 1~6점을 부여하였으며, 이후 검토와 논의를 통해 '웹툰 관련 연구'는 1점을 받은 논문들만 최종 포함시키기로 결정하였음.

**서지정보 스프레드 시트** : [스프레드시트 바로가기](https://docs.google.com/spreadsheets/d/1zSQmuXPDgIP8dNm2F6_x3AtksZY_SFJlrrsa4rAMSuo/edit?usp=sharing)
  * 스프레드시트 데이터에 대해서는 댓글을 통해 수정 의견을 제시할 수 있습니다.


