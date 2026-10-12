# Sınıflar (Classes) ve Nesneler (Objects)

Sınıflar (Classes) ve Nesneler (Objects), nesne yönelimli programlamanın (Object-Oriented Programming - OOP) temelini oluşturur. Gerçek dünyadaki varlıkları yazılım ortamında modelleyebilmek için sınıf ve nesne kavramları kullanılır. Bir sınıf, belirli özelliklere ve davranışlara sahip olacak nesnelerin şablonu veya planı olarak düşünülebilir. Örneğin bir "Araba" sınıfı oluşturduğumuzda, bu sınıf arabaların sahip olabileceği renk, marka, model ve hız gibi özellikleri ile çalıştırma, durdurma veya hızlanma gibi davranışlarını tanımlar. Ancak sınıfın kendisi gerçek bir araba değildir; yalnızca arabaların nasıl oluşturulacağını belirten bir taslaktır.

Nesne ise bir sınıftan üretilen somut bir örnektir. Gerçek dünyada aynı araba modelinden birçok farklı araç bulunabileceği gibi, programlama dünyasında da aynı sınıftan birçok nesne oluşturulabilir. Örneğin "Araba" sınıfından kırmızı renkli bir BMW ve beyaz renkli bir Toyota nesnesi üretilebilir. Bu nesneler aynı sınıfa ait olmalarına rağmen farklı değerlere sahip olabilirler. Böylece her nesne kendi verilerini saklar ve sınıfta tanımlanan davranışları kullanabilir. Bir video oyunu örneği üzerinden açıklayacak olursak, "Karakter" adında bir sınıf oluşturulabilir. Bu sınıf, oyun içerisindeki bilgisayar tarafından kontrol edilen karakterlerin genel özelliklerini ve davranışlarını tanımlar. Daha sonra bu sınıftan karakter1, karakter2 ve karakter3 gibi farklı nesneler türetilir. Oluşturulan karakterlerin görünüşleri, güç seviyeleri, kullandıkları silahlar veya ekipmanlar birbirinden farklı olabilir. Ancak hepsi aynı "Karakter" sınıfından üretildikleri için ortak özellik ve davranışlara sahiptir.

Sınıfların en önemli amacı, verileri ve bu veriler üzerinde işlem yapan fonksiyonları bir araya getirerek programın daha düzenli, anlaşılır ve yeniden kullanılabilir olmasını sağlamaktır. Büyük yazılım projelerinde yüzlerce hatta binlerce nesne bulunabilir. Sınıflar sayesinde bu nesneler belirli kurallara göre oluşturulur ve yönetilir. Bu yaklaşım, kod tekrarını azaltırken bakım ve geliştirme süreçlerini de kolaylaştırır.

Örneğin bir üniversite otomasyon sistemi geliştirildiğini düşünelim. Öğrencilerin ad, soyad, numara ve bölüm bilgileri vardır. Bunun yanında ders kaydı yapma veya not görüntüleme gibi işlemler de gerçekleştirebilirler. Bu durumda bir "Öğrenci" sınıfı oluşturulur ve tüm öğrenciler bu sınıftan nesne olarak üretilir. Ahmet isimli öğrenci bir nesne, Ayşe isimli öğrenci başka bir nesne olur. Her ikisi de aynı sınıfın özelliklerine sahip olsa da kendi bilgilerini ayrı ayrı saklar.

Kısacası, sınıf bir kalıp veya şablon iken, nesne bu şablondan üretilen gerçek varlıktır. Nesne yönelimli programlamada yazılımlar, gerçek dünyadaki varlıkları temsil eden sınıflar ve bu sınıflardan oluşturulan nesneler üzerine kurulur. Bu sayede karmaşık sistemler daha mantıklı, modüler ve yönetilebilir bir yapıya kavuşur. Bahsedildiği gibi programlamada gerçek hayattaki varlıkları (örneğin bir öğrenci, bir araba, bir banka hesabı) kodda temsil etmek isteriz.

Bu varlıkların:

- özellikleri (attributes / properties) vardır → isim, yaş, bakiye…
- davranışları (methods / behaviors) vardır → para yatırma, yaşını artırma, bilgi gösterme…

Bunları tek bir çatı altında toplamak için sınıf (class) kullanırız.

- Sınıf (Class) → Kalıp / şablon / tarifname
- Nesne (Object / Instance) → Bu kalıptan üretilmiş somut örnek

## Sınıf (Class) Oluşturma

Aşağıda Python'da basit bir sınıf (class) tanımlanmaktadır. Bu dilde sınıf tanımlamak için _class_ anahtar sözcüğü kullanılır[^1].

class Student:

pass # şimdilik içi boş

Python'da sınıf isimleri PascalCase olarak adlandırılan kelimenin ilk harfinin büyük yazıldığı biçimde yazılır. Örneğin;

- Student
- BankAccount
- Car
- LibraryMember
- OnlineShoppingCart

