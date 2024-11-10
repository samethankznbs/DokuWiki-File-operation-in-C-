KOCAEL˙I UN¨ ˙IVERS˙ITES˙I
B˙ILG˙ISAYAR MUHEND¨ ˙ISL˙IG˘˙I BOL¨ UM¨ U¨

PROGRAMLAMA LABORATUVARI

Tugba˘ C¸EV˙IKER 210202056

1. G˙IR˙IS¸

Bu dok¨ uman¨ Programlama Laboratuvarı I dersinin 1. Projesi olan Dokuwiki Kocaeli Uni¨ versitesi’nin c¸oz¨ um¨ un¨ u¨ ac¸ıklamaya yonelik¨ olus¸turmulus¸tur. Dok¨ umanda¨ Proje Tanımı; Yontem,¨ Kod Bilgisi ve Algoritma; Deneysel Sonuc¸lar; Sonuc¸ ve Kaynakc¸a kısımlarına yer verilmis¸tir.

2. PROJE TANIMI

Projede bizden istenen C veya C++ dilini kul- lanarak ”universite” klasor¨ un¨ un¨ ic¸inde yer alan ”bolumler” ve ”dersler” olmak uzere¨ en az iki alt klasor¨ un¨ ic¸indeki ”.txt” uzantılı dosyalarda dosya okuma,yazma ve guncelleme¨ is¸lemlerinin yapılması istenmektedir.Her txt dosyasının ic¸erisinde metin ve bu metinler ic¸erisinde etiketler bulunmaktadır.

˙Istenilen is¸lemler etiketler uzerinden¨ belirlenerek yapılmalıdır.

1. Etiket Tanımı

Eger˘ bir kelime etiket ise formatı s¸u s¸ekillerde olmalıdır: [[kelime]], [[kelime1 kelime2]]

Hatalı etiket formatları: [[kelime], [kelime]], [ke- lime], kelime vb.

Yetim etiket: Alt klasorlerde¨ etiketlere ait txt dosyaları bulunmaktadır. Ancak her etikete ait txt dosyası olmak zorunda degildir˘ . Aynı s¸ekilde her txt dosyasının etiketi olmak zorunda degildir˘ . Eger˘ bir etikete ait txt dosyası yoksa o etiket, yetim etikettir.

˙Istenen etiket: Dosyası var fakat etiketi yok.

2. Ders S¸ablon Ic˙¸erigi˘

Her bir dersin bir kodu, adı ve ic¸erigi˘ olmalıdır. Tum¨ dersler bu s¸ablona uygun olmalıdır.

Kullanıcı verilen ”universite” klasor¨ un¨ un¨ ic¸indeki her bir ”.txt” dosyalarının ic¸indeki etiketleri ve

Samethan KAZANBAS¸ 210202043

yetim etiketleri bulup program her c¸alıs¸tıgında˘ ”uni- versite” klasor¨ un¨ un¨ ic¸inde yer alan ”output.txt” dosyasının ic¸inde listelemelidir.

Kullanıcı verilen ”universite” klasor¨ un¨ un¨ ic¸indeki her bir ”.txt” dosyalarının ic¸inde kelime veya etiket araması yapabilmelidir. Arama sonucunda aranan etiketin veya kelimenin hangi dosyada hangi satır veya satırlarda gec¸tigi˘ terminalde ekrana yazdırılmalıdır.

Kullanıcı verilen ”universite” klasor¨ un¨ un¨ ic¸indeki her bir ”.txt” dosyalarının ic¸indeki istedigi˘ etiket- lerin isimlerini degis˘ ¸tirmeli bu durumda da etiketin bulundugu˘ dosyanın ismi de degis˘ ¸tirilen yeni etiket adıyla guncellenmelidir¨ .Ayrıca kullanıcı bas¸langıc¸ta bulunan yetim etiketlerden istedigini˘ sec¸ip onun isminde yeni bir txt dosyası olus¸turup o etiketi yetim etiketler listesinden kaldırabilmelidir. Her bir yapılan guncelleme¨ is¸leminde ”output.txt” dosyasında guncelleme¨ is¸lemi yapılmalıdır.

Kullanıcının yukarıda anlatılan gore¨ vlerin kontrolun¨ u¨ saglayabilmesi˘ ic¸in bir menu¨ taasarlaması gerekmektedir.

3. YO¨ NTEM , KOD B˙ILG˙IS˙I VE ALGOR˙ITMA

