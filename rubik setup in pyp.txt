class A:
    f=[]
    b=[]
    l=[]
    r=[]
    bo=[]
    u=[]
    
    def F(self):
        k=3
        t=[0,0,0,0]
        while(k!=0):
            for i in range(0,2):
                for j in range(i,3-1-i):
                    temp = self.f[i][j]
                    self.f[i][j] = self.f[j][3-1-i]
                    self.f[j][3-1-i] = self.f[3-1-i][3-1-j]
                    self.f[3-1-i][3-1-j] = self.f[3-1-j][i]
                    self.f[3-1-j][i] = temp
            k=k-1
        t[0]=self.l[2][2]
        t[1]=self.l[1][2]
        t[2]=self.l[0][2]
        self.l[0][2]=self.bo[0][0]
        self.l[1][2]=self.bo[0][1]
        self.l[2][2]=self.bo[0][2]
        self.bo[0][0]=self.r[2][0]
        self.bo[0][1]=self.r[1][0]
        self.bo[0][2]=self.r[0][0]
        self.r[0][0]=self.u[2][0]
        self.r[1][0]=self.u[2][1]
        self.r[2][0]=self.u[2][2]
        self.u[2][0]=t[0]
        self.u[2][1]=t[1]
        self.u[2][2]=t[2]
        print("F",end=" ")
    def Fi(self):
        k=3
        t=[0,0,0,0]
        for i in range(0,2):
            for j in range(i,3-1-i):
                temp = self.f[i][j]
                self.f[i][j] = self.f[j][3-1-i]
                self.f[j][3-1-i] = self.f[3-1-i][3-1-j]
                self.f[3-1-i][3-1-j] = self.f[3-1-j][i]
                self.f[3-1-j][i] = temp
        while(k!=0):
            t[0]=self.l[2][2]
            t[1]=self.l[1][2]
            t[2]=self.l[0][2]
            self.l[0][2]=self.bo[0][0]
            self.l[1][2]=self.bo[0][1]
            self.l[2][2]=self.bo[0][2]
            self.bo[0][0]=self.r[2][0]
            self.bo[0][1]=self.r[1][0]
            self.bo[0][2]=self.r[0][0]
            self.r[0][0]=self.u[2][0]
            self.r[1][0]=self.u[2][1]
            self.r[2][0]=self.u[2][2]
            self.u[2][0]=t[0]
            self.u[2][1]=t[1]
            self.u[2][2]=t[2]
            k=k-1
        print("Fi",end=" ")
    def L(self):
        k=3
        t=[0,0,0,0]
        while(k!=0):
            for i in range(0,2):
                for j in range(i,3-1-i):
                    temp = self.l[i][j]
                    self.l[i][j] = self.l[j][3-1-i]
                    self.l[j][3-1-i] = self.l[3-1-i][3-1-j]
                    self.l[3-1-i][3-1-j] = self.l[3-1-j][i]
                    self.l[3-1-j][i] = temp
            k=k-1
        k=3
        while(k!=0):
            t[0]=self.bo[0][0]
            t[1]=self.bo[1][0]
            t[2]=self.bo[2][0]
            self.bo[0][0]=self.b[0][0]
            self.bo[1][0]=self.b[1][0]
            self.bo[2][0]=self.b[2][0]
            self.b[0][0]=self.u[0][0]
            self.b[1][0]=self.u[1][0]
            self.b[2][0]=self.u[2][0]
            self.u[0][0]=self.f[0][0]
            self.u[1][0]=self.f[1][0]
            self.u[2][0]=self.f[2][0]
            self.f[0][0]=t[0]
            self.f[1][0]=t[1]
            self.f[2][0]=t[2]
            k=k-1
        print("L",end=" ")
    
    def Li(self):
        k=3
        t=[0,0,0,0]
        for i in range(0,2):
            for j in range(i,3-1-i):
                temp = self.l[i][j]
                self.l[i][j] = self.l[j][3-1-i]
                self.l[j][3-1-i] = self.l[3-1-i][3-1-j]
                self.l[3-1-i][3-1-j] = self.l[3-1-j][i]
                self.l[3-1-j][i] = temp
        t[0]=self.bo[0][0]
        t[1]=self.bo[1][0]
        t[2]=self.bo[2][0]
        self.bo[0][0]=self.b[0][0]
        self.bo[1][0]=self.b[1][0]
        self.bo[2][0]=self.b[2][0]
        self.b[0][0]=self.u[0][0]
        self.b[1][0]=self.u[1][0]
        self.b[2][0]=self.u[2][0]
        self.u[0][0]=self.f[0][0]
        self.u[1][0]=self.f[1][0]
        self.u[2][0]=self.f[2][0]
        self.f[0][0]=t[0]
        self.f[1][0]=t[1]
        self.f[2][0]=t[2]
        print("Li",end=" ")
        
    def R(self):
        k=3
        t=[0,0,0]
        while(k!=0):
            for i in range(0,2):
                for j in range(i,3-1-i):
                    temp = self.r[i][j]
                    self.r[i][j] = self.r[j][3-1-i]
                    self.r[j][3-1-i] = self.r[3-1-i][3-1-j]
                    self.r[3-1-i][3-1-j] = self.r[3-1-j][i]
                    self.r[3-1-j][i] = temp
            k=k-1
        t[0]=self.bo[0][2]
        t[1]=self.bo[1][2]
        t[2]=self.bo[2][2]
        self.bo[0][2]=self.b[0][2]
        self.bo[1][2]=self.b[1][2]
        self.bo[2][2]=self.b[2][2]
        self.b[0][2]=self.u[0][2]
        self.b[1][2]=self.u[1][2]
        self.b[2][2]=self.u[2][2]
        self.u[0][2]=self.f[0][2]
        self.u[1][2]=self.f[1][2]
        self.u[2][2]=self.f[2][2]
        self.f[0][2]=t[0]
        self.f[1][2]=t[1]
        self.f[2][2]=t[2]
        print("R",end=" ")

    def Ri(self):
        k=3
        t=[0,0,0,0]
        for i in range(0,2):
            for j in range(i,3-1-i):
                temp = self.r[i][j]
                self.r[i][j] = self.r[j][3-1-i]
                self.r[j][3-1-i] = self.r[3-1-i][3-1-j]
                self.r[3-1-i][3-1-j] = self.r[3-1-j][i]
                self.r[3-1-j][i] = temp
        while(k!=0):
            t[0]=self.bo[0][2]
            t[1]=self.bo[1][2]
            t[2]=self.bo[2][2]
            self.bo[0][2]=self.b[0][2]
            self.bo[1][2]=self.b[1][2]
            self.bo[2][2]=self.b[2][2]
            self.b[0][2]=self.u[0][2]
            self.b[1][2]=self.u[1][2]
            self.b[2][2]=self.u[2][2]
            self.u[0][2]=self.f[0][2]
            self.u[1][2]=self.f[1][2]
            self.u[2][2]=self.f[2][2]
            self.f[0][2]=t[0]
            self.f[1][2]=t[1]
            self.f[2][2]=t[2]
            k=k-1
        print("Ri",end=" ")
        
    def U(self):
        k=3
        t=[0,0,0,0]
        while(k!=0):
            for i in range(0,2):
                for j in range(i,3-1-i):
                    temp = self.u[i][j]
                    self.u[i][j] = self.u[j][3-1-i]
                    self.u[j][3-1-i] = self.u[3-1-i][3-1-j]
                    self.u[3-1-i][3-1-j] = self.u[3-1-j][i]
                    self.u[3-1-j][i] = temp
            k=k-1
        t[0]=self.f[0][0]
        t[1]=self.f[0][1]
        t[2]=self.f[0][2]
        self.f[0][0]=self.r[0][0]
        self.f[0][1]=self.r[0][1]
        self.f[0][2]=self.r[0][2]        
        self.r[0][0]=self.b[2][2]
        self.r[0][1]=self.b[2][1]
        self.r[0][2]=self.b[2][0]
        self.b[2][0]=self.l[0][2]
        self.b[2][1]=self.l[0][1]
        self.b[2][2]=self.l[0][0]
        self.l[0][0]=t[0]
        self.l[0][1]=t[1]
        self.l[0][2]=t[2]
        print("U",end=" ")
        
    def Ui(self):
        k=3
        t=[0,0,0,0]
        for i in range(0,2):
            for j in range(i,3-1-i):
                temp = self.u[i][j]
                self.u[i][j] = self.u[j][3-1-i]
                self.u[j][3-1-i] = self.u[3-1-i][3-1-j]
                self.u[3-1-i][3-1-j] = self.u[3-1-j][i]
                self.u[3-1-j][i] = temp
        while(k!=0):
            t[0]=self.f[0][0]
            t[1]=self.f[0][1]
            t[2]=self.f[0][2]
            self.f[0][0]=self.r[0][0]
            self.f[0][1]=self.r[0][1]
            self.f[0][2]=self.r[0][2]        
            self.r[0][0]=self.b[2][2]
            self.r[0][1]=self.b[2][1]
            self.r[0][2]=self.b[2][0]
            self.b[2][0]=self.l[0][2]
            self.b[2][1]=self.l[0][1]
            self.b[2][2]=self.l[0][0]
            self.l[0][0]=t[0]
            self.l[0][1]=t[1]
            self.l[0][2]=t[2]
            k=k-1
        print("Ui",end=" ")
            
    def B(self):
        k=3
        t=[0,0,0]
        while(k!=0):
            for i in range(0,2):
                for j in range(i,3-1-i):
                    temp = self.b[i][j]
                    self.b[i][j] = self.b[j][3-1-i]
                    self.b[j][3-1-i] = self.b[3-1-i][3-1-j]
                    self.b[3-1-i][3-1-j] = self.b[3-1-j][i]
                    self.b[3-1-j][i] = temp
            k=k-1
        t[0]=self.l[0][0]
        t[1]=self.l[1][0]
        t[2]=self.l[2][0]
        self.l[0][0]=self.u[0][2]
        self.l[1][0]=self.u[0][1]
        self.l[2][0]=self.u[0][0]
        self.u[0][0]=self.r[0][2]
        self.u[0][1]=self.r[1][2]
        self.u[0][2]=self.r[2][2]
        self.r[0][2]=self.bo[2][2]
        self.r[1][2]=self.bo[2][1]
        self.r[2][2]=self.bo[2][0]
        self.bo[2][0]=t[0]
        self.bo[2][1]=t[1]
        self.bo[2][2]=t[2]
        print("B",end=" ")
        
    def Bi(self):
        k=3
        t=[0,0,0,0]
        for i in range(0,2):
            for j in range(i,3-1-i):
                temp = self.b[i][j]
                self.b[i][j] = self.b[j][3-1-i]
                self.b[j][3-1-i] = self.b[3-1-i][3-1-j]
                self.b[3-1-i][3-1-j] = self.b[3-1-j][i]
                self.b[3-1-j][i] = temp
        while(k!=0):
            t[0]=self.l[0][0]
            t[1]=self.l[1][0]
            t[2]=self.l[2][0]
            self.l[0][0]=self.u[0][2]
            self.l[1][0]=self.u[0][1]
            self.l[2][0]=self.u[0][0]
            self.u[0][0]=self.r[0][2]
            self.u[0][1]=self.r[1][2]
            self.u[0][2]=self.r[2][2]
            self.r[0][2]=self.bo[2][2]
            self.r[1][2]=self.bo[2][1]
            self.r[2][2]=self.bo[2][0]
            self.bo[2][0]=t[0]
            self.bo[2][1]=t[1]
            self.bo[2][2]=t[2]
            k=k-1
        print("Bi",end=" ")
            
    def Bo(self):
        k=3
        t=[0,0,0,0]
        while(k!=0):
            for i in range(0,2):
                for j in range(i,3-1-i):
                    temp = self.bo[i][j]
                    self.bo[i][j] = self.bo[j][3-1-i]
                    self.bo[j][3-1-i] = self.bo[3-1-i][3-1-j]
                    self.bo[3-1-i][3-1-j] = self.bo[3-1-j][i]
                    self.bo[3-1-j][i] = temp
            k=k-1
        t[0]=self.b[0][0]
        t[1]=self.b[0][1]
        t[2]=self.b[0][2]
        self.b[0][0]=self.r[2][2]
        self.b[0][1]=self.r[2][1]
        self.b[0][2]=self.r[2][0]
        self.r[2][0]=self.f[2][0]
        self.r[2][1]=self.f[2][1]
        self.r[2][2]=self.f[2][2]
        self.f[2][0]=self.l[2][0]
        self.f[2][1]=self.l[2][1]
        self.f[2][2]=self.l[2][2]
        self.l[2][0]=t[2]
        self.l[2][1]=t[1]
        self.l[2][2]=t[0]
        print("Bo",end=" ")
        
    def Boi(self):
        k=3
        t=[0,0,0,0]
        for i in range(0,2):
            for j in range(i,3-1-i):
                temp = self.bo[i][j]
                self.bo[i][j] = self.bo[j][3-1-i]
                self.bo[j][3-1-i] = self.bo[3-1-i][3-1-j]
                self.bo[3-1-i][3-1-j] = self.bo[3-1-j][i]
                self.bo[3-1-j][i] = temp
        while(k!=0):
            t[0]=self.b[0][0]
            t[1]=self.b[0][1]
            t[2]=self.b[0][2]
            self.b[0][0]=self.r[2][2]
            self.b[0][1]=self.r[2][1]
            self.b[0][2]=self.r[2][0]
            self.r[2][0]=self.f[2][0]
            self.r[2][1]=self.f[2][1]
            self.r[2][2]=self.f[2][2]
            self.f[2][0]=self.l[2][0]
            self.f[2][1]=self.l[2][1]
            self.f[2][2]=self.l[2][2]
            self.l[2][0]=t[2]
            self.l[2][1]=t[1]
            self.l[2][2]=t[0]
            k=k-1
        print("Boi",end=" ")
    
