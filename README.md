<table>
  <tr>
    <th colspan="2">DATA MAHASISWA</th>
  </tr>
  <tr>
    <td>Nama</td>
    <td>Roswanda Nuraini</td>
  </tr>
  <tr>
    <td>NIM</td>
    <td>312210328</td>
  </tr>
  <tr>
    <td>Kelas</td>
    <td>TI.22.A3</td>
  </tr>
</table>

# <p align="center">Praktikum4 : CSS Layout</p>

# 1. Membuat Box Element

### Langkah-langkah praktikum

- Persiapan membuat dokumen HTML dengan nama file <b>lab4_box.html</b> seperti berikut:

      <!DOCTYPE html>
      <html lang="en">
      <head>
          <meta charset="UTF-8">
          <meta http-equiv="X-UA-Compatible" content="IE=edge">
          <meta name="viewport" content="width=device-width, initial-scale=1.0">
          <title>Box Element</title>
      </head>
      <body>
          <header>
              <h1>Box Element</h1>
          </header>
      </body>
      </html>

### Membuat Box Element

- Kemudian tambahkan kode untuk membuat box element dengan tag div seperti berikut:

      <section>
          <div class="div1">Div 1</div>
          <div class="div2">Div 2</div>
          <div class="div3">Div 3</div>
          <div class="div4">Div 4</div>
      </section>

### CSS Float Property

- Selanjutnya tambahkan deklarasi CSS pada head untuk membuat float element, seperti berikut:

      <style>
          div {
          float:left;
          padding: 10px; 
          }
          .div1 {
          background: red;
          }
          .div2 {
          background: yellow;
          }
          .div3 {
          background: green;
          }
          .div4 {
          background-color: blue;
          clear: both;
          float: none;
          }
         </style>

- Kemudian buka browser untuk melihat hasilnya.

