pada folder sql dan postman ada 1. database article 
2. screenshot pembuatan tabel posts pada database article secara manual menggunakan query ( perubahan pembuatan awal query dan database sekarang adalah pada kolom status sudah saya rubah dari enum menjadi varchar (100) karena menggunakan validasi dari code )
3. screenshot postman sukses sesuai dengan validasi data minimun dan status yang hanya bisa menerima publish, draft dan thrash dan screenshot postman dengan data yang tidak sesuai dengan validasi.
4. json postman untuk import di dalam postman
5. postmantest.html untuk bikin fork postman sendiri

untuk pemanggilan postman jalankan dulu filenya local lalu bisa menggunakan http://127.0.0.1:8000/api/posts (bisa berubah sesuai dengan local masing2)

file db_create_article.py adalah file untuk pembuatan database article menggunakan python, database yang di buat masih database kosong karena di minta pembuatan tabel pada database secara manual.

untuk pemanggilan API di laravel bisa di cek di route/API

untuk controller ada di App\Http\Controllers\Api\PostsController, di controller juga terdapat validasi minimun karakter dan status yang hanya bisa draft,publish dan thrash

untuk deklarasi dan pemanggilan database json ada di App\Http\Resources\PostsResource

untuk models ada di App\Models\Posts

karena env. pada laravel defaultnya tidak terupload ke git gunakan env.example dan hilangkan tulisan example.
untuk setting env. 
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=article
DB_USERNAME=(sesuaikan)
DB_PASSWORD=(sesuaikan)
