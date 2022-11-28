#include<stdio.h>
#include<conio.h>
void nhapmang(int a[],int n){
    for (int i=0;i<n;i++){
        printf("a[%d]=",i);
        scanf ("%d",&a[i]);
    }
}
void xuatmang(int a[],int n){
 for (int i=0;i<n;i++){
     printf ("a[%d]=%d\n",i,a[i]);
 }   
}
int tong(int a[],int n){
    int t=0;
    for (int i=0;i<n;i++){
        t +=a[i];
    }
    return t;
}
int gttb(int a[],int n){
    float t=0;
    for (int i=0;i<n;i++){
    t += a[i];
    }
     float tb = t*1.0/n; 
     return tb;
}
int tongduong(int a[],int n){
    int tong=0;
    for (int i=0;i<n;i++){
        if (a[i]>0){
            tong +=a[i];
        }
    }
    printf("tong cac gia tri duong la %d\n",tong);
}
void daonguocmang(int a[],int n){
    for (int i=0;i<n/2;i++){
        int t = a[i];
        a[i] = a[n-1-i];
        a[n-1-i] = t;
    }
        for(int i=0;i<n;i++){
        printf("mang dao nguoc la ");
        printf("a[%d]=%d \n ",i,a[i]);
    }
}
int kiemTraDoiXung(int a[],int n){
    for(int i=0;i<n/2;i++){
     if(a[i] != a[n-i-1]){
         return -1;
     }   
    }return 0;
}
int main(){
    int n;
    printf ("nhap so phan tu trong mang\n");
    scanf ("%d",&n);
    int a[n];
    nhapmang(a,n);
    xuatmang(a,n);
   printf ("tong cac phan tu trong mang la %d\n " ,tong(a,n));
   printf ("gia tri trung binh trong mang la %d\n",gttb(a,n));
   tongduong(a,n);
   daonguocmang(a,n);
  if (kiemTraDoiXung(a,n)==1){
      printf("mang doi xung");
  }
  else {
        printf("mang khong doi xứng !");    
}
 getch();  
}
