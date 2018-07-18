# psw_checkers

import re
while True:
    psw = str(input())
    if len(psw) > 8:   #should be longer than 8
        pswRegexCap = re.compile('[A-Z]+')   #re  
        pswRegexNum = re.compile(r'\d+')
        pswRegexWord = re.compile('[a-z]')
        if pswRegexCap.search(psw):                        
            if pswRegexNum.search(psw):                
                if pswRegexWord.search(psw):
                    print('your psw is '+ psw)
                    break
                else:print('make sure your psw contains one word')
            else:print('make sure your psw contains one digit')
        else:print('make sure your psw contains one cap')
    else:print('len of psw should be more than 8,plese re-input your psw')
