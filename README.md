# h5url.txt
t11 = '1.1.2005'
t12 = '12.30.2010'

def tariholustur(t1, t2):
    tarih1 = t1.split('.')
    tarih2 = t2.split('.')
    
    yıl1 = int(tarih1[-1])
    yıl2 = int(tarih2[-1])
    ay1 = int(tarih1[-2])
    ay2 = int(tarih2[-2])
    gun1 = int(tarih1[-3])
    gun2 = int(tarih2[-3])
    def format_tarih(gun, ay):
        return f"{gun:02d}.{ay:02d}"

    print(yıl1, format_tarih(gun1, ay1))
    
    kategory = ["saglik", "dunya", "teknoloji"]
    gazeteler = ["sabah", "hurriyet"]
    
    for m in gazeteler:
        gaste = f"www.{m}.com.tr"
        for k in kategory:
            for i in range(yıl1, yıl2 + 1):  
                for j in range(1, 13): 
                    for gun in range(1, 31):  
                        formatted_gun = f"{gun:02d}"
                        formatted_ay = f"{j:02d}"
                        print(f"{i}.{formatted_ay}.{formatted_gun} - {gaste} - {k}")

tariholustur(t11, t12)
