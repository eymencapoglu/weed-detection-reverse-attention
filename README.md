# Agricultural Weed Detection with ResNet-50 + Reverse Attention

*[English](#english) | [Türkçe](#türkçe)*

---

<a name="english"></a>
## English

### Overview
This project implements a PyTorch computer-vision classifier for **agricultural weed detection** (distinguishing broad-leaved dock / *Rumex obtusifolius* — *Geniş Yapraklı Labada* and *ridderzuring* — *Yabani Labada Otu*) by combining a **ResNet-50** backbone with a custom **`ReverseAttention`** module and 90-degree rotational data augmentation (`Random90Rotation`).

### Development Timeline & Process
- **Development Date:** June 11, 2026 (based on original notebook and output timestamps)
- **Process:** Built end-to-end in `Weed_Detection.ipynb`: automated dataset fetching via `kagglehub`, custom PyTorch `Dataset` & 90° rotation augmentation, custom `ReverseAttention` block on top of ResNet-50, 100-epoch Adam training (`lr = 1e-4`), confusion matrix evaluation (`confusion_matrix.png`), and Turkish-labeled 15-sample visual test predictions (`model_15_test_ciktisi_turkce.png`).
- **Excluded Weights:** The trained checkpoint (`resnet50_reverse_attention_weed.pth`, ~141.6 MB) was excluded because it exceeds GitHub's 100 MB file limit.

### Visual Results
- **Confusion Matrix:** `confusion_matrix.png`
- **Sample Test Predictions (Turkish Labels):** `model_15_test_ciktisi_turkce.png`

### Acknowledgments & Open-Source Credits
- **[Kaggle & `kagglehub`](https://www.kaggle.com/)** — Open-access Rumex / weed image dataset.
- **[PyTorch & Torchvision (ResNet-50)](https://pytorch.org/)** — Deep learning framework and pretrained backbone (He et al., CVPR 2016).
- **Reverse Attention Mechanism** — Inspired by Reverse Attention in medical/salient object networks (Chen et al., ECCV 2018; Fan et al., PraNet MICCAI 2020).
- **[Scikit-Learn](https://scikit-learn.org/)** & **[Seaborn](https://seaborn.pydata.org/)**.

---

<a name="türkçe"></a>
## Türkçe

### Genel Bakış
Bu proje, tarımsal görüntülerde **yabani ot tespiti** (*Rumex obtusifolius* / Geniş Yapraklı Labada ve *ridderzuring* / Yabani Labada Otu) için **ResNet-50** omurgası ile özel **`ReverseAttention`** modülünü birleştiren bir PyTorch sınıflandırma çalışmasıdır.

### Geliştirme Süreci ve Tarihçesi
- **Geliştirme Tarihi:** 11 Haziran 2026 (orijinal notebook ve çıktı tarihlerine göre)
- **Süreç:** `Weed_Detection.ipynb` içerisinde `kagglehub` ile veri indirme, 90 derecelik rastgele döndürme artırması (`Random90Rotation`), ResNet-50 + Ters Dikkat (`ReverseAttention`) mimarisi, 100 epoch eğitim, karmaşıklık matrisi (`confusion_matrix.png`) ve 15 örneklik Türkçe etiketli test çıktısı (`model_15_test_ciktisi_turkce.png`) uçtan uca geliştirildi.
- **Hariç Tutulan Ağırlık:** ~141.6 MB boyutundaki `resnet50_reverse_attention_weed.pth` dosyası GitHub'ın 100 MB dosya sınırını aştığı için hariç tutulmuştur.

### Açık Kaynak Teşekkürler ve Kaynaklar
- **[Kaggle & `kagglehub`](https://www.kaggle.com/)** — Açık erişimli yabani ot (Rumex) görüntü veri seti.
- **[PyTorch & Torchvision (ResNet-50)](https://pytorch.org/)** — Derin öğrenme altyapısı ve ResNet-50 omurgası.
- **Reverse Attention Yaklaşımı** — Ters dikkat (Reverse Attention) literatüründen (Chen vd., ECCV 2018; Fan vd., PraNet MICCAI 2020) esinlenilmiştir.