Sınıf, bir varlığı veya kavramı temsil ettiği için isim kullanılır. Fiil veya sıfat kullanmaktan kaçınmak gerekir. Örneğin;

- Doğru: Student, Engine, Order
- Yanlış: Calculate, ProcessData, Fast

Sınıfın ne işe yaradığını isminden anlayabilmeliyiz. Kod hem birden fazla geliştiricinin üzerinde çalışacağı hem de tek bir geliştirici tarafından yazılsa bile ileride anlam karmaşası yaşanmaması için kısaltmalardan ve anlamsız isimlerden kaçınılarak yazılmalıdır.

- İyi: BankAccount, StudentGrade
- Kötü: BA, SG, MyClass, Data1

Ayrıca sınıf ismi oluşturulurken teknik olarak aşağıdaki kurallara uymak gerekmektedir.

- Harf veya alt çizgi ile başlamalıdır.
- Harf, rakam ve alt çizgi içerebilir.
- Python anahtar sözcükleri (class, def, if vb.) kullanılamaz.
- Büyük-küçük harf duyarlıdır (Student ile student farklıdır).

Python'da sınıf oluşturulurken varsayılan değerler girilebilir. Aşağıda bu örnek verilmektedir.

class Karakter:

&nbsp; def \__init_\_(self, isim, can=100, seviye=1):

&nbsp; self.isim = isim

&nbsp; self.can = can

&nbsp; self.seviye = seviye

Python'da sınıfa ait değerler genellikle iki şekilde tanımlanır; bunlardan ilki \__init__ içerisinde tanımlamaktadır. Genellikle bu yaygındır.

class Karakter:

&nbsp; def \__init_\_(self, isim, can):

&nbsp; self.isim = isim

&nbsp; self.can = can

Burada isim ve can, her nesneye özel olarak oluşturulur.

k1 = Karakter("Savaşçı", 100)

k2 = Karakter("Okçu", 80)

Örneğin yukarıdaki gibi iki nesne oluşturulduğunda bellekte kabaca şöyle bir görünüm olacaktır.

k1

&nbsp;├─ isim = Savaşçı

&nbsp;└─ can = 100

k2

&nbsp;├─ isim = Okçu

&nbsp;└─ can = 80

Bazı özelliklerin başlangıç değeri aynı olabilir. Bunun için \__init__ tanımlanırken varsayılan değer atanır.

class Karakter:

&nbsp; def \__init_\_(self, isim, can=100):

&nbsp; self.isim = isim

&nbsp; self.can = can

Aşağıda dikkat edileceği üzere **Savaşçı** yani **k1** nesnesine **can** değeri atanmasına gerek kalmamıştır.

k1 = Karakter("Savaşçı")

k2 = Karakter("Ejderha", 500)

Bazı durumlarda bir bilginin sınıftan (class) türetilen tüm nesnelerde (object) aynı olması istenebilir. Bu durumda **sınıf değişkeni** şeklinde değişken tanımlanır.

class Karakter:

&nbsp; oyun_adi = "Canavar Avcıları"

Aşağıdaki gibi bir kod yazıldığında

k1 = Karakter()

k2 = Karakter()

print(k1.oyun_adi)

print(k2.oyun_adi)

Şu sonuç alınacaktır.

Canavar Avcıları

Canavar Avcıları

Eğer istenirse nesnelere sonradan özellik eklenebilir. Aşağıda bununla ilgili örnek verilmektedir.

class Karakter:

&nbsp; pass

k1 = Karakter()

k1.isim = "Savaşçı"

k1.can = 100

Fakat bu büyük projelerde çok tercih edilen bir yöntem değildir. Çünkü takip edilmesi zordur.

## Nesne (Object) Oluşturma

Nesne Oluşturma (Object Instantiation), nesne yönelimli programlamanın en önemli adımlarından biridir. Bir sınıf (class) oluşturduktan sonra, o sınıfı kullanarak gerçek nesneler üretiriz. Çünkü sınıf tek başına yalnızca bir şablondur; program içerisinde kullanılabilen asıl varlıklar nesnelerdir.

Örneğin bir oyun geliştirdiğimizi düşünelim. Oyunda düşman karakterler bulunacak olsun. Öncelikle bu düşmanların genel özelliklerini tanımlayan bir sınıf oluştururuz:

class Dusman:

&nbsp; def \__init_\_(self, isim, can):

&nbsp; self.isim = isim

&nbsp; self.can = can

Bu kod çalıştığında henüz hiçbir düşman oluşturulmamıştır. Sadece "Bir düşman nasıl olmalıdır?" sorusunun cevabı verilmiştir. Bu nedenle sınıfı bir bina projesine benzetebiliriz. Mimarın çizdiği proje vardır ancak ortada henüz gerçek bir bina yoktur. Bir nesne oluşturmak için sınıf adı kullanılmaktadır. Aşağıda Dusman sınıfından bir düşman oluşturulmaktadır.

dusman1 = Dusman("Goblin", 100)