Klasorde¨ bulunan tum¨ ”.txt” uzantlı dosyaları bulabilmek ic¸in oncelikle¨ but¨ un¨ dosyalara ulas¸mamız gerekiyordu. Yaptıgımız˘ aras¸tırmalarda bunun saglanabilmesi˘ ic¸in buludgumuz˘ en mantıklı yol ”dirent.h” kut¨ uphanesini¨ kullanmak oldu. Bu kut¨ uphanede¨ yer alan fonksyonlar sayesinde ”universite” klasor¨ un¨ un¨ ic¸inde yer alan ”bolumler”,”dersler” ve ”ogretimelemanlari” klasorlerinin¨ ic¸indeki tum¨ dosyalara ulas¸tık.

Kullandıgımız˘ bir if yapısı ve ”string.h” kut¨ uphanesi¨ sayesinde dosyalardan sadece ”.txt” uzantılı olanları ayırabildik.

Dosyalarda istenen gore¨ vlerin yapılırken tekrar tekrar ac¸ılmaması ve zamandan kazanmak ic¸in

dosyaları ac¸tıgımızda˘ dosya uzantılarını ,dosya adını ve dosya ic¸erigini˘ ”string.h” kut¨ uphanesiyle¨ bir structa tanımlamaya karar verdik. Boylece¨ ya- pacagımız˘ tum¨ is¸lemleri bu struct uzerinden¨ yapa- bilecektik.