class B(A):
    def read(self):
        print("\nBACK")
        for i in range(3):
            self.b.append([0]*3)
        for i in range(3):
            for j in range(3):
                self.b[i][j]=input("ENTER COLOUR: ")
        print("\nupper")
        for i in range(3):
            self.u.append([0]*3)
        for i in range(3):
            for j in range(3):
                self.u[i][j]=input("ENTER COLOUR: ")
        print("\nleft")
        for i in range(3):
            self.l.append([0]*3)
        for i in range(3):
            for j in range(3):
                self.l[i][j]=input("ENTER COLOUR: ")
        print("\nfront")
        for i in range(3):
            self.f.append([0]*3)
        for i in range(3):
            for j in range(3):
                self.f[i][j]=input("ENTER COLOUR: ")
        print("\nright")
        for i in range(3):
            self.r.append([0]*3)
        for i in range(3):
            for j in range(3):
                self.r[i][j]=input("ENTER COLOUR: ")
        print("\nBottom")
        for i in range(3):
            self.bo.append([0]*3)
        for i in range(3):
            for j in range(3):
               self.bo[i][j]=input("ENTER COLOUR: ")
    def display(self):
        print("\nBACK")
        for i in range(3):
            for j in range(3):
                print(self.b[i][j],end=" ")
            print()

        print("UPPER")
        for i in range(3):
            for j in range(3):
                print(self.u[i][j],end=" ")
            print()

        print("LEFT")
        for i in range(3):
            for j in range(3):
                print(self.l[i][j],end=" ")
            print()

        print("FRONT")
        for i in range(3):
            for j in range(3):
                print(self.f[i][j],end=" ")
            print()

        print("RIGHT")
        for i in range(3):
            for j in range(3):
                print(self.r[i][j],end=" ")
            print()

        print("BOTTOM")
        for i in range(3):
            for j in range(3):
                print(self.bo[i][j],end=" ")
            print()

