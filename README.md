# Kredi Kartı Onay Tahmini

Bu proje, Kaggle'dan alınan iki farklı veri setini birleştirerek kredi kartı başvurularının onaylanıp onaylanmayacağını tahmin etmeyi amaçlar. Makine öğrenimi teknikleri kullanılarak müşterilerin demografik, finansal ve geçmiş kredi bilgilerinden yararlanılmıştır.

---

## Proje Özeti

- **Amaç**: Kredi kartı başvurularının onaylanma veya reddedilme durumunu tahmin etmek.
- **Veri Kaynağı**: Kaggle
- **Yaklaşım**:
  - Veri temizleme ve ön işleme
  - Keşifçi veri analizi (EDA)
  - Makine öğrenimi modelleme
  - Dengesiz sınıflar için veri dengeleme

---

## Veri Seti Detayları

### 1. **Müşteri Bilgileri Veri Seti**
| **Sütun Adı**         | **Açıklama**                       |
|------------------------|------------------------------------|
| ID                    | Müşteri kimlik numarası            |
| CODE_GENDER           | Cinsiyet                          |
| FLAG_OWN_CAR          | Araba sahibi olup olmama durumu   |
| FLAG_OWN_REALTY       | Mülk durumu    |
| CNT_CHILDREN          | Çocuk sayısı                      |
| NAME_INCOME_TYPE      | Gelir kategorisi                       |
| NAME_EDUCATION_TYPE   | Eğitim seviyesi                   |
| NAME_FAMILY_STATUS    | Medeni durum                      |
| NAME_HOUSING_TYPE     | Yaşam Biçimi                       |
| DAYS_BIRTH            | Doğumdan itibaren geçen gün sayısı |
| DAYS_EMPLOYED         | İşe Başlama Tarihi                |
| FLAG_MOBIL            | Telefonu var mı                      |
| FLAG_WORK_PHONE      | İş telefonu var mı                   |
| OCCUPATION_TYPE       | Meslek türü                       |
| CNT_FAM_MEMBERS       | Aile üye sayısı                   |

### 2. **Kredi Geçmişi Veri Seti**
| **Sütun Adı**     | **Açıklama**                                 |
|--------------------|---------------------------------------------|
| ID                | Müşteri kimlik numarası                    |
| MONTHS_BALANCE    |Rekor Ay           |
| STATUS            | Kredi ödeme durumu                         |

---

## Kullanılan Araçlar ve Teknolojiler

- **Programlama Dili**: Python
- **Kütüphaneler**:
  - Pandas
  - NumPy
  - Matplotlib
  - Seaborn
  - Scikit-learn
  - Imbalanced-learn (SMOTE için)
- **Makine Öğrenimi Modelleri**:
  - Decision Tree
  

---

## Adımlar

### 1. Veri Ön İşleme
- İki veri seti `ID` sütunu üzerinden birleştirildi.
- Eksik değerler temizlendi.
- Kategorik veriler sayısal formata dönüştürüldü.

### 2. Keşifçi Veri Analizi (EDA)
- Müşteri gelir ve aile yapısına göre analizler yapıldı.
- Kredi ödeme durumlarının dağılımı incelendi.
- Standard Scaler

### 3. Veri Dengeleme
- Veri setinde "onaylandı" ve "onaylanmadı" sınıfları dengesiz olduğundan, **SMOTE** kullanıldı.

### 4. Modelleme
 **Decision Tree**, ve karşılaştırıldı.
- Performans metrikleri:
  - Doğruluk (Accuracy)
  - Hassasiyet (Precision)
  - Duyarlılık (Recall)
  - F1 Skoru


---

## Kurulum

Projeyi çalıştırmak için aşağıdaki adımları izleyin:

1. Bu projeyi klonlayın:
   ```bash
   git clone https://github.com/beyzanrgülec/kredi-karti-onay-tahmini.git

