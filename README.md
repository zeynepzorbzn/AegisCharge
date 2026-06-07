# AegisCharge 🛡️

**AegisCharge**, elektrikli araç şarj istasyonu (EVCS) altyapılarında operasyonel güvenlik zafiyetlerinin analiz edilmesi ve protokol manipülasyonlarının modellenmesi üzerine geliştirilmiş bir güvenlik araştırma projesidir.

## 🎯 Proje Amacı
EV şarj ekosistemi, **OCPP (Open Charge Point Protocol)** ve **ISO 15118** gibi endüstriyel haberleşme standartlarına dayanır. Bu proje;
* Şarj istasyonu ile merkezi yönetim sistemi (CSMS) arasındaki haberleşme süreçlerini incelemeyi,
* Yetkisiz erişim ve "man-in-the-middle" (MitM) saldırı senaryolarının nasıl tetiklenebileceğini anlamayı,
* Olası zafiyetleri Proof-of-Concept (PoC) seviyesinde belgeleyerek güvenlik açıklarını analiz etmeyi amaçlar.

## 🛠 Kullanılan Teknolojiler ve Araçlar
Proje geliştirme ve analiz süreçlerinde aşağıdaki teknolojiler kullanılmıştır:

* **Programlama Dili:** Python
* **Haberleşme Protokolleri:** OCPP (1.6/2.0.1) ve ISO 15118 (Plug & Charge) mimarisi
* **Siber Güvenlik & Analiz:** * Protokol manipülasyonu ve zafiyet tetikleme senaryoları
    * Trafik izleme ve PoC geliştirme scriptleri
* **Makine Öğrenmesi (Anomali Tespiti):**
    * `Scikit-learn` (Random Forest Regressor)
    * `Pandas` & `NumPy` (Veri işleme ve analiz)
* **Web & Servis:** `FastAPI` (Performans odaklı API yönetimi)
* **Model Dağıtımı:** `Pickle` (Model ve Scaler serileştirme)

## ⚠️ Uyarı ve Sorumluluk Reddi
Bu repo, **sadece eğitim ve araştırma amaçlıdır.** Burada yer alan kodlar, herhangi bir cihaz veya ağ üzerinde izinsiz kullanılamaz. Kullanıcı, yaptığı tüm testlerin yasal sorumluluğunun kendisine ait olduğunu kabul eder.

## 📂 İçerik Özeti
* `app.py`: Protokol manipülasyonu veya zafiyet tetikleme süreçlerini yöneten temel mantık.
* `rf_model.pkl / scaler.pkl`: Şarj istasyonu kullanım davranışlarındaki anormallikleri tespit etmek için eğitilmiş model.
* `temiz_veri_v4.csv`: Protokol mesajları ve sistem loglarından oluşan eğitim veri seti.

## 🔧 Kurulum ve Çalıştırma

1. **Güvenli bir sandbox ortamı oluşturun.**
2. Repoyu klonlayın:
   ```bash
   git clone [https://github.com/zeynepzorbzn/AegisCharge.git](https://github.com/zeynepzorbzn/AegisCharge.git)
