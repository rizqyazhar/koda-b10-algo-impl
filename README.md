# Algorithm Implementation

## Algoritma penentuan denda pengembalian buku perpustakaan

### Deskriptif
1. Mulai
2. Masukkan harga denda
3. Masukkan jumlah hari keterlambatan
4. Masukkan tipe anggota perpustakaan
5. Jika jumlah hari keterlambatan lebih dari 15 hari
6. Maka harga denda dikali 2
7. Hitung total denda dengan jumlah hari dikali harga denda
8. Jika jumlah hari keterlambatan tidak lebih dari 15 hari
9. maka harga denda dikali 1
10. Jika tipe anggota perpustakaan adalah "member"
11. maka harga diskon nya adalah harga denda dikali 20%
12. Hitung total denda dengan jumlah hari dikali harga denda yang sudah dikurangi dengan harga diskon
13. Jika bukan member
14. Hitung total denda dengan jumlah hari dikali harga denda
15. Tampilkan total denda
16. Selesai

### Flowchart
```mermaid
flowchart LR
  A@{shape: start, label: "Start"}
  B@{shape: stop, label: "End"}
  C@{shape: diam, label: "jumlahHari > 15"}
  D@{shape: diam, label: "tipeAnggota == #quot;member#quot;"}
  E@{shape: lean-r, label: "hargaDenda"}
  F@{shape: lean-r, label: "jumlahHari"}
  G@{shape: lean-r, label: "tipeAnggota"}
  H@{shape: lean-r, label: "totalDenda"}
  I@{shape: rect, label: "hargaDenda = hargaDenda x 2"}
  J@{shape: rect, label: "totalDenda = hargaDenda x jumlahHari"}
  K@{shape: rect, label: "hargaDiskon = hargaDenda x 20%"}
  L@{shape: rect, label: "totalDenda = jumlahHari x (hargaDenda - hargaDiskon)"}
  M@{shape: rect, label: "totalDenda = jumlahHari x hargaDenda"}

  A --> E --> F --> G --> C --iya--> I --> J 
  C --tidak--> D --iya--> K --> L
  D --tidak--> J 

  J & L  --> H --> B
```

### Pseudocode
```
DECLARE hargaDenda : INTEGER
DECLARE jumlahHari : INTEGER
DECLARE totalDenda : REAL
DECLARE hargaDiskon : REAL
DECLARE tipeAnggota : STRING

IF jumlahHari > 15 THEN
  hargaDenda <- hargaDenda * 2
  totalDenda <- hargaDenda * jumlahHari
ELSE
  IF tipeAnggota = "member" THEN
    hargaDiskon <- hargaDenda * 0.2
    totalDenda <- jumlahHari * (hargaDenda - hargaDiskon)
  ELSE
    totalDenda <- jumlahHari * hargaDenda
  ENDIF
ENDIF

OUTPUT totalDenda
```

## Algoritma konversi suhu 

### Deskriptif 
1. Mulai
2. Masukkan nilai suhu celcius
3. Hitung nilai suhu fahrenheit dengan suhu celcius dikali 1.8 kemudian ditambah 32
4. Hitung nilai suhu reamur dengan suhu celcius dikali 0.8
5. Hitung nilai suhu kelvin dengan nilai suhu celcius ditambah 273.15
6. Tampilkan nilai suhu fahrenheit
7. Tampilkan nilai suhu reamur
8. Tampilkan nilai suhu kelvin
9. Selesai 

### Flowchart 

```mermaid
flowchart LR

A@{shape: sm-circ, label: "Start"}
B@{shape: fr-circ, label: "End"}
C@{shape: lean-r, label: "suhuCelcius"}
D@{shape: rect, label: "suhuFahrenheit = (suhuCelcius * 1.8) + 32"}
E@{shape: rect, label: "suhuReamur = suhuCelcius * 0.8"}
F@{shape: rect, label: "suhuKelvin = suhuCelcius + 273.15"}
G@{shape: lean-r, label: "suhuFahrenheit"}
H@{shape: lean-r, label: "suhuReamur"}
I@{shape: lean-r, label: "suhuKelvin"}

A --> C --> D --> E --> F --> G --> H --> I --> B
```

### Pseudocode 
DECLARE suhuFahrenheit : REAL
DECLARE suhuReamur: REAL
DECLARE suhuKelvin: REAL

INPUT suhuCelcius 

suhuFahrenheit <- (suhuCelcius * 1.8) + 32
suhuReamur <- suhuCelcius * 0.8
suhuKelvin <- suhuCelcius + 273.15

OUTPUT suhuFahrenheit 
OUTPUT suhuReamur 
OUTPUT suhuKelvin