class Cross(B):
    def cross(self):
        Cross.scan(self,self.bo,1)
        Cross.scan(self,self.f,3)
        Cross.scan(self,self.b,4)
        Cross.scan(self,self.r,5)
        Cross.scan(self,self.l,6)
        Cross.scan(self,self.bo,1)
        Cross.scan(self,self.f,3)
        Cross.scan(self,self.b,4)
        Cross.scan(self,self.r,5)
        Cross.scan(self,self.l,6)
        Cross.scan(self,self.bo,1)
        Cross.scan(self,self.f,3)
        Cross.scan(self,self.b,4)
        Cross.scan(self,self.r,5)
        Cross.scan(self,self.l,6)
        Cross.scan(self,self.bo,1)
        Cross.scan(self,self.f,3)
        Cross.scan(self,self.b,4)
        Cross.scan(self,self.r,5)
        Cross.scan(self,self.l,6)
        Cross.white_cross(self,self.f,3)
        Cross.white_cross(self,self.b,4)
        Cross.white_cross(self,self.r,5)
        Cross.white_cross(self,self.l,6)
    def scan(self,a,x):
        p=0
        q=0
        k=0
        for i in range(0,3):
            for j in range(0,3):
                if((i==1 and j==0)and(a[i][j]==self.bo[1][1])or(i==0 and j==1)and(a[i][j]==self.bo[1][1])or(i==2 and j==1)
                   and(a[i][j]==self.bo[1][1])or(i==1 and j==2)and(a[i][j]==self.bo[1][1])):
                    k=k+1
        while(k!=0):
            for i in range(0,3):
                for j in range(0,3):
                    if((i==1 and j==0)and(a[i][j]==self.bo[1][1])):
                        p=i
                        q=j
            if (x==1):
                if(p==1 and q==0):
                    if(self.u[1][0]!=self.bo[1][1]):
                        Cross.Li(self)
                        Cross.Li(self)
                        k=k-1
                    else:
                        Cross.U(self)
                else:
                    Cross.Bo(self)
            elif (x==3):
                if (p==1 and q==0):
                    if(self.u[1][0]!=self.bo[1][1]):
                        Cross.Li(self)
                        k=k-1
                    else:
                        Cross.U(self)
                else:
                    Cross.F(self)
            elif (x==4):
                if (p==1 and q==0):
                    if(self.u[1][0]!=self.bo[1][1]):
                        Cross.L(self)
                        k=k-1
                    else:
                        Cross.U(self)
                else:
                    Cross.B(self)
            elif (x==5):
                if (p==1 and q==0):
                    if(self.u[2][1]!=self.bo[1][1]):
                        Cross.Fi(self)
                        k=k-1
                    else:
                        Cross.U(self)
                else:
                    Cross.R(self)
            elif (x==6):
                if (p==1 and q==0):
                    if(self.u[0][1]!=self.bo[1][1]):
                        Cross.Bi(self)
                        k=k-1
                    else:
                        Cross.U(self)
                else:
                    Cross.L(self)
    def white_cross(self,a,x):
        k=4
        while(k!=0):
            if(x==3):
                if((a[1][1]==a[0][1])and(self.u[2][1]==self.bo[1][1])):
                    Cross.F(self)
                    Cross.F(self)
                else:
                    Cross.U(self)
            elif(x==4):
                if((a[1][1]==a[2][1])and(self.u[0][1]==self.bo[1][1])):
                    Cross.B(self)
                    Cross.B(self)
                else:
                    Cross.U(self)
            elif(x==5):
                if((a[1][1]==a[0][1])and(self.u[1][2]==self.bo[1][1])):
                    Cross.R(self)
                    Cross.R(self)
                else:
                    Cross.U(self)
            elif(x==6):
                 if((a[1][1]==a[0][1])and(self.u[1][0]==self.bo[1][1])):
                     Cross.L(self)
                     Cross.L(self)
                 else:
                     Cross.U(self)
            k=k-1
