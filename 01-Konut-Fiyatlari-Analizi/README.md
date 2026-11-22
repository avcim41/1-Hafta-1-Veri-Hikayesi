# Proje 01 — Türkiye'de Nominal ve Reel Konut Fiyatları

**1 Hafta, 1 Veri Hikâyesi** serisinin ilk projesi.

## Araştırma sorusu
Konut fiyatlarındaki nominal artış enflasyondan arındırıldığında nasıl değişiyor?

## Veriler
- TCMB EVDS: Türkiye geneli Konut Fiyat Endeksi (KFE), aylık **Düzey**
- TÜİK Veri Portalı: Genel Tüketici Fiyat Endeksi (TÜFE), aylık **Endeks**
- İncelenen dönem: Ocak 2020 – Ekim 2026 (82 ay)

Resmî kaynaklar: https://evds3.tcmb.gov.tr/ ve https://veriportali.tuik.gov.tr/

## Çalıştırma
1. Ham Excel dosyalarını `data/konut_fiyat_endeksi.xlsx` ve `data/tufe.xlsx` adlarıyla yerleştirin.
2. `pip install -r requirements.txt` komutunu çalıştırın.
3. `konut_fiyat_analizi.ipynb` dosyasını Jupyter'da açıp tüm hücreleri sırasıyla çalıştırın.
4. Grafikler `visuals/` klasörüne kaydedilir.

## Bulgular (özgün notebook çıktıları)
- Nominal değişim: +%1.810,63
- Reel değişim: +%90,36
- Reel zirve: Haziran 2023
- Zirveden reel değişim: −%24,03
- Son 12 ay nominal / reel: +%21,15 / −%6,64

**Not:** Ham kaynak Excel dosyaları burada sağlanmadığından bu rakamlar yeniden hesaplanarak doğrulanmamıştır. Yayın öncesi resmî seri tanımlarını ve baz yılı değişikliklerini kontrol edin.

## Yöntem
KFE ve TÜFE endeksleri Ocak 2020 = 100'e normalize edilir. Reel KFE = (normalize KFE / normalize TÜFE) × 100. Yıllık değişimler 12 aylık gecikmeyle hesaplanır.

## Sınırlılıklar
Türkiye geneli endeksler bireysel konut getirisi değildir; bölgesel farklılıklar, kira, vergi ve işlem maliyetleri hesaba katılmaz.
