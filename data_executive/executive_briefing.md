# Executive Briefing






   <br /> 
   <br />

<div align='center' ><font size= 50 >Where Worth to Invest? </font></div>  

   <br /> 
   <br />
<div align='center' ><font size= 20 > Depicting the Spatial Pattern of Airbnb Local Market </font></div> 

   <br /> 
   <br />
<div align='center' ><font size= 20 > In London</font></div> 


   <br /> 
   <br /> 
   <br /> 


## Executive summary
Airbnb has rapidly grown to be the dominant sharing accommodation platform in these years. Continuously expanding enterprise-scale and constantly rising academic enthusiasm indicate a promising investment prospect on Airbnb. This report depicts the Airbnb market in London and gives targeted investment advice according to local markets' spatial discrepancy. Lower Layer Out Put Areas (LSOAs) are set as the scale of the local market. Integrating eight listing attributes that impact Airbnb's market performance into LSOA level and using an approach of Kmeans clustering, the London Airbnb market is divided into six clusters:  cluster in central metropolitan, cluster in outer suburbs, cluster in the suburbs with poor listing quality, cluster in the suburbs with fine listing quality, cluster in suburbs which operated by commercial hosts, and cluster which loosely distributing in the city. Investment in the central metropolitan area should be discreet because the high listing saturation creates an intensely competitive market. Instead, the investment could be considered in the suburbs with poor listing quality or outer suburbs since the market still has considerable shortfalls in these areas.    


   <br /> 
   <br />

## Background  
In recent years, the booming sharing economy has brought enormous economic benefits by creating markets based on digital platforms that enable connected users to exchange, share, and rent goods (Sundararajan, cited in Sarkar, Koohikamali and Pick, 2020, p984). Airbnb is one of the dominant shared accommodation platforms. With an innovative business model that operates as a transaction facilitator for users to share and rent their spaces, Airbnb has displayed huge market potential with unexpected fast expansion since its birth in 2007. Guttentag (2015), one of the earliest scholars who paid attention to Airbnb, praised it as one of the most significant innovations in tourism and foresaw it would profoundly impact the traditional tourism industry. In fact, the development and influence of Airbnb are much over Guttentag's expectation, even reflected in rapid growing academic concerns. Airbnb studies experienced an exponential increase after 2016, and the hosts and guests are the most popular topics, revealing the popularity in researching Airbnb's profit model (Guttentag, 2019). In 2020, journal articles about Airbnb had diversly expanded into five categories covering host-guest relationships, hosts, guests, hotel industry and local destination, and nine sub-topics (Sainaghi and Baggio, 2020). According to Airbnb's latest report in 2021, the platform has owned more than 5.6 million listings in over 100000 cities covering 220 countries and regions (Airbnb, 2021a). The revenue of the third quarter of 2021 has achieved 2.2 billion dollars, with a net income of 834 million dollars (Airbnb, 2021b). Indubitably, Airbnb has gained phenomenal success worldwide in the sharing economy trend.

The rapidly expanding enterprise-scale and continuously rising academic enthusiasm reveal Airbnb's foreseeably promising future. Following the market trend, seizing sharing economy opportunities and investing in Airbnb would be a wise choice. This report tries to give investment suggestions within the scope of the London Airbnb market. By exploring the spatial pattern of Airbnb listings and drawing portraits for local markets by using listings' characteristics, the report hopes to give targeted investment advice according to local markets' spatial discrepancy.
 

   <br /> 
   <br />

## Data Analysis

#### Data
* The report uses publicly available data from Inside Airbnb, scraped from the Airbnb website in October 2021. There is a total of 67903 listings in London, of each has 73 attributes about price per night, room type, review, rating, and so on.
* Besides, the LSOA boundary obtained from London Datastore is used as the geographical scale for the report.