![Aspose Words e230bca6-83b4-4554-b5c3-bf3a2eeb3a06 001](https://github.com/user-attachments/assets/82426a51-1fb5-4558-a801-2366a023e151)

Fig. 1. Ornek¨ Struct Yapısı

Proje Tanımı kısmında ac¸ıkladıgımız˘ yapıda etiketleri bulabilmek ic¸in ic¸ ic¸e kurulmus¸ iki dong¨ u¨ kullandık. Dıs¸taki dong¨ u¨ structa atadıgımız˘ her bir ”.txt” uzantılı dosyanın ic¸erigini˘ donerk¨ en ic¸ kısımdaki dong¨ u¨ o ic¸erigin˘ indislerindeki karak- terleri don¨ uyor¨ ve ic¸indeki if yapısı sayesinde indislerde arka arkaya gelen ”[” ve ”]”’leri bu- luyor.Boylece¨ etiketlerin ic¸erikteki bas¸langıc ve bitis¸ indislerini elde edebldik. Etiketleri farklı bir structa atayıp listeleyebilmek ic¸in buldugumuz˘ bas¸langıc¸ ve bitis¸ indislerini,dosyanın ic¸erigini˘ ve yolunu ara bir structa atadık.

Etiketleri listeleyebilmek ic¸in atadıgımız˘ ara structı kullanarak bir dong¨ u¨ sayesinde baslangıc ve bitis indisleri arasındaki karaktereleri bas¸ka bir diziye atayıp o diziyi de etiketlerin isimlerinin adreslerinin ve baslangic indislerinin bulundugu˘ bas¸ka bir structa atadık.

Yetim etiketleri liseleyebilek ic¸in bas¸langıc¸ta ”dirent.h” kut¨ uphanesni¨ kullandıktan sonra dosya isimlerini,dosya yollarını ve ic¸eriklerini atadıgımız˘ structı ve etiketleri atadıgımız˘ structı

kars¸ılas¸tırmamız gerekiyordu.˙Ic¸ ic¸e kurudgumuz˘ iki fordan dıs¸taki etiketlerin isimlerini donerk¨ en

ic¸teki for dosya isimlerini dond¨ u.¨ ˙Ic¸teki forun ic¸ine kurdugumuz˘ if yapısı ve ”string.h” kut¨ uphanesi¨

sayesinde bu iki veriyikars¸ılas¸tırdık ve aynı olmayanları yetim etiketlerin isimlernin bulundugu˘ structa atadık ve yetim etiketleri de listeleyebildik.

˙Istenen etiketleri liseleyebilmek ic¸in bas¸langıc¸ta ”dirent.h” kut¨ uphanesni¨ kullandıktan sonra

dosya isimlerini,dosya yollarını ve ic¸eriklerini atadıgımız˘ structı ve etiketleri atadıgımız˘ structı

kars¸ılas¸tırmamız gerekiyordu.˙Ic¸ ic¸e kurudgumuz˘

iki fordan dıs¸taki dosya isimlerini donerk¨ en ic¸teki for etiket isimlerini dond¨ u.¨ ˙Ic¸teki forun ic¸ine

kurdugumuz˘ if yapısı ve ”string.h” kut¨ uphanesi¨ sayesinde bu iki veriyi kars¸ılas¸tırdık ve aynı olmayanları istenen etiketlerin isimlernin bulundugu˘ structa atadık ve istenen etiketleri de listeleyebildik.

Bizden istenen ”output.txt” dosyasını olus¸turabilmek ic¸in ”fopen” fonksiyonuyla ”universite” klasor¨ un¨ un¨ ic¸inde ”output.txt” dosyasını ac¸tık ve structa atadıgımız˘ yetim etiketleri ve etiketleri dosyaya ”fprintf” fonksiyonu sayesinde yazdırdık.

˙Istenilen Arayuz¨ tasarımını yapmak ic¸in Switch- Case yapısını kullandık.

![Aspose Words e230bca6-83b4-4554-b5c3-bf3a2eeb3a06 002](https://github.com/user-attachments/assets/3af1273d-9de3-4b97-bbd4-c1fe582d14af)
Fig. 2. Terminalde Goz¨ uk¨ en Arayuz¨

ilk caseimizde kelime arama gore¨ vini yaptık. Ca- sein ic¸inde ilk olarak aramak istenilen kelimeyi aldık. Ardından kurdugumuz˘ dong¨ uyle¨ fonksiy- ona her bir dosyanın ic¸erigini˘ ,aranan kelimeyi ve dosyanın adresini gonderdik.¨ Fonksiyonda kul- landıgımız˘ if yapısı ve kars¸ılas¸tırma fonksiyonuyla kelimenin var olup olmadıgını˘ ,eger˘ varsa ic¸erikteki indisini ve structaki yolunu ekrana yazdırdık.

ikinci caseimizde etiket arama gore¨ vini yaptık.Casein ic¸inde ilk olarak aramak istenilen etiketi aldık.Ardından kurdugumuz˘ dong¨ uyle¨ fonksiyonu her bir etiketin adını ,yolunu,bas¸langıc¸ indisini ve aranan etiketi gonderdik.F¨ onksiyonda kullandıgımız˘ if yapısı ve kars¸ılas¸tırma fonksiyonuyla etiketin var olup olmadıgını,e˘ ger˘ varsa indisini ve adresini ekrana yazdırdık.

Uc¨ ¸unc¨ u¨ caseimiz etiket guncelleme¨ caseidir. Etiketleri structa atamak ic¸in kullandıgımız˘ ara

struct sayesinde etiketlerin dosyalarda bulundugu˘ indisleri biliyorduk ve o indislere ulas¸arak etiketer- imizi guncelle¨ yebildik.

Dord¨ unc¨ u¨ caseimiz Yetim Etiket C¸evirme casei- dir.Oncelikle¨ casein ic¸inde c¸evrilmek istenen yetim

etiket istenir.Ardından kurdugumuz˘ dong¨ uyle¨ alınan

yetim etiketle,yetim etiket listesi kars¸ılas¸tırılır.Eger˘ girilen yetim etiket listede varsa fonksiyonla ”dersler” klasor¨ un¨ un¨ ic¸inde girilen yetim etiket adında ”.txt” uzantılı dosya olus¸turulur. Ardından yetim etiketi listesinden girilen etiket ”memset” fonksiyonuylu silinir.Guncel¨ ”output.txt” dosyası olus¸turmak ic¸in yine dord¨ unc¨ u¨ casein ic¸inde eski olus¸turulan ”output.txt” dosyasına ekleme yapılarak etiket listesi ve yeni yetim etiket listesi yazılır.

A. Kullanılan Kut¨ uphaneler¨

Kullandıgımız˘ kut¨ uphaneler¨ ve ne ic¸in kul- landıgımız˘ kabaca as¸agıdaki˘ gibidir:

stdio.h :

Girdi ve c¸ıktı almak ic¸in kullandık.

dirent.h :

Programın c¸alıs¸tıgı˘ klasordeki¨ dosyaları bulmak ic¸in kullandık.

string.h :

Kars¸ılas¸tırma yapmak,structa atama yapmak gibi ”str...” is¸lemler ic¸in kullandık.

locale.h :

Turkc¨ ¸e karakter kullanabilmek ic¸in kullandık. time.h :

Yeni olus¸turulan ”.txt” uzantılı dsoyalara sayı atamak ic¸in kullandık.

4. DENEYSEL SONUC¸ LAR

Dosya ic¸erigini˘ bir structa atadıgımızda˘ terminale yazdırabildigimizi˘ gord¨ uk.¨

Etikeleri sorunsuz bir s¸ekilde bulabildik ve lis- teleyebildik.

”.txt” uzantılı dosyaları sadece ”dersler”, ”bolum- ler” ve ”ogretimelemanlari” klasorlerinde¨ arama ya- pabildik.

Etiketler arasından turkc¨ ¸e karakter ic¸eren etiket- leri bulamama sorununu c¸ozemedik.¨

Kelime aramasında aynı kelimenin aynı dosya ic¸erisinde gec¸mesi durumunda sadece ilk kelimeyi bulması soununu c¸ozemedik.¨

Etiket ve kelime aramasında bulunan yerin satırını bulamadık ve ekrana yazdıramadık. Fakat yerini ve indisini yazdırabildik.(Fig. 3)(Fig. 4)

Etiket duncellemesinde¨ bir dosyada aynı etiketten birden fazla olursa ilkini guncelle¨ yebildik.Diger˘ etiket indis kayması yas¸adı ve eksik goz¨ ukt¨ u.¨ ”rename” fonksiyonunu c¸alıs¸tıramadık ve dosya ismini guncelle¨ yemedik.

![Aspose Words e230bca6-83b4-4554-b5c3-bf3a2eeb3a06 003](https://github.com/user-attachments/assets/c7ec344b-0823-4ec9-a427-cc6c4eeb4c65)

Fig. 3. Terminalde Kelime Arama C¸ıktısı

![Aspose Words e230bca6-83b4-4554-b5c3-bf3a2eeb3a06 004](https://github.com/user-attachments/assets/3800ff63-c08f-4a02-89cf-9bc93379feb0)

Fig. 4. Terminalde Etiket Arama C¸ıktısı

Etiketleri listelerken hangi etiketten kac¸ tane oldugunu˘ yazdıramadık. Bir etiketten kac¸ tane varsa o kadar yazdırabildik.

Yetim Etiketlerden dosya olus¸turma is¸lemini yapabildik ve yetim etiket lis- tesinden silebildik.”output.txt” dosyasını guncelle¨ yebildik.(Fig. 5)(Fig. 6)(Fig. 7)(Fig. 8)

Fig. 5. Program ˙Ilk C¸alıs¸tıgında˘ Olus¸an ”output.txt” orne¨ gi˘
![Aspose Words e230bca6-83b4-4554-b5c3-bf3a2eeb3a06 006](https://github.com/user-attachments/assets/4f35bce9-85c5-4373-b51c-bf80e7d996a3)
![Aspose Words e230bca6-83b4-4554-b5c3-bf3a2eeb3a06 005](https://github.com/user-attachments/assets/2e7a3578-36b6-45b0-ac64-64862ddb925c)

Fig. 8. ”output.txt” dosyasının guncellenmesi¨

5. SONUC¸ LAR
![Aspose Words e230bca6-83b4-4554-b5c3-bf3a2eeb3a06 007](https://github.com/user-attachments/assets/627f1dc6-4e55-4952-bf7b-f3352f03cb2b)

Sonuc¸ olarak bu proje sonunda,dosya operasyon- larını, struct yapısını daha iyi kavradık ve bunun yanı sıra yeni fonksiyonlar kullanmayı o¨grendik.˘ Eksiklerimizin farkına vardık. Verilen klasordeki¨ ic¸ ic¸e dosyaların okunmasını ve guncellenmesini¨ saglayan˘ bir program yazdık.

6. KAYNAKC¸ A

https://www.quora.com/Is-it-possible-to-make-an- Fig. 6. Terminalde Yetim Etiket c¸evrilemsinin gosterilmesi¨ array-of-files-in-c-programming

https://codeforwin.org/2018/03/c-program-to-list- all-files-in-a-directory-recursively.html

https://stackoverflow.com/questions/37225244/error- assignment-to-expression-with-array-type-error- when-i-assign-a-struct-f https://www.tutorialspoint.com/c![Aspose Words e230bca6-83b4-4554-b5c3-bf3a2eeb3a06 008](https://github.com/user-attachments/assets/6bcaf3ee-cb59-4baa-a7c7-18e44706e20a)

https://www.web-gelistirme-sc.com/tr/c/c-stringi- bosaltmanin-dogru-yolu/941301178/

https://www.youtube.com/watch?v=j9yL30R6npk

https://www.youtube.com/watch?v=P3VqA8WQza0

https://www.tutorialspoint.com/cstandardlibrary/

cf unctionstrstr.htm

https://www.bilgigunlugum.net/prog/cprog/cstdkut/ string/strstr

Fig. 7. Yetim Etiketin Dosyasının olus¸turuldugunun˘ gosterilmesi¨ https://www.bilgigunlugum.net/prog/cprog/cstdkut/

string/strcat
