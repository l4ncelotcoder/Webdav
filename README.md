# Webdav
CVE-2009-1676 güvenlik bülteni ile Microsoft IIS 6.0 web sunucusunun dosya paylaşımı için kullandığı “Webdav” servisinde uzakdan kimlik doğrulamayı bypass eden bir zaafiyet bulunduğu duyuruldu.

Web sunucuda bulunan klasorlere ve dosyalara erişim için Windows Authentication gerektiren kimlik doğrulama unicode kullanılarak bypass edilebiliniyor.
Yetki dahilinde dosya okumak, dizin listelemek ve uzak sunucuya dosya yazmak (içerik eklemek) mümkün.

Bu makalede bu işlemin nasıl yapıldığı ve korunma yollarına değinilmiştir.

Aktif Webdav Servisinin Tespiti

IIS 5.0 da Webdav servisi varsayılan olarak açık gelir.IIS 6.0 sunucularda ise webdav servisi varsayılan olarak aktif değildir.

Genelde "Zambia" gibi gelişmemiş ülkelerin sitelerinde bulunan bu zafiyet ile site hacklemek kolay olsada, Hacklediğiniz siteler için taktir almazsınız çünkü çok basit bir açıktır.

![image](https://user-images.githubusercontent.com/78283095/224557901-b86718cc-e03d-4484-8e3d-9ee0c8774887.png)
