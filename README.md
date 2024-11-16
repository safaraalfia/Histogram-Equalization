# Histogram-Equalization
alfia Rohmah Safara (23422039) - UTS Pengolahan Cirta Digital

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
from google.colab import files

# 1. Unggah file gambar
print("Silakan unggah gambar Anda:")
uploaded = files.upload()  # Pilih file gambar yang ingin digunakan

# 2. Membaca file gambar
# Ganti 'nama_file_gambar.jpg' dengan nama file yang Anda unggah
image_name = list(uploaded.keys())[0]  # Mengambil nama file yang diunggah
image = cv2.imread(image_name, cv2.IMREAD_GRAYSCALE)

# 3. Validasi apakah gambar berhasil dibaca
if image is None:
    print("Gambar tidak ditemukan atau gagal dibaca!")
else:
    # Menampilkan gambar asli
    plt.figure(figsize=(12, 6))
    plt.subplot(1, 2, 1)
    plt.title("Gambar Asli")
    plt.imshow(image, cmap="gray", aspect="auto")

    # Histogram Equalization
    equalized_image = cv2.equalizeHist(image)

    # Menampilkan hasil gambar setelah histogram equalization
    plt.subplot(1, 2, 2)
    plt.title("Gambar Setelah Histogram Equalization")
    plt.imshow(equalized_image, cmap="gray", aspect="auto")
    plt.show()

    # Menampilkan histogram asli dan histogram setelah equalization
    plt.figure(figsize=(12, 6))
    plt.subplot(1, 2, 1)
    plt.title("Histogram Asli")
    plt.hist(image.ravel(), bins=256, range=(0, 256), color="blue", alpha=0.7)

    plt.subplot(1, 2, 2)
    plt.title("Histogram Setelah Equalization")
    plt.hist(equalized_image.ravel(), bins=256, range=(0, 256), color="green", alpha=0.7)
    plt.show()
import cv2
import numpy as np
import matplotlib.pyplot as plt
from google.colab import files

# 1. Unggah file gambar
print("Silakan unggah gambar Anda:")
uploaded = files.upload()  # Pilih file gambar yang ingin digunakan

# 2. Membaca file gambar
# Ganti 'nama_file_gambar.jpg' dengan nama file yang Anda unggah
image_name = list(uploaded.keys())[0]  # Mengambil nama file yang diunggah
image = cv2.imread(image_name, cv2.IMREAD_GRAYSCALE)

# 3. Validasi apakah gambar berhasil dibaca
if image is None:
    print("Gambar tidak ditemukan atau gagal dibaca!")
else:
    # Menampilkan gambar asli
    plt.figure(figsize=(12, 6))
    plt.subplot(1, 2, 1)
    plt.title("Gambar Asli")
    plt.imshow(image, cmap="gray", aspect="auto")

    # Histogram Equalization
    equalized_image = cv2.equalizeHist(image)

    # Menampilkan hasil gambar setelah histogram equalization
    plt.subplot(1, 2, 2)
    plt.title("Gambar Setelah Histogram Equalization")
    plt.imshow(equalized_image, cmap="gray", aspect="auto")
    plt.show()

    # Menampilkan histogram asli dan histogram setelah equalization
    plt.figure(figsize=(12, 6))
    plt.subplot(1, 2, 1)
    plt.title("Histogram Asli")
    plt.hist(image.ravel(), bins=256, range=(0, 256), color="blue", alpha=0.7)

    plt.subplot(1, 2, 2)
    plt.title("Histogram Setelah Equalization")
    plt.hist(equalized_image.ravel(), bins=256, range=(0, 256), color="green", alpha=0.7)
    plt.show()
