>>git --version

>>mkdir myproject
>>cd myproject
>>git init //depo oluşturuldu
>>git config --global user.name "kamilbahram"
>>git config --global user.email "kamil.bahram@bil.omu.edu.tr"
>>git status ile bunun durumunu gösterir.

>>touch index.html   //oluşturalım

>>git add index.html

>>touch README.md
>>touch blue.css 

>>git add --all veya -A //oluşturulan dosyaları git ekleme

      //git commit//
**Taahhütler eklemek, ilerlememizi 
ve çalışırken yaptığımız değişiklikleri takip eder.
Git, her bir commit değişiklik noktasını veya "kaydetme 
noktasını" dikkate alır. Bir hata bulursanız veya bir 
değişiklik yapmak istiyorsanız, projede geri dönebileceğiniz 
bir noktadır.
**Biz commit işleminde her zaman bir mesaj eklemeliyiz .

>>git commit -m "çalişmanın 1. değişiklik noktası."


//index.html dosyasında değişiklik yapalım.

>>git status --short     girelim
---M index.html

git status --short Bu komutun sonunda aşağisaki çıktıları
alabiliriz.
?? - İzlenmeyen dosyalar
A - Sahneye eklenen dosyalar
M - Değiştirilmiş dosyalar
D - Silinen dosyalar


>>git commit -a -m "Bu ikinci versiyon"

>>git log   //versionlar görüntülenir.

>>git command -help - Belirli komut için mevcut tüm seçenekleri görün
>>git help --all - Tüm olası komutları görün


 ***Git Branch***
 projemizde yeni bir dal oluşturuyoruz.
 >>git branch ilk-branch   //branc olusur. Ana projenin(master) kopyası oluşur.

 >>git branch  //brancları listeler. başında * işaretli olan branch hangisi ise 
 o anda o branch da bulunulur.

>> git checkout ilk-branch //komutu ile bu branch a girilir.

--image.html oluşturalım
--index.html de değişiklikler yapalım ve aşağdaki komutu çalıştırlım.
>>git add --all  //burda ilk-branch da değişiklikler yüklenir.
>>git commit -m "ilk-branch :: version1"

>>git checkout master //checkout ile gecmek istediğimiz branch geçeriz.

>>git branchn -D ilk-branch // Branch silme işlem 
>>git checkout -b acil-branch //acil-branch isminde branch oluşturur ve o branch a girer.
--index.html de geğişiklik yap
>>git add index.html
>>git commit -m "problem cözüldü"
**acil-branch da yaptıgımız değişiklikleri ana branch a kaydedeceğiz.(merge)
yani problemi yan dalda çözdüm ve ana dala ekliyorum.

>>git checkout master //master a geç 
>>git merge acil-branch //ana daldaki(master) index.html e acil-branch da yaptıgımız değişiklik kaydedildi.

**ilk branch ı master merge edelim.
bunu yaparken index.html çakışması olacak.
bunu onlemek için once şu komutları girin
--master branch ında olmalıtız.
>>git add index.html 
>>git commit -m "cakılma noktası"
>>git merge ilk-branch

>>ls
index.html image.html  //merge işlemimizi yapmış olduk.

***Projeyi GitHub a yükleme***
>>git remote add origin (Repostory URL)
>>git push --set-upstream origin master
**kullanıcı adı ve access token girilir

>>git pull origin //uzak Repoda yapılan değişikliği local e cekeriz.

**yerel ropoda yapılan değişiklikleri gönderme
>>git commit -a -m "push origin deneniyor"
>>git push origin

>>https://aliozgur.gitbooks.io/git101/   //git ile ilgili eğitim içeren side. 

git branch silme komutları
>>git branch -d version1.1  //kendi projemizden silmek için 
>>git branch -dr  origin/version1.1   //remote repodan silmek için
>>git push origin :version1.1       //Githup üzerindegi dalımızı siler

GitHup üzrerinden repo çekme
>>mkdir ProjeAdi
>>cd proje adi
>>git init
>>git config --global user.name "kamilbahram"
>>git config --global user.email "kamilbhrm@gmail.com"
>>git clone https://github.com/kamilbahram/gitWork.git   // projenin url si




