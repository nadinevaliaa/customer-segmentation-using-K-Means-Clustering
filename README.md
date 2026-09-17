# Customer Segmentation using K-Means Clustering

## Gambaran Umum Project

Project ini menerapkan algoritma **K-Means Clustering** untuk melakukan segmentasi pelanggan berdasarkan karakteristik perilaku pembelian. Pendekatan yang digunakan merupakan **unsupervised learning**, sehingga pelanggan dikelompokkan berdasarkan kemiripan karakteristik tanpa menggunakan label kelas yang telah ditentukan sebelumnya. Analisis berfokus pada karakteristik numerik pelanggan, yaitu usia, frekuensi pembelian, dan jumlah transaksi.

## Tujuan

- Mengidentifikasi kelompok pelanggan dengan karakteristik yang serupa.
- Menganalisis perbedaan perilaku pembelian antar kelompok pelanggan.
- Menentukan jumlah cluster yang sesuai menggunakan Elbow Method.
- Mengevaluasi hasil clustering menggunakan Silhouette Score.
- Menginterpretasikan karakteristik dari setiap segmen pelanggan.

## Dataset

Dataset yang digunakan adalah **Customer Shopping Behavior Dataset** yang diperoleh dari Kaggle.

| Informasi | Keterangan |
|---|---|
| Jumlah pelanggan | 3.900 |
| Jumlah atribut | 18 |
| Missing values | 0% |
| Sumber | Kaggle |

Fitur yang menjadi fokus dalam proses clustering:

- **Age**
- **Purchase Amount (USD)**
- **Frequency of Purchases**

## Metodologi

Alur analisis yang digunakan:

```text
Input Data
    ↓
Data Cleaning
    ↓
Feature Selection
    ↓
Feature Scaling
    ↓
Elbow Method
    ↓
K-Means Clustering
    ↓
3D Visualization
    ↓
Silhouette Score
    ↓
Cluster Interpretation
```

## Evaluasi

Kualitas hasil clustering dievaluasi menggunakan **Silhouette Score** dengan Optimal Number of Clusters = 4, yang mengukur tingkat kedekatan data terhadap cluster-nya dibandingkan dengan cluster lainnya.

| Metrik | Hasil |
|---|---:|
| Jumlah Cluster | 4 |
| Silhouette Score | 0.319 |

## Hasil Segmentasi

![3D Visualization](results/cluster_visualization(3D).png)

Berdasarkan hasil K-Means Clustering, pelanggan dikelompokkan menjadi empat segmen berdasarkan karakteristik usia, frekuensi belanja, dan nilai transaksi.

| Cluster | Profil Pelanggan | Karakteristik |
|---|---|---|
| Cluster 0 | Pelanggan Loyal Menengah | Usia dewasa menengah, frekuensi belanja relatif tinggi, dan nilai transaksi menengah |
| Cluster 1 | Pelanggan Low Engagement | Frekuensi belanja rendah dengan nilai transaksi relatif tinggi |
| Cluster 2 | Pelanggan Muda Impulsif | Usia relatif muda, frekuensi belanja rendah, dan nilai transaksi tinggi |
| Cluster 3 | Pelanggan Eksklusif Dewasa | Usia relatif lebih tua, frekuensi belanja rendah, dan nilai transaksi paling tinggi |

### Insight

- **Cluster 0** menunjukkan pola pembelian yang relatif konsisten dengan frekuensi belanja yang tinggi.
- **Cluster 1** memiliki frekuensi belanja rendah, tetapi nilai transaksi relatif tinggi.
- **Cluster 2** didominasi pelanggan muda dengan nilai transaksi tinggi dan frekuensi pembelian yang relatif rendah.
- **Cluster 3** memiliki nilai transaksi tertinggi dibandingkan cluster lainnya dengan frekuensi belanja yang relatif rendah.

Hasil ini merepresentasikan bahwa perbedaan antar segmen terutama terlihat pada **frekuensi pembelian dan nilai transaksi**.

### Tech Stack
- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
Google Colab
