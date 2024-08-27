# Dijital Saat

Bu proje, HTML, CSS ve JavaScript kullanılarak oluşturulmuş basit bir dijital saat uygulamasıdır. Saat, `SS:DD:SS` formatında mevcut saati gösterir ve her saniye güncellenir.

## Proje Yapısı

- `index.html`: Dijital saatin HTML yapısını içeren ana dosya.
- `style.css`: Saati stilize etmek için kullanılan CSS dosyası.
- `script.js`: Saati güncelleme mantığını yöneten JavaScript dosyası (bu örnekte HTML dosyasına dahil edilmiştir).

## Nasıl Çalışır?

- Saat, JavaScript'in `Date` nesnesini kullanarak mevcut zamanı alır.
- Saat, dakika ve saniyeler çıkarılır ve ilgili `<span>` etiketlerinde görüntülenir.
- Zaman, `setInterval` fonksiyonu kullanılarak her saniye güncellenir.

## Kullanım

Bu dijital saati kullanmak veya değiştirmek için:

1. Bu depoyu klonlayın veya dosyaları indirin.
2. `index.html` dosyasını tarayıcınızda açarak saatin çalışmasını izleyin.
3. Saatin görünümünü değiştirmek için `style.css` dosyasını düzenleyin.


## Ekran Görüntüsü
![image](https://github.com/user-attachments/assets/c45b6150-c300-4a51-a51f-3968c83e4bac)

## Örnek

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Dijital Saat</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
<div class="hero">
    <div class="container">
        <div class="clock">
            <span id="hrs">00</span>
            <span>:</span>
            <span id="min">00</span>
            <span>:</span>
            <span id="sec">00</span>
        </div>
    </div>
</div>

<script>
    let hrs = document.getElementById("hrs");
    let min = document.getElementById("min");
    let sec = document.getElementById("sec");

    setInterval(()=>{
        let currentTime = new Date();
        hrs.innerHTML = (currentTime.getHours()<10?"0":"")+currentTime.getHours()
        min.innerHTML = (currentTime.getMinutes()<10?"0":"")+currentTime.getMinutes()
        sec.innerHTML = (currentTime.getSeconds()<10?"0":"")+currentTime.getSeconds()
    }, 1000);
</script>

</body>
</html>







