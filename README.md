# baike_spider
It's my first web crawler program based on Python.
My purpose was to copy the titles and abstractions of the first few items on Baidu Baike related to 'python' to a html file.

### structure of the program
- __init__.py
- spider_main.py
- url_manager.py
- html_parser.py
- html_downloader.py
- html_outputer.py
- output.html

Now, let's take a look at what they are doing in this program:

__spider_main.py__

This is the entrance of the program.
``` python
if __name__=="__main__":
    root_url = "http://baike.baidu.com/item/python" #URL entrance
    obj_spider = SpiderMain()
    obj_spider.craw(root_url) #dispatcher
```

__url_manager__

This is the url manager that manages the crawled and to-be-crawled urls.
It stores the crawled urls so that the program doesn't have to visit the page again, and returns a new url to the downloader.

__html_downloader__