#### Description of Analysis 
Eight characteristics of Airbnb listings covering host attributes, property attributes, rental rules, and review attributes are selected to depict the spatial pattern of Airbnb in London (Table 1). These characteristics have been proved in a prior study (Wang and Nicolau, 2017) to impact Airbnb's market performance. However, only 28% of listings have at least one review in the past 12 months and are regarded as currently active listings on the platform, while inactive listings are not included in the scope of this report. The report only focuses on the entire home and private room since over 98% of listings fall into the two room-type categories. After cleaning, tidying, and removing nan values, 19008 listings are kept in the end. 



<center>
    <img style="border-radius: 0.3125em;
    #box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);"  src="https://github.com/Siricvbl/i2p/blob/00f85ec19fab45981aea61a58861af9d4e455252/data_executive/img/listing_description.png?raw=true" width="468" height="175"> 
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">Table 1. Description of Airbnb Listings Attributes</div>
</center>
  <br /> 
  <br /> 
  

The following map shows the distribution of Airbnb listings in London for each listing characteristic, respectively (Figure 1). Overall, the listings display a central scattering distribution that listings are concentrated in urban centers and decrease with distance decay. Listings near the city center are primarily entire homes, predominately operated by hosts with multi-listings, with a relatively high price per night. However, listings in the central area are generally rated lower than suburban areas. There are no particular patterns in characteristics of the total number of reviews, reviews per month, superhosts, and minimum booking nights. Most listings receive single digits reviews and welcome a minimum 1-2 night booking. Most hosts are not superhosts.  

<center>
    <img style="border-radius: 0.3125em;
    #box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);"  src="https://github.com/Siricvbl/i2p/blob/3115ca0b416ffef29a4fb1e164308f7b10799065/data_executive/img/listings.png?raw=true" width="1036.36" height="851.11">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    #display: inline-block;
    color: #999;
    padding: 2px;">Figure 1. Distribution of Airbnb Listings in London</div>
</center>

  <br /> 
  <br /> 
  

#### Approach
After exploring the distribution of listing attributes, the report hopes to display the spatial pattern of current Airbnb's local markets with the attributes above. For this purpose, an approach of KMeans clustering is used. There are several preparatory works before clustering. 

* First, listing characteristics are integrated into LSOA to count the number of the entire home and private room listings, calculate the superhost proportion and compute the mean of other attributes for each LSOA unit. 

* Next, a power transformer is used to make data more Gaussian-like. 

* Then, by calculating silhouette scores in a range between 2 and 15, 6 is determined as the optimal number of clusters to interpret Airbnb's local market with a score of 0.44.



   <br /> 
   <br />

#### Results
The result indicates a distinct spatial discrepancy of Airbnb's local market that is divided into 6 clusters. There is an apparent gathering (cluster 4) in the central metropolitan area, and some parts of Hillingdon, Bromley, and Richmond are also grouped into this cluster (Figure 2). These areas have the most listings, with a moderate average price per night but low review numbers and superhost proportion (Figure 3, Table 2). Listings in cluster 0 are loosely distributed in the city, having many more homes than private rooms, relatively high prices, and the highest minimum booking nights. In cluster 3, the average price is the highest, and hosts own the most listings, but the review rating is meager. These listings are mainly in suburban areas. Cluster 2 and 5 have similar low average prices, a great number of private rooms, and both are in the suburbs. The difference is that listings in cluster 2 have the highest superhost proportion and receive plenty of good review ratings, which is at opposite poles of those in cluster 5 . Cluster 0 are those outer suburbs yet out of Airbnb's coverage.


<center>
    <img style="border-radius: 0.3125em;
    #box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);"  src="https://github.com/Siricvbl/i2p/blob/3115ca0b416ffef29a4fb1e164308f7b10799065/data_executive/img/cluster_result_map.png?raw=true" width="1000" height="600">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">Figure 2. Airbnb Clusters in London</div>
</center>
 
   <br /> 
   <br /> 
   <br /> 
   <br /> 
   <br /> 
<center>
    <img style="border-radius: 0.3125em;
    #box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);"  src="https://github.com/Siricvbl/i2p/blob/3115ca0b416ffef29a4fb1e164308f7b10799065/data_executive/img/cluster_result_variables.png?raw=true" width="800" height="600">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">Figure 3. Airbnb Listing Attributes in Each Cluster</div>
