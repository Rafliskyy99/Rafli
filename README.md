<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Penyemangat Hidup</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: linear-gradient(135deg, #ff7e5f, #feb47b); /* Background gradien yang cerah */
            background-size: cover;
            color: white;
        }

        h1 {
            color: white;
            font-size: 2.5em;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }

        .container {
            background-color: rgba(255, 255, 255, 0.8); /* Transparan agar background tetap terlihat */
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.2);
            width: 80%;
            max-width: 600px;
            text-align: center;
        }

        p {
            color: #333;
            font-size: 1.2em;
            margin-top: 10px;
            font-weight: 500;
        }

        select, button {
            padding: 12px;
            font-size: 16px;
            margin-top: 20px;
            cursor: pointer;
            border-radius: 5px;
            width: 100%;
        }

        button {
            background-color: #4CAF50;
            color: white;
            border: none;
            margin-top: 15px;
            font-size: 18px;
            transition: background-color 0.3s ease;
        }

        button:hover {
            background-color: #45a049;
        }

        .message {
            margin-top: 20px;
            font-size: 18px;
            font-weight: bold;
            color: #333;
        }

        footer {
            margin-top: 30px;
            font-size: 14px;
            color: #777;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>Penyemangat Hidup</h1>
        <p>Selamat datang di situs penyemangat! Pilih masalah yang kamu alami, dan kami akan memberikan kata-kata penyemangat untukmu.</p>
        
        <select id="problemSelect">
            <option value="cape">Capek dengan kehidupan</option>
            <option value="sekolah">Capek sekolah</option>
            <option value="kepikiran">Capek kepikiran terus</option>
            <option value="cinta">Masalah cinta</option>
            <option value="kerja">Capek kerja</option>
            <option value="keuangan">Masalah keuangan</option>
            <option value="teman">Masalah dengan teman</option>
            <option value="keluarga">Masalah keluarga</option>
            <option value="buntu">Buntu, nggak tahu mau ngapain</option>
            <option value="lainnya">Masalah lainnya</option>
        </select>
        
        <button onclick="generateMessage()">Dapatkan Penyemangat</button>
        
        <div class="message" id="message"></div>
        
        <footer>
            <p>by Rafliskyy99</p>
        </footer>
    </div>

    <script>
        function generateMessage() {
            const problem = document.getElementById("problemSelect").value;
            let message = "";

            switch (problem) {
                case "cape":
                    message = "Ingat, meski terasa berat, kamu pasti bisa melewati semua ini. Setiap langkah kecil menuju kedamaian!";
                    break;
                case "sekolah":
                    message = "Sekolah itu memang menantang, tapi bayangkan betapa berharganya usaha kamu. Terus maju, kamu pasti bisa!";
                    break;
                case "kepikiran":
                    message = "Tenang, semuanya akan berjalan dengan baik. Lepaskan beban pikiran dan beri diri kamu ruang untuk bernafas.";
                    break;
                case "cinta":
                    message = "Cinta itu memang bisa rumit, tapi jangan lupa untuk tetap mencintai diri sendiri terlebih dahulu. Semua akan menemukan jalannya!";
                    break;
                case "kerja":
                    message = "Kerja keras itu penting, tapi jangan lupa untuk memberi ruang bagi dirimu untuk istirahat. Keseimbangan adalah kunci!";
                    break;
                case "keuangan":
                    message = "Keuangan memang sering bikin pusing, tapi percayalah, setiap masalah ada jalan keluarnya. Tetap semangat dan terus usaha!";
                    break;
                case "teman":
                    message = "Terkadang, teman bisa membuat kita merasa sendiri, tapi ingatlah bahwa kamu tidak sendirian. Ada orang yang peduli dan akan selalu ada untukmu.";
                    break;
                case "keluarga":
                    message = "Keluarga mungkin tidak selalu memahami, tapi mereka tetap mencintaimu. Jangan ragu untuk membuka hati dan berbicara.";
                    break;
                case "buntu":
                    message = "Ketika merasa buntu, itu hanya tanda bahwa kamu sedang mencari arah yang lebih baik. Bersabarlah, kamu akan menemukan jalanmu!";
                    break;
                case "lainnya":
                    message = "Apapun masalahnya, kamu lebih kuat dari yang kamu kira. Jangan ragu untuk melangkah dan tetap positif!";
                    break;
                default:
                    message = "Terus semangat! Kamu lebih hebat dari apa yang kamu pikirkan.";
            }

            document.getElementById("message").textContent = message;
        }
    </script>
</body>
</html>
