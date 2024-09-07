uygulamamızın kullandığı sql tablosu : 
CREATE TABLE `etiket` (
  `etiketID` int NOT NULL AUTO_INCREMENT,
  `urunBarkod` varchar(45) DEFAULT NULL,
  `urunIsim` varchar(45) DEFAULT NULL,
  `urunFiyat` decimal(18,2) DEFAULT NULL,
  `urunTur` varchar(45) DEFAULT NULL,
  `etiketIP` varchar(45) DEFAULT NULL,
  PRIMARY KEY (`etiketID`)
) ENGINE=InnoDB AUTO_INCREMENT=20 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;


Uygulamamız 2 ayrı sayfadan oluşmaktadır. biri sql girişinin yapıldığı diğeri ise kullanıcı dashboardının sunulduğu sayfadır.

kullanıcı girişi :
![image](https://github.com/user-attachments/assets/f4768547-7e99-4e30-89ea-171b0b3214da)

kullanıcı dashboardı :
![image](https://github.com/user-attachments/assets/4dac0010-2fec-4b9d-b420-d17e5ad6c073)


uygulamamızda değiştirebilen ve eklenen değerler arasında sadece urunBarkod, urunTur ve etiketIP değerleri vardır. bunun sebebi etiketID pk olduğu için auto increment olarak çalışmaktadır bu sayede otomatik şekilde eklenen etiketlere id değeri verilmektedir. urunFiyat ve urunIsim değerleri de urunBarkod değeri sayesinde api consumer tarafından atanmaktadır veya değiştirildi ise güncellenmesini sağlamaktadır.

