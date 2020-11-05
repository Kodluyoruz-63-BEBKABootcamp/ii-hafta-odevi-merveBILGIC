# GOF nedir araştırınız.
Tasarım kalıpları, gerçek dünya uygulama geliştirmede tekrar tekrar bulduğunuz yazılım tasarım sorunlarına yönelik çözümlerdir.
Desenler, nesnelerin yeniden kullanılabilir tasarımları ve etkileşimleriyle ilgilidir.
23 Gang of Four (GoF) kalıpları genellikle diğer tüm modellerin temeli olarak kabul edilir.
Üç grupta kategorize edilirler: Yaratıcı, Yapısal ve Davranışsal . Bu referans, 23 GoF modelinin her biri için kaynak kodu sağlar.  
yaralanılan [kaynak](https://dofactory.com/net/design-patterns)

# Interface ve Abstract sınıflar arasındaki farklar nelerdir?
#### Abstraction (Soyutlama) Nedir?
Abstraction, OOP (Object Oriented Programming-Nesne Tabanlı Programlama) içerisindeki önemli kavramlardan birisidir. 
C#’taki soyutlama; diğer Object Oriented dillerde olduğu gibi iç detayları gizleyerek sadece işlevleri göstermeye denir
Abstract sınıfları genel olarak inheritance (kalıtım) uygularken kullanırız.
new anahtar sözcüğü ile nesneleri oluşturulamaz.
İçerisinde değişken ve metod bulundurabilir.
Abstract sınıflardan türetilen sınıfların abstract metodları implement etmesi zorunludur. Diğer metodları override etmeden de kullanabilir.
Constructors (yapıcı metodlar) ve destructors (yıkıcı metodlar) bulundurabilirler.
Static tanımlanamazlar. ( Tanımlanmaya çalışılırsa compiler “an abstract class cannot be sealed or static” hatası verir)
Bir sınıf yalnızca bir abstract sınıfı inheritance yoluyla implement edebilir. Çoklu kalıtım (multiple inheritance) desteklenmez.
Abstract olmayan metodları da bulundurabilir.
Kendisinden inherit alacak sınıflar ile arasında “is-a” ilişkisi vardır.
#### Interface
new keywordü ile nesneleri oluşturulamaz.
Bir sınıfın ne yapması gerektiğini belirtir, nasıl yapması gerektiğini değil.
Default olarak tüm Interface üyeleri abstract ve public olarak tanımlanır. Sizin özellikle belirtmeniz gerekmez.
Bir sınıf birden fazla interface’i inherit edebilir, çoklu kalıtım (multiple-inheritance) desteklenir.
İçerisinde yalnızca metodların imzaları yer alır, içi dolu metod bulunduramazlar.
Kendisinden inherit alacak sınıflar ile arasında “can-do” ilişkisi vardır.


### Kendi yorumum 
Biri arayüzdür biri sınıftır ve ikiside soyutlama için kullnılabilir.İnterface sınıf yapısının özelliklerini bulundurmaz ve bir sınıf istediği kadar interface inherit
edebilirken sadece bir tane absract sınıf inherit edebilir.  
[kaynak 1](https://medium.com/software-development-turkey/abstract-class-ve-interface-aras%C4%B1ndaki-farklar-nelerdir-3c0a4f956eba)  
[kaynak 2](http://cozvelioglu.com/abstract-class-ve-interface-arasindaki-farklar-nelerdir/)
# Yeni bir Gitthub repository oluştururken, repomuza ekleyebileceğimiz lisanslar nelerdir, bu lisanslar arasındaki farklar nelerdir?
- MIT
En yaygın kullanılan lisans türlerinden biridir. MIT tarafından yayınlandığı için adı da aynı şekilde MIT olarak geçer.
 MIT licence sizi birçok konuda özgür kılar. Yani yazılıma ait kaynak kodu veya derlenmiş yazılımı istediğiniz gibi değiştirebilir, yayabilir, kullanabilirsiniz.
 Ticari olarak bile kullanımında herhangi bir sorun olmaz. Fakat sizi özgür kıldığı kadar yazılımı geliştirenleri de özgür kılar. 
 Yani bir sorun çıkması durumunda geliştiriciler için herhangi bir yükümlülük söz konusu bile olamaz. 
 Dolayısı ile MIT ile lisanslanmış bir yazılımı gönül rahatlığı ile kullanabilirsiniz. Sadece yazılımın buglardan temizlenmiş, 
 yaygın bir kitle tarafından kullanılıyor olması sizi ilerde çıkabilecek yazılımsal sorunlar konusunda daha rahat ettirecektir.
 MIT ile lisanslanmış bir yazılımı kullandığınızda, o yazılıma referans vermeniz gerekiyor.
 - Apache Licence
 Apache lisansının MIT’den bir farkı yoktur. Sadece yazılımınızı dağıtırken kullandığınız Apache lisanslı ürünlerin lisanslarını da dağıtımınıza eklemeniz gerekiyor.
- GNU General Public Licence
GNU lisansı da MIT gibi aynı şekilde size yazılımın kodlarına erişim konusunda herhangi bir kısıtlama getirmez.
Fakat MIT lisansına göre kullanım açısından bazı kısıtlamalar getirir. 
Bu kısıtlamaların en önemlisi eğer yazılımında GNU lisansına sahip bir ürün kullandıysanız ve ürünü dağıtmaya başlarsanız sizin yazılımınız da GNU lisansına sahip olmalıdır.
Yani yazılımın kendi geliştirdiğiniz kısımlarının da kaynak kodlarını paylaşmak zorundasınız. 
Fakat MIT lisansı için aynı durum söz konusu değildir.
MIT lisansına sahip bir ürünü kullanarak geliştirdiğiniz bir üründeki kendi kodlarınızı kimseyle paylaşmak zorunda değilsiniz.
Yani kısaca GNU lisanslama konusunda kalıtsal davranır.  
[kaynak](https://medium.com/@mehmet.baran/yaz%C4%B1l%C4%B1m-lisans-tipleri-mit-apache-gnu-1397af4d1fbb)  
# Merge - Squash-Rebase arasındaki farklar nelerdir?
- Merge 
Git merge ile yaptığımız birleştirmede yeni bir commit yaratacak ve yeni branch’deki tüm history tarafını kaybetmeden birleştirme işlemi gerçekleşmiş olcaktır.
- Rebase
Git rebase ile birleştirdiğimizde ise branch deki commit’lerimizi tek tek alıp istediğmiz branch üzerine ekleyecektir.
Böylelikle tek bir history oluşturacak ve istenmeyen history ortadan kalkacaktır.
Bu iki komutun farkına baktığımız noktada, aslında benzer işi yaptıklarını ve
fark olarak ise git rebase kullanımında history’nin temizlendiğini ve git merge kullandığımızda ise tüm geçmişin korunduğunu görüyoruz.
- Squash
 git squash komutu aslında farklı bir rebase kullanımı olarak değerlendirmek daha doğru olacaktır. 
 Geçmişte atılan commit’leri yeniden düzenlemek, isimlendirmek veya birleştirmek için kullanıyoruz.
 Bu geçmişte atılan commit’ler, local’de veya uzak bir git sunucusunda olabilir. Unutmamamız gereken bir nokta da, 
 git squash işlemi yaptıktan sonra ‘force push’ kullanmamız gerektiğidir.
 İstenilen commit aralığını geri gidip yeniden düzenleme yaptıgımız için ‘force push’ kullanımı zorunludur.   
 [kaynak](https://medium.com/neyasistechnology/git-rebase-squash-ile-ge%C3%A7mi%C5%9Fi-yeniden-d%C3%BCzenlemek-9de36441f947)   
 # Agile-Scrum-Kanban kavramlarını araştırınız
 - Agile
 (çevik) yöntem, yazılım geliştirmede kullanılan proje yönetimine özel bir yaklaşımdır.
 Bu yöntem ekiplerin yazılım geliştirme süreçlerinin öngörülemezliğine cevap vermesine yardımcı olur.
 Genellikle sprint olarak bilinen artımlı, yinelemeli iş dizilerini kullanır.  
[kaynak](https://www.toptalent.co/agile-nedir-agile-metodu-nasil-uygulanir )    
- Scrum
Agile proje yönetim metodolojilerinden biridir. Kompleks yazılım süreçlerinin yönetilmesi için kullanılır. 
Bunu yaparken bütünü parçalayan; tekrara dayalı bir yöntem izler. Düzenli geri bildirim ve planlamalarla hedefe ulaşmayı sağlar.
Bu anlamda ihtiyaca yönelik ve esnek bir yapısı vardır. Müşteri ihtiyacına göre şekillendiği için müşterinin geri bildirimine göre yapılanmayı sağlar.
İletişim ve takım çalışması çok önemlidir. 3 temel prensip üzerine kurulmuştur;
  - Şeffaflık; Projenin ilerleyişi, sorunlar,gelişmeler herkes tarafından görülebilir olmalıdır.
  - Denetleme; Projenin ilerleyişi düzenli olarak kontrol edilir.
  - Uyarlama; Proje, yapılabilecek değişikliklere uyum sağlayabilmelidir.  
  [kaynak](https://medium.com/@secilcor/scrum-nedi%CC%87r-6a4326951dd8)  
- Kanban 
üretim sürecinde yer alan aşamaları görsel olarak işaretlemek için kartların kullanılmasıdır. 
Kanban aynı zamanda, birçok endüstri dalında dağıtım ekibini çevreleyen kargaşayı organize etmenin ve
iş akışını ortaya çıkarmanın ve işlem problemlerini çözmenin bir yoludur.
Bitmemiş işlerin ne kadar sürede işlem gördüğünü belirleyerek, işlem süresinin azaltılmasını sağlar. 
Atıkları azaltmak ve üretimi en üst düzeye çıkarmak için süreçlerin standart hale gelmesini sağlar.
[kaynak](https://www.muhendisbeyinler.net/kanban-nedir/)

