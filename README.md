###### tags: `Task` `Dataset` `Mediaad`
# Mediaad Dataset Description

[toc]

---


## Data Download
The files can be downloded from [here](https://drive.google.com/file/d/1tVYbSaG0JdxTLLPSAESnBNvj_RIxKg5B/view?usp=sharing).
## File Descriptions
- **document.csv**
Here, by document we mean a page of a website. Each row of this file is about a page metadata. The information is about the website and the publisher that the page(document) belongs to.
<!--     - *docId*
    - *source(website)*
    - *publisher* -->
:::info
```json=
docId,source,publisher
1,0,0
3,1,1
4,2,2
5,3,3
6,4,4
7,1,1
8,5,3
9,6,5
10,7,6
```
:::
- **document_topic.csv**
This file describes the topic distributions of pages. Each row shows a pair of a page and a topic and a confidence level. We gathered this data by preprocessing the page contents.  The fields and samples are as follows:
<!--     - docId
    - topicId
    - Confidence -->
:::info
```json=
docId,topicId,confidence
10743259,37,0.49709868
10743259,23,0.016993675
10743259,10,0.37149945
10743259,4,0.105349235
10743258,33,0.24575157
10743258,28,0.60887676
10743258,5,0.10920001
10743257,33,0.24552396
10743257,28,0.60861677
```
:::
- **creative.csv**
This file contains the metadata about the ads we show users. Each row describes a different ad(creative), its campaign and its advertiser.
:::info
```json=
creativeId,campaignId,advertiserId
7867,5918,8414
7866,5918,8414
7865,5918,8414
7863,8343,8414
7862,8343,8414
7861,8343,8414
7860,8343,8414
7859,8343,8414
7858,8343,8414
```
:::
- **creative_title.csv**
The bag of word representation of creative titles. Each row describes a pair of a creative and q word the present in its title. ==For anonymization we present the id of words not the true values==.

:::info
```json=
creativeId,wordId
6,24
6,25
6,26
6,27
6,28
6,29
6,30
6,31
7,32
```
:::
- **creative_image.csv**
This file describes the information about the creative images. For reasons such as anonymization, fewer ram usage and  ease of training, we present some extracted features for creative images. The features are  a list of 512 features that are string coded.

:::info
```jsonld=
creativeId,imageFeatures
7867,"[0.0524589940905571, 0.0, 0.04262353479862213, 0.3335827887058258, 0.38356322050094604, 0.0016337124397978187, 0.34486910700798035, 0.5254691243171692, 0.05376036837697029, 0.0790339931845665, 0.5009145736694336, 0.6770318150520325, 0.0, 0.04745246469974518, 0.11314650624990463, 0.00764562888070941, 0.0, 0.1501387357711792, 0.03241937980055809, 0.004932682495564222, 0.0, 0.0, 0.5730596780776978, 0.019595881924033165, 0.0, 0.09223274141550064, 0.02514776773750782, 0.07260636240243912, 0.0, 0.5376994609832764, 0.0, 0.1540597379207611, 0.9559652805328369, 0.10546236485242844, 0.003840308403596282, 0.0, 0.09895025938749313, 0.0, 0.17928677797317505, 0.0, 0.5366105437278748, 0.2375306487083435, 0.04689086228609085, 0.8058763742446899, 0.0, 0.0, 0.01303254533559084, 1.113734483718872, 0.44265198707580566, 0.09719770401716232, 0.6938168406486511, 0.28377801179885864, 0.1759302318096161, 0.0, 0.012601906433701515, 0.3471967279911041, 0.0, 0.0766461044549942, 0.0, 0.00262973690405488, 0.0063209836371243, 0.74350905418396, 0.0, 0.0, 0.13608892261981964, 0.0, 0.24228109419345856, 0.7389951348304749, 0.0, 0.1485598236322403, 1.3823773860931396, 0.2141677439212799, 0.027074171230196953, 0.0, 0.0, 0.0, 0.26120033860206604, 0.28101813793182373, 0.0, 0.08263696730136871, 0.1578405648469925, 0.10821836441755295, 0.0, 0.0057042865082621574, 0.0, 0.019689170643687248, 0.0, 0.17585083842277527, 0.011907795444130898, 0.002454791683703661, 0.23566392064094543, 0.10202024132013321, 0.11496552079916, 0.012451911345124245, 1.870426058769226, 0.14807745814323425, 0.42014285922050476, 0.10208401829004288, 0.25753581523895264, 0.04493357986211777, 0.09856701642274857, 0.11120041459798813, 0.22483405470848083, 0.25453343987464905, 0.0032995236106216908, 0.9838165044784546, 0.8109205961227417, 0.4817812442779541, 0.014035709202289581, 0.04418061673641205, 0.011374461464583874, 0.12863709032535553, 0.03337208926677704, 0.0, 1.4399311542510986, 0.0, 0.49707287549972534, 0.2588406801223755, 0.5210369825363159, 0.0, 0.10058943182229996, 0.05463501811027527, 0.8610427975654602, 0.5020743012428284, 0.030319757759571075, 0.8928760290145874, 0.506088376045227, 0.2090473473072052, 0.003232160583138466, 1.6961923837661743, 0.028163563460111618, 0.05816756933927536, 0.35724321007728577, 1.9972378015518188, 0.4023135304450989, 0.03822699934244156, 0.47549718618392944, 0.8358854055404663, 0.442721962928772, 0.004401505459100008, 0.2167019248008728, 0.0018225357634946704, 0.11354278773069382, 0.0, 1.4138048887252808, 0.3715467154979706, 0.20260004699230194, 0.0011393165914341807, 0.24493104219436646, 0.0422644168138504, 0.07470837980508804, 0.44676506519317627, 0.6388846039772034, 0.21214638650417328, 0.9269633293151855, 0.1876787394285202, 0.0, 0.014485415071249008, 0.14804451167583466, 0.0, 0.10219316929578781, 0.0, 0.0, 0.0011359964264556766, 0.6181788444519043, 0.012399531900882721, 0.023947902023792267, 0.0002116563991876319, 0.054431620985269547, 0.2317836433649063, 0.14420899748802185, 0.6919376254081726, 0.5663913488388062, 0.01806214265525341, 0.0, 0.0, 0.8541684746742249, 0.0, 0.04821351170539856, 0.0, 0.13298183679580688, 0.26571476459503174, 0.2441360503435135, 0.11967230588197708, 0.43411985039711, 0.6160688400268555, 0.19833825528621674, 0.0, 0.0, 0.06707854568958282, 0.024971941486001015, 0.9891048669815063, 0.0, 0.1065264344215393, 0.09542371332645416, 0.6286377310752869, 0.06564754992723465, 0.9165804982185364, 0.022102609276771545, 0.01808992587029934, 0.0713435634970665, 0.004327212926000357, 0.18033963441848755, 0.2409106194972992, 0.19836527109146118, 0.0, 0.0, 0.0831923633813858, 0.1496896892786026, 0.14142830669879913, 0.2097349762916565, 0.0, 0.4512734115123749, 0.8316828608512878, 0.025351183488965034, 0.7340601682662964, 0.0, 0.1781339794397354, 0.11174163967370987, 0.08710390329360962, 0.18852172791957855, 0.02282477356493473, 0.10788831859827042, 0.04018762335181236, 0.6255924701690674, 0.09888948500156403, 0.3072219491004944, 0.5751482248306274, 0.0, 0.25533074140548706, 0.0, 0.142370343208313, 0.36775970458984375, 0.0012231525033712387, 0.0, 0.09687993675470352, 0.42802900075912476, 0.04800980165600777, 0.0, 0.05185330659151077, 0.4435133934020996, 0.0, 0.0, 0.045000672340393066, 0.0, 0.010632830671966076, 0.14304840564727783, 0.4098302125930786, 0.046728916466236115, 0.03777185082435608, 1.3611832857131958, 2.5127615928649902, 0.1033560261130333, 0.010225065983831882, 0.28524771332740784, 0.11239043623209, 0.7252575755119324, 0.8900536298751831, 0.0, 0.38185858726501465, 0.06111784651875496, 0.0, 0.040989700704813004, 0.0, 0.008436067961156368, 0.01430627889931202, 0.36651307344436646, 0.13438716530799866, 0.0193697027862072, 0.0, 0.22299551963806152, 0.03810221701860428, 0.0777783989906311, 0.01994059421122074, 0.045812010765075684, 0.0, 0.4665735065937042, 0.0, 0.277442067861557, 0.8755587339401245, 0.2046937644481659, 0.050224144011735916, 0.1398463100194931, 0.062250956892967224, 0.03436265140771866, 0.21302521228790283, 0.1241559311747551, 1.8673889636993408, 0.38291168212890625, 0.011038499884307384, 0.06205926835536957, 0.02232370525598526, 0.0, 0.0, 0.041719697415828705, 0.04538219794631004, 0.2916184961795807, 0.049691107124090195, 0.5081413984298706, 0.11252861469984055, 0.3664450943470001, 0.531741201877594, 0.11930695176124573, 0.5198532938957214, 0.8124033212661743, 0.4518541097640991, 0.21484598517417908, 0.6128281354904175, 0.0, 0.3964100480079651, 0.9020141363143921, 0.18474553525447845, 0.038612764328718185, 0.0, 0.0, 1.7949954271316528, 0.1832423210144043, 0.0, 0.15385232865810394, 1.3681594133377075, 0.15732046961784363, 0.04315795749425888, 0.0, 0.0, 0.06659245491027832, 0.010794873349368572, 0.0, 0.16922619938850403, 0.004929518327116966, 0.09100309759378433, 0.0, 0.0008615456172265112, 0.0, 0.014330863952636719, 0.3634317219257355, 0.5796082615852356, 0.004235472530126572, 0.0866054818034172, 0.19918595254421234, 0.0, 0.012094324454665184, 0.008820407092571259, 0.0003866589686367661, 0.07019684463739395, 0.37010496854782104, 0.051394619047641754, 0.18688522279262543, 0.06396914273500443, 0.39068594574928284, 0.1060214713215828, 0.010107624344527721, 0.0, 0.0, 0.022860363125801086, 0.5025042295455933, 0.5866639018058777, 0.9520065784454346, 0.08304600417613983, 0.38530126214027405, 0.27544865012168884, 0.007508657407015562, 0.26225095987319946, 0.0, 0.8277463912963867, 0.0, 0.793016791343689, 0.2730690538883209, 0.0, 0.13819585740566254, 0.027830492705106735, 0.18068702518939972, 2.417189836502075, 0.0, 1.1181780099868774, 0.0, 1.9062105417251587, 0.08524265885353088, 0.0, 0.0815972313284874, 1.2653571367263794, 0.0, 0.6985716223716736, 0.0, 0.044726401567459106, 0.12374112010002136, 0.23629596829414368, 0.14078129827976227, 0.47028273344039917, 0.0, 0.2854258716106415, 0.5492580533027649, 0.31275811791419983, 0.15689019858837128, 0.0, 0.1441369354724884, 0.0071984343230724335, 0.609931230545044, 0.14004181325435638, 0.585576057434082, 0.0, 0.22358006238937378, 0.25531983375549316, 1.235224962234497, 2.5459024906158447, 0.12151942402124405, 0.04073060303926468, 0.0037157435435801744, 0.1867835372686386, 0.5576404333114624, 0.0, 0.26616135239601135, 0.01987653411924839, 0.0, 0.15705813467502594, 0.17579331994056702, 0.23685690760612488, 0.0, 0.08871358633041382, 0.11719027161598206, 0.05135223641991615, 0.00845278985798359, 0.0, 0.0011314277071505785, 0.0954841673374176, 0.0, 0.29563120007514954, 0.0, 0.5004280209541321, 0.15429893136024475, 1.0944734811782837, 1.399240255355835, 0.0, 0.024041304364800453, 0.0, 0.02393883839249611, 0.0, 0.11461999267339706, 0.0, 0.32238876819610596, 0.11020731180906296, 0.0, 0.2500244081020355, 0.0845474824309349, 0.0, 0.47124549746513367, 0.10645349323749542, 0.9488299489021301, 0.5220524072647095, 0.01650909334421158, 0.8671882748603821, 0.0, 0.02164115197956562, 0.4217461347579956, 0.016102958470582962, 0.17660780251026154, 0.23909291625022888, 0.0053427438251674175, 0.1923588663339615, 0.1154368445277214, 0.0, 0.10403607785701752, 0.0, 0.10917922109365463, 0.22670328617095947, 1.838025450706482, 0.1935068964958191, 0.4185929000377655, 0.0, 0.30573517084121704, 0.01434508990496397, 0.0, 0.10782365500926971, 0.0, 0.0, 1.0141878128051758, 0.14969369769096375, 0.10680084675550461, 0.16886450350284576, 0.019656404852867126, 0.08190245181322098, 0.33918142318725586, 0.13427631556987762, 0.01647268421947956, 0.19352316856384277, 0.4094108045101166, 0.12720051407814026, 0.4061034321784973, 0.0, 0.0, 0.007430760655552149, 0.2954533100128174, 0.34858548641204834, 0.11279997229576111, 0.0, 0.2815641760826111, 0.04496641457080841, 0.14596092700958252, 0.0, 0.14465385675430298, 0.09087847173213959, 0.07650305330753326, 0.22364288568496704, 0.23372770845890045, 0.5394803881645203, 0.15250787138938904, 0.34451788663864136, 0.7787312865257263, 0.07829540222883224, 0.16016195714473724, 0.0, 0.3051452338695526, 0.018119463697075844]"
```
:::
- **user_page_view.csv**
It is the log of users visiting documents. Here, by document we mean the page that user visits. Each row belongs to a page visit with the follwing fields:
<!--     - userId
    - docId
    - timetamp -->
:::info
```json=
userId,docId,timestamp
821961,8116,1579599211445
15321,9533442,1579599211443
1125090,9410379,1579599211440
407101,8616213,1579599211429
781615,9543366,1579599211429
1210398,9395724,1579599211426
470110,9546771,1579599211423
767395,9523927,1579599211423
630846,9531785,1579599211409
```
:::

- **event.csv**
This file contains the information about the **Context** in which the ad is shown to the user. The *displayId* is an Id that unifies the display and can link this contextual information to the click data. In each display multiple ads are shown to the user and one or none of them is clicked. *widgetId* is the id of the widget that the ads is shown to user in it. Each page may contain multiple widgets and in each widget multiple ads are shown to the user.
A sample page with multiple widgets:

<img src="https://i.imgur.com/aUNYHDM.jpg" width="500">

Each row describes the context of a display in which some ads are shown to a user:
:::info
```json=
displayId,timestamp,docId,widgetId,userId,device,OS,browser
4706262,1578429005696,3543873,6262,2688642,0,0,0
4706267,1578429007726,6245475,607,2688641,1,3,0
4706260,1578429012060,4416499,11458,2688638,0,0,1
4706255,1578429017218,6246028,9358,1962852,0,0,0
4706256,1578429021388,5327047,9358,2687719,0,0,0
4706235,1578429023501,6245689,9358,2688634,0,0,0
4706181,1578429029640,83625,5802,2688629,0,0,5
4706228,1578429035793,4096624,11458,745082,1,1,4
4706234,1578429036317,6244430,7691,2688626,0,0,0
```
:::
- click_train.csv
This file shows for each displayId the user clicked on which ad. For each displayId there is multiple entries, but one of them is clicked. You can gather the display context information by joining this  data with **event.csv** data. This data is the main data for learning the classifier to predict the click events.

:::info
```json=
displayId,creativeId,clicked
1210227,7182,0
1210227,7125,0
1210227,7181,0
1210227,535,0
1210227,7174,1
1214987,7125,0
1214987,7092,1
1214987,5652,0
1248098,7182,0
```
:::

- click_test.csv
This file is the same ad **click_train.csv** but the clicked column is removed. This data is for evaluating your predictor and your predictor should guess the click label for this data. We evaluate your performance by this data.
:::info
```json=
displayId,creativeId
151650,7585
151650,6257
151650,6690
151938,7454
151938,7370
151938,123
151938,6690
151938,7715
151938,7379
```
:::

