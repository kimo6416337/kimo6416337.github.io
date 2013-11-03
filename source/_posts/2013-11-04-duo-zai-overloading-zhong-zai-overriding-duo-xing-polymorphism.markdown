---
layout: post
title: "多載(overloading)、重載(overriding)、多型(polymorphism)"
date: 2013-11-04 00:15
comments: true
sharing: true
categories: [programming,OOP]
---
1. **一、多載(overloading)**  
一個類別(class)中具有複數個相同名稱的函數(method)時，利用下列兩種方式判斷函數呼叫該載入哪個函數：  
　　1.參數(argument)的型態(type)不同  
　　例：  
　　　　function foo(char c){code statements;}  
　　　　function foo(int num){code statements;}  
　　2.參數載入數量不同(包含0個)  
　　例：  
　　　　function foo(int a){code statements;}  
　　　　function foo(int a,int b){code statements;}  
2. **二、重載(overriding)**  
用於類別的繼承(inheritance)上。當父類別與子類別具有相同名稱的函數時，則被宣告為子類別之物件(object)呼叫該函數會執行子類別中的函數，而非父類別中的函數。  
　　例：  
　　　　class A {  
　　　　　function foo() {print "I am in class A.";}  
　　　　}  
　　　　class B inherit A {  //B繼承A，A為父類別，B為子類別  
　　　　　function foo() {print "I am in class B.";}  
　　　　}  
　　　　B b=new B();  //b被宣告為B類別之物件  
　　　　b.foo;  //output:I am in class B.  
3. **三、多型(polymorphism)**  
用於類別的繼承上。在父類別與子類別有共同名稱的函數情況下(也就產生了函數重載)，若呼叫相同名稱的函數時，則函數的行為會依照宣告類別之不同而產生不同結果。  
　　例：  
　　　　class A {  
　　　　　function foo(){}  
　　　　class B inherit A {  
　　　　　function foo() {print "This is foo in class B.";}  
　　　　}  
　　　　class C inherit A {  
　　　　　function foo() {print "This is foo in class C.";}  
　　　　}  
　　　　A var1=new A();  //output:This is foo in class B.  
　　　　B var2=new B();  //output:This is foo in class C.
