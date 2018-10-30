# linebot
- in this repository, just demo a bot it only can reply a specific word for reply
## included files
- procfile
  - for heroku web service
- requirements
  - pip
- app.py
  - coding with python
  - flask for frame
- runtime.txt
def loadPMJson():
    with urllib.request.urlopen("http://opendata2.epa.gov.tw/AQX.json") as url:
        data = json.loads(url.read().decode())
        for ele in data:
            pm_site[ele['SiteName']] = ele['PM2.5']
