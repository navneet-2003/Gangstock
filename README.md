# Gangstock
#include <cctype> 
#include <cstring> 
int count(char arr[]){    
    int count=0;    
    for (int i=0;arr[i]!='\0';i++){    
        count++;    
    }    
    return count;    
} 
void minLengthWord(char arr[], char output[]){ 
 int n=count(arr);   
    int i=0; 
    int minwordlength=99999999; 
    char arr2[100]; 
    for (i;i<n;i++){   
        int j=0;   
        char arr1[100];   
        while(!isspace(arr[i]) and i<n){    
            arr1[j]=arr[i];   
            j++;   
            i++;   
        }   
        arr1[j]='\0';   
        int word_length=count(arr1); 
        if  (word_length<minwordlength){ 
            minwordlength=count(arr1); 
            strcpy(arr2,arr1); 
             
        } 
    } 
    strcpy(output,arr2); 
   
 
}

