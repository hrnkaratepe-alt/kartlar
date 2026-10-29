# kartlar

Telefonda çalışan, başlangıçtan ileri seviyeye İngilizce öğrenme uygulaması.

## Özellikler

- **Seviyeler:** A1 (Başlangıç) → A2 (Temel) → B1 (Orta) → B2 (Orta-üstü) → C1 (İleri)
- **Kelimeler:** Her seviyede sık kullanılandan seyreğe sıralı kelimeler. Her kelimede Türkçe anlam, Türkçe harflerle okunuş, örnek cümle ve çevirisi var.
- **Cümleler:** Konulara ayrılmış günlük konuşma cümleleri (selamlaşma, alışveriş, yol sorma…)
- **Dilbilgisi:** Her seviyenin konuları Türkçe anlatım, kalıplar, örnekler ve anında geri bildirim veren alıştırmalarla
- **Seviye önerisi:** Bir seviyedeki kelimelerin %80'ini öğrenince sonraki seviye önerilir
- Sesli dinleme (normal / yavaş), otomatik okuma
- Cümlelerdeki her kelimeye dokununca anlamı, okunuşu ve sesi (tüm seviyelerin kelimeleri, düzensiz fiiller ve kısaltmalar)
- **Hafıza kartı:** Aynı kelimeye ikinci kez dokununca açılır. Kulağa benzeyen Türkçe bir anahtar kelime (anahtar kelime yöntemi), kısa komik bir hikaye, emoji ve hikayeyi Türkçe sesle okuma düğmesi içerir. Şimdilik en sık kullanılan 300 kelime için var (`data/hafiza.json`).
- Bilmediğin kartları daha sık gösteren tekrar sistemi (Leitner kutuları)
- Günde 20 kartlık hedef ve 🔥 seri sayacı
- İlerleme telefonun tarayıcısında saklanır

## İçerik

| Seviye | Kelime | Cümle | Dilbilgisi dersi |
|---|---|---|---|
| A1 · Başlangıç | 798 | 98 | 15 (82 alıştırma) |
| A2 · Temel | 876 | 70 | 15 (80 alıştırma) |
| B1 · Orta | 1025 | 60 | 14 (74 alıştırma) |
| B2 · Orta-üstü | 1033 | 44 | 12 (60 alıştırma) |
| C1 · İleri | 1246 | 40 | 12 (62 alıştırma) |
| **Toplam** | **4978** | **312** | **68 (358 alıştırma)** |

## Çalıştırma

İçerik `data/` klasöründeki JSON dosyalarından yüklendiği için uygulama bir web adresinden açılmalıdır:

- **GitHub Pages:** Depo ayarlarından Pages'i açman yeterli; telefondan adrese girip "Ana ekrana ekle" diyebilirsin.
- **Bilgisayarda:** Klasörde `python3 -m http.server` çalıştırıp `http://localhost:8000` adresini aç.

## İçerik dosyaları

- `data/seviyeler.json`: uygulamadaki seviyelerin listesi
- `data/a1.json`, `data/a2.json`, …: her seviyenin içeriği
  - `kelimeler`: `en`, `tr`, `ok` (okunuş), `ornek`, `ornekTr`
  - `cumleler`: `konu`, `en`, `tr`, `ok`, isteğe bağlı `ornek`, `ornekTr`
  - `dersler`: `id`, `baslik`, `ozet`, `aciklama` (paragraflar, `**kalın**` desteklenir), `kaliplar`, `ornekler`, `alistirmalar` (`soru` içinde boşluk `___`, `secenekler`, `dogru` = doğru şıkkın sırası, `aciklama`)

İlerleme kartın İngilizcesiyle kaydedildiği için bir kelime ya da cümle tüm seviyelerde yalnızca bir kez geçer.
