# EPIC — An Epidemiological Investigation of COVID-19 Dataset for Chinese Named Entity Recognition
EPIC(EPidemiological Investigation of COVID-19) is a COVID-19 epidemiological investigation dataset for Chinese named entity recognize (CNER).
## Corpus
"Zhengzhou Release"  is a government social media platform in Zhengzhou, the capital of Henan Province, and is the official channel for updating Zhengzhou's epidemic information. We crawled the epidemiological investigation reports released by "Zhengzhou Release" as the corpus.  
**范文：**
**病例168**:**病例31**的密切接触者，现住址:孙庄北院小区（中原区西四环）。  
* 5月1日，20:00到仲景生活（众业街店）购物，20:12—20:14在孙庄北院小区门口阳光超市购物。  
* 5月2日，8:00—17:30在钱塘衣城一层活动，期间13:00到弓背街核酸检测点进行核酸检测，18:20—19:00在鸿兴川菜馆（孙庄北院）就餐。  
* 5月3日—8日，集中隔离医学观察。  
* 5月9日，闭环转运至定点医院。  
##
**Sample:**
**Case 168**: close contact of **Case 31**, address: Sunzhuang North Yard Community (West Fourth Ring Road, Central Plains District).  
* On May 1st, go to Zhongjing Life (Zhongye Street Store) for shopping at 20:00, and shop at Sunshine Supermarket at the entrance of Sunzhuang North Yard Community from 20:12 to 20:14.
* On May 2, 8:00-17:30 at the first floor of Qiantang Clothes Store, during which time he/she goes to the nucleic acid testing point in Gongbei Street for nucleic acid testing at 13:00, and dinner at Hongxing Sichuan Restaurant (Sunzhuang North Yard Community) from 18:20 to 19:00.
* From May 3rd to 8th, centralized isolation and medical observation.
* On May 9, closed-loop transfer to a designated hospital.
## Entity categories
EPIC contains 10 entity categories, including Case, Relationship, Residence, Work Address, Location, Date, Time, Means of Transportation, Quarantine, Closed-loop Transfer.  
|  Category   |   Definition  |
|  :----:  | :----  |
| Case  | Case entity contains the prefix "Case" followed by a numeric suffix. Numerical suffix was given by epidemiological investigators and represented unique numerical identifiers for confirmed cases between April 17, 2022, and May 10, 2022. |
| Relationship  | Relationship entity includes spatiotemporal and social relations. Spatiotemporal relationship includes close contact and simultaneous space-time accompaniment, where simultaneous space-time accompaniment means that different cases appear in the same place at the same time. Social relations refer to family, colleagues, and classmates among cases. |
| Residence   | The residential address of the case and the pronoun of the residential address. |
| Work Address  | The work address of the case and the pronoun of the work address. |
| Location  | The Location entity refers to all entities in the text that represent spatial locations except Residence entities and Work Address entities. Note that entities that nest Residence entities or Work Address entities appearing in the text should be annotated as Location entities, for example, "nucleic acid testing sites near home" should be annotated as Location entity instead of Residence entity. |
| Date  | Specific dates, date periods and date pronouns. |
| Time  | Specific times, periods of time, and temporal pronouns. |
| Means of Transportation  | The mode of transportation chosen by the case. If specific mode of transportation information is included in the report, such as vehicle license plate number, flight number, train number, etc., these details should also be considered within the Means of Transportation entity. |
| Quarantine  | The status of case isolation mainly includes home isolation, medical observation isolation, and centralized isolation. It is worth noting that when nested Residence entity appear, such as "home isolation", the entirety should be annotated as a Quarantine entity rather than a Residence entity. |
| Closed-loop Transfer  | The status of closed-loop transfer of the case to designated hospitals, and the appearance of Closed-loop Transfer entity also indicates the end of a report. |
