### malloc & free

- 함수이며 stdlib.h에 내장
- 사용자가 수동으로 동적할당한 메모리를 수거하지 않으면, 메모리 누수 발생
- 함수가 void* 이므로 각 타입에 맞게 미리 캐스팅 해줘야 함

### new & delete

- 연산자로 라이브러리 없이도 사용가능
- 자동으로 생성자를 호출해줌
- 할당과 동시에 초기화가 가능
- 할당할 메모리 크기 몰라도됨
- sizeof와 캐스트 연산이 불필요

### new 와 malloc의 차이점

- new는 자동으로 생성자를 호출해줌
- malloc은 후에 realloc으로 바로 메모리 재할당이 가능하지만, new는 메모리 해제후 다시 할당을 해야 함.

```cpp
int* ptr = (int*)malloc(sizeof(int)*4);

(int*) : 형변환

sizeof(int)*4 : 할당할 메모리 크기

int* ptr = new int;
int* arr = new int[3];   // 길이3인 int형배열 할당

출처: https://heurinbada.tistory.com/92 [흐린바다]
```
