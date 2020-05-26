# TikTok API Reverse Engineering
Initial commit as old code is deprecated because urls now require anti-spam parameters and signatures.

# Instructions
Sample Implementation given in lower part of api.py

To download all videos of a username, change the value of username
```
        ###############################
        # change target username here #
        ###############################
        username = 'ENTER_USERNAME_HERE'
        ###############################
        details = tt.getUserDetails(username)
```

To download all trending videos, just change this line from
```
        # change videos to number of videos you want to return
        reply = tt.getUserTikToks(_id, videos)
```

to this, where videos is the number of videos you would like to get
```
        # change videos to number of videos you want to return
        reply = tt.getTrending(videos)
```

### api.py
```
class TikTok:
    def __init__(self, path: str):
        pass
        
    def _signURL(self, url) -> str:
        pass
        
    def getUserDetails(self, username) -> dict():
        pass
    
    def getTrending(self, count: int) -> list(): 
        pass
        
    def getUserTikToks(self, userid, count: int) -> list():
        pass
```

### robots.py
```
    def getAllowedAgents() -> list():
        pass
```

### Work In Progress
- [x] Integrate Selenium/Chrome Webdriver
- [x] Partial concurrency
- [x] robots.py - Reads User-Agents from https://www.tiktok.com/robots.txt
- [x] Function: _signURL(url:str) -> str
- [x] Function: getUserDetails(username:str) -> dict()
- [x] Function: getTrending(count: int) -> list(dict())
- [x] Function: getUserTiktoks(id:int, count:int) -> list(dict())
- [ ] Complete all API functions
- [ ] Add rotating proxies
- [ ] Profile crawler
- [ ] Trend crawler
- [ ] Full concurrency

### Install Packages
```
pip install -r requirements.txt
```

### Donate BTC

<p align="left">
<img width="300" height="300" src="https://i.imgur.com/PhC1zJG.png">
</p>
1zdraxHPQfZ8wvpMXt2VYhnGwmkLCf7UL