![Screenshot (401)](https://github.com/roswanda11/lab4web/assets/115516632/1271a885-eac3-453c-adf9-513157ff0f17)

### Mengatur Clearfix Element

- <b>Clearfix</b> digunakan untuk mengatur element setelah float element. Property <i>clear</i> digunakan untuk mengaturnya.

- Tambahkan element div lainnya seteleah div3 seperti berikut:

      <section>
        <div class="div1">Div 1</div>
        <div class="div2">Div 2</div>
        <div class="div3">Div 3</div>
        <div class="div4">Div 4</div>
      </section>

- Kemudian atur property clear pada CSS, seperti berikut:
  
      .div4 {
        background-color: blue;
        clear: left;
        float:
      ]

- Selanjutnya buka browser dan refresh kembali.

![image](https://github.com/roswanda11/lab4web/assets/115516632/0e77c778-e508-4b05-a3c7-fe53af6f4ade)

### Melakukan validasi dokumen html ```lab4_box.html``` dengan mengakses http://validator.w3.org

![Screenshot (403)](https://github.com/roswanda11/lab4web/assets/115516632/1eeed811-a406-46c3-b777-52b1134359d4)

# 2. Membuat Layout Sederhana

- Kita akan membuat layout web sederhana seperti gambar berikut:

![image](https://github.com/roswanda11/lab4web/assets/115516632/aedeb93a-4772-4c1c-b6a2-9bb2cdf25b5d)

- Buat <b>folder baru</b> dengan nama <b>lab4_layout</b>, kemudian buatlah <b>file baru</b> didalamnya dengan nama <b>home.html</b>, dan file <i>css</i> dengan nama <b>style.css</b>.

      <!DOCTYPE html>
      <html lang="en">
      <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Layout Sederhana</title>
        <link rel="stylesheet" href="style.css">
      </head>
      <body>
       <div id="container">
       </div>
      </body>
      </html>

- Kemudian buat kerangka layout dengan semantics element dengan kode berikut :

      <header>
        <h1>Layout Sederhana</h1>
      </header>
      <nav>
        <a href="home.html" class="active">Home</a>
        <a href="artikel.html">Artikel</a>
        <a href="about.html">About</a>
        <a href="kontak.html">Kontak</a>
      </nav>
      <section id="hero"></section>
      <section id="wrapper">
        <section id="main"></section>
        <aside id="sidebar"></aside>
      </section>
      <footer>
        <p>&copy; 2021 - Universitas Pelita Bangsa</p>

- Kemudian buka browser dan lihat hasilnya.
 
![image](https://github.com/roswanda11/lab4web/assets/115516632/96569859-c83c-4663-b7a0-0b120e9e2bf5)

- Kemudian tambahkan kode <i>CSS</i> untuk membuat layoutnya.

      /* import google font */
      @import
      url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400;0,600;0,700;0,800;1,300;1,400;1,600;1,700;1,800&display=swap');
      @import
      url('https://fonts.googleapis.com/css2?family=Open+Sans+Condensed:ital,wght@0,300;0,700;1,300&display=swap');
      
      /* Reset CSS */
      * {
          margin: 0;
          padding: 0;
      }
      
        body {
            line-height:1;
            font-size:100%;
            font-family:'Open Sans', sans-serif;
            color:#5a5a5a;
      }
      
        #container {
            width: 980px;
            margin: 0 auto;
            box-shadow: 0 0 1em #cccccc;
      }
      
        /* header */
        header {
            padding: 20px;
      }
      
        header h1 {
            margin: 20px 10px;
            color: #b5b5b5;
      }
      /* navigasi */
      nav {
          display: block;
          background-color: #1f5faa;
      }
      nav a {
          padding: 15px 30px;
          display: inline-block;
          color: #ffffff;
          font-size: 14px;
          text-decoration: none;
          font-weight: bold;
      }
      nav a.active,
      nav a:hover {
          background-color: #2b83ea;
      }
      /* Hero Panel */
      #hero {
          background-color: #e4e4e5;
          padding: 50px 20px;
          margin-bottom: 20px;
      }
      #hero h1 {
          margin-bottom: 20px;
          font-size: 35px;
      }
      #hero p {
          margin-bottom: 20px;
          font-size: 18px;
          line-height: 25px;
      }
      
      /* main content */
      #wrapper {
          margin: 0;
      }
      #main {
          float: left;
          width: 640px;
          padding: 20px;
      }
      /* sidebar area */
      #sidebar {
          float: left;
          width: 260px;
          padding: 20px;
      }
      
      /* widget */
      .widget-box 
      {border:1px solid #eee;
          margin-bottom:20px;
      }
      .widget-box  .title {
          padding:10px 16px;
          background-color:#428bca;
          color:#fff;
      }
      .widget-box ul {
          list-style-type:none;
      }
      .widget-box li {
          border-bottom:1px solid#eee;
      }
      .widget-box li a {
          padding:10px
          16px;
          color:#333;
          display:block;
          text-decoration:none;
      }
      .widget-box li:hover a {
          background-color:#eee;
      }
      .widget-box p {
          padding:15px;
          line-height:25px;
      }
       /* footer */
       footer {
          clear:both;
          background-color:#1d1d1d;
          padding:20px;
          color:#eee;
         }
         /* box */
      .box {
          display:block;
          float:left;
          width:33.333333%;
          box-sizing:border-box;
          -moz-box-sizing:border-box;
          -webkit-box-sizing:border-box;padding:0 10px;
          text-align:center;
         }
         .box h3 {
          margin: 15px 0;
         }
         .box p {
          line-height: 20px;
          font-size: 14px;
          margin-bottom: 15px;
         }
         box img {
          border: 0;
          vertical-align: middle;
         }
         .image-circle {
          border-radius: 50%;
         }
         .row {
          margin: 0 -10px;
          box-sizing: border-box;
          -moz-box-sizing: border-box;
          -webkit-box-sizing: border-box;
         }
         .row:after, .row:before,
         .entry:after, .entry:before {
          content:'';
          display:table;
         }
         .row:after,
         .entry:after {
          clear:both;
         }
         .divider {
          border:0;
          border-top:1px solid #eeeeee;
          margin:40px 0;
         }
         /* entry */
         .entry {
          margin: 15px 0;
         }
         .entry h2 {
          margin-bottom: 20px;}
          .entry p {
           line-height: 25px;
          }
          .entry img {
           float: left;
           border-radius: 5px;
           margin-right: 15px;
          }
          .entry .right-img {
           float: right;
          }
          .jumbotron img {
              border: 3px solid #343a40;
              width: 100px;
              height: 100px;
              border-radius: 90%;
              
          }   

