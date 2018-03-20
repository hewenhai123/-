### 排序算法

> 选择排序：</br>
原理：</br>
&nbsp;&nbsp;循环（1）所有项，拟定当前项为最小项，循环（2）当前项后面所有项和当前项进行对比，</br>
如果小于拟定最小项，让拟定最小项等于当前循环项，从而可以找到后面的最小项，然后让当前循环项和最小项对调。


<div  align="center">    
 <img src='./selected.gif' width="100%"/>
</div>

```js

var ary=[2,34,5,6,2,2,34,7654,123,324];
const selectSort=arr=>{
    let len=arr.length,
        minIndex,temp;
    for(let i=0;i<len-1;i++){
        minIndex=i;
        for(let j=i+1;j<len;j++){
             if(arr[j]<arr[minIndex]){
                minIndex=j;
             }
        }       
        temp=arr[i];
        arr[i]=arr[minIndex];
        arr[minIndex]=temp;
    }
    return arr;
}

```








