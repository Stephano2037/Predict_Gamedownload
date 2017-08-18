# IndieGame-and-Social-phenomenon


원래 생각했던 주제는 인디개발자가 게임개발을 할 경우,  그 게임이 얼마나 팔릴 수 있는지  매출액에 대해서 예측하는 시스템(Predict_gamedownload)을 만들려 하였습니다.
그리고 이를 머신러닝을 적용하여 만드려고했으나, 실질적으로 데이터를 모으는데 오랜 시간이 걸리고, 다른작업들과 병행하기가 힘들어서 이 부분은 포기하게되었고,
제가 모으는 데이터로 사회적인 현상을 분석하는건 어떨까 싶어서 주제이름을 IndieGamedevelop-and-Social-phenomenon으로 변경하게되었습니다.

변경하면서 선정한 주제들입니다.

1. 회사존속기간 대비 매출액,보유자수 상관관계 (ex) 회사존속기간이 10년이 된 회사들은 보통 매출액이높더라, 반면 회사존속기간이 3년이안된 회사들은 보통 매출액이 낮더라)

2. 게임발매 이전의 동영상 홍보기간 대비 각 회사의 매출액과 보유자수 상관관계 (ex) 동영상 홍보를 게임발매하기 1년전에 하면 게임 판매량이 높더라, 게임발매하고 동영상을 등록해서 홍보하니 게임이 안팔리더라 )

3. OECD 연평균 국가 근로시간이 적을수록 각 나라의 게임개발 StartUp 비율이 높을 것이라는 상관관계 

4. OECD 연평균 국가 근로시간 대비 각 나라 게임개발자들혹은 회사들의 평균 매출액, 평균보유자수 상관관계 

한국은 OECD국가기준  연평균 국가 근로시간이 매년 최상위에 위치하는걸로 알고 있는데,이는 곧 한국의 거의 모든 산업분야에서 야근을 기본적으로
시키는 회사가 많다는걸 알 수 있습니다.

그리고 더나아가 한국 게임회사는 창의적인 게임, 재밌는 게임보다는 항상 과금시스템을 기반으로 온라인 게임을 만드는데 좀 더 공을 들이는 면이 많이 부각됩니다.
이러한 시스템구조로, 꿈을 펼치고 싶어하는 인디개발자들과 취업하고 난 이후, 업무에만 집중하게되어 여가 시간이 없어 자신이 만들고자 하는 게임을 만들지 못하는 사람들이 많다고 판단하여서,
다른나라와도 비교해 한국의 잘못된점과 다른나라에서 배울점을 찾고자 이 같은 주제를 선정하였습니다.


우선 주제가 인디게임과 사회현상이다보니, 인디게임들이 많이 출시되는 steam에서 데이터를 이용하기로 하였고, 동시에 특정 스팀게임의 보유자 수 정보를 갖고있는 steamspy에서
데이터들을 Crawling하였습니다.

스팀데이터를 모두 동일한 'Puzzle'태그(장르)에서 1000개 데이터를 모았고, 이 중에서 steamspy에 나오지않는 게임들(DLC추가판등등)은 모두 제외하고 보니, 실질적으로 987개의 데이터가 남았습니다.



각 column별 검색 우선순위를 아래와 같이 하여 데이터를 집어넣었습니다.


1. EngineorLanguage / 엔진

구글검색 > indie db > youtube질문 or 개발자,혹은 회사에 직접 질문(메일)

2. FoundingdateofCompany / 회사설립년도

각 게임회사(혹은 게임개발자) 웹사이트 presskit > facebook or twitter > linkedin site (해외 이력서 사이트)>  google검색 > 못찾음

3.   Nationaility / 개발자 의 국적 혹은 회사가 설립된 장소(국가)


각 게임회사(혹은 게임개발자) 웹사이트 presskit > facebook or twitter > linkedin site (해외 이력서 사이트)>  웹사이트 국가 IP 확인> 못찾음


사실 제일 민감한 부분인데, 웹사이트 국가 IP를 확인하면 실질적으로 안맞을 가능성이 높다고 판단되지만, 생각보다 맞는게 많아서 , 특정 게임개발자의 웹사이트를 찾았는데 아무런 정보가 없을경우 이 방법을 취하게되었습니다.

또한 공공 개발(ex) 특정게임은 일본인과 스웨덴인이 함께 만들었습니다.)이라고 써져있는경우도, 도메인 IP를 찾아 해당 IP와 일치하는 나라(혹은 가까운 나라)를 데이터로 넣었습니다.

그리고 회사설립국가가 명확하게 명시된곳은  , 해당 국적(동일한 국적)을 가진 사람이 해당 국가에 회사를 세웠다고 판단하여, 사이트에서 명시한 국가를 데이터로 집어넣었습니다.




----추후 추가 작성



