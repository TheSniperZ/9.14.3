# 9.14.3
对象数组的使用
//头文件Point.h
#include"stdafx.h"
#ifndef _POINT_H
#define _POINT_H

class Point{
public:
	Point();
	Point(int x,int y);
	~Point();
	void move(int newX,int newY);
	int getX() const {return x;}
	int getY() const {return y;}
	static void ShowCount();
private:
	int x,y;

};
#endif //_POINT_H

//源文件Point.cpp
#include"stdafx.h"
#include"Point.h"
#include<iostream>
using namespace std;

Point::Point ():x(0),y(0){
	cout<<"Default Constructor called"<<endl;
}
Point::Point(int  x,int y):x(x),y(y){
	cout<<"Constructor called"<<endl;
}
Point::~Point(){
    cout<<"Destructor called"<<endl;
}
void Point::move (int newX,int newY){
	cout<<"Move point to ("<<newX<<" , "<<newY<<")"<<endl;
	x=newX;
	y=newY;
}

// 9.14.4对象数组的使用.cpp : 定义控制台应用程序的入口点。
//

#include "stdafx.h"
#include"Point.h"
#include<iostream>
using namespace std;


int _tmain(int argc, _TCHAR* argv[])
{
	cout<<"Enter main..."<<endl;
	Point a[3];
	for(int i=0;i<3;i++){
		a[i].move (i+10,i+13);
	}
	cout<<"End main..."<<endl;
	return 0;
}

