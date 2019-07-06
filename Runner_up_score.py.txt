if __name__ == '__main__':
    n = int(raw_input())
    arr = map(int, raw_input().split())
    a=list(arr)
    for i in range (0,n):
       for j in range(i+1):
           if(a[i]<a[j]):
               temp=a[j]
               a[j]=a[i]
               a[i]=temp
    large=a[n-1]
    for i in range(2,n+1):
        if(large!=a[n-i]):
            low=a[n-i]
            break
    print(low)