Bu satır çalıştığında Python bellekte yeni bir nesne oluşturur. Ardından otomatik olarak \__init_\_() metodu çağrılır ve verilen değerler nesnenin özelliklerine atanır. Artık dusman1 isimli gerçek bir nesne vardır ve özelliklerine erişebiliriz:

print(dusman1.isim)

print(dusman1.can)

Bir sınıftan yalnızca bir nesne oluşturmak zorunda değiliz. Aynı sınıftan istediğimiz kadar nesne oluşturabiliriz:

dusman1 = Dusman("Goblin", 100)

dusman2 = Dusman("Ork", 150)

dusman3 = Dusman("Ejderha", 500)

Burada dikkat edilmesi gereken nokta, bütün nesnelerin aynı sınıftan oluşturulmuş olmalarına rağmen farklı değerlere sahip olmalarıdır. Yani her nesne kendi verilerini saklar. dusman1 nesnesinin can değerini değiştirmek diğer nesneleri etkilemez.

dusman1.can = 50

print(dusman1.can)

print(dusman2.can)

Çıktı şu şekilde olacaktır:

50

150

## \__init__ Metodu (Constructor) ve Self Kavramı

\__init__metodu (constructor), bir sınıftan yeni bir nesne oluşturulduğu anda otomatik olarak çalışan özel bir metottur. Temel amacı, oluşturulan nesnenin ilk değerlerini belirlemek ve nesneyi kullanıma hazır hale getirmektir. Python'da bir nesne oluşturulduğunda programcının ayrıca çağırmasına gerek kalmadan \_*init*_ metodu kendiliğinden çalışır.

Bunu gerçek hayattan bir örnekle açıklayabiliriz. Bir araba fabrikasını düşünelim. Fabrikanın elinde bir araba tasarımı, yani bir sınıf vardır. Ancak fabrikadan yeni bir araba çıktığında bu arabanın markası, modeli, rengi ve motor gücü gibi bilgilerinin belirlenmesi gerekir. İşte \__init__ metodu da nesne oluşturulurken bu başlangıç bilgilerinin atanmasını sağlar. Böylece her yeni nesne oluşturulduğunda gerekli özellikler otomatik olarak tanımlanmış olur.

Örneğin bir oyun geliştirdiğimizi düşünelim. Oyunda oluşturulan her karakterin bir adı, can puanı ve saldırı gücü olması gerekiyor olabilir. Karakter nesnesi oluşturulurken bu bilgilerin sonradan tek tek atanması yerine, \__init__ metodu sayesinde karakter yaratıldığı anda gerekli değerler verilebilir. Böylece nesne eksik bilgilerle oluşmaz ve doğrudan kullanılabilir hale gelir.

\__init__ metodunun ilk parametresi her zaman self olur. **self**, oluşturulan nesnenin kendisini temsil eder. Nesneye ait özellikler bu nesne üzerinde saklanır. Bu nedenle **self.isim**, **self.can** veya **self.saldiri_gucu** gibi ifadeler kullanılarak değerler nesnenin içerisine kaydedilir. Daha sonra bu değerlere nesnenin herhangi bir yerinden erişilebilir.

Bir sınıfta \__init__metodu bulunmak zorunda değildir. Ancak çoğu durumda nesnelerin başlangıç değerlerini belirlemek gerektiğinden kullanılır. Eğer bir sınıfta \_*init*_ tanımlanmamışsa Python yine nesne oluşturabilir fakat nesne oluşturulurken başlangıç ayarlamaları otomatik olarak yapılmaz. Aşağıda bununla ilgili örnek verilmektedir:

class Student:

def \__init_\_(self, name, age, student_id):

self.name = name

self.age = age

self.student_id = student_id

Teknik olarak olabilir. Python için self özel bir anahtar kelime değildir, sadece bir isimlendirme geleneğidir. Tercih edilmemesine rağmen aşağıdaki kodda çalışır.

class Karakter:

&nbsp; def \__init_\_(ben, isim):

&nbsp; ben.isim = isim

karakter1 = Karakter("Savaşçı")

print(karakter1.isim)

\__init__ metodunda self anahtar sözcüğünden sonra tanımlanan değişken isimleri dışarından gelen geçici parametrelerdir. Asıl önemli olan ve dışarıdan çağırılabilen self.degisken şeklinde verilen isimdir. Aşağıda bununla ilgili örnek verilmektedir.

class Student:

&nbsp; def \__init_\_(self, name, age, grade):

&nbsp; self.adi = name

&nbsp; self.yasi = age

&nbsp; self.notu = grade

ogrenci1 = Student("Mehmet Yılmaz", 16, 85)

Burada self sözcüğünden sonra gelen kelime ile ona atanan farklıdır. Bu durumda:

print(ogrenci1.name)

Bu şekilde yazılan bir hataya sebep olacaktır. Doğrusu aşağıdaki gibidir. Burada name, age ve grade sözcükleri geçici parametrelerdir. Ama genelde aynı isim kullanılır. Burada sözdiziminin (syntax) mantığının anlaşılması açısından bu örnek verilmiştir.

