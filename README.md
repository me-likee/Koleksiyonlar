# Koleksiyonlar
using System.Collections.Generic;

List<int> sayiListesi= new List<int>();
    sayiListesi.Add(1);
    sayiListesi.Add(10);
    sayiListesi.Add(100);
    sayiListesi.Add(1000);

List<String> RenkListesi=new List<string>();
    RenkListesi.Add("Kırmızı");
    RenkListesi.Add("Mor");
    RenkListesi.Add("Yeşil");

Console.WriteLine(sayiListesi.Count);
Console.WriteLine(RenkListesi.Count);

foreach (var item in sayiListesi)
    Console.WriteLine(item);
foreach (var item in RenkListesi)
    Console.WriteLine(item);

sayiListesi.ForEach(sayi=>Console.WriteLine(sayi));
RenkListesi.ForEach(renk=>Console.WriteLine(renk));

Console.WriteLine("-----------Elemena Çıkarma---------------");
sayiListesi.Remove(2);
RenkListesi.Remove("Kırmızı");
sayiListesi.RemoveAt(3);

sayiListesi.ForEach(sayi=>Console.WriteLine(sayi));
RenkListesi.ForEach(renk=>Console.WriteLine(renk));

  Console.WriteLine("-------Liste İçerisinde Arama-------------");

        if (sayiListesi.Contains(10))
        {
        Console.WriteLine("Sayi Bulundu");  
        }

        Console.WriteLine(RenkListesi.BinarySearch("Yeşil"));

  Console.WriteLine("----------Diziyi Listeye Çevirme--------");

        string[] hayvanlar={"kedi","köpek","inek"};
        List<string> hayvanlistesi=new List<string>(hayvanlar);

    Console.WriteLine("---------Listeyi Temizleme -----------");

        hayvanlistesi.Clear();

    Console.WriteLine("----Liste İçerisinde Nesne Tutmak-----");
    
    List<Kullanıcılar> kullanıcıListesi=new List<Kullanıcılar>();
    Kullanıcılar kullanıcı1=new Kullanıcılar();
    kullanıcı1.Isim="melike";
    kullanıcı1.Soyisim="tutkun";
    kullanıcı1.Soyisim="22";

    Kullanıcılar kullanıcı2=new Kullanıcılar();
    kullanıcı2.Isim="hazal";
    kullanıcı2.Soyisim="tutkun";
    kullanıcı2.Soyisim="20";

    kullanıcıListesi.Add(kullanıcı1);
    kullanıcıListesi.Add(kullanıcı2);

    List<Kullanıcılar> yeniListe=new List<Kullanıcılar>();
    yeniListe.Add(new Kullanıcılar(){
        Isim="Deniz",
        Soyisim="Tutkun",
        Yas="28"
    });
    foreach (var item in kullanıcıListesi)
    {
        Console.WriteLine("Kullanıcı Adı:"+item.Isim);
        Console.WriteLine("Kullanıcı Soyadı:"+item.Soyisim);
        Console.WriteLine("Kullanıcı Yaş:"+item.Yas);
    }
    public  class Kullanıcılar
    {
        private string isim;
        private string soyisim;
        private string yas;


        public string Isim { get => isim ; set=> isim =value; }
        public string Soyisim { get => soyisim ; set=> soyisim =value; }
        public string Yas { get => yas ; set=> yas =value; }
    }
    
