# Metro Ağ Projesi
Bu proje, bir metro ağının istasyonları ve hatları arasındaki bağlantıları modelleyen bir Python uygulamasıdır. Kullanıcılar, istasyonlar arasında en az aktarma veya en hızlı rota seçenekleriyle yolculuk yapabileceklerdir.

## Özellikler
İstasyonlar ve Hatlar: Farklı hatlarda bulunan istasyonlar tanımlanabilir.

Bağlantılar: İstasyonlar arasındaki süreler belirlenerek bağlantılar oluşturulabilir.

En Az Aktarmalı Rota: BFS algoritması kullanarak, iki istasyon arasındaki en az aktarmalı rotayı bulur.

En Hızlı Rota: A* algoritması kullanarak, iki istasyon arasındaki en hızlı rotayı ve toplam süreyi hesaplar.

## Kullanım
1. İstasyon Ekleme
```
metro.istasyon_ekle("K1", "Kızılay", "Kırmızı Hat")
```
2. Bağlantı Ekleme
```
metro.baglanti_ekle("K1", "K2", 4)  # Kızılay -> Ulus
```
3. En Az Aktarmalı Rota Bulma
```
rota = metro.en_az_aktarma_bul("M1", "K4")
```
4. En Hızlı Rota Bulma
```
rota, sure = metro.en_hizli_rota_bul("M1", "K4")
```
## Örnek Kullanım
Proje, MetroAgi sınıfının örneği oluşturularak, metrodaki istasyonlar arasında en az aktarma ve en hızlı rotaların bulunmasını sağlar.

## Örnek Çıktı:
En az aktarmalı rota: AŞTİ -> Kızılay -> Demetevler -> OSB
En hızlı rota (12 dakika): AŞTİ -> Kızılay -> Demetevler -> OSB

## Gereksinimler
Python 3.x

heapq ve collections modülleri