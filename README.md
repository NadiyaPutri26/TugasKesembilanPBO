# TugasKesembilanPBO

Tugas ini dibuat untuk memenuhi tugas mata kuliah Pemrograman Berorientasi Objek (PBO). Dengan dosen pangampu, Bapak Bayu Adhi Nugroho. Dimana dalam praktikum ini akan menerapkan konsep _persistence_ dengan _entity class_ dalam projek CRUD (_Create, Read, Update, Delete_).

# Persistence

_Persistence_ dalam konteks pemrograman berarti penyimpanan data secara permanen, agar data tetap tersimpan walaupun program dihentikan. Dalam praktikum ini _persistence_ diterapkan menggunakan JPA (_Java Persistance API_). Dimana dalam JPA ini ada 3 hal utama yakni:

**1. Entity Class**

   Biasanya, _entity_ itu seperti gambaran sebuah tabel di database. Setiap objek (_instans_) dari _entity_ mewakili satu baris data di tabel tersebut. Sehingga kalau dalam JAVA _Class_, _persistence_ adalah JAVA _class_ yang dipetakan ke tabel _database_ dan setiap objeknya merepresentasikan satu _record_ (baris data).
   
**2. Entity Manager**

  _EntityManager_ adalah bagian utama dari JPA yang digunakan untuk berhubungan dengan database. Melalui _EntityManager_, CRUD dapat diterapkan dan membantu menjalankan _query_ serta mengatur transaksi, jadi pengembang tidak perlu menulis banyak kode SQL secara langsung. Dengan _EntityManager_, kita bisa membuat objek baru lalu menyimpannya ke _database_ menggunakan perintah **em.persist(newUser)**. Sebelum data disimpan, kita perlu memulai transaksi dengan **beginTransaction()**, dan setelah selesai, kita menutup transaksi dengan **commit()** agar perubahan benar-benar tersimpan di _database_.

**3. Persistence Context**

   _Persistence Context_ adalah _cache_ sementara yang menyimpan dan mengelola entitas aktif. Ia memastikan setiap entitas unik, memantau perubahan secara otomatis, dan menyinkronkannya ke _database_ saat transaksi di _commit_ melalui _EntityManager_.
   
# Penerapan Persistence menggunakan Entitiy Class dalam Projek CRUD
**1. Membuat Persistence unit dengan cara klik New pada package lalu klik "Entity Classes From Database"**

   <img width="654" height="453" alt="Cuplikan layar 2025-10-28 144714" src="https://github.com/user-attachments/assets/5318af1f-21c5-4495-b246-a6c9e0b4f348" />

**2. Memilih _Database_**

   <img width="900" height="640" alt="Cuplikan layar 2025-10-28 144742" src="https://github.com/user-attachments/assets/77a9f44f-cc17-40d6-8dc2-ed84ad61bbe2" />

**3. Memindahkan semua tabel ke panel sebelah kanan**

   <img width="897" height="640" alt="Cuplikan layar 2025-10-28 144751" src="https://github.com/user-attachments/assets/9d97b5d9-2d40-4a22-b0ba-5c92f8e4c2d4" />

**4. Centang "Generate Named Query Annotations for Persistent Fields" dan klik Next**

   <img width="960" height="646" alt="Cuplikan layar 2025-10-28 145418" src="https://github.com/user-attachments/assets/cf0df854-44be-4cc3-84b2-faf45a059c5f" />

**5. Klik Finish**

   <img width="960" height="648" alt="Cuplikan layar 2025-10-28 144909" src="https://github.com/user-attachments/assets/6bc82918-b31d-44a7-8108-d3f0db70dc09" />

**6. Maka akan muncul package dan class sebagai berikut:**

   <img width="416" height="344" alt="Cuplikan layar 2025-10-30 114828" src="https://github.com/user-attachments/assets/1baef7c9-b6ca-4c84-aac1-147181c91906" />
   
**7. Code untuk setiap button**
   
  **a. Button Insert di Insert Dialog**

   <img width="602" height="697" alt="image" src="https://github.com/user-attachments/assets/6a0e3e20-2a96-4d42-9d62-920c45967256" />

   **b. Button Update di Update Dialog**

   <img width="1005" height="642" alt="image" src="https://github.com/user-attachments/assets/60bfdddb-cb71-4e0a-aee0-7a86b96bf73f" />

   <img width="900" height="472" alt="image" src="https://github.com/user-attachments/assets/77d14962-9f99-4e69-bec0-1259f58900b8" />

   **c. Button Delete di Delete Dialog**

   <img width="724" height="685" alt="image" src="https://github.com/user-attachments/assets/6ce8d1dc-445b-45f4-9d94-7676adc7e5f3" />

   **d. Button Print di Jframe Utama**

     Tetap menggunakan JDBC, karena agar bisa terhubung langsung ke database dan kompatibel dengan library laporan seperti JasperReports, tanpa bergantung pada Entity Manager milik JPA.

   <img width="1106" height="470" alt="image" src="https://github.com/user-attachments/assets/41c251f2-a4e0-4249-9e5d-e4190ec023e5" />

   **e. Button Upload di Jframe Utama**

   <img width="936" height="775" alt="image" src="https://github.com/user-attachments/assets/699c1087-77f2-43a8-bded-9f0f5be0b504" />

   <img width="845" height="800" alt="image" src="https://github.com/user-attachments/assets/4cdecc89-c08b-42b3-a464-dbf186b98e18" />

**8. Method ShowTable()**

   <img width="1312" height="422" alt="image" src="https://github.com/user-attachments/assets/30830d3a-e109-44d5-9f81-f667f80164f6" />
   
# Catatan

Berikut adalah penjelasan mengenai konsep persistence menggunakan entitiy class di projek CRUD Java. Semoga dapat memberikan ilmu yang bermanfaat.

Sekian,

Nadiya Putri Intan Nur Rahmadhani, Mahasiswa Semester 3 Program Studi Sistem Informasi,

Fakultas Sains dan Teknologi, UIN Sunan Ampel Surabaya
