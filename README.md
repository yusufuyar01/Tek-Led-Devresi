# Tek Led Devresi

Bu proje, Arduino kullanarak bir LED'i belirli aralıklarla yakıp söndürmeyi amaçlar.

## İçindekiler

- [Açıklama](#açıklama)
- [Gereksinimler](#gereksinimler)
- [Kurulum](#kurulum)
- [Kullanım](#kullanım)
- [Kod Açıklaması](#kod-açıklaması)

## Açıklama

Bu proje, Arduino platformunda basit bir LED kontrol uygulamasını göstermektedir. Projede, bir LED Arduino'nun 8. pinine bağlanır ve belirli bir süre boyunca yanıp söndürülür. Bu, temel Arduino programlama ve elektronik kontrol kavramlarını anlamak için harika bir başlangıç noktasıdır.

## Gereksinimler

- Arduino kartı (Örneğin, Arduino Uno)
- 1 adet LED
- 1 adet 220 ohm direnç (LED'i korumak için)
- Jumper kabloları
- Arduino IDE (En son sürümü önerilir)

## Kurulum

1. Arduino IDE'yi bilgisayarınıza indirin ve kurun.
2. LED'i Arduino'nun 8. pinine bağlayın. LED'in uzun bacağını (anot) 8. pine, kısa bacağını (katot) ise bir 220 ohm direnç üzerinden GND'ye bağlayın.
3. Jumper kabloları kullanarak bağlantıları tamamlayın.
4. Arduino IDE'de, "Araçlar" menüsünden Arduino kartınızı ve portunuzu seçin.
5. Aşağıdaki kodu Arduino IDE'ye kopyalayın ve yükleyin.  
  ![Image](https://github.com/user-attachments/assets/41a2e45d-7635-4add-abf2-3a997702318f)

## Kullanım

Kod yüklendikten sonra, LED belirli aralıklarla yanıp sönecektir. Kodda yer alan `delay()` fonksiyonu ile yanıp sönme aralıklarını değiştirebilirsiniz.

## Kod Açıklaması

```c++
int led = 8; // LED'in bağlı olduğu pin

void setup() {
  pinMode(led, OUTPUT); // 8. pini çıkış olarak ayarla
}

void loop() {
  digitalWrite(led, HIGH); // LED'i yak
  delay(1000); // 1 saniye bekle

  digitalWrite(led, LOW); // LED'i söndür
  delay(1000); // 1 saniye bekle
}
