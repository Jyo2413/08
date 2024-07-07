class Complex():
 def __init__(self, a, b):
 self.real=a
 self.imaginary=b

 def add(self,C1):
 temp=Complex(0, 0)
 temp.real = self.real + C1.real;
 temp.imaginary = self.imaginary + C1.imaginary;
 return temp;
 def displayComplex(self):
 print(self.real,'+i',self.imaginary, sep="")
complexList = []
n=int(input('Enter the value of n: '))
if n>=2:
 for i in range(n):
 a=int(input('Enter real part of the complex number '+str(i+1)+':'))
 b=int(input('Enter imaginary part of the complex number '+str(i+1)+':'))
 Complex_Obj=Complex(a,b)
 complexList.append(Complex_Obj)
 print("\nEntered Complex numbers are : ")
 for obj in complexList:
 obj. displayComplex()
 sumObj = Complex(0,0)
 for obj in complexList:
 sumObj=sumObj.add(obj)
 print("\nSum of N complex numbers is", end = " ")
  sumObj.displayComplex()
else:
 print('Invalid input. Enter number greater than 2')
