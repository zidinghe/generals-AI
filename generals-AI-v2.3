#include<bits/stdc++.h>
#include<windows.h>
#include<conio.h>
#define random(a,b) rand()%(b-a+1)+a
using namespace std;
struct square{
	int color=0;
	int type=0;//0:mountain 1:temple 2:field 3:general
	int popu=0;
	square()=default;
	square(int c,int t,int p){
		color=c;
		type=t;
		popu=p;
	}
}a[51][51];
bool alive[11]={0};
int val[51][51]={0};
int s[2501][2501]={0};
int q[2501][2501]={0};
int n=20,turn=0,lastColPos[11];
int totalField[11]={0};
int colPosX,colPosY;
int GetTotalPopu(int Color){
	int sum=0;
	for(int i=0;i<n;i++){
		for(int j=0;j<n;j++){
			if(a[i][j].color==Color){
				sum+=a[i][j].popu;
			}
		}
	}
	return sum;
}
int GetTotalField(int Color){
	int sum=0;
	for(int i=0;i<n;i++){
		for(int j=0;j<n;j++){
			if(a[i][j].color==Color){
				sum++;
			}
		}
	}
	return sum;
}
void Check(int Color){
	memset(val,0,sizeof(val));
	memset(s,-1,sizeof(s));
	memset(q,0,sizeof(q));
	int g=random(45,85);
	cout<<g<<"    "<<endl;
	for(int i=0;i<n;i++){
		for(int j=0;j<n;j++){
			int x=a[i][j].popu;
			if(a[i][j].type==0) val[i][j]=-1e6;
			else if(a[i][j].type==1){
				if(a[i][j].color==0) val[i][j]=0-2*x+int(turn/2);
				else if(a[i][j].color==Color) val[i][j]=-5+15*x+int(turn/4);
				else val[i][j]=0-x+int(turn/8);//若对方庙人数少则占庙 
			}
			else if(a[i][j].type==2){
				if(a[i][j].color==0) val[i][j]=2+3*int(turn/25);
				else if(a[i][j].color==Color) val[i][j]=2*x+int(turn/50);
				else val[i][j]=2-int(x/2)+int(turn/25);//避开对方主力部队 
			}
			else if(a[i][j].type==3){
				if(a[i][j].color==Color) val[i][j]=int(x/2);
				else val[i][j]=-int(x/2)+150*turn+10000;
			}
		}
	}
	int mx=-2e6,mxa=-1,mxb=-1,mxv=-2e6,mxva=-1,mxvb=-1;
	for(int i=0;i<n;i++){
		for(int j=0;j<n;j++){
			if(val[i][j]>mxv){
				mxv=val[i][j];
				mxva=i;
				mxvb=j;
			}
			if(a[i][j].color==Color&&val[i][j]>mx&&a[i][j].popu>1&&i*n+j!=lastColPos[Color]){
				mx=val[i][j];
				mxa=i;
				mxb=j;
			}
			else if(a[i][j].color==Color&&a[i][j].type==3&&val[i][j]>=mx*2
			&&a[i][j].popu>1&&i*n+j!=lastColPos[Color]){//己方主城，保留一半兵力 
				mx=a[i][j].popu/2;
				mxa=i;
				mxb=j;
			}
		}
	}
	colPosX=mxa;
	colPosY=mxb;
//	cout<<colPosX<<" "<<colPosY<<endl;
	for(int i=0;i<n;i++){
		for(int j=0;j<n;j++){
			if(i<n-1) s[i*n+j][i*n+n+j]=(val[i][j]+val[i+1][j])/2;
			if(i>0) s[i*n+j][i*n-n+j]=(val[i][j]+val[i-1][j])/2;
			if(j<n-1) s[i*n+j][i*n+j+1]=(val[i][j]+val[i][j+1])/2;
			if(j>0) s[i*n+j][i*n+j-1]=(val[i][j]+val[i][j-1])/2;
		}
	}
	for(int i=1;i<=n*n;i++){
		int pos=random(0,n*n-1);
		while(pos!=mxva*n+mxvb){
			int to=random(0,n*n-1);
			int mx=-2e6,mxa=pos;
			if(s[pos][to]>-1){
				for(int k=0;k<n*n;k++){
					if(q[to][k]>mx){
						mx=q[to][k];
						mxa=k;
					}
				}
				q[pos][to]=s[pos][to]+g*1.0*q[to][mxa]*0.01+0.5;
			}
			pos=to;
		}
	}
	int mmx=0,mxdir=0;
	for(int i=0;i<n*n;i++){
		if(i==lastColPos[Color]) continue;
		int p=random(80,120);
		if(q[colPosX*n+colPosY][i]*p*1.0/100.0>mmx){
//			cout<<i<<"  ";
			mmx=q[colPosX*n+colPosY][i]*p*1.0/100.0;
			mxdir=colPosX*n+colPosY-i;
		}
	}
//	cout<<colPosX<<" "<<colPosY<<" "<<mxdir<<endl;
	lastColPos[Color]=colPosX*n+colPosY;
//	cout<<lastColPos[Color]<<endl;
	int movePopu=a[colPosX][colPosY].popu-1;
	if(mxdir==1&&colPosY>0){//move left
		if(a[colPosX][colPosY-1].color==Color) a[colPosX][colPosY-1].popu+=movePopu;
		else{
			a[colPosX][colPosY-1].popu-=movePopu;
			if(a[colPosX][colPosY-1].popu<0){
				a[colPosX][colPosY-1].color=Color;
				a[colPosX][colPosY-1].popu=0-a[colPosX][colPosY-1].popu;
			}	
		}
		a[colPosX][colPosY].popu=1;
	}
	if(mxdir==-1&&colPosY<n-1){//move right
		if(a[colPosX][colPosY+1].color==Color) a[colPosX][colPosY+1].popu+=movePopu;
		else{
			a[colPosX][colPosY+1].popu-=movePopu;
			if(a[colPosX][colPosY+1].popu<0){
				a[colPosX][colPosY+1].color=Color;
				a[colPosX][colPosY+1].popu=0-a[colPosX][colPosY+1].popu;
			}	
		}
		a[colPosX][colPosY].popu=1;
	}
	if(mxdir==n&&colPosX>0){//move up
		if(a[colPosX-1][colPosY].color==Color) a[colPosX-1][colPosY].popu+=movePopu;
		else{
			a[colPosX-1][colPosY].popu-=movePopu;
			if(a[colPosX-1][colPosY].popu<0){
				a[colPosX-1][colPosY].color=Color;
				a[colPosX-1][colPosY].popu=0-a[colPosX-1][colPosY].popu;
			}	
		}
		a[colPosX][colPosY].popu=1;
	}
	if(mxdir==0-n&&colPosX<n-1){//move down
		if(a[colPosX+1][colPosY].color==Color) a[colPosX+1][colPosY].popu+=movePopu;
		else{
			a[colPosX+1][colPosY].popu-=movePopu;
			if(a[colPosX+1][colPosY].popu<0){
				a[colPosX+1][colPosY].color=Color;
				a[colPosX+1][colPosY].popu=0-a[colPosX+1][colPosY].popu;
			}	
		}
		a[colPosX][colPosY].popu=1;
	}
	return;
}
int main(){
	srand(time(NULL));
	/*
	a[0][0]={2,3,10};
	a[0][1]={2,2,3};
	a[0][2]={2,2,3};
	a[0][3]={1,2,2};
	
	a[1][0]={2,1,10};
	a[1][1]={2,2,4};
	a[1][2]={2,2,2};
	a[1][3]={1,2,1};
	
	a[2][0]={1,2,4};
	a[2][1]={1,2,3};
	a[2][2]={2,2,15};
	a[2][3]={1,2,1};
	
	a[3][0]={0,0,0};
	a[3][1]={1,2,3};
	a[3][2]={1,2,2};
	a[3][3]={1,3,30};
	*/
	for(int i=0;i<n;i++){
		for(int j=0;j<n;j++){
			a[i][j]={0,2,0};
		}
	}
	a[0][0]={2,3,1};
	a[n-1][n-1]={1,3,1};
	a[2][2]={0,1,20};
	a[n-3][n-3]={0,1,20};
	a[1][n-2]={0,1,20};
	a[n-2][1]={0,1,20};
	a[0][n-1]={0,0,0};
	a[0][1]={0,0,0};
	a[n-1][0]={0,0,0};
	a[n-1][n-2]={0,0,0};
	while(1){
		COORD pos;
		pos.X=0;
		pos.Y=0;
		SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE),pos);
		turn++;
		cout<<"Turn "<<turn<<"   "<<endl<<endl;
		for(int i=0;i<n;i++){
			for(int j=0;j<n;j++){
				int t=a[i][j].type;
				if((t==1||t==3)&&a[i][j].color!=0){
					a[i][j].popu++;	
				}
				if(turn%25==0&&a[i][j].color!=0){
					a[i][j].popu++;
				}
			}
		}