&nbsp; print(ogrenci1.adi)

&nbsp; print(ogrenci1.yasi)

&nbsp; print(ogrenci1.notu)

Python'da yer alan \__init__ yani kurucu metot (constructor) diğer birçok nesne yönelimli dillerde de vardır. Aşağıda daha önce de verilen Python kodu verilmektedir.

class Student:

&nbsp; def \__init_\_(self, name, age):

&nbsp; self.name = name

&nbsp; self.age = age

#

Ogrenci1 = Student("Mehmet", 16)

Burada Student adında bir sınıf oluşturulmuş ve sonrasında bu sınıfa \__init__ metodu içerisinde name ve age parametreleri tanımlanmıştır. Bunun Java kodu aşağıda verilmektedir.

public class Student {

&nbsp; String name;

&nbsp; int age;

&nbsp; public Student(String name, int age) {

&nbsp; this.name = name;

&nbsp; this.age = age;

&nbsp; }

}

Student ogrenci1 = new Student("Mehmet", 16);

Dikkat edileceği üzere her iki dildeki mantık birbirine oldukça yakındır. Temel fark sözdizimindedir (syntax). Java'da değişkenlerin veri türleri (String, int vb.) önceden belirtilmek zorundayken, Python dinamik tipli bir dil olduğu için böyle bir zorunluluk bulunmaz. Ayrıca Java, erişim denetimini (access control) daha sıkı uygulayan bir dildir. Bu nedenle sınıf, metot ve değişken tanımlamalarında public, private ve protected gibi erişim belirleyicileri kullanılabilir. Python'da ise bu yapı bulunmaz ve erişim denetimi daha çok geliştiricilerin uyması beklenen kurallar üzerinden sağlanır.

Aşağıda ise aynı kod C++ dilinde verilmektedir.

# include &lt;iostream&gt;

# include &lt;string&gt;

using namespace std;

class Student {

public:

&nbsp; string name;

&nbsp; int age;

&nbsp; Student(string name, int age) {

&nbsp; this->name = name;

&nbsp; this->age = age;

&nbsp; }

};

int main() {

&nbsp; Student ogrenci1("Mehmet", 16);

&nbsp; cout << ogrenci1.name << endl;

&nbsp; cout << ogrenci1.age << endl;

&nbsp; return 0;

}

Python ve Java'da olduğu gibi C++'de class takısı ile bir sınıf oluşturulmuştur. Python'daki self.name, Java'daki this.name C++'da this->name şeklinde olmaktadır. Üçü de aynı görevi yerine getirmektedir.

## Metotlar (Methods)

Nesne Yönelimli Programlamada metotlar (methods), nesnenin "davranışlarını" (behavior) temsil eder. Sınıfları bir şablon, nitelikleri (attributes) o şablonun taşıdığı veri/durum (state) olarak tanımladıktan sonra; metotlar bu veriyi işleyen, değiştiren ve dış dünyayla konuşturan mekanizmadır.

### Metot ve Fonksiyon Arasındaki Fark

Fonksiyon, herhangi bir sınıf yapısının içinde yer almayan, bağımsız olarak tanımlanmış kod bloğudur. Adı doğrudan yazılarak çağrılır ve genellikle dışarıdan aldığı girdileri işleyip bir sonuç döner. Python'un yerleşik olarak sunduğu print() ve len() gibi yapılar veya bir sınıf hiyerarşisi dışında **def** anahtar kelimesiyle kendi tanımladığınız işlemler birer fonksiyondur.

Metot ise özünde bir fonksiyondur ancak bir sınıfın (class) içine yazıldığı ve o sınıftan türetilen bir nesneye ya da doğrudan sınıfın kendisine ait olduğu için metottur. Metotlar bağımsız çağrılamaz; mutlaka bağlı oldukları nesne üzerinden nokta notasyonu kullanılarak çalıştırılır. Örneğin bir listenin eleman eklemek için kullandığı **liste.append**() veya bir metni büyük harfe dönüştüren **metin.upper()** ifadeleri birer metottur. Metotlar, ilk parametre olarak genellikle **self** alırlar ve çağrıldıkları nesnenin mevcut durumuna, verilerine doğrudan erişip bu verileri değiştirebilirler.

Sonuç olarak her metot aslında bir fonksiyondur, ancak yalnızca bir nesneye veya sınıfa ait olan ve o nesne üzerinden çağrılan fonksiyonlara metot denir.

### Metot Tanımlama

Python'da metotlar, nesne yönelimli programlamanın (OOP) kalbinde yer alan ve bir nesnenin neler yapabileceğini, yani onun davranışlarını belirleyen kod bloklarıdır. Bir sınıfı bir varlığın şablonu, o sınıftan üretilen nesneyi de somut bir varlık olarak düşünürseniz; metotlar o varlığın yetenekleridir. Örneğin bir "Araba" sınıfı tanımladığınızda arabanın rengi ve modeli onun verisi (özelliği) iken; "çalış", "hızlan" veya "fren yap" gibi eylemleri o sınıfın metotlarıdır.