- Kemudian lihat hasilnya pada browser.

![image](https://github.com/roswanda11/lab4web/assets/115516632/4433327a-9187-4d35-9599-44d2dbc339f8)

### Membuat Navigasi

- Kemudian selanjutnya mengatur navigasi.

      /* navigasi */
      nav {
        display: block;
        background-color: #1f5faa;
      }
      nav a {
        padding: 15px 30px;
        display: inline-block;
        color: #ffffff;
        font-size: 14px;
        text-decoration: none;
        font-weight: bold;
      }
        nav a.active,
        nav a:hover {
        background-color: #2b83ea;
      }

- Kemudian lihat hasilnya.

![image](https://github.com/roswanda11/lab4web/assets/115516632/df73087d-f1ae-4c1d-90f6-da32bac77d19)

# Membuat Hero Panel

- Selanjutnya membuat hero panel. Tambahkan kode HTML dan CSS seperti berikut.

      <section id="hero"><h1>Hello World!</h1>
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem 
         elit, iaculis innisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, 
         vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc 
         pretium ac.</p>
          <a href="home.html" class="btn btn-large">Learn more &raquo;</a>
      </section>

      /* Hero Panel */
      #hero {
        background-color: #e4e4e5;
        padding: 50px 20px;
        margin-bottom: 20px;
      }
      #hero h1 {
        margin-bottom: 20px;
        font-size: 35px;
      }
      #hero p {
        margin-bottom: 20px;
        font-size: 18px;
        line-height: 25px;
      }

![image](https://github.com/roswanda11/lab4web/assets/115516632/e6dbbc36-aa5b-484e-937d-65f1d71fc1b4)

### Mengatur Layout Main dan Sidebar

- Selanjutnya mengatur main content dan sidebar, tambahkan CSS float.

      /* main content */
      #wrapper {
          margin: 0;
      }
      #main {
          float: left;
          width: 640px;
          padding: 20px;
      }
      /* sidebar area */
      #sidebar {
          float: left;
          width: 260px;
          padding: 20px;
      }

### Membuat Sidebar Widget

- Kemudian selanjutnya menambahkan element lain dalam sidebar.

      <aside id="sidebar">
        <div class="widget-box">
          <h3 class="title">Widget Header</h3>
          <ul>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
          </ul>
        </div>
        <div class="widget-box">
          <h3 class="title">Widget Text</h3>
          <p>Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt
      arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer
      pharetra est nunc, nec pretium nunc pretium ac.</p>
        </div>
      </aside>
  
- Kemudian tambahkan CSS.

      /* widget */
      .widget-box 
      {border:1px solid #eee;
          margin-bottom:20px;
      }
      .widget-box  .title {
          padding:10px 16px;
          background-color:#428bca;
          color:#fff;
      }
      .widget-box ul {
          list-style-type:none;
      }
      .widget-box li {
          border-bottom:1px solid#eee;
      }
      .widget-box li a {
          padding:10px
          16px;
          color:#333;
          display:block;
          text-decoration:none;
      }
      .widget-box li:hover a {
          background-color:#eee;
      }
      .widget-box p {
          padding:15px;
          line-height:25px;
      }
  
