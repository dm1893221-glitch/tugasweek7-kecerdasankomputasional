# tugasweek7-kecerdasankomputasional

#PROGRAM DECISION TREE SEDERHANA
#PRESENSI MAHASISWA

#Data mahasiswa
mahasiswa = [
    {"nama": "Andi", "kehadiran": "Tinggi", "tugas": "Lengkap"},
    {"nama": "Budi", "kehadiran": "Rendah", "tugas": "Tidak Lengkap"},
    {"nama": "Citra", "kehadiran": "Tinggi", "tugas": "Tidak Lengkap"},
    {"nama": "Deni", "kehadiran": "Rendah", "tugas": "Lengkap"},

    # Data mahasiswa baru
    {"nama": "Eka", "kehadiran": "Tinggi", "tugas": "Lengkap"}
]

print("=" * 55)
print("SISTEM PRESENSI MAHASISWA")
print(" Decision Tree Sederhana (IF - ELSE)")
print("=" * 55)

#fitur tambahan
jumlah_aktif = 0
jumlah_tidak_aktif = 0

#proses data
for data in mahasiswa:

    nama = data["nama"]
    kehadiran = data["kehadiran"]
    tugas = data["tugas"]

    # Decision Tree sederhana
    if kehadiran == "Tinggi":
        status = "Aktif"
        jumlah_aktif += 1
    else:
        status = "Tidak Aktif"
        jumlah_tidak_aktif += 1

    # pengecekan tambahan
    if kehadiran == "Tinggi" and tugas == "Lengkap":
        keterangan = "Mahasiswa Disiplin"
    else:
        keterangan = "Perlu Peningkatan"

    # output data
    print("\nNama        :", nama)
    print("Kehadiran   :", kehadiran)
    print("Tugas       :", tugas)
    print("Status      :", status)
    print("Keterangan  :", keterangan)

print("\n" + "=" * 55)

# fitur tambahan
print("Jumlah Mahasiswa Aktif       :", jumlah_aktif)
print("Jumlah Mahasiswa Tidak Aktif :", jumlah_tidak_aktif)

print("=" * 55)
print("Program selesai dijalankan.")
