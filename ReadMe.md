## 버블정렬

### 코드 구현

```
순서를 어느 한 쪽에서 부터 순서대로 바꾸는 기본적인 방식이다. 아래 코드는 임시로 변수를 저장할 temp를 이용해서 만약 앞에 있는 수가 뒤에 있는 수 보다 크다면 앞에 있는 수와 뒤에 있는 수를 바꾸게 한다. for문을 2번 이용하여 n^2번 만큼 곧이곧대로 정렬을 시도하는 방식.
```

```
import java.util.*;
public class bubble_sort{
    static void bubble(int[] arr, int n){
        for(int i= 0; i<n-1;i++){
            for(int j= 1; j<n-i;j++){
                if(arr[j]<arr[j-1]){
                    int temp = arr[j];
                    arr[j]=arr[j-1];
                    arr[j-1]= temp;
                }
            }
        }
    }
    public static void main(String[] args){
        int[] arr =new int[] {4, 3, 1, 2, 6, 5};
        int n = 6;
        System.out.println("======before sort======");
        for(int i = 0; i<n; i++){
            System.out.println("[Index"+(i+1)+"]: "+arr[i]);
        }
        System.out.println("======after sort======");
        bubble(arr, n);
        for(int i = 0; i<n; i++){
            System.out.println("[Index"+(i+1)+"]: "+arr[i]);
        }
    }
}
```

### 결과

