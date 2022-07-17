# spell-corrector
# c program
# Let's make a spelling corrector that puts a capital letter at the beginning of a string and a period at the end. 문자열의 처음 시작은 대문자로 마지막 끝에는 마침펴를 찍어주는 철자 교정기를 만들어보자.
#include <stdio.h>
#include <string.h>
int check_str(char *str);
int main(void) {
    char str[100];
    printf("텍스트를 입력하시오: ");
    gets(str);
    check_str(str);
    printf("결과 텍스트 출력: ");
    puts(str);
    return 0;
} 
int check_str(char *str) {
    if(str[0] >= 'a' && str[0] <= 'z')
        str[0] -= 'a' - 'A';
    if(str[strlen(str)-1] != '.') {
        str[strlen(str)+1] = NULL;
        str[strlen(str)] = '.';
    }
}
#input--> i am a girl
# result--> I am a girl.
