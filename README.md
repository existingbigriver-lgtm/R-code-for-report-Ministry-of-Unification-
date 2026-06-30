Data Explanations
아래의 변수 명들은 실제 regression table에서는 조정해서 적용되었음.

사용 데이터
1.	GWF: 정권 유형
2.	NAM membership
3.	WDI: ODA 총액, National Resource 총액
4.	Vdem: 지역 변수 (e_regiongeo), 정권 유형 (v2x_regime), ideology(v2exl_legitideolcr_1, “GWF: 정권 유형”을 다르게 측정한 것. Leader가 political legitimacy를 위해 얼마나 socialist/communist ideology를 강조하는가)
5.	(Surplus and Gross) Domestic Product Data: GDP, GDPperCapita
A.	Anders, Therese, Christopher J. Fariss, and Jonathan N. Markowitz. 2020. "Bread Before Guns or Butter: Introducing Surplus Domestic Product (SDP)" International Studies Quarterly 64(2): 392–405.
6.	Gibler-Miller-Little (GML) Militarized Interstate Dispute (MID) data: conflict level을 측정. 기존 COW MID data와 동일.
A.	Gibler, Douglas M., Steven V. Miller, and Erin K. Little. 2016. “An Analysis of the Militarized Interstate Dispute (MID) Dataset, 1816-2001.” International Studies Quarterly 60(4): 719-730.
7.	foreign policy similarity measures: DV
A.	Haege, Frank M. 2011. "Choice or Circumstance? Adjusting Measures of Foreign Policy Similarity for Chance Agreement." Political Analysis 19(3): 287-305.
8.	COW 국제기구 data: 국제기구 가입수 (추가 control variable)
A.	Pevehouse, Jon C.W., Timothy Nordstrom, Roseanne W McManus, Anne Spencer Jamison, 2020. “Tracking Organizations in the World: The Correlates of War IGO Version 3.0 datasets”, Journal of Peace Research 57(3): 492-503.
종속변수: kappavv_prk
-	Cohen’s kappa 값이며, UNGA 총회 투표에서 대다수가 찬성하는 안건 등 우연히 투표가 겹칠 수 있음을 보정하였다. 
	Cohen, Jacob. 1960. "A Coefficient of Agreement for Nominal Scales." Educational and Psychological Measurement 20(1): 37-46.
-	Haege (2011)의 “What follows is a rationale for why users should think of kappa as a default measure for dyadic foreign policy similarity, though why the "valued" equivalent for the alliance data is an inadvisable default.”권고에 따라 해당 값 사용. 이외의 값들은 우연성을 correction하지 못함.
	Haege, Frank M. 2011. "Choice or Circumstance? Adjusting Measures of Foreign Policy Similarity for Chance Agreement." Political Analysis 19(3): 287-305.
-	Dyad 변수를 monodic으로 변경함. 북한과의 차이를 DV로 사용.
독립변수 1: is_nam_member
-	NAM
독립변수 2: ideology
-	해당 국가에서 사회주의 혹은 공산주의를 얼마나 내세우는지를 측정. 
-	To what extent does the current government promote a specific ideology or societal  model (an officially codified set of beliefs used to justify a particular set of social, political, and economic relations; for example, socialism, nationalism, religious traditionalism, etc.) in order to justify the regime in place?를 답한 다음, 해당 지수에 대해서 사회주의/공산주의의 중요도를 답한 문항임.
-	아래의 사회주의 정권의 또 다른 변수

독립변수 3: socialist~
-	GWF변수. 
-	Socialist_nar은 narrow definition of the socialist state로, party-based인 것만 의미
-	Socialist_wide는 wide definition으로, party-based에 party-personal도 포함함.

독립변수 4: region
-	V-dem 지역변수(e_regiongeo) 사용. 
독립변수 5: global south
-	V-dem의 e_regiongeo에서 아프리카, 아시아, 오세아니아, 중남미, 카리브해 국가 일 경우 Global South로 코딩. 단, 일본, 한국, 대만, 호주, 뉴질랜드, 이스라엘은 예외적으로 global north 처리.
독립변수 6: sub_region: V-dem의 e_regiongeo에서 주는대로, 북아프리카, 서아프리카, 중앙아프리카, 동아프리카, 남아프리카로 구분
독립변수 7: Sub_global
-	3-5 가설 2 측정용. V-dem의 e_regiongeo에서 아프리카, 중동, 중남미, 동남아, 그외 아시아로 구분. 이외에는 제외
독립변수 8: ColdWar

통제변수들
-	sum_igo_full: 해당 국가의 국제기구 참여 수. 통제변수이기에 max값 사용.
-	max_hostlev: 해당 국가의 MID 기준 conflict level.
-	Mrgdppc: gdp per capita
-	oda_total: ODA 받는 수준
-	totlaNR: 자원의 화폐가치

