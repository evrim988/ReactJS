# REACT JS GEREKLİ KURULUMLAR VE NOTLAR

# KURULUM

* ilk olarak react.js çalıştırabilmek için bunu yayınlayacak ve kodları yorumlayacak bir sunucuya ihtiyaç var.
Ayrıca paket kurulumları için bir paket yöneticisine ihtiyaç bulunmaktadır.

* NodeJS tüm gerekli servis ve paket yönetim araçlarını içerisinde barındırmaktadır.

```link
kurulum linki 
---------------------
https://nodejs.org/en/download/package-manager
```
* nodeJS yüklenmesi bittiğinde terminal ekranına "node -v" yazdığımızda "v22.11.0" gibi bir çıktı alıyorsak ve;
yine terminal ekranına "npm -v" dediğimizde "10.9.0" gibi bir sonuç alıyorsak iki şekilde de kurulum tamamlanmış oluyor.

```bash
# node js kurulumunu kontrol etmek için
node -v

# paket yöneticisini kontrol etmek için
npm -v 
```

* reactJS uygulamalrını kurmak için ve dökümantasyonlar için aşağıdaki linkleri ziyaret ediniz.

```
https://react.dev/learn/start-a-new-react-project
https://create-react-app.dev/docs/getting-started
```
* JS doğası gereği tip güvenliği sağlamamaktadır, bu nedenle kodlarımızı daha güvenli ve yönetilebilir yapmak için projelerimizi TypeScript(TS) ile kuracağız ya da önceden standart olarak kurmuş isek ek olarak TS kurulumu ekleyerek TS haline getireceğiz.

```bash
#TS olmadan kurulum yapmak için yani JS
npx create-react-app uygulama-adi
```

```bash
# TypeScript destekli şekilde uygulamayı kurmak
npx create-react-app uygulama-adi --template typescript
```

```bash
# Örnek Proje
npx create-react-app ilkuygulama --template typescript

```

* DİKKAT!! kurulumlar ve başlatma işlmeleri için öncelikle terminal ekranına geçiniz. Burada hangi dizin içerisine projeyi atacak iseniz öncelikle o klasöre geçin.
>cd uygulamalarim

* sonra buraya oluşturmak istediğiniz proje komutunu giriyorsunuz.
> npx create-react-app ilkuygulama --template typescript

## Çalıştırmak - Uygulamayı başlatmak
uygulamayı başlatmak için "npm start" yeterlidir. Ancak,
uygulamanın başlaması için uygulama configlerini içeren 
package.json dosyasına gerek vardır. Eğer konum olarak uygulamanın dizininde
değilseni npm start dediğinizde hata verecktir.

ÖRN:
uygulamanızın paket yapısı şöyle olsun
-- REACTJS (Ana Klasör)
---IlkIslemler 
---- uygulamalarim
------ ilkuygulama (uygulama klasörü)

CMD: reactJS>Uygulamalarim>npm start
Hata verecektir. Çünkü konum olarak projenin içinde değilsin.
ÇÖZÜM:
uygulamanızın dizinine gitmek gerekir.
CMD: ReactJS>Uygulamalarim>cd ilkuygulama
CMD: ReactJS>Uygulamalarim>ilkuygulama>npm start

## Uygulamanın Portunu Değiştirmek

* Aşağıdaki şekille de kendinize uygun işletim sistemini seçerek port bilgisini güncelleyebilirsiniz.
Bu işlemi yapmak için package.json içerisinde ki scripts alanında değişiklik yapmalısınız.

```json

"scripts": {

    //default olarak çalışır 3000 portunu kullanır.
    // "start": "react-script start,
    //Windows için
    //"start": "set PORT=9990 && react-scripts start",
    // MACOS & farklı versiyonlar
    //yeni versiyon "start": "POST=9990 react-scripts start",
    //Eski versiyon MACOS = "start": "export PORT=9990 react-scripts start"

    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test",
    "eject": "react-scripts eject"
  }
```

npm start dediğimizde proje çalışır.
CTRL + C ile projeyi durdurmuş oluruz.

projeyi build almak için -> npm run build
