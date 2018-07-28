# Podcast-for-AIY
Code for playing Podcast in Python  (Example from Tony Evans Podcast)
>>> import urllib.request
>>> url = 'https://www.oneplace.com/ministries/the-alternative/subscribe/podcast.xml'
>>> response = urllib.request.urlopen(url)
>>> data = response.read()
>>> text = data.decode('utf-8')
>>> startmp3 = text.find('<enclosure url="')+16
>>> endmp3 = text.find('.mp3',startmp3)+4
>>> command = text[startmp3:endmp3]
>>> command
'http://www.oneplace.com/ministries/the-alternative/subscribe/podcast/fasting-for-marriage-702578.mp3'
p = subprocess.Popen(["/usr/bin/cvlc",command],stdin=subprocess.PIPE,stdout=subprocess.PIPE)
pkill = subprocess.Popen(["/usr/bin/pkill","vlc"],stdin=subprocess.PIPE
p.kill()