Metotları normal fonksiyonlardan ayıran en kritik detay **self** parametresidir. Bir sınıfın içine sıradan bir metot yazdığınızda, Python ilk parametre olarak her zaman self ifadesini bekler. self, o metodun hangi somut nesne tarafından çağrıldığını temsil eder. Yani araba nesne üzerinden araba.hizlan() denildiğinde, Python arka planda o hızlanma eylemini tam olarak "o arabaya" uygular ve arabanın hız verisini günceller. Metot bu sayede nesnenin kendi iç dünyasındaki verilere erişebilir ve onları dilediği gibi değiştirebilir.

Python'da metotlar tek bir kalıptan ibaret değildir; işlevlerine göre farklı türlere ayrılırlar. En sık kullanılan tür, nesnenin kendi verilerini değiştiren örnek (instance) metotlarıdır. Bunun yanında başında ve sonunda çift alt çizgi barındıran ve genellikle "dunder[^2]" ya da "sihirli metot" denen özel metotlar vardır. Örneğin yeni bir nesne oluşturulduğu an otomatik çalışan \__init__kurucu metodu ya da bir nesneyi ekrana yazdırdığınızda nasıl görüneceğini belirleyen \_*str*_ metodu bu gruba girer. Bu metotlar Python'un yerleşik davranışlarını kendi nesnelerinize öğretmenizi sağlar.

Bir sınıf içerisinde metot tanımlamak, sözdizimi açısından sıradan bir Python fonksiyonu tanımlamaya oldukça benzer. **def** anahtar kelimesi kullanılır, metoda açıklayıcı bir isim verilir ve ardından parantezler içerisinde parametreler listelenir. Ancak daha önce de vurgulandığı gibi, metot bir sınıfa ait olduğu için ilk parametresi her zaman o anki nesneyi temsil eden **self** olmak zorundadır.

Aşağıda bir banka hesabı üzerinden örnek bir sınıf ve bu sınıfa ait metotların tanımı verilmektedir:

class BankaHesabi:

def \__init_\_(self, hesap_sahibi, bakiye=0):

self.hesap_sahibi = hesap_sahibi

self.bakiye = bakiye

\# Nesneye ait davranışı tanımlayan örnek metodu

def bakiye_bilgisi(self):

print(f"Sayın {self.hesap_sahibi}, mevcut bakiyeniz: {self.bakiye} TL'dir.")

\# Parametre alan ve nesnenin durumunu (state) değiştiren metot

def para_yatir(self, miktar):

if miktar > 0:

self.bakiye += miktar

print(f"{miktar} TL yatırıldı. Güncel bakiye: {self.bakiye} TL")

else:

print("Geçersiz yatırma miktarı!")

\# Koşula bağlı işlem yapan ve değer döndüren metot

def para_cek(self, miktar):

if 0 < miktar <= self.bakiye:

self.bakiye -= miktar

print(f"{miktar} TL çekildi. Kalan bakiye: {self.bakiye} TL")

return miktar

else:

print("Yetersiz bakiye veya hatalı miktar!")

return 0

Bu sınıf tanımlandıktan sonra metotların nesneler üzerinden nasıl çağrıldığına bakalım:

\# Sınıftan somut bir nesne türetme

hesap1 = BankaHesabi("Zeynep Kaya", 1500)

\# Metotları çalıştırma (nokta notasyonu ile)

hesap1.bakiye_bilgisi()

hesap1.para_yatir(500)

cekilen = hesap1.para_cek(300)

hesap1.bakiye_bilgisi()

Kod çalıştırıldığında konsol çıktısı şu şekilde olacaktır:

Sayın Zeynep Kaya, mevcut bakiyeniz: 1500 TL'dir.

500 TL yatırıldı. Güncel bakiye: 2000 TL

300 TL çekildi. Kalan bakiye: 1700 TL

Sayın Zeynep Kaya, mevcut bakiyeniz: 1700 TL'dir.

Burada dikkat edilmesi gereken temel ayrıntı, **hesap1.para_yatir(500)** çağrısı yapıldığında fonksiyona yalnızca tek bir argüman (500) gönderilmiş olmasıdır. Tanımda ise **def para_yatir(self, miktar)** şeklinde iki parametre yer almaktadır. Python arka planda bu çağrıyı otomatik olarak şu biçime dönüştürür:

BankaHesabi.para_yatir(hesap1, 500)

Görüldüğü üzere Python, nokta operatörünün solundaki **hesap1** nesnesini ilk argüman olan **self** yerine sessizce yerleştirir. Bu sayede metodun gövdesinde kullanılan **self.bakiye**, doğrudan o nesnenin kendi bakiyesini bulur ve günceller.

### Metot Türleri: Örnek, Sınıf ve Statik Metotlar

Python'da metotlar nesneyle ve sınıfla kurdukları bağa göre üçe ayrılır: Bunlar örnek metotları, sınıf metotları ve statik metotlardır.

