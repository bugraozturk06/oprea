# OPREA — Tek Sayfalık Tanıtım Metni
*Rev 1.0 · 02.10.2026 · Kullanım: tanıtım filmi ve pazarlama üretimlerine kaynak girdi. Tüm sayılar mühür defterinden; abartı içermez.*

## OPREA nedir?
OPREA, küçük ve orta ölçekli üreticiler için geliştirilmiş bir **kapasite planlama yazılımıdır**. Şirketin zaten elinde olan Excel verilerinden (ürünler, reçeteler, kaynaklar, stoklar, açık siparişler, maliyetler) yola çıkar ve matematiksel optimizasyonla — yapay zekâ tahmini değil, kanıt üreten yöneylem araştırması modeliyle — önümüzdeki aylara ait üretim, satın alma ve teslimat planını hesaplar. Çıktısı bir öneri listesi değil, hesabı sorulabilir bir plandır: hangi üründen ne zaman ne kadar üretileceği, hangi kaynağın ne kadar dolacağı, hangi siparişin ne zaman karşılanacağı ve karşılanamayanın neden karşılanamadığı.

## Hangi derdi çözer?
KOBİ'lerde plan çoğunlukla tecrübeyle ve Excel'de elle yönetilir. Bu, işler rahatken görünmez; sıkışınca pahalıdır: darboğazlar geç fark edilir, fazla mesai plansız kullanılır, kıt hammadde yanlış siparişe gider, teslim tarihleri kayar. OPREA bu kararların tamamını — yüzlerce sipariş, onlarca ürün, kapasiteler, alternatif rotalar ve fazla mesai — **tek seferde, birlikte** düşünür ve toplam maliyeti en küçükleyen planı bulur.

## Nasıl çalışır? (üç adım)
1. **Veri kapısı:** Standart Excel şablonu doldurulur (ilk hazırlık birkaç saat sürer). Her satırın hesabı tutulur; bozuk veri, hücre adresi ve düzeltme tarifiyle koşuyu durdurur. Hiçbir satır sessizce kaybolmaz, hiçbir değer sessizce düzeltilmez.
2. **Çözüm:** Model, planlama ufkunun tamamını (örnek sette 87 gün, 400 sipariş, 99 bin karar değişkeni) dakikalar içinde çözer. İki planlama modu (hızlı Kaba plan / birim-hassas Detaylı plan) ve sekiz ayrı hedef sunar: toplam maliyet, karşılanamayan sipariş sayısı, teslimat oranı, gecikme, fazla mesai ve benzerleri — öncelik şirketindir.
3. **Rapor:** Kapasite ısı haritası, üretim/satın alma planı, sipariş karşılama, gecikme ve kayıp raporları. Karşılanamayan her sipariş için sistem gerekçe gösterir; kıt kaynağın hangi siparişe neden ayrıldığı izlenebilir.

## Neden güvenilir?
- **Çift çözücü:** Aynı model hem ticari (Gurobi) hem ücretsiz (HiGHS) çözücüyle koşturulur; kritik sonuçlar iki bağımsız yolla çapraz doğrulanır. Ücretsiz kademede ek lisans ücreti yoktur.
- **Kanıt disiplini:** 1.100'ün üzerinde otomatik test; her referans senaryonun sonucu mühürlenir ve sürümden sürüme değişmediği denetlenir.
- **Şeffaflık:** Sistem hiçbir kararı gizlemez — okunan/atlanan satır mutabakatından kayıp gerekçesine kadar her adım görünürdür.

## Kanıtlanmış sonuç (örnek setler, elle-plan vekiline karşı)
- Gerçekçi demo setinde: **maliyet −%13,7, teslimat oranı +5,7 puan.**
- Darboğazlı sıkışık fabrika setinde: **maliyet −%29,7, sipariş karşılama %88,8 → %98,8.** Kazanç, fabrika sıkıştıkça büyür — en çok ihtiyaç duyulan yerde en çok kazandırır.
- Aynı sette model, senaryoyu kurgulayan mühendisin sezgisini bile düzeltti: kıt hammaddeyi, kayıp maliyeti gerçekte daha yüksek olan ürüne kendisi ayırdı — gerekçesiyle.

## Tek cümlelik kapanış
**OPREA: Excel'inizden başlayan, kanıtıyla konuşan kapasite planlama.**

---
*Film/metin kullanım notu: sayılar her zaman "örnek set" ibaresiyle verilir ve genel vaat gibi sunulmaz; kıyas tabanı elle-planlama vekilidir (EDD kuralı); ürün görüntülerinde gerçek koşum ekranları kullanılır, taslak/mock-up kullanılmaz.*
