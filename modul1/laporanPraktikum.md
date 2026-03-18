# <h1 align="center">Laporan Praktikum Modul 1 - ... </h1>
<p align="center">[Eric Setiawan] - [109082500197]</p>

## Unguided 

### 1. [Soal]
#### soal1.go

```go
package main

import "fmt"

func factorial(n int) int {
	if n == 0 || n == 1 {
		return 1
	}
	result := 1
	for i := 2; i <= n; i++ {
		result *= i
	}
	return result
}

func permutation(n, r int) int {
	if r > n {
		return 0
	}
	return factorial(n) / factorial(n-r)
}

func combination(n, r int) int {
	if r > n {
		return 0
	}
	return factorial(n) / (factorial(r) * factorial(n-r))
}

func main() {
	var a, b, c, d int
	fmt.Scan(&a, &b, &c, &d)

	p1 := permutation(a, c)
	c1 := combination(a, c)

	p2 := permutation(b, d)
	c2 := combination(b, d)

	// output
	fmt.Println(p1, c1)
	fmt.Println(p2, c2)
}
```
### Output Unguided :

##### Output 
![Screenshot Output Unguided 1_1](https://github.com/ericstwn/109082500197_Eric-Setiawan/blob/main/modul1/output/output-soal1.png)
[Penjelasan: Jadi program ini berguna untuk merubah posisi dari variabelnya dimana temp
menyimpan nomor satu,satu menyimpan variabel nomor dua,dua menyimpan variabel
nomor tiga,dan tiga menyimpan variabel punya temp dimana tempnya sudah diganti dengan variabel nomor satu.]

### 2. [Soal]
#### soal2.go

```go
package main

import "fmt"

func f(x int) int {
	return x * x
}
func g(x int) int {
	return x - 2
}
func h(x int) int {
	return x + 1
}
func fogog(x int) int {
	return f(g(h(x)))
}
func gohof(x int) int {
	return g(h(f(x)))
}
func hofog(x int) int {
	return h(f(g(x)))
}
func main() {
	var a, b, c int
	fmt.Scan(&a, &b, &c)

	fmt.Println(fogog(a))
	fmt.Println(gohof(b))
	fmt.Println(hofog(c))
}
```
### Output Unguided :

##### Output 
![Screenshot Output Unguided 1_2](https://github.com/ericstwn/109082500197_Eric-Setiawan/blob/main/modul1/output/output-soal2.png)
[Penjelasan: Jadi Program ini memakai perulangan untuk input empat warna sebanyak lima kali,
lalu membandingkan input tersebut dengan urutan standar atau true "merah", "kuning",
"hijau", dan "ungu". Variabel berhasil itu sebagai true, namun akan diubah
menjadi false jika ditemukan satu saja percobaan yang urutan warnanya tidak sesuai, sehingga
program akan menghasilkan nilai true jika lima percobaan memiliki
urutan yang tepat.]

### 3. [Soal]
#### soal3.go

```go
package main

import "fmt"

func dalamLingkaran(cx, cy, r, x, y int) bool {
	dx := x - cx
	dy := y - cy
	return dx*dx+dy*dy <= r*r
}

func main() {
	var cx1, cy1, r1 int
	var cx2, cy2, r2 int
	var x, y int

	fmt.Scan(&cx1, &cy1, &r1)
	fmt.Scan(&cx2, &cy2, &r2)
	fmt.Scan(&x, &y)

	dalam1 := dalamLingkaran(cx1, cy1, r1, x, y)
	dalam2 := dalamLingkaran(cx2, cy2, r2, x, y)

	if dalam1 && dalam2 {
		fmt.Println("Titik di dalam lingkaran 1 dan 2")
	} else if dalam1 {
		fmt.Println("Titik di dalam lingkaran 1")
	} else if dalam2 {
		fmt.Println("Titik di dalam lingkaran 2")
	} else {
		fmt.Println("Titik di luar lingkaran 1 dan 2")
	}
}
```
### Output Unguided :

##### Output 
![Screenshot Output Unguided 1_2](https://github.com/ericstwn/109082500197_Eric-Setiawan/blob/main/modul1/output/output-soal3.png)
[Penjelasan: Jadi program ini menghitung biaya pengiriman parsel dengan membagi total berat gram
menjadi jumlah kilogram dan sisa gram, di mana biaya dasar ditetapkan sebesar Rp10.000
per kilogram. Program kemudian menerapkan aturan khusus: jika berat total kurang dari 10
kg, sisa gram akan dikenakan biaya Rp5 per gram jika jumlahnya 500 gram atau lebih, dan
Rp15 per gram jika kurang dari 500 gram; namun, jika berat total sudah melebihi 10 kg,
maka sisa gram tersebut digratiskan, sehingga total biaya hanya dihitung berdasarkan berat
kilogramnya saja.]