**1\. Örnek Metotları (Instance Methods)**

En sık kullanılan ve varsayılan metot türüdür. İlk parametre olarak **self** alırlar. Bu metotlar hem nesneye özgü niteliklere **(self.nitelik)** hem de sınıf değişkenlerine erişebilir ve bunları değiştirebilirler. Yukarıdaki banka hesabı örneğinde yer alan tüm işlemler birer örnek metodudur.

**2\. Sınıf Metotları (Class Methods)**

Belirli bir nesneye değil, doğrudan sınıfın kendisine bağlı olan metotlardır. İlk parametre olarak nesneyi (self) değil, sınıfı temsil eden **cls** parametresini alırlar. Sınıf metotları tanımlanırken üzerlerine **@classmethod** dekoratörü (decorator) eklenir. Genellikle alternatif nesne oluşturma yapıları (factory methods)[^3] kurmak veya tüm nesneleri ilgilendiren sınıf düzeyindeki değişkenleri yönetmek amacıyla kullanılırlar.

class Personel:

personel_sayisi = 0 # Sınıf değişkeni

def \__init_\_(self, ad, maas):

self.ad = ad

self.maas = maas

Personel.personel_sayisi += 1

@classmethod

def toplam_personel(cls):

print(f"Sistemde kayıtlı toplam personel sayısı: {cls.personel_sayisi}")

\# Alternatif kurucu metot: Metin formatından nesne üretme

@classmethod

def metinden_olustur(cls, veri_metni):

ad, maas = veri_metni.split("-")

return cls(ad, float(maas))

Burada personel_sayisi sınıf değişkenidir. Bir nesneye (object) değil sınıfın (class) kendisine bağlıdır. Burada dikkat edilecek bir diğer nokta; bir nesne oluşturulduğunda **Personel.personel_sayisi += 1** ile sınıfa ait olan **personel_sayisi** değişkeni bir arttırılmaktadır. Kodun kullanımı aşağıdaki gibi olacaktır.

p1 = Personel("Ali", 35000)

p2 = Personel.metinden_olustur("Ayşe-42000")

Personel.toplam_personel() # Çıktı: Sistemde kayıtlı toplam personel sayısı: 2

Bu kodda üç temel konu bulunmaktadır. Bunlar:

- **Sınıf değişkeni:** Toplam personel sayısını tutuyor.
- **Sınıf metodu (@classmethod):** Sınıfın kendisi üzerinden işlem yapıyor.
- **Alternatif kurucu metot:** Metin biçimindeki verilerden yeni personel nesnesi oluşturuyor.

@classmethod

def toplam_personel(cls):

print(f"Sistemde kayıtlı toplam personel sayısı: {cls.personel_sayisi}")

Burada @classmethod ile hemen altındaki metodun bir sınıf metodu olduğu belirtilir. Bir nesneyi temsil eden self in aksine cls sınıf temsil eder. Şu şekilde bir işlem yapıldığında;

ahmet = Personel("Ahmet", 35000)

ayse = Personel("Ayşe", 42000)

Personel.toplam_personel()

Ekran çıktısı aşağıdaki gibi olacaktır.

Sistemde kayıtlı toplam personel sayısı: 2

Dikkat edileceği üzere toplam_personel() metodunu çağırırken Ahmet veya Ayşe nesnesini kullanmak zorunda değildir. Doğrudan Personel sınıfı üzerinden istek çağırılmaktadır. Burada cls.personel_sayisi, Personel.personel_sayisi ile aynı sınıf değişkenine erişir. Kodun bir diğer kısmında alternatif kurucu metot uygulanmıştır.

@classmethod

def metinden_olustur(cls, veri_metni):

ad, maas = veri_metni.split("-")

return cls(ad, float(maas))

Normalde nesne oluşturmak için aşağıdaki gibi bir kod yazmak gerekmektedir.

ahmet = Personel("Ahmet", 35000)

Fakat metinden_olustur() alternatif kurucu metodu ile bu olmadan nesne oluşturmak mümkündür. Aşağıda bunun örneği verilmektedir.

mehmet = Personel.metinden_olustur("Mehmet-45000")

print(mehmet.ad)

print(mehmet.maas)

Ekran çıktısı aşağıdaki gibi olacaktır.

Mehmet

45000.0

Metot içerisindeki **veri_metni.split("-")** işlemi bunu gerçekleştirmektedir. Sonrasında string formunda olan maaş float haline getirilmiştir. Aşağıda farklı şekillerde nesne oluşturma gösterilmiştir.

p1 = Personel("Ali", 30000)

p2 = Personel("Zeynep", 40000)

p3 = Personel.metinden_olustur("Can-50000")

**3\. Statik Metotlar (Static Methods)**

Ne nesneye (self) ne de sınıfa (cls) doğrudan bağımlı olmayan metotlardır. Sınıfın içinde mantıksal bir küme oluşturduğu için barındırılırlar; ancak sıradan bir bağımsız fonksiyon gibi davranırlar. Tanımlanırken **@staticmethod** dekoratörü kullanılmaktadır.

