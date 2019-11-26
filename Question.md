질문 및 답변코딩
====
[김준영]  
질문 : **t는왜 앞에있는 포인터를 가르키나요?

[손정우]  
질문 : 트리가 그래프와 어떤 연관이 있고 그래프에 대한 코딩이 무엇인지 궁금합니다.

[박형민]  
질문 : 링크드 리스트와 밑에 있는 코드에 대해 설명해주세요.
```c++
#include <stdio.h>
#include <stdlib.h>
typedef struct list {
 int d;
 struct list* p; 
} LIST;
LIST* root = NULL;
LIST* last = NULL;
void AddList(int a){
 LIST* r = (LIST*)malloc(sizeof(LIST));
 r->d = a;
 r->p = NULL;
 if(root==NULL) root = r;
 else           last->p = r;
 last = r;
}
int main(void){
 AddList(35);
 AddList(40);
 AddList(45);
 while(root){
  printf("%d\n", root->d);
  root = root->p;
 }
}  
```  
[이진욱]
질문 : 더블 포인트에 대한 자세한 설명과 예제가 필요합니다.

[천준영]
질문 : const 함수 와 static 함수의 사용법에 대해 궁금합니다
* * *  
> ## 활동 사진
![KakaoTalk_20191126_161606342_01](https://user-images.githubusercontent.com/50895748/69607253-3c262f00-1068-11ea-8b7e-e08aeb2b24f2.jpg)
![KakaoTalk_20191126_161606342_02](https://user-images.githubusercontent.com/50895748/69607475-a63ed400-1068-11ea-962f-e524982a2e83.jpg)

* * *
> ## 선정 질문
    [박형민] 링크드 리스트와 밑에 있는 코드에 대해 설명해주세요.
> ## 답변
    해당 코드소스에 중요한 부분을 주석처리 하여 코드에 대한 설명을 함.
```c++
#include <stdio.h>
#include <stdlib.h>
typedef struct list {
 int d;
 struct list* p; 
} LIST; //LIST라는 이름의 구조체 형식을 정의해줌.
LIST* root = NULL;
LIST* last = NULL; //root와 last라는 구조체를 선언하고 비워둠.
void AddList(int a){  //AddList라는 함수를 만듦.
 LIST* r = (LIST*)malloc(sizeof(LIST)); //r 이라는 포인터의 메모리를 할당.
 r->d = a; //a의 값을 r의 d에 저장
 r->p = NULL; //r의 p값을 비워둠.
 if(root==NULL) root = r; //root를 비교해 if문을 실행.
 else           last->p = r; //last를 r로 링크
 last = r;
}
int main(void){ //main함수 실행.
 AddList(35);
 AddList(40);
 AddList(45);
 while(root){
  printf("%d\n", root->d); //root값을 출력.
  root = root->p;
 }
}  
```  
![68186413-6e072100-ffe7-11e9-8784-c858e1e9332c](https://user-images.githubusercontent.com/50895748/69608307-827c8d80-106a-11ea-80a9-08cbd86ca294.png)

* * *
> ## 소감
