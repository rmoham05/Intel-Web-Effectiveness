# Intel-Web-Effectiveness
Analysing the Effectiveness of the Intel Website

<h1>Analysis on Effectiveness of <span>Intel</span> Website</h1>
<h2>Introduction:</h2>
            <p>Intel is one of the most famous American global technology companies and the world’s largest semiconductor chip producer. The majority of computing devices are equipped with at least one of the Intel processors. Intel also produces motherboard chipsets, integrated circuits, graphic chips, network interface controllers, and other communications and computing utility devices. Therefore, tons of companies and individuals require access to a supporting website, which provides them with the information they look for. In this article, we are going to analyze the effectiveness of the Intel website based on its customers' experience through navigating in Intel website.</p>
        
<h2>Dataset Description:</h2>
<p>The dataset is consists of 116208 rows (samples) and 24 columns (features). A clear description of the dataset can be seen in the picture below.</p>

            <pre>
                RangeIndex: 116208 entries, 0 to 116207
                Data columns (total 24 columns):
                RawID                                                     116208 non-null int64      
                Improve site to better meet needs                         364 non-null object       <span class=red>%99 null</span>
                Url most time                                             116208 non-null object    <span class=green>%0 null</span>
                Year                                                      116208 non-null int64     <span class=green>%0 null</span>
                Satisfaction                                              116208 non-null int64     <span class=green>%0 null</span>
                Found Primary Information                                 85068 non-null float64    <span class=orange>%27 null</span>
                Easy To Find                                              91915 non-null float64    <span class=orange>%20 null</span>
                Up To Date                                                80659 non-null float64    <span class=orange>%30 null</span>
                Easy To Understand                                        92553 non-null float64    <span class=orange>%20 null</span>
                Right Level of Detail                                     89771 non-null float64    <span class=orange>%23 null</span>
                Business (1) vs Personal (2)                              114124 non-null float64   <span class=orange>%1.7 null</span>
                Reason for visit                                          73693 non-null float64    <span class=orange>%36.5 null</span>
                Purchase decision process                                 17015 non-null float64    <span class=red>%85 null</span>
                Planned spending                                          15707 non-null float64    <span class=red>%86 null</span>
                Intel.com makes it easy to determine where to purchase    13553 non-null float64    <span class=red>%88 null</span>
                Adoption                                                  54637 non-null float64    <span class=red>%53 null</span>
                Frequency of visit                                        54520 non-null float64    <span class=red>%53 null</span>
                Audience                                                  65160 non-null float64    <span class=red>%43 null</span>
                Section                                                   116208 non-null object    <span class=green>%0 null</span>
                Directory                                                 116208 non-null object    <span class=green>%0 null</span>
                Sub-Directory                                             116208 non-null object    <span class=green>%0 null</span>
                Domains                                                   116208 non-null int64     <span class=green>%0 null</span>
                Target Audience Filter                                    116208 non-null int64     <span class=green>%0 null</span>
                Quarters                                                  116208 non-null int64     <span class=green>%0 null</span>
                </pre>

<p>As can be seen in some columns, we have more than %50 of Null value that we showed them by red. These columns in the next step (pre-processing step) will be removed from our dataset. The columns in which there is no Null value are shown in green colour. We will not touch them in the preprocessing step, but the columns with less than %50 Null value need some modification for better analysis. we will explain better in the Preprocessing step how to do the cleaning step for these columns.</p>
        
<h2>Preprocessing step:</h2>
<p>Having removed the columns with more than %50 Null value, we need to fill the null value for the columns with less than %50 Null value. To this aim, we can apply different methods:</p>
            <ul>
                <li>Method 1: Most Common Class</li>
                <li>Method 2: “Unknown” Class</li>
            </ul>
<p>Method 2 is chosen for filling the Null value, and it is because we want to see the actual differences between various groups. In this case, the unknown information by itself is valuable information for us because it shows the percentage of viewers who were not willing to answer some specific questions, which might be because of their bad experience and so on.</p>

<p>In the table below, you can see the Dataset information after being cleaned.</p>

            <pre>
                    RangeIndex: 116208 entries, 0 to 116207
                    Data columns (total 18 columns):
                    RawID                           116208 non-null int64
                    Url most time                   116208 non-null object
                    Year                            116208 non-null int64
                    Satisfaction                    116208 non-null int64
                    Found Primary Information       116208 non-null object
                    Easy To Find                    116208 non-null object
                    Up To Date                      116208 non-null object
                    Easy To Understand              116208 non-null object
                    Right Level of Detail           116208 non-null object
                    Business (1) vs Personal (2)    116208 non-null object
                    Reason for visit                116208 non-null object
                    Audience                        116208 non-null object
                    Section                         116208 non-null object
                    Directory                       116208 non-null object
                    Sub-Directory                   116208 non-null object
                    Domains                         116208 non-null int64
                    Target Audience Filter          116208 non-null int64
                    Quarters                        116208 non-null int64
            </pre>

        