class MatematikselAraclar:

@staticmethod

def cift_mi(sayi):

return sayi % 2 == 0

Burada statik metot kullanılarak nesne oluşturmaya gerek kalmadan doğrudan **MatematikselAraclar.cift_mi(14)** biçiminde sınıf adı üzerinden işlem yapılmıştır. Normalde bir sınıf (class) içine fonksiyon yazdığınızda Python sizden ilk parametre olarak özel bir bağlayıcı beklemektedir. Statik metotta buna ihtiyaç yoktur. Özet olarak üç metot türünde durum aşağıdaki gibidir.

- **Normal Metotlar (Instance Method):** İlk parametre olarak self alırlar. Bu, metodun çağrıldığı **özel nesneyi** temsil eder. Nesnenin kendi değişkenlerine (self.isim, self.yas) erişebilir.
- **Sınıf Metotları (@classmethod):** İlk parametre olarak cls alırlar. Bu, doğrudan **sınıfın kendisini** temsil eder. Sınıf düzeyindeki değişkenlere erişir veya alternatif nesne üreticileri (factory) oluşturur.
- **Statik Metotlar (@staticmethod):** Ne self alır ne de cls. Sınıfın veya nesnenin iç durumundan (state) tamamen habersizdir. Sadece dışarıdan fonksiyona parametre olarak ne gönderilirse onunla ilgilenir.

Statik metotlar sınıfın içinde mantıksal bir küme oluşturduğu için barındırılırlar; fakat daha önce de belirtildiği gibi sıradan bir bağımsız fonksiyon gibi davranırlar. Bunun yapılmasındaki amaç:

- **İsim Alanı Düzeni (Namespacing):** Projeniz büyüdükçe yüzlerce fonksiyon olur. cift_mi, asal_mi, faktoriyel gibi fonksiyonları dağınık bırakmak yerine MatematikselAraclar çatısı altında toplayarak düzen sağlanır.
- **Okunabilirlik:** Kodu okuyan biri MatematikselAraclar.cift_mi(14) gördüğünde bu fonksiyonun amacını ve hangi konu alanına ait olduğunu anında anlar.

Eğer statik değil de normal metot olarak yazılmış olsaydı işlem yapmak için aşağıdaki gibi kod yazmak gerektirecekti.

arac = MatematikselAraclar() # Nesne türetildi (bellekte yer açıldı)

print(arac.cift_mi(14))

### Özel (Sihirli / Dunder) Metotlar

Python'da sınıf mekanizmasını esnek kılan en güçlü unsurlardan biri "Özel Metotlar"dır (Special Methods). Bu metotların isimlerinin başında ve sonunda ikişer alt çizgi yer alır (Double Underscore ifadesinin kısaltması olarak toplulukta sıklıkla "dunder" metotlar olarak anılır).

Dunder metotlar, Python'un yerleşik fonksiyonları (len(), str(), print(), del vb.) veya operatörleri (+, -, ==, < vb.) çağrıldığında arka planda tetiklenen kancalardır (hooks). Bu metotları sınıfınızın içinde ezerek (override ederek), kendi nesnelerinizin Python'un doğal veri tipleri gibi davranması sağlanabilir.

Sık karşılaşılan özel metotlar aşağıda verilmektedir.

**Nesne Temsili: \__str__ ve \__repr__**

Bir nesneyi print() ile ekrana yazdırmaya veya str() ile metne dönüştürmeye çalıştığımızda, Python varsayılan olarak nesnenin bellekteki adresini gösterir (örneğin &lt;\__main_\_.Kitap object at 0x7c8a11&gt;). Kullanıcıya veya geliştiriciye anlamlı bir çıktı sunmak için bu metotlar override edilir:

- \__str_\_(self): Kullanıcı odaklı, okunaklı ve anlaşılır bir metin döndürür. print(nesne) dendiğinde çalışır.
- \__repr_\_(self): Geliştirici odaklı, nesnenin nasıl oluşturulduğunu açıkça belirten teknik bir metin döndürür.

class Kitap:

def \__init_\_(self, baslik, yazar, sayfa_sayisi):

self.baslik = baslik

self.yazar = yazar

self.sayfa_sayisi = sayfa_sayisi

def \__str_\_(self):

return f"'{self.baslik}' - {self.yazar}"

def \__repr_\_(self):

return f"Kitap(baslik='{self.baslik}', yazar='{self.yazar}', sayfa_sayisi={self.sayfa_sayisi})"

def \__len_\_(self):

return self.sayfa_sayisi

Kullanımı:

kitap1 = Kitap("Nesne Yönelimli Programlama", "Yılmaz Ağca", 220)

print(kitap1) # \__str__ çağrılır: 'Nesne Yönelimli Programlama' – Yılmaz Ağca

print(len(kitap1)) # \__len__ çağrılır: 220

