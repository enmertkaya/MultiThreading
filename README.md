Multi-thread Programlama
Bir işin/işlerin birden fazla thread tarafından gerçekleştirilmesidir. Örneğin, 5 adet .csv uzantılı metin dosyasını senkron okuyacağımızı düşünelim. Her bir .csv uzantılı dosyayı okumak ortalama 50 saniye sürse, işlemin tamamlanması kaba hesap, 50 saniye x 5 dosya = 250 saniye⌛sürecektir. Ancak multi-thread programlama yardımıyla 5 adet .csv uzantılı dosyayı 5 farklı thread kullanarak okursanız ortalama 50 saniye içerisinde tüm işlem tamamlanacaktır.
Mail gönderme uygulaması ve multithread mantığını içeren bir uygulamadır.Smtp provider ve mail objemizi yarattık.MailTask sınıfı icerisine INotifyPropertyChanged interface ini ekledik.Grid üstünde etkilidir.
![mt1](https://github.com/enmertkaya/MultiThreading/assets/151652097/e9e90df0-a428-453b-a8a9-34fe2f498a75)
60 sn de bir calısan bir uygulamadır.Veritabanından gönderilmesi gereken verileri okuyup providerlar aracılığı ile gönderen bir uygulamadır.
![mt2](https://github.com/enmertkaya/MultiThreading/assets/151652097/63156e12-6e84-4e16-85cc-26e83a494b28)
Smtp ve GoogleMail ayrı bir thread üzerinden çalışıyor ve birbirlerini beklemiyolar(farklı sınıflar)..Burada aynı islemi birden fazla yapabiliyor olmak gibi bir durum söz konusu.Burada birbirinden bagımsız 2 tane islem var. Bu islemlerin icinde threadler var.
![mt3](https://github.com/enmertkaya/MultiThreading/assets/151652097/52eee73f-128a-4615-baec-1e506c096d49)
