#!usr/bin/env python
#coding:utf-8

import random

guesslist = ["石头","剪刀","布"]
guize = [["布","石头"],["石头","剪刀"],["剪刀","布"]]

while True:
    computer = random.choice(guesslist)
    people = raw_input('请输入：石头，简单，布\n你的输入：').strip()
    print "电脑输入："+ computer

    if people not in guesslist:
        people = raw_input('请输入：石头，剪刀，布\n你的输入：').strip()
        print "电脑输入：" + computer
        continue
    if computer == people:
        print ("平手，再玩一次！")

    elif [computer,people] in guize:
        print ("逗比了吧，电脑获胜！")

    else:
        print ("蛋疼，好吧，你赢了！")
        break
        
