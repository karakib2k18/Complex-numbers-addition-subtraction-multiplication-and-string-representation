# Complex-numbers-addition-subtraction-multiplication-and-string-representation
import math
class MyComplex(object):
    def __init__(self, c1, c2):
        '''Creates Complex Number'''
        self.c1 = c1
        self.c2 = c2

    def __str__(self):
        '''Returns complex number as a string'''
        return '(%s, %s)' % (self.c1, self.c2) 

    def __add__(self, rhs):
        '''Adds complex numbers'''
        return MyComplex(self.c1 + rhs.c1, self.c2 + rhs.c2)
    
    def __sub__(self, rhs):
        '''Subtracts complex numbers'''
        return MyComplex(self.c1 - rhs.c1, self.c2 - rhs.c2)
    
    def __mul__(self, rhs):
        '''multiply complex numbers'''
        return MyComplex(self.c1 + rhs.c1, self.c2 + rhs.c2)
def main():
  c1 = MyComplex(3,-5)
  c2 = MyComplex(2,3)
  print(c1,c2)
  print('c1+c2=', c1+c2)
  print('c1-c2=', c1-c2)
  print('c1*c2=', c1*c2)
if __name__=="__main__":main()
