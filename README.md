# Anlık Cache Silme 

PHP ile yaptığımız altyapılarda son yapılan işlemin güncellenmesini zaman zaman göremeyebiliriz. Web tarayıcılar, hızlı işlem yapabilmek için sitelerin ön belleklerini kullanırlar ve verileri tutarlar, böylece biz bir defa daha aynı adrese girdiğimizde hızlıca açılır. 

Örneğin sürekli güncellenen haber sitelerinde bu işlem nasıl yapılıyor? Yani tarayıcımızın ön belleğine web sitesinin kaydedilmemesi için ne yapıyorlar?  Web sayfalarının başlarına ön belleğin tutulmaması için ekstra kod ekliyorlar.

Kullanımı : 

- header.tpl , header.php , header.html Yani Kısacası Başlıkların Her Sayfada Bulunduğu Dosyamızın İçersine Şu Kodları Ekliyoruz.


- header("Cache-Control: no-store, no-cache, must-revalidate, max-age=0");
header("Cache-Control: post-check=0, pre-check=0", false);
header("Pragma: no-cache");
