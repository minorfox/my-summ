## context-aware-ABS
This is the codes for the paper: Effective Abstractive Summarization with a Context-Aware Attention Mechanism. After review, I will upload the complete version.
For now, I present examples on three datasets and the full resluts of ROUGE155.

### CNN/Daily mail
#### example in paper with complete source text of 400 tokens
```
cnn chris copeland of the indiana pacers was stabbed after leaving a trendy new york nightclub early wednesday , and two atlanta hawks -- who had just finished a home game hours before the incident -- were among those arrested , according to police and cnn affiliates . the hawks were not involved in the stabbing incident , police said , but were arrested on obstruction and other charges later . though new york police department det. kelly ort initially told cnn the incident occurred just before 4 a.m. at 1oak , a club in new york 's chelsea neighborhood known to draw celebrities among its clientele , the club later told cnn that the stabbing occurred in front of the fulton houses project down the street . `` 1oak staff was unaware of the incident when it happened , as it occurred beyond their view in a different location . however , 1oak 's team assisted mr. copeland to their fullest capabilities , and called for help as soon as he was seen walking back towards the venue , '' the statement said . the statement continued , `` a review of the video footage seems to reveal the incident did not originate from the venue or its immediate surroundings that are under 1oak supervision . '' copeland and a female companion , katrine saltara , were in the club for about 10 minutes before leaving and walking down the street toward fulton houses , where their car was parked , said a 1oak spokesperson . the spokesperson gave cnn additional details on condition of anonymity because 1oak 's legal team had approved only the club 's official statement . the suspect , who the spokesperson said never entered 1oak , stabbed copeland and saltara in front of fulton houses , and according to the club 's statement , `` mr. copeland 's driver sprang to accost and detain the apparent perpetrator and that individual is now in police custody . '' charges against the suspect are pending , and his name will be released once charges are filed , ort said . copeland and saltara tried to make their way back to the club to seek help from the 20 or so security personnel on hand , leaving a `` bloody trail of handprints '' between the site of the stabbing and the club , the spokesperson said. (400 truncated tokens of 1109)
Ref: hawks say neither thabo sefolosha nor pero antic will play wednesday against brooklyn . chris copeland left `` bloody trail of handprints '' as he returned to club seeking help , club says . suspect in custody , police say , adding they will release his name once charges are filed .  
---------------------------------------------
Ours:chris copeland was stabbed after leaving a trendy new york nightclub early wednesday . the hawks were not involved in the stabbing incident , police say .
```

#### complete results of ROUGE155 on CNN/Daily mail
```
---------------------------------------------
1 ROUGE-1 Average_R: 0.35698 (95%-conf.int. 0.35457 - 0.35942)
1 ROUGE-1 Average_P: 0.39254 (95%-conf.int. 0.38976 - 0.39505)
1 ROUGE-1 Average_F: 0.36706 (95%-conf.int. 0.36455 - 0.36929)
---------------------------------------------
1 ROUGE-2 Average_R: 0.15257 (95%-conf.int. 0.15035 - 0.15475)
1 ROUGE-2 Average_P: 0.16880 (95%-conf.int. 0.16628 - 0.17130)
1 ROUGE-2 Average_F: 0.15725 (95%-conf.int. 0.15493 - 0.15951)
---------------------------------------------
1 ROUGE-3 Average_R: 0.08659 (95%-conf.int. 0.08465 - 0.08859)
1 ROUGE-3 Average_P: 0.09632 (95%-conf.int. 0.09411 - 0.09847)
1 ROUGE-3 Average_F: 0.08940 (95%-conf.int. 0.08739 - 0.09142)
---------------------------------------------
1 ROUGE-4 Average_R: 0.05676 (95%-conf.int. 0.05504 - 0.05846)
1 ROUGE-4 Average_P: 0.06345 (95%-conf.int. 0.06144 - 0.06542)
1 ROUGE-4 Average_F: 0.05868 (95%-conf.int. 0.05688 - 0.06049)
---------------------------------------------
1 ROUGE-L Average_R: 0.25970 (95%-conf.int. 0.25743 - 0.26185)
1 ROUGE-L Average_P: 0.28651 (95%-conf.int. 0.28391 - 0.28896)
1 ROUGE-L Average_F: 0.26728 (95%-conf.int. 0.26500 - 0.26946)
---------------------------------------------
1 ROUGE-W-1.2 Average_R: 0.10037 (95%-conf.int. 0.09945 - 0.10127)
1 ROUGE-W-1.2 Average_P: 0.23382 (95%-conf.int. 0.23167 - 0.23599)
1 ROUGE-W-1.2 Average_F: 0.13776 (95%-conf.int. 0.13654 - 0.13892)
---------------------------------------------
1 ROUGE-S* Average_R: 0.11962 (95%-conf.int. 0.11781 - 0.12137)
1 ROUGE-S* Average_P: 0.14481 (95%-conf.int. 0.14260 - 0.14697)
1 ROUGE-S* Average_F: 0.12271 (95%-conf.int. 0.12093 - 0.12441)
---------------------------------------------
1 ROUGE-SU* Average_R: 0.13064 (95%-conf.int. 0.12878 - 0.13238)
1 ROUGE-SU* Average_P: 0.15765 (95%-conf.int. 0.15540 - 0.15988)
1 ROUGE-SU* Average_F: 0.13405 (95%-conf.int. 0.13226 - 0.13574)
```


