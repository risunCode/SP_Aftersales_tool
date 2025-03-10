## **Repair NVDATA & Fix IMEI 1 / IMEI 2 Null pada Xiaomi MediaTek**

**Ditulis oleh:** risunturu  
**Arsip repositori:** [GitHub - SP Aftersales Tool](https://github.com/risunCode/SP_Aftersales_tool)

### **Bahan yang Dibutuhkan**
1. **ENG ROM Xiaomi** – Cari di Telegram/Google  
   📌 [ENG ROM Telegram](https://t.me/xiaomiengs) (Gunakan codename perangkat)  
2. **File md1img** (Diambil dari stock ROM, bukan ENG ROM)  
3. **Modem META (MAUIMETA)** – [Download](https://androidmtk.com/download-sp-meta-tool)  
4. **Minimal ADB Fastboot / 15 Second ADB Installer** – [Download](https://github.com/risunCode/SP_Aftersales_tool/releases/download/Mediatek_Drivers/15.Second.ADB.Installer.v1.5.6.exe)  
5. **SP Flashtool** – Digunakan untuk flash ENG ROM  
6. **TFTUNLOCK** – Untuk flash ROM original  
7. **MTK Bypass & LIB USB Filter** – [Download](https://github.com/risunCode/SP_Aftersales_tool)  
8. **Custom ROM** (Opsional)  

---

### **Langkah 1: Unbrick & Persiapan**
1. **Flash ENG ROM** menggunakan **SP Flashtool (SPFT)**.  
2. Setelah proses flashing selesai, **jangan langsung nyalakan HP, kalau udah nyala matiin aja & cabut kabel dari pc.**.
3. Lanjut ke langkah 2
![image](https://github.com/user-attachments/assets/89778282-7450-4d9e-896e-cccfbc1358d7)

---

### **Langkah 2: Erase NVDATA & NVRAM**
1. Buka **ModemMETA**, lalu klik **Connect**.  
2. Masuk **Fastboot Mode** dengan perintah di **Minimal ADB and Fastboot**:
   ![image](https://github.com/user-attachments/assets/625c69cd-9b20-45f9-b270-0216d7f39978)

   ```
   fastboot erase nvdata
   ```
   ```
   fastboot erase nvram
   ```
   ```
   fastboot reboot
   ```
   ⚠ **Jangan tutup ModemMETA selama proses ini!**
   ![image](https://github.com/user-attachments/assets/816be55e-6b3c-4c33-99f1-3da7c3481db6)

4. Setelah reboot, ModemMETA akan otomatis mendeteksi perangkat (tunggu hingga progress bar 100%).  

### **Jika Stuck di Proses Ini:**
- Matikan HP.  
- Gunakan **Android Utility v170**, lalu klik **Reboot META**.
  ![image](https://github.com/user-attachments/assets/faa8d007-5c04-468a-b2d5-c7288af39d91)

- Tekan **Volume Down**, lalu colok USB ke PC hingga masuk ke mode META.  
- Kembali ke **MAUIMETA**, pilih **More DUT in META Mode**, lalu klik **Connect** dan tunggu hingga tersambung.  

---

### **Langkah 3: Restore IMEI**
![image](https://github.com/user-attachments/assets/ecf3df53-438e-40d0-8695-5e769334ab2e)

1. Setelah HP connected di ModemMETA, tekan **LOAD DB > From Target**.  
2. Cari **IMEI DOWNLOAD** di kolom pencarian.
   ![image](https://github.com/user-attachments/assets/c1aa9e72-9945-4216-aab6-08b17b674057)

4. Masukkan **IMEI 1** dan **IMEI 2** perangkat (1 digit terakhir akan masuk sebagai checksum).  
5. Klik **WRITE**, tunggu hingga proses selesai.
   ![image](https://github.com/user-attachments/assets/3b853025-79ca-4846-82df-5e30e2256343)

7. Jika sukses, klik **Disconnect** dan cabut perangkat.  

---

### **Langkah 4: Flash ROM Original**
1. Matikan HP, **jangan nyalakan dulu**.  
2. Flash **ROM Fastboot ORIGINAL** via **TFT Unlock/SPFT!**).  
3. **Uncheck** bagian **Preloader, Cust, Exaid**, lalu flash ROM.  
4. Setelah selesai, **cabut USB** (Jangan langsung nyalakan HP!).  

---

### **Langkah 5: Unlock Bootloader (UBL)**
![image](https://github.com/user-attachments/assets/1c543652-9acb-4570-9a58-f9e670cc1739)

1. Buka **Xiaomi Bootloader Tool**.  
2. Pilih model HP atau gunakan **Auto Detect**.  
3. Klik **Bootloader Unlock 1**.  
4. Tekan **Volume Up + Volume Down + Power**, lalu colok USB ke PC.  
5. Tunggu hingga proses selesai.  
6. Setelah UBL sukses, lanjut masuk ke **Fastboot Mode** (**Power + Volume Down**).  

---

### **Langkah 6: Flash md1img.img (Modem File)**
1. Flash **md1img.img** dari stock ROM fastboot ORI dengan perintah:  
   ```
   fastboot flash md1img md1img.img
   ```
   ```
   fastboot reboot
   ```
2. HP akan reboot secara otomatis.  

---

### **Langkah 7: Backup NVDATA (Opsional)**
1. Setelah masuk ke sistem, matikan HP.  
2. Colok USB, tahan **Volume Up + Volume Down** hingga proses backup selesai.  

---

### **Kesimpulan**
- Metode ini berlaku untuk **Chip MediaTek**.   

✅ **DONE! Siahkan cek imei anda!** 🎉  
 
