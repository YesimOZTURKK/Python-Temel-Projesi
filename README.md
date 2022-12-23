# Python Temel Projesi
---
## SORULAR

1-) Bir listeyi düzleştiren (flatten) fonksiyon yazın. Elemanları birden çok katmanlı listelerden ([[3],2] gibi) oluşabileceği gibi, non-scalar verilerden de oluşabilir. Örnek olarak:

```
input: [[1,'a',['cat'],2],[[[3]],'dog'],4,5]

output: [1,'a','cat',2,3,'dog',4,5]
```

2-) Verilen listenin içindeki elemanları tersine döndüren bir fonksiyon yazın. Eğer listenin içindeki elemanlar da liste içeriyorsa onların elemanlarını da tersine döndürün. Örnek olarak:
```
input: [[1, 2], [3, 4], [5, 6, 7]]

output: [[[7, 6, 5], [4, 3], [2, 1]]
```
---

## CEVAPLAR
1-)
```
l=[[1,'a',['cat'],2],[[[3]],'dog'],4,5]
flattenl=[]
def flatten(l):
    for a in l:
        if type(a)==list:
            flatten(a)
        else:
            flattenl.append(a)
    return flattenl
print(flatten(l))
```

2-)
```
a= [[1, 2], [3, 4], [5, 6, 7]]
a.reverse()
for l in range(len(a)):
    (a[l])=(a[l])[::-1] 
print(a)
```
