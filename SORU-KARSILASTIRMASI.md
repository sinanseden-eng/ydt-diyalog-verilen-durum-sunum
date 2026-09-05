# Kitap ve sunum soru karşılaştırması

İncelenen kaynak: Kullanıcının yüklediği `Diyalog-Verilen Duruma Uygun Cümle.pdf`.
PDF: 75 sayfa; basılı kitap sayfaları 575-649.
Sunum: `sinanseden-eng/ydt-diyalog-verilen-durum-sunum`, `index.html`.
Karşılaştırılan kaynak dosyanın GitHub blob kimliği: `67fd3d8caed8bf20a759fe91766cad4af127164d`.

## Sonuç

Sayılar ve soru içerikleri örtüşmüyor. Kitapta 185 test sorusu ve konu anlatımında 19 örnek soru, toplam 204 soru bulunuyor. Sunumun Deneme bölümünde 24 farklı özgün soru var.

| Soru türü | Kitaptaki test soruları | Anlatımdaki örnekler | Kitap toplamı | Sunumun Deneme bölümü |
| --- | ---: | ---: | ---: | ---: |
| Diyalog Tamamlama | 125 | 14 | 139 | 12 |
| Verilen Duruma Uygun Cümle | 60 | 5 | 65 | 12 |
| Toplam | 185 | 19 | 204 | 24 |

Salt sayısal fark 180'dir; ancak bunu "180 kitap sorusu eksik" olarak okumamak gerekir. Sunumun 24 sorusuyla kitap soruları arasında birebir eşleşme tespit edilmedi. Kitap sorularının sunuma aktarılmış olduğu doğrulanamadı. Mevcut kod da 24 soruyu bu sayfa için yazılmış özgün sorular olarak tanımlıyor.

Sunumdaki 16 İşlev Lab ifadesi ek bir sınıflandırma etkinliğidir; 24 soruluk Deneme sayısına dahil değildir. Sunumda 6 diyalog bulunur ve her diyalog iki boşluk sorusuna bağlanır: toplam 12 diyalog sorusu.

## Test ve sayfa dökümü

| Bölüm | PDF sayfaları | Basılı kitap sayfaları | Soru numaraları | Sayı |
| --- | --- | --- | --- | ---: |
| Diyalog konu anlatımı örnekleri | 1-10 | 575-584 | Numarasız örnekler | 14 |
| Diyalog Test 1 | 11-16 | 585-590 | 1-25 | 25 |
| Diyalog Test 2 | 17-22 | 591-596 | 1-25 | 25 |
| Diyalog Test 3 | 23-29 | 597-603 | 1-25 | 25 |
| Diyalog Test 4 | 30-36 | 604-610 | 1-25 | 25 |
| Diyalog Test 5 | 37-47 | 611-621 | 1-25 | 25 |
| Durum konu anlatımı örnekleri | 48-52 | 622-626 | Numarasız örnekler | 5 |
| Durum Test 1 | 53-57 | 627-631 | 1-20 | 20 |
| Durum Test 2 | 58-65 | 632-639 | 1-20 | 20 |
| Durum Test 3 | 66-75 | 640-649 | 1-20 | 20 |
| Toplam | 1-75 | 575-649 | | 204 |

## Konu anlatımındaki örneklerin sayımı

| Tür | PDF sayfası | Basılı sayfa | Yeni örnek soru sayısı |
| --- | ---: | ---: | ---: |
| Diyalog | 1 | 575 | 1 |
| Diyalog | 2 | 576 | 1 |
| Diyalog | 3 | 577 | 1 |
| Diyalog | 4 | 578 | 2 |
| Diyalog | 5 | 579 | 2 |
| Diyalog | 6 | 580 | 1 |
| Diyalog | 7 | 581 | 2 |
| Diyalog | 8 | 582 | 2 |
| Diyalog | 9 | 583 | 1 |
| Diyalog | 10 | 584 | 1 |
| Durum | 48 | 622 | 0 |
| Durum | 49 | 623 | 2 |
| Durum | 50 | 624 | 1 |
| Durum | 51 | 625 | 1 |
| Durum | 52 | 626 | 1 |

