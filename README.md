# Pertemuan ke 12
---
*Endah Sukma Kuncari*
---
Kata Koda

Langkah Untuk Menjalankan Docker
1. Mendefinisikan container pertama
	*web:*
		*build: .*
		![]()
	File ini mendefinisikan semua container, format file mengunakan YAML
	---
2. Mendefinisikan Pengaturan
	*links:*
		*- redis*
		![]()
		menghubungkan dua container secara bersama-sama untuk menentukan tautan dan mencantumkan koneksi yang dibutuhkan.
	*ports:*
	---
    *- "3000"*
    *- "8000"*
	![]()
	Properti port
	---
3. Mendefinisikan dua container
	*redis:
	image: redis:alpine
	volumes:
		- /var/redis/data:/data*
	![]()
	Menentukan dua container mengunakan nama redis dan format masih mengunakan YAML
	---
4. Docker Up
	*docker-compose up -d*
	![]()
	mengunakan argumen -d menyatakan untuk menjalankan latar belakang container
	---
5. Manajemen Docker
	*docker-compose ps*
	![]()
	untuk menandakan container sudah running 
	---
	*docker-compose logs*
	![]()
	mengakses semua log melalui satu container
	---
	*docker-compose*
	![]()
	Mengikuti pola yang sebelumya
	
	---
6. Skala docker
	*docker-compose scale web = 3*
	![]()
	Jumlah dari container yang digunakan disini mengunakan 3 container
	---
	docker-compose web = 1
	![]()
	Melakukan Skala kembali dengan 1 skala
	---
3. Docker Stop
	*docker-compose stop*
	![]()
	untuk menghentikan satu set container
	---
	*docker-compose rm*
	![]()
	untuk menghapus semua container
	---
	