//		/*
		for(int i=0;i<n;i++){
			for(int j=0;j<n;j++){
				if(a[i][j].color==1) SetConsoleTextAttribute(GetStdHandle(STD_OUTPUT_HANDLE),4*17);
				else if(a[i][j].color==2) SetConsoleTextAttribute(GetStdHandle(STD_OUTPUT_HANDLE),1*17);
				else SetConsoleTextAttribute(GetStdHandle(STD_OUTPUT_HANDLE),0*17);
				cout<<"  ";
				if(a[i][j].type==0) SetConsoleTextAttribute(GetStdHandle(STD_OUTPUT_HANDLE),2*17);//mountain
				if(a[i][j].type==1) SetConsoleTextAttribute(GetStdHandle(STD_OUTPUT_HANDLE),8*17);//temple
				if(a[i][j].type==2) SetConsoleTextAttribute(GetStdHandle(STD_OUTPUT_HANDLE),7*17);//field
				if(a[i][j].type==3) SetConsoleTextAttribute(GetStdHandle(STD_OUTPUT_HANDLE),6*17);//general
				cout<<"  ";
			}
			SetConsoleTextAttribute(GetStdHandle(STD_OUTPUT_HANDLE),15);
			cout<<endl;
			for(int j=0;j<n;j++){
				cout<<setw(4)<<a[i][j].popu;
			}
			SetConsoleTextAttribute(GetStdHandle(STD_OUTPUT_HANDLE),15);
			cout<<endl;
		}
		cout<<endl;