Açıklama veya çeviri amacıyla tekrar basılan seçenekler ikinci soru olarak sayılmadı. Testlerdeki her numaralı soru ayrı bir soru birimi olarak sayıldı.

## Karşılaştırma yöntemi ve sınırı

PDF görüntülerden oluştuğu için 75 sayfanın tamamına OCR uygulandı. Test başlıkları, numara aralıkları ve örnek soruların sayfa yerleşimleri kontrol edildi. Sunumun QUESTIONS ve DLGS verileri JavaScript ile okundu. Tüm seçenek metinleri PDF'nin OCR metniyle karşılaştırıldı; uzun ortak seçenek ifadeleri veya aynı soru setine işaret eden bir eşleşme bulunmadı. OCR, tarama ve noktalama hataları içerebilir; bu yüzden sonuç "birebir eşleşme tespit edilmedi" biçiminde ifade edilmiştir.

Bu pakete kitaptaki soru metinleri veya sayfa görüntüleri topluca eklenmedi. Paket mevcut 24 özgün soruyu korur. Kitabın tüm soru içeriğinin sunumda bulunması hedefi henüz karşılanmış değildir.

## Teknik düzeltmeler

- İşlev Lab'ın karıştırılmış ifade sırası, geçerli konumu ve son seçimi birlikte kaydedilir.
- Yenileme sonrası cevap kilidi ve geri bildirim geri yüklenir; aynı ifadeye tekrar cevap verilerek puan artırılamaz.
- İkinci ve sonraki turlarda doğru sıradan devam edilir.
- Bilinmeyen soru kimlikleri, geçersiz seçenek indeksleri, bozuk işaretler ve geçersiz sayaçlar yüklenirken ayıklanır.
- Geçerli eski deneme cevapları ve işaretler korunur. Eski sürüm ifade sırasını hiç kaydetmediği için bu eski sıra geri getirilemez; yeni sürümden itibaren sıra saklanır.
- Soru içeriği değiştiğinde eski cevapların farklı sorulara uygulanması önlenir.
- Veri blokları eksik yüklenirse önceki kaydın üzerine yazılmaz.
- Tarayıcı kayıt yazmayı reddederse kullanıcıya görünür bir mesaj gösterilir.
- Deneme seçenekleri gerçek düğmelere dönüştürülür; Tab, Enter ve Boşluk ile seçim yapılabilir. İşaretleme düğmesi ayrı tutulur.
- Seçim ve işaretleme durumları erişilebilirlik özelliklerine yansıtılır; klavye odağı görünür hale getirilir.
- Küçük ekranlar için menü ve seçenek düzenine uyarlamalar eklenir.
- Yanlış karakterler ve iki kısa Türkçe ifade düzeltilir.

## Doğrulama ve yayın durumu

Altı JavaScript bloğu sözdizimi kontrolünden geçti. Yenileme, tek puanlama, tur devamı, bozuk kayıt, kayıt hatası, veri değişikliği, ayrı cevap düğmeleri ve eksik veri sırasında eski kaydı koruma dahil 15 davranış kontrolü geçti. Kontroller gerçek uygulama işlevlerini Node.js içinde çalıştırdı; DOM ve tarayıcı deposu testte taklit edildi. 24 deneme sorusunun metinleri ve cevapları değişmedi.

Tarayıcı ortamı yerel kopyayı açmayı engellediği için tam tarayıcı etkileşimi, mobil görünüm ve yazdırma çıktısı görsel olarak doğrulanamadı.

GitHub güncellemesi 403 "Resource not accessible by integration" hatasıyla reddedildi. Depodaki dosya ve canlı yayın bu işlemle güncellenmedi. Düzeltilmiş index.html bu paketin içindedir.
