
# CloudFile
Amazon S3 - Google Cloud Dosya İşlemleri
Programlama dili C#
Kullanılan Veritabanı MongoDB ( MongoDB, proje içerisinde, dosyaya unique bir id atamak amacıyla kullanılmıştır. )

Cloud File projesi, bir şirketin kendi iş süreçleri içerisinde, depoladıkları ve kullandıkları dosyaların kendi servisleri aracılığıyla Google Cloud ve Amazon S3 veya her ikisine birden -both- yükleme / silme / indirme işlemlerinin yapılabilmesi amacıyla gerçekleştirilmiş bir projedir.

Bahsedilen işlemler, öncelikle dosyanın yükleme isteği yapılmasıyla başlatılır. Bu istek ile birlikte öncelikle dosya byte byte okunarak içeriğinin ne olduğuna karar verilir ve proje içerisinde bu uzantının yüklenmesine izin verilip verilmediğine göre kontrol gerçekleştirildikten sonra devam ettirilir. Belirtilen uzantılar arasından olan dosya öncelikle MongoDB'ye kaydedilir. Ardından istenilen rotaya göre ( Amazon S3 / Google / Both ) yükleme işlemi gerçekleştirilir. Bu dosya, kendi ismiyle değil, MongoDB 'de adına oluşturulan unique id ile kaydedilir. Örneğin; 3ad7d4f32gg743.jpg


*******************************************************************************************************************************************

Amazon S3 - Google Cloud File Operations
Programming language C #
Used Database MongoDB (MongoDB is used in the project to assign a unique id to the file.)

The Cloud File project is a project that allows a company to upload / delete / download files in their own business processes, stored and used by Google Cloud and Amazon S3 or both via their own services.

These processes are initiated by first requesting the upload of the file. With this request, first the file is read by byte and byte and it is decided what the contents are, and it is continued after the control is performed according to whether or not the extension is confirmed in the project. The file from the specified extensions is saved in MongoDB first. Then the upload is performed according to the desired route (Amazon S3 / Google / Both). This file is saved with the unique id created in MongoDB instead of its own name. For example; 3ad7d4f32gg743.jpg