print(repr(kitap1) # \__repr__ çağrılır:

Kodun çıktısı aşağıdaki gibi olacaktır.

'Nesne Yönelimli Programlama' - Yılmaz Ağca

220

Kitap(baslik='Nesne Yönelimli Programlama', yazar='Yılmaz Ağca', sayfa_sayisi=220)

Eğer \__str__özel metodu kullanılmamış olsaydı. Kod şu şekilde yazılmak zorunda kalınacaktı. Burada kendi metodumuzu yazmak yerine Python'ın kendi özel metodunu yani \_*str*_ yi kullanmış olduk.

class Kitap:

def \__init_\_(self, baslik, yazar, sayfa_sayisi):

self.baslik = baslik

self.yazar = yazar

self.sayfa_sayisi = sayfa_sayisi

def yazdir(self):

print(f"'{self.baslik}' - {self.yazar}")

**Operatör Aşırı Yükleme (Operator Overloading)**

Python'da iki sayı toplanırken kullanılan + operatörü aslında arka planda \__add__metodunu çalıştırır. Sınıfa bu metodu tanımlanarak iki nesnenin + işaretiyle toplanabilmesini sağlanmaktadır. Bu ismin verilme sebebi +, -, \*, == gibi işlemlerin farklı veri tipleri üzerinde farklı işlemler yapabilmesinden dolayıdır. Aşağıda arka planda \_*add*_ özel metodu işlemektedir ve sayı olan veri tipinde matematiksel işlem yaparken metin veri tipinde ekleme yapmaktadır.

print(10 + 20) # 30: Sayıları toplar

print("Merhaba " + "Dünya") # Merhaba Dünya: Metinleri birleştirir

print(\[1, 2\] + \[3, 4\]) # \[1, 2, 3, 4\]: Listeleri birleştirir

Python'da yukarıda da belirtildiği gibi + işlemi aslında \__add__ işlemi yapmaktadır. Bir sınıf içerisinde bu özel metot kullanılarak toplama işlemi yapılabilmektedir.

class Konum:

def \__init_\_(self, x, y):

self.x = x

self.y = y

def \__add_\_(self, hareket):

return Konum(self.x + hareket.x, self.y + hareket.y)

def \__str_\_(self):

return f"({self.x}, {self.y})"

savasci_konumu = Konum(10, 5) # Karakter şu an burada

saga_adim = Konum(3, 0) # 3 birim sağa

yukari_adim = Konum(0, 2) # 2 birim yukarı

yeni_konum = savasci_konumu + saga_adim + yukari_adim

print(yeni_konum) # Çıktı: (13, 7)

Eğer \__add__ ile metot yazılmamış olsaydı aşağıdaki kodda olduğu gibi hata alınacaktı.

class Envanter:

def \__init_\_(self, altin):

self.altin = altin

e1 = Envanter(100)

e2 = Envanter(50)

print(e1 + e2) # HATA: TypeError, Python iki Envanter'i nasıl toplayacağını bilmiyor

Python'da farklı operatörler için farklı dunder metotları kullanılır. Aşağıda bununla ilgili tablo verilmektedir.

| **Tablo 2.1:** Python'daki Özel (Dunder) Metotlar                       |              |                    |
| ----------------------------------------------------------------------- | ------------ | ------------------ |
| **Operatör**                                                            | **Açıklama** | **Örnek Kullanım** |
| +                                                                       | \__add__     | a + b              |
| \-                                                                      | \__sub__     | a - b              |
| \*                                                                      | \__mul__     | a \* b             |
| /                                                                       | \__truediv__ | a / b              |
| \==                                                                     | \__eq__      | a == b             |
| !=                                                                      | \__ne__      | a != b             |
| <                                                                       | \__lt__      | a < b              |
| \>                                                                      | \__gt__      | a > b              |
| <=                                                                      | \__le__      | a <= b             |
| \>=                                                                     | \__ge__      | a >= b             |
| **Kaynak:** <https://www.w3schools.com/python/python_magic_methods.asp> |              |                    |

[^1]:
    **Parantezsiz Kullanım (class Kullanici:):** Python 3'te bir sınıf başka bir sınıftan (base class) miras almıyorsa, sınıf tanımının sonundaki parantezler isteğe bağlıdır. Günümüzde en yaygın ve modern yazım tarzı budur.

    **Parantezli Kullanım (class Kullanici():):** Python 2'den kalma bir alışkanlıktır veya başka bir dilden (örneğin C++ veya Java'daki fonksiyon çağrısı alışkanlığıyla) gelen geliştiricilerin tercih ettiği bir yazılımdır.

[^2]: Bunu açıkla

[^3]: Python'da standart bir sınıfın sadece tek bir \__init__ kurucu metodu (constructor) olabilir. Ancak bazen bir nesneyi farklı veri formatlarından (örneğin bir dizeden, bir sözlükten veya bir dosyadan) başlatmak istenebilir. Bu durumda bu tasarım deseni kullanılır.