import urllib
import json
import os
import sys
import colorama
from colorama import Fore, Back, Style
import urllib2

os.system("clear")

#afficher votre ip :
url = "http://ip-api.com/json/"
load1 = urllib2.urlopen(url)
read1 = load1.read()
result1 = json.loads(read1)


print("""\033[40m\33[32m



  ##  ||  #HH|     H|        #HH|            ##HH||                   ##
  ##  || ##  ||    H|         #|  ##H|         #|   ## H| ##|    #HH| ## H|
  ##  || ## H||  #HH|         #|  ## H| #H||   #|   ##H|    H|  ##    ##H|
   #HH|  ##H || ## H|         #|  ##H|         #|   ##    ##H|  ##    ##H|
    #|    #HH|   #HH|        #HH| ##           #|   ##    ##HH|  #HH| ## H|
                      ##HH||      ##








""")

print("""\033[32m

 ____________________
|                   |
| ip Tracker Tool   |
|                   |
|                   |
|  by Cableyz,rj45  |
|___________________|""")

print("")

print ("\n\033[1;33mYour IP: \033[1;33m" + result1['query'])
while True :
        ip = raw_input("\033[32m press enter to track ! : ")
        ip = raw_input("\033[33m Enter Target IP (ex : 1.1.1.1) : ")
        url = 'http://ip-api.com/json/'
        response = urllib.urlopen(url + ip)
        data = response.read()
        rkt = json.loads(data)
        print
        print (data)
        print
        print ('Done')
        print