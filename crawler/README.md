# About Solution
With This peace of code we crawl the web page and inner components . By Allowing Specific domain we can make extension to parse other domain pages also .

# Step to Execute :- 

1) Download Zip from Git Repository .

2) From Eclipse Import project and run maven goal as
	clean compile test spring-boot:run
	
	For Command Line 
	mvn clean compile test spring-boot:run
	
# About Implementation :-

A. We Have Crawl Site Class with member AS allowedDomains this allow us to crawl all the page belong to Domain .This Function recursively crawl the pages which are belong to allowed Domain and till max no of pages to be crawl which is set in constants.    

B. In Crawl Service we call Crawl site Function by setting member values Service .

C. CrawlerController :- This Is Controller Class Which map to url " crawler/crawl/site " . This controller Class Takes CrawlRequest As a input which has  3 member .

	1. url (mandetory)		:- This is the page url which we want to crawl .
	2. noOfPagesToCrawl	:- This number indicated how many link or menu system need to crawl
									(Optional) - Default is 10 .
	3. allowedDomain		:- This indicates if we want to crawl for specific domain then we can 									set this .		(Optional)
	
	At this moment in Controller For given site if allowes Domain is not provided we extract domain of input site (url) , and crawl page belong to this domain .
	
	  	 