# Lacak
Melacak penipu
<!DOCTYPE html>
<html>
<head>
<title>Info Pengunjung</title>
<style>
body{
font-family:Arial;
background:#111;
color:white;
text-align:center;
padding:40px;
}
.box{
background:#222;
padding:20px;
border-radius:10px;
display:inline-block;
}
</style>
</head>

<body>

<div class="box">
<h2>Informasi Pengunjung</h2>

<p>IP Address : <span id="ip"></span></p>
<p>Negara : <span id="negara"></span></p>
<p>Kota : <span id="kota"></span></p>
<p>Provider : <span id="isp"></span></p>

</div>

<script>
fetch("http://ip-api.com/json/")
.then(res => res.json())
.then(data => {
document.getElementById("ip").innerText = data.query;
document.getElementById("negara").innerText = data.country;
document.getElementById("kota").innerText = data.city;
document.getElementById("isp").innerText = data.isp;
});
</script>

</body>
</html>