### DUC-2004 
#### examples with CNN/Daily mail train set and 5w-vocabulary
```
Text:Top finance officials from 14 countries in the Asia-Pacific region advised Asia's battered economies on Sunday to adopt further reforms in their effort to restore stability. Among the necessary steps is for countries to restructure their economies and corporations to make them less susceptible to abuse by narrow political interests, the officials suggested. The deputy finance ministers and deputy central bank governors met for two days to review progress on the ``Manila Framework,'' an agreement reached last November that aims to promote regional economic stability. Many of Asia's economies have plunged into recession since that agreement. Collapsed currencies, weakened demand and higher unemployment now characterize a region that once boasted some of the world's highest economic growth rates. The worsening financial gloom is likely to dominate talks at next week's summit in Kuala Lumpur of leaders from the 18-nation Asia-Pacific Economic Cooperation forum. The summit is to take place on Nov. 17-18. In a joint statement, the officials cited risks including slower global growth, with particular mention of Russia's worsening economy, and the need to speed up social programs to help the poor in the worst-hit countries. Stanley Fischer, deputy managing director of the International Monetary Fund, noted that some countries have already reformed their banking sectors. But he stressed the need for corporate restructuring as well. ``These are not easy things to do,'' he said. Meanwhile, Malaysia's most prominent dissident predicted that the country's prime minister would declare ``a state of emergency'' after the APEC meeting ends in Kuala Lumpur, a report said Sunday. Former Deputy Prime Minister Anwar Ibrahim, now on trial on charges of corruption and sexual misconduct, made the warning in an interview with Monday's edition of Time magazine. Prime Minister Mahathir Mohamad fired Anwar in September, saying he was morally unfit to lead, then had him expelled from Malaysia's ruling party. Anwar denies the allegations and says they were fabricated because Mahathir considered his popularity a threat to the prime minister's 17-year rule.
Ref1:unk economic summit in unk unk faces severe problems
Ref2:unk officials advise unk topic likely to dominate at unk unk
Ref3:unk countries advised to restructure economies and corporations
ref4:unk faces unk unk unk unk turmoil in host unk
---------------------------------------------
Ours:finance officials from 14 countries advised unk battered economies on unk to adopt further reforms in their effort to restore
```

#### complete results of ROUGE155 on DUC-2004 (After 2 days, we have a little raise than paper record)
```
---------------------------------------------
1 ROUGE-1 Average_R: 0.50492 (95%-conf.int. 0.49392 - 0.51572)
1 ROUGE-1 Average_P: 0.18694 (95%-conf.int. 0.18237 - 0.19161)
1 ROUGE-1 Average_F: 0.27188 (95%-conf.int. 0.26585 - 0.27803)
---------------------------------------------
1 ROUGE-2 Average_R: 0.20502 (95%-conf.int. 0.19604 - 0.21420)
1 ROUGE-2 Average_P: 0.07095 (95%-conf.int. 0.06767 - 0.07425)
1 ROUGE-2 Average_F: 0.10498 (95%-conf.int. 0.10032 - 0.10968)
---------------------------------------------
1 ROUGE-3 Average_R: 0.09053 (95%-conf.int. 0.08383 - 0.09726)
1 ROUGE-3 Average_P: 0.02882 (95%-conf.int. 0.02664 - 0.03107)
1 ROUGE-3 Average_F: 0.04351 (95%-conf.int. 0.04038 - 0.04680)
---------------------------------------------
1 ROUGE-4 Average_R: 0.04124 (95%-conf.int. 0.03626 - 0.04648)
1 ROUGE-4 Average_P: 0.01182 (95%-conf.int. 0.01038 - 0.01332)
1 ROUGE-4 Average_F: 0.01832 (95%-conf.int. 0.01611 - 0.02063)
---------------------------------------------
1 ROUGE-L Average_R: 0.47046 (95%-conf.int. 0.46086 - 0.47971)
1 ROUGE-L Average_P: 0.17383 (95%-conf.int. 0.16996 - 0.17776)
1 ROUGE-L Average_F: 0.25305 (95%-conf.int. 0.24782 - 0.25833)
---------------------------------------------
1 ROUGE-W-1.2 Average_R: 0.25932 (95%-conf.int. 0.25353 - 0.26465)
1 ROUGE-W-1.2 Average_P: 0.15334 (95%-conf.int. 0.14985 - 0.15678)
1 ROUGE-W-1.2 Average_F: 0.19186 (95%-conf.int. 0.18780 - 0.19578)
---------------------------------------------
1 ROUGE-S* Average_R: 0.25912 (95%-conf.int. 0.24842 - 0.26901)
1 ROUGE-S* Average_P: 0.03422 (95%-conf.int. 0.03256 - 0.03594)
1 ROUGE-S* Average_F: 0.05983 (95%-conf.int. 0.05715 - 0.06259)
---------------------------------------------
1 ROUGE-SU* Average_R: 0.29771 (95%-conf.int. 0.28681 - 0.30783)
1 ROUGE-SU* Average_P: 0.04351 (95%-conf.int. 0.04162 - 0.04548)
1 ROUGE-SU* Average_F: 0.07519 (95%-conf.int. 0.07223 - 0.07820)
```


