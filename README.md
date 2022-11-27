# -*- coding: utf-8 -*-
"""
Created on Sat Nov 26 13:52:00 2022

@author: cat
"""
import time
pay_list=[]
x=1
pay=-1
while True :
    pay=eval(input("輸入第 %s 筆賠率(離開請輸入0):"%x))
    if pay<=0:
        break
    pay_list.append(pay)
    print("共%s注"%x)
    x=x+1
total_bet=0    
for i in range(len(pay_list)):
    print(1/(pay_list[i]+1))
    total_bet=total_bet+(1/(pay_list[i]+1))
print(total_bet)
for i in range(10):
    time.sleep(1)