//		*/
		memset(alive,0,sizeof(alive));
		for(int i=0;i<n;i++){
			for(int j=0;j<n;j++){
				for(int col=1;col<=2;col++){
					if(a[i][j].color==col&&a[i][j].type==3) alive[col]=1;
				}
			}
		}
		if(!alive[1]){
			cout<<endl<<endl<<endl<<"Blue won!"<<endl;
			system("pause");
			break;
		}
		if(!alive[2]){
			cout<<endl<<endl<<endl<<"Red won!"<<endl;
			system("pause");
			break;
		}
		memset(totalField,0,sizeof(totalField));
		cout<<"    Field    Popu    "<<endl; 
		for(int col=1;col<=2;col++){
			if(col==1) SetConsoleTextAttribute(GetStdHandle(STD_OUTPUT_HANDLE),4*17);
			else if(col==2) SetConsoleTextAttribute(GetStdHandle(STD_OUTPUT_HANDLE),1*17);
			else SetConsoleTextAttribute(GetStdHandle(STD_OUTPUT_HANDLE),0*17);
			cout<<"  ";
			SetConsoleTextAttribute(GetStdHandle(STD_OUTPUT_HANDLE),15);
			cout<<"  "<<setw(5)<<GetTotalField(col)<<"    "<<setw(4)<<GetTotalPopu(col)<<"    "<<endl;
		}
		if(turn%2==1){
			for(int col=1;col<=2;col++){
				Check(col);
			}	
		}
		else{
			for(int col=2;col>=1;col--){
				Check(col);
			}
		}
		
//		system("pause");
	}
	return 0;
}
