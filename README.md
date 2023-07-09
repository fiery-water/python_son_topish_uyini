# python_son_topish_uyini
Bu dasturda kompyuter uylagan sonnni foydalanuvchi topadi,
foydalanuvchi uylagan sonni esa kompyuter topadi

import random
print("Keling o'ylagan sonni topish o'ynaymiz!")
x=random.randint(1, 10)
print("1 dan 10 gacha son o'yladim. Topa olasizmi?:")
taxmin1=0
while True:
    taxmin1+=1
    taxmin=int(input(">>  "))
    if taxmin > x:
        print("Xato, men o'ylagan son bundan kichikroq. Yana urinib ko'ring")
    elif taxmin < x:
        print("Xato, men o'ylagan son bundan kattaroq. Yana urinib ko'ring")
    else:
        print(f"TOPDINGIZ! {x} sonini o'ylagan edim. {taxmin1} ta taxmin bilan topdingiz. Tabriklayman!!")
        break
print("1 dan 10 gacha son o'ylang. Men topishga harakat qilaman.")
#input("Son o'ylagan bo'lsangiz istalgan tugmani bosing.")
son=list(range(1,11))
taxmin2=0
quyi=1
yuqori=10
while True:
    taxmin2+=1
    ran=random.randint(quyi,yuqori)
    str=input(f"Siz {ran} sonini o'yladingiz: to'g'ri (T), men o'ylagan son bundan kattaroq (+), yoki kichikroq (-)?   ")
    if str=='+':
        quyi=ran+1
    if str=='-':
        yuqori=ran-1
    if str=='T':
        print(f"Soningizni {taxmin2} ta taxmin bilan topdim!")
        break

if taxmin1==taxmin2:
    print(f"Durrang! Ikkimiz ham {taxmin1} ta taxmin bilan topdik.")
elif taxmin1<taxmin2:
    print(f"Siz {taxmin1} ta taxmin bilan yutdingiz!")
else:
    print(f"Men {taxmin2} ta taxmin bilan yutdim!")
