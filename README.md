# spell-checking
#-*- coding: utf-8 -*-

import nltk
import re

input_file = open("C:/Users/FILE/Desktop/test3.txt" , encoding="utf8")
input_file1 = open("C:/Users/FILE/Desktop/distinct1.txt" , encoding="utf8")

#inp = "پولیس"
inp=input("enter word")
#print(inp)
text = ""
for line in input_file:
    #print(st)
    lines = line.strip()
    line1=re.sub("\n" , "" , lines)
    if inp == line1:
   # if inp == input_file:
        text1 = inp
        print(text1 , line1)
    else:

        text=nltk.edit_distance(inp,line1)
        #text = nltk.word_tokenize(inp)
        #p = nltk.pos_tag(text)

        print(text,line1)
for line in input_file:
    if nltk.edit_distance(inp,line1)<=2 :
        text1=nltk.ngrams(line1,2)
        print(text1)
        #text1 = nltk.HiddenMarkovModelTagger(inp, line1)
    else:
        print("value")








