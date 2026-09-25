# ziro_7
اختيار كلمه سر عشوائية# 
import random
import string
zmaso=int(input("كم تريد طول كلمه السر:\n"))

if zmaso>0:
    dan=int(input("كم عدد الحرف:\n"))
    if dan>0:
        dan1=int(input("كم عدد الرقام:\n"))
        if dan1>0:
            dan2=int(input("كم عدد الرموز:\n"))
            if dan2>0:
                paswrd=dan+dan1+dan2
                if paswrd==zmaso:
                    print("اكتملت الشروط")
                    zx=[]
                    zx+=random.choices(string.ascii_letters,k=dan)
                    zx+=random.choices(string.digits,k=dan1)
                    zx+=random.choices(string.punctuation,k=dan2)
                    int_paswrd="".join(zx)
                    print(f"كلمه السر:{int_paswrd}")
                else:
                    print("ارجاء مراجعه المدخلات ")
            else:
                print("اختار رقم صحيح")
        else:
            print("اكتب رقم صحيح")
    else:
        print("اكتب رقم صحيح")
else:
    print("خطاء حاول من جديد")
    