### LCSTS
#### examples of LCSTS
```
Text:较早进入中国市场的星巴克，是不少小资钟情的品牌。相比在美国的平民形象，星巴克在中国就显得“高端”得多。用料并无差别的一杯中杯美式咖啡，在美国仅约合人民币12元，国内要卖21元，相当于贵了75%。第一财经日报
Ref:媒体称星巴克美式咖啡售价中国比美国贵
---------------------------------------------
Ours:星巴克美式咖啡中国比美国贵因中国人不差钱
```
```
Text:个税属于二次分配，主要起到调节两极分化、杀富济贫的作用，但现在并没有解决这个问题。政府要让利，不要指望个税能对整个税收做出什么大文章。这些年，公众要求进一步深化个税改革的呼声越来越高，大家希望进一步提高起征点。
Ref:现行个税沦为工薪税不能见鹅就拔毛
---------------------------------------------
Ours:新华社公众要求进一步提高个税起征点
```

#### complete results of ROUGE155 on LCSTS（word-based）

```
---------------------------------------------
1 ROUGE-1 Average_R: 0.50663 (95%-conf.int. 0.48397 - 0.53003)
1 ROUGE-1 Average_P: 0.62118 (95%-conf.int. 0.59661 - 0.64604)
1 ROUGE-1 Average_F: 0.54428 (95%-conf.int. 0.52135 - 0.56736)
---------------------------------------------
1 ROUGE-2 Average_R: 0.36569 (95%-conf.int. 0.33985 - 0.39288)
1 ROUGE-2 Average_P: 0.44569 (95%-conf.int. 0.41766 - 0.47619)
1 ROUGE-2 Average_F: 0.39072 (95%-conf.int. 0.36448 - 0.41928)
---------------------------------------------
1 ROUGE-3 Average_R: 0.29552 (95%-conf.int. 0.26967 - 0.32454)
1 ROUGE-3 Average_P: 0.36170 (95%-conf.int. 0.33231 - 0.39463)
1 ROUGE-3 Average_F: 0.31433 (95%-conf.int. 0.28781 - 0.34396)
---------------------------------------------
1 ROUGE-4 Average_R: 0.24660 (95%-conf.int. 0.22076 - 0.27455)
1 ROUGE-4 Average_P: 0.30112 (95%-conf.int. 0.27150 - 0.33319)
1 ROUGE-4 Average_F: 0.26082 (95%-conf.int. 0.23393 - 0.28966)
---------------------------------------------
1 ROUGE-L Average_R: 0.49413 (95%-conf.int. 0.47166 - 0.51814)
1 ROUGE-L Average_P: 0.60391 (95%-conf.int. 0.57849 - 0.62894)
1 ROUGE-L Average_F: 0.53021 (95%-conf.int. 0.50696 - 0.55500)
---------------------------------------------
1 ROUGE-W-1.2 Average_R: 0.31061 (95%-conf.int. 0.29519 - 0.32695)
1 ROUGE-W-1.2 Average_P: 0.57784 (95%-conf.int. 0.55324 - 0.60348)
1 ROUGE-W-1.2 Average_F: 0.39384 (95%-conf.int. 0.37576 - 0.41347)
---------------------------------------------
1 ROUGE-S* Average_R: 0.32427 (95%-conf.int. 0.29822 - 0.35194)
1 ROUGE-S* Average_P: 0.45198 (95%-conf.int. 0.42352 - 0.48272)
1 ROUGE-S* Average_F: 0.35024 (95%-conf.int. 0.32409 - 0.37741)
---------------------------------------------
1 ROUGE-SU* Average_R: 0.35835 (95%-conf.int. 0.33335 - 0.38544)
1 ROUGE-SU* Average_P: 0.49879 (95%-conf.int. 0.47083 - 0.52738)
1 ROUGE-SU* Average_F: 0.38883 (95%-conf.int. 0.36341 - 0.41495)
```