</center>
   
  <br /> 
  <br /> 
  <br /> 
  
<center>
    <img style="border-radius: 0.3125em;
    #box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);"  src="https://github.com/Siricvbl/i2p/blob/0bc4b4615c3f2e27f715ce1b9db4b96911da0693/data_executive/img/cluster_result_table.png?raw=true" width="1000 " height=""> 
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">Table 2. Mean of Airbnb Listing Attributes in Each Cluster</div>
</center>

  <br /> 
  <br /> 


## Conclusion
Depending on the clustering results, Airbnb's market could be  mainly divided into three spatial distribution patterns in London: central metropolitan, suburbs, and outer suburbs. 


Listings in the central metropolitan (cluster 4) are a mixed bunch. The non-remarkable values of average prices and the average number of listings each host may be due to the areas containing plenty and various grades of listings and simultaneously favored by individual hosts and commercial hosts. Listings may face fierce competition in these areas. So investment in the central metropolitan should be considered carefully in the condition of high market saturation.

Airbnb market in the suburbs displays three distinct business models:  fine listings held by individual superhosts(cluster 2), poor listings held by individual hosts(cluster 5), and high-end listings operated by commerical hosts(cluster 3). The hosts' small average number of listings reveals that commercial hosts have not entered clusters 2 and 5. In cluster 2, listings seem mostly held by individual hosts who aim to provide prime-quality listings with low prices, accumulating good feedbacks. Investments in these areas have to make many efforts to compete with these superhosts. By contrast, cluster 5 has poor performance in the Airbnb market. It is necessary to evaluate the market potential in these areas, but it could be an opportunity for investors since the current listings are uncompetitive. Another model is high-end listings operated by commercial hosts. These listings take a high-end route with a high price and high review ratings. Investment in these areas means having to compete with existing commerical hosts.

Outer suburbs identity a gap in the Airbnb market (cluster 1). Far away from the city center and tourist attractions made these areas unappealing, but it does not mean those areas are not worth to invest. Instead, investing in suburbs could be an excellent opportunity to get ahead of the market if tourism develops in these areas soon.

Finally, the report restates that it only depicts the spatial pattern of performance of the Airbnb market based on listing attributes, and tries to provide references for Airbnb investments. However, other variables besides listing attributes such as local housing price and the competition of traditional tourism accommodation should also be considered when making an investment decision.

   <br />  
   <br />  
   <br />  
   <br />   

<div STYLE="page-break-after: always;"></div>  


# Bibliography


[Airbnb (2021a). About Us.](https://news.airbnb.com/about-us/)


[Airbnb (2021b). Airbnb third quarter 2021 financial results.](https://news.airbnb.com/airbnb-third-quarter-2021-financial-results/)

[Guttentag, D](https://doi.org/10.1080/13683500.2013.827159) . (2015). Airbnb: disruptive innovation and the rise of an informal tourism accommodation sector. Current Issues in Tourism, 18(12), 1192–1217. 

[Guttentag, D](https://doi.org/10.1108/JHTT-08-2018-0075). (2019). Progress on Airbnb: a literature review. In Journal of Hospitality and Tourism Technology (Vol. 10, Issue 3, pp. 233–263). Emerald Group Holdings Ltd. 

[Sarkar, A., Koohikamali, M., & Pick, J. B.](https://doi.org/10.1108/ITP-10-2018-0481) (2020). Spatial and socioeconomic analysis of host participation in the sharing economy: Airbnb in New York City. Information Technology and People, 33(3), 983–1009. 

[Sainaghi, R., & Baggio, R.](https://doi.org/10.1016/j.ijhm.2019.102393) (2020). Clusters of topics and research designs in peer-to-peer accommodation platforms. International Journal of Hospitality Management, 88. 

[Wang, D., & Nicolau, J. L.](https://doi.org/10.1016/j.ijhm.2016.12.007) (2017). Price determinants of sharing economy based accommodation rental: A study of listings from 33 cities on Airbnb.com. International Journal of Hospitality Management, 62, 120–131. 

