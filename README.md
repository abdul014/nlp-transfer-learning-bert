# 🧠 NLP Transfer Learning with BERT (Bahasa Indonesia)

Eksperimen ini membahas konsep **Transfer Learning** dalam konteks *Natural Language Processing (NLP)*, dengan fokus pada penerapan model **BERT berbahasa Indonesia** untuk memahami teks, analisis sentimen, dan klasifikasi tugas berbasis bahasa.

---

## 📘 Apa itu Transfer Learning?

**Transfer Learning** adalah teknik pembelajaran mesin yang memanfaatkan pengetahuan yang telah diperoleh dari satu domain atau tugas untuk meningkatkan kinerja pada domain atau tugas lain yang berbeda namun masih terkait.  
Dalam konteks NLP, hal ini memungkinkan model seperti **BERT**, yang telah dilatih pada korpus teks besar, untuk digunakan kembali dan di-*fine-tune* pada dataset baru yang lebih kecil dan spesifik.

<p align="center">
  <img src="https://miro.medium.com/max/2000/0*Cf4ymGKtghF3W4um" width="600"/>
</p>

### ⚙️ Inti dari Transfer Learning:
- Model yang telah **dilatih sebelumnya (pre-trained)** digunakan kembali pada dataset baru.
- Menghemat waktu, data, dan sumber daya komputasi.
- Hasil pelatihan biasanya lebih stabil dan akurat dibanding model yang dilatih dari nol.

---

## 🔍 Konsep Utama

### 🧩 Traditional ML vs Transfer Learning
<p align="center">
  <img src="https://miro.medium.com/max/1400/1*b4GiiiIgxhfd3pUd86ZUuw.png" width="600"/>
</p>

Pada *traditional machine learning*, setiap model dilatih dari awal untuk tugas tertentu.  
Sedangkan pada *transfer learning*, model memanfaatkan **pengetahuan lama** (knowledge transfer) untuk mempercepat dan memperkuat proses pembelajaran baru.

---

## 🧠 Pre-Trained Model (BERT Indonesia)

Model **BERT (Bidirectional Encoder Representations from Transformers)** telah dilatih pada korpus teks Bahasa Indonesia berukuran besar untuk memahami konteks semantik dan sintaksis.  
Beberapa model populer yang digunakan dalam proyek ini antara lain:

| Model Name | Link |
|-------------|------|
| `bert-base-indonesian-522M` | [HuggingFace Link](https://huggingface.co/cahya/bert-base-indonesian-522M) |
| `indonesia-bert-sentiment-classification` | [HuggingFace Link](https://huggingface.co/mdhugol/indonesia-bert-sentiment-classification) |
| `IndoBERT` | [IndoLEM Link](https://indolem.github.io/IndoBERT/) |

---

## 💻 Implementasi di Python

Eksperimen ini menggunakan pustaka **Transformers** dari HuggingFace dengan pipeline klasifikasi teks sebagai dasar implementasi.  
Langkah umum penerapan meliputi:

1. Memuat *pre-trained model* (mis. `bert-base-indonesian-522M`)  
2. Melakukan *tokenization* terhadap data teks  
3. *Fine-tuning* model terhadap dataset lokal  
4. Mengevaluasi performa model terhadap metrik akurasi dan F1-score  

```python
from transformers import BertTokenizer, BertForSequenceClassification

tokenizer = BertTokenizer.from_pretrained("cahya/bert-base-indonesian-522M")
model = BertForSequenceClassification.from_pretrained(
    "cahya/bert-base-indonesian-522M",
    num_labels=3
)
```
---

## 🚀 Eksperimen Langsung di Google Colab

Untuk melihat cara kerja model BERT dalam analisis teks dan implementasi lainnya, silakan kunjungi tautan berikut:

🔗 [Jalankan di Google Colab](https://colab.research.google.com/github/abdul014/nlp-transfer-learning-bert/blob/main/Aplikasi%20BERT%20untuk%20NLP.ipynb)

<p align="center">
  <img src="https://github.com/abdul014/nlp-transfer-learning-bert/blob/main/show%20code%201.gif?raw=true" width="600" alt="Demo BERT in Colab"/>
</p>

> 📊 Gambar di atas memperlihatkan hasil implementasi model BERT untuk tugas analisis sentimen dan klasifikasi teks.

---

## ✍️ Disusun Oleh
**Abd Rahman**  
_From Komunitas EraNusaData_  
Magister Statistika dan Sains Data, IPB University  
📧 [LinkedIn](https://linkedin.com/in/abd-rahman-ysf)


