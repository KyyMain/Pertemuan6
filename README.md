# Praktikum 3

| Keterangan | Data                |
| ---------- | ------------------- |
| **Nama**   | Eky Fikri Yamansyah |
| **NIM**    | 312310572           |
| **Kelas**  | TI.23.A6            |

# Bangun Datar OOP dengan Java

Proyek ini merupakan contoh implementasi dari konsep **inheritance** dan **polymorphism** dalam pemrograman berorientasi objek (OOP) menggunakan bahasa Java. Tiga jenis bangun datar yang digunakan dalam contoh ini adalah:
- Lingkaran
- Segitiga
- Persegi

## Struktur Kelas

1. **BangunDatar (Kelas Abstrak)**  
   Kelas ini mendefinisikan dua metode abstrak: `luas()` dan `keliling()`. Semua kelas turunan (Lingkaran, Segitiga, Persegi) harus mengimplementasikan kedua metode ini.
   ### Code
   ```java
    abstract class BangunDatar {
   
    public abstract float luas();
    public abstract float keliling();
   
   }
   ```

3. **Lingkaran**  
   Menghitung luas dan keliling lingkaran berdasarkan jari-jari.
   ### Code
   ```java
   public class Lingkaran extends BangunDatar {
    private int r;

    public Lingkaran(int r) {
        this.r = r;
    }

    public float luas() {
        return (float) (3.14 * this.r * this.r);
    }

    public float keliling() {
        return (float) (2 * 3.14 * this.r);
    }
   }
   ```


5. **Segitiga**  
   Menghitung luas dan keliling segitiga berdasarkan alas dan tinggi. Untuk keliling, menggunakan rumus Pythagoras untuk menghitung sisi miring.
   ### Code
   ```java
   public class Segitiga extends BangunDatar {
    private int alas, tinggi;

    public Segitiga(int alas, int tinggi) {
        this.alas = alas;
        this.tinggi = tinggi;
    }

    public float luas() {
        return (float) (0.5 * alas * tinggi);
    }

    public float keliling() {
        double sisiMiring = Math.sqrt(alas * alas + tinggi * tinggi);
        return (float) (alas + tinggi + sisiMiring);
    }
   }
   ```

7. **Persegi**  
   Menghitung luas dan keliling persegi berdasarkan panjang sisi.
   ```java
   public class Persegi extends BangunDatar {
    private int sisi;

    public Persegi(int sisi) {
        this.sisi = sisi;
    }

    public float luas() {
        return (float) (sisi * sisi);
    }

    public float keliling() {
        return (float) (2 * sisi);
    }
   }
   ```

8. **Main**
   Program utama untuk menjalankan programnya.
   ```yaml
   Menghitung Luas dan Keliling Lingkaran:
   Luas Lingkaran: 1256.0
   Keliling Lingkaran: 125.600006

   Menghitung Luas dan Keliling Segitiga:
   Luas Segitiga: 100.0
   Keliling Segitiga: 42.36068

   Menghitung Luas dan Keliling Persegi:
   Luas Persegi: 400.0
   Keliling Persegi: 40.0



## Cara Menjalankan Program

1. Clone repositori ini.
2. Buka terminal atau command prompt di direktori proyek.
3. Jalankan perintah berikut untuk meng-compile dan menjalankan program:
   ```bash
   javac main.java
   java main
