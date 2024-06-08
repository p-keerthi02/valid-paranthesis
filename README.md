class Solution(object):
    def isValid(self, s):
       x=[]
       input = {")":"(","}":"{","]":"["}
       for p in s:
        if p in input.values():
            x.append(p)
        elif x and input[p] == x[-1]:
            x.pop()
        else:
            return False 
       return x == []     
    