class FirstLayer(Cross):
    def first(self):
        k=4
        while(k!=0):
            FirstLayer.first_layer(self,self.f,3)
            FirstLayer.first_layer(self,self.f,3)
            FirstLayer.first_layer(self,self.u,2)
            FirstLayer.first_layer(self,self.f,3)
            FirstLayer.first_layer(self,self.b,4)
            FirstLayer.first_layer(self,self.f,3)
            FirstLayer.first_layer(self,self.f,3)
            FirstLayer.first_layer(self,self.u,2)
            FirstLayer.first_layer(self,self.f,3)
            FirstLayer.first_layer(self,self.b,4)
            FirstLayer.first_layer(self,self.f,3)
            FirstLayer.first_layer(self,self.f,3)
            FirstLayer.first_layer(self,self.b,4)
            FirstLayer.first_layer(self,self.f,3)
            FirstLayer.first_layer(self,self.f,3)
            FirstLayer.first_layer(self,self.b,4)
            FirstLayer.first_layer(self,self.f,3)
            FirstLayer.first_layer(self,self.f,3)
            FirstLayer.first_layer(self,self.l,6)
            FirstLayer.first_layer(self,self.f,3)
            FirstLayer.first_layer(self,self.f,3)
            FirstLayer.first_layer(self,self.r,5)
            FirstLayer.first_layer(self,self.f,3)
            FirstLayer.first_layer(self,self.f,3)
            FirstLayer.first_layer(self,self.u,2)
            FirstLayer.first_layer(self,self.f,3)
            FirstLayer.first_layer(self,self.b,4)
            FirstLayer.first_layer(self,self.f,3)
            FirstLayer.first_layer(self,self.f,3)
            FirstLayer.first_layer(self,self.u,2)
            FirstLayer.first_layer(self,self.f,3)
            FirstLayer.first_layer(self,self.b,4)
            FirstLayer.first_layer(self,self.f,3)
            FirstLayer.first_layer(self,self.f,3)
            k=k-1
    def first_layer(self,a,x):
        k=0
        p=1
        q=1
        m=1
        n=1
        count=0
        for i in range(0,3):
            for j in range(0,3):
                if((i==0 and j==0) and (a[i][j]==self.bo[1][1])or(i==0 and j==2) and (a[i][j]==self.bo[1][1])):
                    p=i
                    q=j
                if((i==2 and j==0) and (a[i][j]==self.bo[1][1])or(i==2 and j==2) and (a[i][j]==self.bo[1][1])):
                    m=i
                    n=j
        if(x==2):
            for i in range(0,3):
                for j in range(0,3):
                    if(((i==0 and j==0)and(a[i][j]==self.bo[1][1]))or((i==0 and j==2)and(a[i][j]==self.bo[1][1]))or((i==2 and j==0)and(a[i][j]==self.bo[1][1]))
                       or((i==2 and j==2) and (a[i][j]==self.bo[1][1]))):
                          k=k+1
            while(k!=0):
                if(a[0][0]==self.bo[1][1] and self.bo[2][0]!=self.bo[1][1]):
                    FirstLayer.L(self)
                    FirstLayer.U(self)
                    FirstLayer.Li(self)
                    FirstLayer.Ui(self)
                    k=0
                elif(a[0][2]==self.bo[1][1] and self.bo[2][2]!=self.bo[1][1]):
                    FirstLayer.Ri(self)
                    FirstLayer.U(self)
                    FirstLayer.R(self)
                    FirstLayer.Ui(self)
                    k=0
                elif(a[2][0]==self.bo[1][1] and self.bo[0][0]!=self.bo[1][1]):
                    FirstLayer.Li(self)
                    FirstLayer.U(self)
                    FirstLayer.L(self)
                    FirstLayer.Ui(self)
                    k=0
                elif(a[2][2]==self.bo[1][1] and self.bo[0][2]!=self.bo[1][1]):
                    FirstLayer.R(self)
                    FirstLayer.U(self)
                    FirstLayer.Ri(self)
                    FirstLayer.Ui(self)
                    k=0
                else:
                    FirstLayer.U(self) 
        if(x==3):                                                                                       #case 3
            for i in range(0,3):
                for j in range(0,3):
                    if(((i==0 and j==0) and (a[i][j]==self.bo[1][1]))or((i==0 and j==2) and (a[i][j]==self.bo[1][1]))or((i==2 and j==0)and (a[i][j]==self.bo[1][1]))or((i==2 and j==2) and (a[i][j]==self.bo[1][1]))):
                          k=k+1
            while(k!=0):
                for i in range(0,3):
                    for j in range(0,3):
                        if((i==0 and j==0) and (self.f[i][j]==self.bo[1][1])or(i==0 and j==2) and (self.f[i][j]==self.bo[1][1])):
                            p=i
                            q=j
                        if((i==2 and j==0) and (self.f[i][j]==self.bo[1][1])or(i==2 and j==2) and (self.f[i][j]==self.bo[1][1])):
                            m=i
                            n=j
                if((p==0 and q==0)or(p==0 and q==2)):
                    if(p==0 and q==0):
                        if((self.l[1][1]==self.l[0][2]) and (self.f[0][0]==self.bo[1][1])):
                            FirstLayer.F(self)
                            FirstLayer.U(self)
                            FirstLayer.Fi(self)
                            k=k-1
                        elif((self.f[1][1]==self.f[0][2]) and (self.r[0][0]==self.bo[1][1])):
                            FirstLayer.R(self)
                            FirstLayer.U(self)
                            FirstLayer.Ri(self)
                            k=k-1
                        elif((self.r[1][1]==self.r[0][2]) and (self.b[2][2]==self.bo[1][1])):
                            FirstLayer.B(self)
                            FirstLayer.U(self)
                            FirstLayer.Bi(self)
                            k=k-1
                        elif((self.b[1][1]==self.b[2][0]) and (self.l[0][0]==self.bo[1][1])):
                            FirstLayer.L(self)
                            FirstLayer.U(self)
                            FirstLayer.Li(self)
                            k=k-1
                        else:
                            FirstLayer.Ui(self)
                    elif(p==0 and q==2):
                        if((self.r[1][1]==self.r[0][0]) and (self.f[0][2]==self.bo[1][1])):
                            FirstLayer.Fi(self)
                            FirstLayer.Ui(self)
                            FirstLayer.F(self)
                            k=k-1
                        elif((self.f[1][1]==self.f[0][0]) and (self.l[0][2]==self.bo[1][1])):
                            FirstLayer.Li(self)
                            FirstLayer.Ui(self)
                            FirstLayer.L(self)
                            k=k-1
                        elif((self.l[1][1]==self.l[0][0]) and (self.b[2][0]==self.bo[1][1])):
                            FirstLayer.Bi(self)
                            FirstLayer.Ui(self)
                            FirstLayer.B(self)
                            k=k-1
                        elif((self.b[1][1]==self.b[2][2]) and (self.r[0][2]==self.bo[1][1])):
                            FirstLayer.Ri(self)
                            FirstLayer.Ui(self)
                            FirstLayer.R(self)
                            k=k-1
                        else:
                            FirstLayer.U(self)
                elif((m==2 and n==0)or(m==2 and n==2)):
                    if(m==2 and n==0):
                        FirstLayer.Li(self)
                        FirstLayer.U(self)
                        FirstLayer.L(self)
                        k=0
                    if(m==2 and n==2):
                        FirstLayer.R(self)
                        FirstLayer.Ui(self)
                        FirstLayer.Ri(self)
                        k=0
                if(count==5):
                        k=0
                else:
                    count=count+1
        if (x==4):                                                  #case 4
                if((m==2 and n==0)or(m==2 and n==2)):
                     FirstLayer.U(self)
                     FirstLayer.U(self)
                elif((p==0 and q==0)or(p==0 and q==2)):
                    if(p==0 and q==0):
                        FirstLayer.L(self)
                        FirstLayer.Ui(self)
                        FirstLayer.Li(self)
                        FirstLayer.U(self)
                        FirstLayer.U(self)
                    elif(p==0 and q==2):
                        FirstLayer.Ri(self)
                        FirstLayer.U(self)
                        FirstLayer.R(self)
                        FirstLayer.U(self)
                        FirstLayer.U(self)
        if(x==5):                                                        #case 5
                if((p==0 and q==0)or(p==0 and q==2)):
                    FirstLayer.U(self)
                elif((m==2 and n==0)or(m==2 and n==2)):
                    if(m==2 and n==0):
                        FirstLayer.Fi(self)
                        FirstLayer.U(self)
                        FirstLayer.F(self)
                        FirstLayer.U(self)
                    elif(m==2 and n==2):
                        FirstLayer.B(self)
                        FirstLayer.Ui(self)
                        FirstLayer.Bi(self)
                        FirstLayer.U(self)
        if(x==6):                                                        #case 6
                if((p==0 and q==0)or(p==0 and q==2)):
                    FirstLayer.Ui(self)
                elif((m==2 and n==0)or(m==2 and n==2)):
                    if(m==2 and n==2):
                        FirstLayer.F(self)
                        FirstLayer.Ui(self)
                        FirstLayer.Fi(self)
                        FirstLayer.Ui(self)
                    elif(m==2 and n==0):
                        FirstLayer.Bi(self)
                        FirstLayer.U(self)
                        FirstLayer.B(self)
                        FirstLayer.Ui(self) 
class APP(FirstLayer):
    c=FirstLayer()
    print("\n^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^");
    print("|  U=upper clockwise\tUi =upper anti clockwise\t|\n"
          "|  F=Front clockwise\tFi =Front anti clockwise\t|\n"
          "|  B=back clockwise\tBi=back anticlockwise\t\t|\n"
          "|  R=right clockwise\tRi =right anti clockwise\t|\n"
          "|  L=left clockwise\tLi =left anti clockwise\t\t|\n"
          "|  Bo =bottom clockwise\tBoi=bottom  anti clockwise\t|");
    print("^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^\n");
    c.read()
    print("------------")
    print("|FOR CROSS:|")
    print("------------")
    c.cross()
    c.display()
    print("\n-----------------")
    print("|FOR FIRST LAYER|")
    print("-----------------")
    c.first()
    c.display()