<h2>Analysis based on Satisfaction Level and KPI's:</h2>
       
<p>One of the primary reasons to show the website's effectiveness is analyzing customers' level of satisfaction in using the Website. As can be seen from 116208 participants, more than 68 percent of the viewers were satisfied with their experience, and just %12 were dissatisfied. It clearly shows that, in general, Intel Website has had a good impact on the majority of its viewers. </p>
                

<img src="https://i.postimg.cc/NjmD88MB/1.png" alt="">
                

<p>Many reasons can influence customer experience while they are visiting the website. These reasons are called KPI that includes "Easy to Find", "Easy to Understand", "Up to Date", "Right Level of Detail", "Found Primary Info," and so on.</p>
<p>We will check if there is any correlation between KPI factors and customers' satisfaction levels in the following steps. This will help us to analyze further unsatisfied customers and improve the effectiveness of the website.</p>

<img src="https://i.postimg.cc/28PTB9C0/2.png" alt="">
<img src="https://i.postimg.cc/CLZm5ppZ/3.png" alt="">
<img src="https://i.postimg.cc/XN1sn7mS/4.png" alt="">
<img src="https://i.postimg.cc/FzzG02fB/5.png" alt="">
<img src="https://i.postimg.cc/wv00y6BN/6.png" alt="">

<p>As shown in the above figures, there is a positive correlation between all KPI's and customers' level of satisfaction. When the satisfaction is high, KPI's are also at their highest level, and on the other hand, when the customers are not satisfied, KPI's are also considerably low. For example, when customers find the website easy to understand, they are mostly satisfied, or when they see up-to-date information, they will have a satisfactory experience.</p>


<h2>Removing Outliers:</h2>

<h3>Did we consider the outliers in our analysis?</h3>
                
<img src="https://st3.depositphotos.com/1001911/17377/v/450/depositphotos_173773006-stock-illustration-vector-ponder-emoticon.jpg" alt="">
                
<p>One of the most important steps is to define the outliers and delete them from our dataset</p>

<ul>
  <h4>There might be two sort of outlies in our dataset</h4>
  <li>Those who were satisfied but chose all the KPI as not satisfied</li>
  <li>Those who were not satisfied but chose all the KPI as satisfied</li>
</ul>
        
<h2>Analysis based on Reason of Visit:</h2>
 <p>As we mentioned earlier, the Intel website's main objective is preparing customers with information for processors or other new technologies. Therefore, we expect most viewers to visit the website for such purposes, such as Learning about a product or Research before Purchase. This helps us to understand the different categories of our viewers based on the purpose of their visit. After that, we can analyze further in each group the level of satisfaction, which finally increases the website's effectiveness.</p>

<p>More than 68 percent of the viewers on the website consists of those who visited the website to learn about a product or to Search before purchasing an item, and 31.6 percent visited the website for other purposes.</p>
               
<img src="https://i.postimg.cc/kGHssfKX/7.png" alt="">
              

<p>Now that we know the proportion of viewers based on their reason for visiting the website, It is worth analyzing the percentage of satisfied and dissatisfied people among these different groups. It is clear that the more we change the reason for the visit from other purposes to purposeful reasons such as learning about a product or research before purchase, the higher the percentage of satisfied viewers will be.</p>

            
<img src="https://i.postimg.cc/R01Pm15X/8.png" alt="">
<img src="https://i.postimg.cc/q7HmWbYN/9.png" alt="">
<img src="https://i.postimg.cc/TwRt3yTG/10.png" alt="">

<p>For the next step, we need to find which section of the website viewers with the various reason for the visit and who were not successful in any of the KPIs were mostly located. This helps us to find the effectiveness of the website in different sections.</p>


<p>It is shown that more than 74 percent of those who had Learning purposes and were not satisfied with any KPI's were mostly located in the products section, and 18 percent of these viewers were in the Solution and Hompage section.</p>
<img src="https://i.postimg.cc/YqVDzqzf/11.png" alt="">

            
 <p>IIt is shown that more than 79 percent of those who had Search purposes and were not satisfied with any KPI's were mostly located in the products section, and 15 percent of these viewers were in the Solution and Hompage section.</p>
 
<img src="https://i.postimg.cc/T3D77Mk8/12.png" alt="">

            
<p>It is shown that more than 50 percent of those who had Other purposes and were not satisfied with any KPI's were mostly located in the products section, almost 30 percent of these viewers were in the Solution and Hompage section and more than 19 percent in other sections.</p>
               
<img src="https://i.postimg.cc/rFzY4txw/13.png" alt="">


<h2>Conclusion and Recomendation:</h2>

<p>The Intel website's key focus is on its products and providing its clients with the required information about those products. According to our analysis, Intel has been very effective for this aim. However, 12 percent of its customers were not satisfied with their experience. It has been shown that if Intel focuses more on the Product, Solution and Homepage section and makes access to the information easier, especially for those groups whose purpose of the visit is to Learn and Research, it will be able to decrease dramatically the number of dissatisfied viewers.</p>
        

    
