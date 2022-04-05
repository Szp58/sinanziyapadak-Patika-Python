# sinanziyapadak-Patika-Python
Patika-Python(Temel) Project
www.patika.dev

1- Bir listeyi düzleştiren (flatten) fonksiyon yazın. Elemanları birden çok katmanlı listelerden ([[3],2] gibi) oluşabileceği gibi, non-scalar verilerden de oluşabilir. Örnek olarak:  input: [[1,'a',['cat'],2],[[[3]],'dog'],4,5]

               output: [1,'a','cat',2,3,'dog',4,5]
  
Cevap:
            
            flatten_list=[]            
            def flatten (liste):
                for e in liste:
                    if type(e)==list:
                        flatten(e)
                    else:
            .            flatten_list.append(e)
                return flatten_list

            example=[[1,'a',['cat'],2],[[[3]],'dog'],4,5]
            flatten(example)


2- Verilen listenin içindeki elemanları tersine döndüren bir fonksiyon yazın. Eğer listenin içindeki elemanlar da liste içeriyorsa onların elemanlarını da tersine döndürün. Örnek olarak:

input: [[1, 2], [3, 4], [5, 6, 7]]

output: [[[7, 6, 5], [4, 3], [2, 1]]

Cevap:

            def reversing (liste):
                liste.reverse()
                for e in liste:
                    if type(e)==list:
                        reversing(e)
                    else:
                        continue
                return liste

            inputs=[[[1, 2], [3, 4]], [5, 6, 7]]
            reversing(inputs)
