# Course 2 Week 2

 ## Geriye Yayılım(Backpropagation) Nedir?
 Daha öncesinde verilen başlangıç ağırlıkları ve sapmalar ile çıkış katmanına 'ileri' doğru giderdik. Bu sürece ileri yayılım denirdi ve burada bir değer hesaplanır. Hesaplanan değer ile gerçek değer arasındaki fark bir hata veya maliyet oluşturur ve Geriye Yayılım burada devreye girer. Bu hatanın geriye doğru katmanlara yayılması ve minimize edilmesi için oluşan sürece Geriye Yayılım denir. 

 Hatayı minimize etmek için maliyetimizin daha doğrusu maliyet fonksiyonumuzun ağırlıklara göre negatif gradyanını alırız. Gradyan dediğimiz fonksiyonumuzun her parametreye göre türevilerinin bir matrisi veya vektörüdür. Yönlü türev alınırken eğer değerimizi maksimize etmek istiyorsak bu yön olarak gradyan vektörü yönü alınır. Tam tersi minimize etmek için gereken ise sadece negatifini almak.

 O zaman bu maliyet fonksiyonumuzun bağlı olduğu parametrelere yani ağırlık ve sapmalara göre türev almamız gerektiğini biliyoruz. Ağırlık fonksiyonuna göre türevini ele alalım. Direkt olarak türevini alamayız çünkü ağırlığımız doğrudan maliyet fonksiyonumuza bağlı değildir. Maliyet fonksiyonumuz, aktivasyon fonksiyonun ve gerçek değer arasındaki farka, aktivasyon fonksiyonumuz, aktivaston fonksiyonumuzun içindeki z değeri yani katmandaki nöronların aktivasyon öncesi toplam girdisi ağırlığa, sapmaya ve aktivasyona bağlıdır. Görüldüğü üzere doğrudan ağırılığa bağlı değildir bu yüzden türevi alınırken zincir kuralı uygulanır. Önce maliyet fonksiyonun aktivasyona göre, aktivasyon fonksiyonunun z değerine göre z'nin de ağırlığa göre türevi alınır.
 
 ![Backpropagation](![alt text](image.png))