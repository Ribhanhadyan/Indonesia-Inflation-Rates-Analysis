## Indonesia Inflation Rate Analysis

### Background Problem

Inflasi adalah salah satu indikator penting dalam menilai kondisi ekonomi suatu negara, karena tingkat inflasi yang tinggi dan tidak stabil dapat berdampak negatif terhadap kesejahteraan sosial dan ekonomi masyarakat. Salah satu variabel yang sering digunakan dalam memahami dinamika inflasi adalah Produk Domestik Bruto (GDP). GDP mengukur total nilai barang dan jasa yang diproduksi oleh suatu negara, merupakan indikator yang mencerminkan tingkat aktivitas ekonomi secara keseluruhan. Oleh karena itu penting untuk memahami dan menganalisis bagaimana GDP mempengaruhi tingkat Inflasi.

### Dataset

Data yang digunakan bersumber dari kaggle

- https://www.kaggle.com/datasets/billycemerson/indonesian-inflation-and-gdp-data
- https://www.kaggle.com/discussions/accomplishments/477497#2655013

### Result

- Korelasi Inflasi dengan GDP: Dari analisis yang dilakukan, terlihat bahwa terdapat korelasi yang kuat antara inflasi Indonesia dengan GDP. Terutama pada periode krisis seperti tahun 1998-1999, ketika GDP Indonesia turun secara drastis dan diikuti oleh lonjakan inflasi yang signifikan. Hal ini menunjukkan hubungan erat antara penurunan GDP dan peningkatan inflasi pada masa krisis ekonomi.
- Korelasi Inflasi dengan Negara Lain: Korelasi inflasi Indonesia dengan negara-negara tetangga dan Amerika Serikat cenderung rendah atau sangat rendah. Hal ini menunjukkan bahwa inflasi Indonesia lebih dipengaruhi oleh faktor domestik daripada tren inflasi di negara-negara tetangga, termasuk Malaysia, Thailand, Filipina, dan Amerika Serikat. Oleh karena itu, data inflasi negara-negara lain tidak digunakan dalam analisis lebih lanjut karena kurangnya relevansi.
- Identifikasi Outlier: Terdapat outlier yang signifikan dalam data inflasi dan GDP, yang terjadi pada tahun-tahun krisis seperti 1980: Krisis minyak dunia menyebabkan lonjakan inflasi. 1998-1999: Krisis moneter Indonesia, yang berdampak pada inflasi tinggi dan penurunan GDP. 2020: Pandemi COVID-19 mengakibatkan penurunan GDP, tetapi tidak menyebabkan kenaikan inflasi.
  Keberadaan outlier ini perlu diperhatikan karena dapat mempengaruhi hasil model prediksi.
- Transformasi Data: Untuk mengatasi masalah skewness pada data inflasi dan GDP, dilakukan transformasi menggunakan metode yang sesuai:
  Log Transformation pada inflasi, yang berhasil memperbaiki distribusi data.
  Square Root Transformation pada GDP, yang berhasil mengurangi skewness ke kiri. Setelah transformasi, data menjadi lebih sesuai untuk digunakan dalam model prediksi.
- Stasioneritas dan Differencing: Uji stasioneritas menunjukkan bahwa data inflasi tidak stasioner pada awalnya (p-value > 0.05), namun setelah dilakukan differencing, data menjadi stasioner (p-value < 0.05). Hal ini menunjukkan bahwa model ARIMAX yang akan digunakan dapat diterapkan dengan baik.
- Model ARIMAX dan Prediksi: Hasil dari model ARIMAX menunjukkan bahwa model dapat mengikuti pola data historis dengan baik, dan prediksi inflasi untuk tahun 2024-2026 berada dalam interval kepercayaan yang tepat. Ini menunjukkan bahwa model ARIMAX mampu memberikan prediksi yang akurat, terutama dalam kondisi yang stabil.
- Prediksi untuk 2024-2026: Berdasarkan hasil prediksi, inflasi Indonesia untuk periode 2024-2026 diperkirakan stabil, sesuai dengan rata-rata GDP selama beberapa tahun terakhir. Hal ini memberikan indikasi bahwa, selama tidak ada kejadian luar biasa, inflasi akan tetap terkendali dan mengikuti pola yang telah teridentifikasi oleh model.

Secara keseluruhan, analisis ini menunjukkan bahwa inflasi di Indonesia sangat dipengaruhi oleh kondisi domestik, terutama terkait dengan fluktuasi GDP. Sementara itu, data dari negara lain tidak memberikan pengaruh yang signifikan terhadap inflasi Indonesia. Model ARIMAX yang digunakan terbukti mampu memprediksi inflasi dengan baik, dan prediksi untuk 3 tahun ke depan memberikan gambaran yang optimis mengenai stabilitas ekonomi di Indonesia.

### Visualisasi

Selain menggunakan Python, Visualisasi Tingkat Inflasi Indonesia dengan GDP coba disajikan dalam Tableau. Selain itu ditampilkan perbandingan inflasi Indonesia dengan 4 negara lain. visualisasi pada Tableau dapat dilihat pada link dibawah.

https://public.tableau.com/views/IndonesiaInflationRate/Dashboard1?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link
