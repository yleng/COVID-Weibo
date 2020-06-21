## Weibo COVID dataset

Sina Weibo (新浪微博), commonly referred to as “Chinese Twitter”,  is a micro-blogging site. This Weibo data was collected for research in COVID-19 only. The data was crawled on the Weibo platform from December 7, 2019 to April 4, 2020. 

The data is crawled in two phases, covering a total of 4,047,389 Weibo posts. The first crawler ran on February 26, 2020 and collected 3.3 million Weibo posts from January 18, 2020 to February 26, 2020. The second crawler ran on April 4, crawling from December 7, 2020 to April 4, 2020 to complement the original dataset. The temporal distribution of the Weibo data is shown in Figure 1.

![](./images/weibo_temporal.png)

### Citation
If you use this data in your research, please cite the following article. Please feel free to reach out to Yujia Zhai at yjzhai@tjnu.edu.cn for questions. 

Leng, Yan, Yujia Zhai, Shaojing Sun, Yifei Wu, Jordan Selzer, Sharon Strover, Julia Fensel, Alex Pentland, and Ying Ding. "Analysis of misinformation during the COVID-19 outbreak in China: cultural, social and political entanglements." arXiv preprint arXiv:2005.10414 (2020).

## Data collection method

The Weibo data is obtained by a python crawler. The crawler automatically uses Weibo's advanced search function for keyword indexing. 

The keywords we used included:
- COVID-19
- novel coronavirus(新型冠状病毒)
- corona(新冠)
- epidemics(疫情)
- novel pneumonia(新型肺炎)
- pneumonia in Wuhan(武汉+肺炎)

The crawler program automatically entered one of the keywords into the query box, and set the query time range to be a specific hour. As illustrated in Figure 2, the crawler sets the time range to be January 18, 2020 00:00:00 to January 18, 2020 01:00:00. 

For each query, the time range increased by one hour and each query searched all the new posts within an hour. Each query returned a maximum of 50 pages, each contained around 20 posts. Therefore, if the number of posts within that hour exceeded 1000, the posts could not be fully collected due to the limitations of the search function. If the number posts exceed the page limits, we cannot fully collect the information due to the limitations of the search function. 

![](./images/weibo_search.png)

## Metadata of the Weibo data
We illustrate a weibo in Figure 3, which contains user name, content, timestamp, number of reposts, comments and likes. 

![](./images/weibo.png)

We present the Weibo metadata in Table 1 and Figure 4. 

![](./images/weibo_data.png)

