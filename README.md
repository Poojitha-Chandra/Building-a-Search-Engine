# <h1>Building-a-Search-Engine</h1>
Before going to know the code about our search engine,let's know something about *Beautiful Soup*
# <h2>Beautiful Soup installation</h2>
Beautiful Soup installation is done by downloading the code `bs4 zip file` and unzipping the file in the same directory as this file.It contains some python files.If you want to use the Beautiful Soup,then include the import bs4 in the code.
# <h2>Necessity of Beautiful Soup </h2>
Ok then,now assuming that you can import Beautiful Soup!For suppose we have a task of reading some data from net.Then,the duty of Beautiful Soup would be like,it takes the URL from which we want to extract data.BeautifulSoup is smart enough to convert and cleans it up.That means it takes the nasty HTML using parser,which is extremely useful for `web scrapping`.
# <h2>Main steps taken for building a search engine</h2>
- Write a simple web page crawler
- Compute a simple version of Google's Page Rank algorithm
- Visualize the resulting network
# <h2>Search Engine Architecture</h2>
* Web Crawling
* Index building
* Searching
# <h3>Web Crawler</h3>
A `Web Crawler` is a computer program that browses the World Wide Web in a methodical, automated manner.These are mainly used to create a copy of all the visited pages for later processing by a ***Search Engine*** that will index the downloaded pages to provide fast searches.
* Retrieve a page
* Look through the page for links
* Add the links to a list of "to be retrieved" sites
* Repeat...
# <h3>Search Indexing</h3>
Search engine indexing **collects,parses** and **stores** data to facilitate fast and accurate information retrieval.The purpose of *storing the index* is to `optimize speed and performance` in finding relevant documents for a search query.Without an index, the search enginewould scan every document in corpus,which would require considerable time and computing power.
# <h2>Overview</h2>
The way it works is that actually only `spiders a single webpage`.So, we are going to run five chunks of code.The basic spidering code is in **spider.py**.This part includes getting some stuff from the web,in this case webpages.Having a database **spider.sqlite** to capture the stuff.The spidering code parses webpages using *Beautiful Soup* and adds stuff to the database.

**spreset.py** just resets the page rank and **sprank.py** runs as many iterations of page rank.

Now,comes the funny part of the entire chunks that is *Visualisation*.**spdump.py** just runs a SQL query by connecting to our database,creating a cursor,selecting count and justs shows number of links.

Upnext,the visualizing process includes **spjson.py** that looks all the data in the database, produces a Java Script file namely **spider.js** and finally fed into visualization using **force.html**.*d3.js* is a great visualization library.

![visualization](https://github.com/Poojitha-Chandra/Building-a-Search-Engine/issues/1#issue-679805570)