![image](https://github.com/roswanda11/lab4web/assets/115516632/c69aa4c1-7de3-46f8-a683-eb5fa36b4762)
      
### Mengatur Footer

- Selanjutnya mengatur tampilan footer. Tambahkan CSS untuk footer.   
      
       /* footer */
      footer {
        clear:both;
        background-color:#1d1d1d;
        padding:20px;
        color:#eee;
      }     

![image](https://github.com/roswanda11/lab4web/assets/115516632/72da2865-bd3b-4d57-b8a1-3e3a0ec5eab0)

### Menambahkan Elemen lainnya pada Main Content
  
          <section id="main">
            <div class="row">
              <div class="box">
                <img src="https://dummyimage.com/120/db7d25/fff.png" alt=""
          class="image-circle">
                <h3>Heading</h3>
                <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis 
          euismod.</p>
                <a href="#" class="btn btn-default">View detail</a>
              </div>
              <div class="box">
                <img src="https://dummyimage.com/120/3e73e6/fff.png" alt=""
          class="image-circle">
                <h3>Heading</h3>
                <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis 
          euismod.</p>
                <a href="#" class="btn btn-default">View detail</a>
              </div>
            </div>
          </section>
          
   - Kemudian tambahkan CSS.
  
          /* box */
          .box {
            display:block;
            float:left;
            width:33.333333%;
            box-sizing:border-box;
            -moz-box-sizing:border-box;
            -webkit-box-sizing:border-box;
          ]
            padding:0 10px;
            text-align:center;
          }
          .box h3 {
            margin: 15px 0;
          }
          .box p {
            line-height: 20px;
            font-size: 14px;
            margin-bottom: 15px;
          }
            box img {
            border: 0;
            vertical-align: middle;
          }
          .image-circle {
            border-radius: 50%;
          }
          .row {
            margin: 0 -10px;
            box-sizing: border-box;
            -moz-box-sizing: border-box;
            -webkit-box-sizing: border-box;
          }
          .row:after, .row:before,
          .entry:after, .entry:before {
            content:'';
            display:table;
          }
          .row:after,
          .entry:after {
            clear:both;
          }
      
 - Lihat hasilnya dibrowser.     
      
![image](https://github.com/roswanda11/lab4web/assets/115516632/d3d6cf66-4ac0-4926-8720-f12f4250d75d)

### Menambahkan Content Artikel

- Selanjutnya membuat content artikel. Tambahkan HTML berikut pada main content.

                <hr class="divider" />
                <article class="entry">
                    <h2>First featurette heading.</h2>
                    <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="">
                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
                        elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
                        vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
                        pretium ac.</p>
                </article>
                <hr class="divider" />
                <article class="entry">
                    <h2>First featurette heading.</h2>
                    <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="" class="right-img">
                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
                        elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
                        vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
                        pretium ac.</p>
                </article>

- Kemudian tambahkan CSS.

      .divider {
          border:0;
          border-top:1px solid #eeeeee;
          margin:40px 0;
      }
      /* entry */
      .entry {
          margin: 15px 0;
      }
      .entry h2 {
          margin-bottom: 20px;}
      .entry p {
          line-height: 25px;
      }
      .entry img {
          float: left;
          border-radius: 5px;
          margin-right: 15px;
      }
      .entry .right-img {
          float: right;
      }
      .jumbotron img {
          border: 3px solid #343a40;
          width: 100px;
          height: 100px;
          border-radius: 90%;
      }   
      
    ![image](https://github.com/roswanda11/lab4web/assets/115516632/ce5dee10-5933-485e-adc7-418a0633dcef)

### Melakukan validasi dokumen html ```lab4_layout.html``` dengan mengakses http://validator.w3.org


# Pertanyaan dan Tugas
1. Tambahkan Layout untuk menu About
=> buat single layout yang berisi deskripsi, portfolio, dll
2. Tambahkan layout untuk menu Contact
=> yang berisi form isian: nama, email, message, dll

  
