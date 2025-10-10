# 🧮 Aplikasi Pertambahan Dua Angka (Java GUI)

Aplikasi sederhana berbasis **Java Swing** yang berfungsi untuk **menjumlahkan dua angka** yang dimasukkan oleh pengguna.  
Dibuat menggunakan **NetBeans IDE** dan **JFrame Form** untuk tampilan GUI yang interaktif.

---

## 🌐 Link Repository
🔗 [Klik di sini untuk melihat repository di GitHub](https://github.com/Panekuk/AplikasiTambahDuaAngka.git)

---

## 📋 Deskripsi Program

**Fitur utama aplikasi:**
- Pengguna dapat memasukkan **dua angka**.
- Saat tombol **Tambah** diklik → menampilkan hasil penjumlahan.
- Saat tombol **Hapus** diklik → menghapus semua nilai dan mengarahkan fokus ke kolom pertama.
- Saat tombol **Keluar** diklik → aplikasi langsung keluar.

---

## 🧱 Komponen GUI
Aplikasi ini menggunakan komponen berikut:
- 🪟 `JFrame` – jendela utama program.  
- 🧩 `JPanel` – panel utama untuk menampung semua komponen.  
- 🏷️ `JLabel` – label teks ("Angka 1", "Angka 2", "Hasil").  
- ✏️ `JTextField` – kolom input dan output angka.  
- 🔘 `JButton` – tombol aksi: **Tambah**, **Hapus**, **Keluar**.  

---

## ⚙️ Logika Program
1. Mengambil input dari dua `JTextField`.
2. Mengonversi nilai ke tipe `double`.
3. Menjumlahkan kedua angka.
4. Menampilkan hasil pada kolom hasil (`hasilField`).
5. Jika input bukan angka → muncul **pesan error** menggunakan `JOptionPane`.

---

## 🖱️ Event Handling
| Komponen | Event | Fungsi |
|-----------|--------|--------|
| Tombol **Tambah** | `ActionListener` | Menampilkan hasil pertambahan |
| Tombol **Hapus** | `ActionListener` | Menghapus input dan fokus ke kolom pertama |
| Tombol **Keluar** | `ActionListener` | Menutup aplikasi |
| `JTextField` | `KeyAdapter` | Membatasi input agar hanya angka dan titik desimal |
| `JTextField` | `FocusListener` | Menghapus isi field saat mendapat fokus |
| Kesalahan input | `JOptionPane` | Menampilkan peringatan jika input bukan angka |

---

## 🎨 Tampilan Antarmuka

```
+------------------------------------------+
|    APLIKASI PERTAMBAHAN DUA ANGKA        |
|------------------------------------------|
|  Angka 1 : [          ]                  |
|  Angka 2 : [          ]                  |
|  Hasil   : [          ]                  |
|                                          |
| [TAMBAH]   [HAPUS]   [KELUAR]            |
+------------------------------------------+

## SCREENSHOT
![Gambar 1](images/latihan1.PNG)
![Hasil Tambah](images/latihan1-1.PNG)
![Popup window](images/latihan1-2.PNG)

```

> Panel utama (`JPanel`) menggunakan **warna merah muda muda (pink lembut)** dengan border bevel untuk tampilan yang menarik.

---

## 🧠 Validasi Input
- Input hanya dapat berupa angka dan titik desimal.  
- Jika pengguna memasukkan huruf, aplikasi akan menolak input dan menampilkan pesan:
  > ⚠️ “Masukkan angka yang valid!”

---

## 💻 Cara Menjalankan Program
1. Buka **NetBeans IDE**.
2. Pilih **File → New Project → Java Application**.
3. Buat package baru:  
   ```
   aplikasitambahduaangka
   ```
4. Tambahkan file:
   ```
   AplikasiTambahDuaAngka.java
   ```
5. Jalankan program dengan menekan **Shift + F6**.

---

## 🧾 Indikator Penilaian (Tugas)

| Komponen | Persentase | Status |
|-----------|-------------|--------|
| Komponen GUI (JFrame, JPanel, JLabel, dll) | 20% | ✅ Lengkap |
| Logika Program (Penjumlahan dua angka) | 20% | ✅ Berfungsi |
| Event Handling (ActionListener) | 15% | ✅ Sudah diterapkan |
| Kesesuaian UI | 15% | ✅ Sesuai instruksi |
| Variasi (KeyAdapter, FocusListener, JOptionPane) | 30% | ✅ Lengkap |
| **Total** | **100%** | 🏆 **Sempurna** |

---

## 🧰 Teknologi yang Digunakan
- **Java SE 8 atau lebih baru**
- **Swing GUI**
- **NetBeans IDE**

---

## 👩‍💻 Pembuat
**Nama:** ITA KHAIRATI  
**Kelas / Mata Kuliah:** PBO2-LATIHAN1-23100101219    

---






## 💻 Kode Lengkap Aplikasi

```java
package aplikasitambahduaangka;

import javax.swing.JOptionPane; 

public class AplikasiTambahDuaAngka extends javax.swing.JFrame {

     public AplikasiTambahDuaAngka() {
        initComponents();
        angka1Field.requestFocus();
    }
    
    @SuppressWarnings("unchecked")
    // <editor-fold defaultstate="collapsed" desc="Generated Code">                          
    private void initComponents() {

        jLabel4 = new javax.swing.JLabel();
        jPanel1 = new javax.swing.JPanel();
        lblAngka1 = new javax.swing.JLabel();
        lblAngka2 = new javax.swing.JLabel();
        lblHasil = new javax.swing.JLabel();
        jButton1 = new javax.swing.JButton();
        angka1Field = new javax.swing.JTextField();
        angka2Field = new javax.swing.JTextField();
        hasilField = new javax.swing.JTextField();
        jButton2 = new javax.swing.JButton();
        jButton3 = new javax.swing.JButton();

        setDefaultCloseOperation(javax.swing.WindowConstants.EXIT_ON_CLOSE);

        jLabel4.setText("APLIKASI PERTAMBAHAN DUA ANGKA");

        jPanel1.setBackground(new java.awt.Color(255, 204, 204));
        jPanel1.setBorder(javax.swing.BorderFactory.createBevelBorder(javax.swing.border.BevelBorder.RAISED, null, new java.awt.Color(255, 255, 204), null, null));

        lblAngka1.setText("ANGKA1");

        lblAngka2.setText("ANGKA 2");

        lblHasil.setText("HASIL");

        jButton1.setText("TAMBAH");
        jButton1.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton1ActionPerformed(evt);
            }
        });

        angka1Field.addFocusListener(new java.awt.event.FocusAdapter() {
            public void focusGained(java.awt.event.FocusEvent evt) {
                angka1FieldFocusGained(evt);
            }
        });
        angka1Field.addKeyListener(new java.awt.event.KeyAdapter() {
            public void keyTyped(java.awt.event.KeyEvent evt) {
                angka1FieldKeyTyped(evt);
            }
        });

        angka2Field.addFocusListener(new java.awt.event.FocusAdapter() {
            public void focusGained(java.awt.event.FocusEvent evt) {
                angka2FieldFocusGained(evt);
            }
        });
        angka2Field.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                angka2FieldActionPerformed(evt);
            }
        });
        angka2Field.addKeyListener(new java.awt.event.KeyAdapter() {
            public void keyTyped(java.awt.event.KeyEvent evt) {
                angka2FieldKeyTyped(evt);
            }
        });

        jButton2.setText("HAPUS");
        jButton2.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton2ActionPerformed(evt);
            }
        });

        jButton3.setText("KELUAR");
        jButton3.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton3ActionPerformed(evt);
            }
        });

        javax.swing.GroupLayout jPanel1Layout = new javax.swing.GroupLayout(jPanel1);
        jPanel1.setLayout(jPanel1Layout);
        jPanel1Layout.setHorizontalGroup(
            jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(jPanel1Layout.createSequentialGroup()
                .addContainerGap()
                .addGroup(jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addGroup(jPanel1Layout.createSequentialGroup()
                        .addComponent(jButton1)
                        .addGap(18, 18, 18)
                        .addComponent(jButton2)
                        .addGap(18, 18, 18)
                        .addComponent(jButton3))
                    .addGroup(jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.TRAILING, false)
                        .addGroup(javax.swing.GroupLayout.Alignment.LEADING, jPanel1Layout.createSequentialGroup()
                            .addComponent(lblAngka1)
                            .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                            .addComponent(angka1Field, javax.swing.GroupLayout.PREFERRED_SIZE, 173, javax.swing.GroupLayout.PREFERRED_SIZE))
                        .addGroup(javax.swing.GroupLayout.Alignment.LEADING, jPanel1Layout.createSequentialGroup()
                            .addComponent(lblHasil)
                            .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                            .addComponent(hasilField, javax.swing.GroupLayout.PREFERRED_SIZE, 173, javax.swing.GroupLayout.PREFERRED_SIZE))
                        .addGroup(javax.swing.GroupLayout.Alignment.LEADING, jPanel1Layout.createSequentialGroup()
                            .addComponent(lblAngka2)
                            .addGap(18, 18, 18)
                            .addComponent(angka2Field, javax.swing.GroupLayout.PREFERRED_SIZE, 173, javax.swing.GroupLayout.PREFERRED_SIZE))))
                .addContainerGap(23, Short.MAX_VALUE))
        );
        jPanel1Layout.setVerticalGroup(
            jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(jPanel1Layout.createSequentialGroup()
                .addGap(17, 17, 17)
                .addGroup(jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(lblAngka1)
                    .addComponent(angka1Field, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE))
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.UNRELATED)
                .addGroup(jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(lblAngka2)
                    .addComponent(angka2Field, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE))
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.UNRELATED)
                .addGroup(jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(lblHasil)
                    .addComponent(hasilField, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE))
                .addGap(18, 18, 18)
                .addGroup(jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(jButton1)
                    .addComponent(jButton2)
                    .addComponent(jButton3))
                .addContainerGap(javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))
        );

        javax.swing.GroupLayout layout = new javax.swing.GroupLayout(getContentPane());
        getContentPane().setLayout(layout);
        layout.setHorizontalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(layout.createSequentialGroup()
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addGroup(layout.createSequentialGroup()
                        .addGap(59, 59, 59)
                        .addComponent(jLabel4))
                    .addGroup(layout.createSequentialGroup()
                        .addGap(28, 28, 28)
                        .addComponent(jPanel1, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)))
                .addContainerGap(32, Short.MAX_VALUE))
        );
        layout.setVerticalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(layout.createSequentialGroup()
                .addContainerGap()
                .addComponent(jLabel4)
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                .addComponent(jPanel1, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                .addContainerGap(30, Short.MAX_VALUE))
        );

        pack();
    }// </editor-fold>                        

    private void angka2FieldActionPerformed(java.awt.event.ActionEvent evt) {                                            
    }                                           

    private void jButton1ActionPerformed(java.awt.event.ActionEvent evt) {                                         
        try {
            double angka1 = Double.parseDouble(angka1Field.getText());
            double angka2 = Double.parseDouble(angka2Field.getText());
            double hasil = angka1 + angka2;
            if (hasil == (int) hasil) {
                 hasilField.setText(String.valueOf((int) hasil));
            } else {
                  hasilField.setText(String.valueOf(hasil));
            }
    } catch (NumberFormatException e) {
    JOptionPane.showMessageDialog(this, "Masukkan angka yang valid!",
        "Error", JOptionPane.ERROR_MESSAGE);
    }
    }                                        

    private void jButton2ActionPerformed(java.awt.event.ActionEvent evt) {                                         
    angka1Field.setText("");
    angka2Field.setText("");
    hasilField.setText("");
    angka1Field.requestFocus();
    }                                        

    private void jButton3ActionPerformed(java.awt.event.ActionEvent evt) {                                         
      System.exit(0);
    }                                        

    private void angka1FieldKeyTyped(java.awt.event.KeyEvent evt) {                                     
      char c = evt.getKeyChar();
      if (!Character.isDigit(c) && c != '.') {
            evt.consume();
       }
    }                                    

    private void angka2FieldKeyTyped(java.awt.event.KeyEvent evt) {                                     
     char c = evt.getKeyChar();
        if (!Character.isDigit(c) && c != '.') {
        evt.consume();
        }
    }                                    

    private void angka1FieldFocusGained(java.awt.event.FocusEvent evt) {                                        
        angka1Field.setText("");
    }                                       

    private void angka2FieldFocusGained(java.awt.event.FocusEvent evt) {                                        
      angka2Field.setText("");
    }                                       

    public static void main(String args[]) {
        try {
            for (javax.swing.UIManager.LookAndFeelInfo info : javax.swing.UIManager.getInstalledLookAndFeels()) {
                if ("Nimbus".equals(info.getName())) {
                    javax.swing.UIManager.setLookAndFeel(info.getClassName());
                    break;
                }
            }
        } catch (Exception ex) { }
        java.awt.EventQueue.invokeLater(new Runnable() {
            public void run() {
                new AplikasiTambahDuaAngka().setVisible(true);
            }
        });
    }

    private javax.swing.JTextField angka1Field;
    private javax.swing.JTextField angka2Field;
    private javax.swing.JTextField hasilField;
    private javax.swing.JButton jButton1;
    private javax.swing.JButton jButton2;
    private javax.swing.JButton jButton3;
    private javax.swing.JLabel jLabel4;
    private javax.swing.JPanel jPanel1;
    private javax.swing.JLabel lblAngka1;
    private javax.swing.JLabel lblAngka2;
    private javax.swing.JLabel lblHasil;
}
```
