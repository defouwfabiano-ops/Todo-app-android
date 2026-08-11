# Todo App - Local Storage To-Do List Application

**Aplikasi To-Do List Android dengan Local Storage menggunakan SQLite**

## ✨ Fitur Lengkap

### ✅ Main Features
- **Add To-Do** - Tambah tugas baru dengan detail lengkap
- **Edit To-Do** - Edit tugas yang sudah ada
- **Delete To-Do** - Hapus tugas dengan konfirmasi
- **Mark Complete** - Tandai tugas sebagai selesai dengan checkbox
- **Filter** - Filter berdasarkan All/Active/Completed
- **Priority Levels** - HIGH (Red), MEDIUM (Orange), LOW (Green)
- **Categories** - Work, Personal, Shopping, Health, Other
- **Due Date** - Pilih tanggal deadline untuk setiap tugas
- **Descriptions** - Tambahkan deskripsi detail untuk tugas
- **Local Storage** - Semua data tersimpan di SQLite database
- **Active Counter** - Tampil jumlah tugas yang masih aktif
- **Persistent Data** - Data tetap tersimpan setelah app ditutup

### ✅ Database Features
- Auto-increment ID
- Timestamp (Created At)
- Boolean completed status
- Full-text search ready
- Optimized queries dengan sorting

---

## 📁 Project Structure

```
todo-app-android/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/example/todoapp/
│   │   │   │   ├── activities/
│   │   │   │   │   ├── MainActivity.java
│   │   │   │   │   └── AddEditTodoActivity.java
│   │   │   │   ├── models/
│   │   │   │   │   └── TodoItem.java
│   │   │   │   ├── database/
│   │   │   │   │   └── TodoDatabaseHelper.java
│   │   │   │   ├── adapters/
│   │   │   │   │   └── TodoAdapter.java
│   │   │   │   └── helpers/
│   │   │   │       └── PreferencesManager.java
│   │   │   ├── res/
│   │   │   │   ├── layout/
│   │   │   │   │   ├── activity_main.xml
│   │   │   │   │   ├── activity_add_edit_todo.xml
│   │   │   │   │   └── item_todo.xml
│   │   │   │   ├── values/
│   │   │   │   │   ├── colors.xml
│   │   │   │   │   ├── strings.xml
│   │   │   │   │   ├── dimens.xml
│   │   │   │   │   └── styles.xml
│   │   │   │   └── drawable/
│   │   │   │       ├── btn_bg_primary.xml
│   │   │   │       ├── btn_bg_secondary.xml
│   │   │   │       ├── btn_bg_danger.xml
│   │   │   │       ├── edit_text_bg.xml
│   │   │   │       └── card_bg.xml
│   │   │   └── AndroidManifest.xml
│   │   └── test/
│   └── build.gradle
├── build.gradle
├── settings.gradle
├── .gitignore
└── README.md
```

---

## 🚀 Setup di Aide

### 1. Clone Repository
```bash
git clone https://github.com/defouwfabiano-ops/todo-app-android.git
cd todo-app-android
```

### 2. Buka di Aide
- Buka **Aide**
- Pilih **"Open Project"**
- Navigate ke folder `todo-app-android`
- Tunggu Gradle sync

### 3. Run Aplikasi
- Klik **▶ Run** atau `Ctrl+R`
- Pilih emulator/device
- Tunggu compile & install

### 4. Test Aplikasi
✅ Tap **+** button untuk tambah to-do baru  
✅ Isi title, deskripsi (optional), priority, kategori  
✅ Pilih due date dengan date picker  
✅ Tap **Save** untuk simpan  
✅ Centang checkbox untuk mark complete  
✅ Tap edit button untuk ubah to-do  
✅ Tap delete button untuk hapus  
✅ Gunakan filter spinner untuk filter todos  

---

## 📊 Teknologi Stack

| Aspek | Teknologi |
|-------|----------|
| **Platform** | Android |
| **Bahasa** | Java |
| **Database** | SQLite |
| **UI** | XML Layouts + RecyclerView |
| **API Level** | Target 33, Min 21 |
| **IDE** | Aide / Android Studio |

---

## 💾 Data Model

### TodoItem Class
```java
- id: int (Primary Key)
- title: String (Required)
- description: String (Optional)
- completed: boolean
- createdAt: long (Timestamp)
- dueDate: long (Timestamp)
- priority: String (HIGH, MEDIUM, LOW)
- category: String (Work, Personal, Shopping, etc)
```

---

## 🔍 Database Queries

- **getAllTodoItems()** - Get semua todos sorted by status & priority
- **getActiveTodos()** - Get todos yang belum completed
- **getCompletedTodos()** - Get todos yang sudah completed
- **getTodosByCategory()** - Filter by category
- **getTodoItemById()** - Get specific todo by ID
- **getActiveTodoCount()** - Count active todos
- **addTodoItem()** - Insert new todo
- **updateTodoItem()** - Update existing todo
- **deleteTodoItem()** - Delete todo by ID

---

## 🎨 UI Features

- 🎯 Clean & minimal design
- 🌈 Color-coded priorities
- 📱 Responsive layout
- ⚡ Smooth animations
- ♿ User-friendly interface
- 🎭 Material Design principles

---

## 🚧 Future Enhancements

- [ ] Cloud sync dengan Firebase
- [ ] Dark mode support
- [ ] Push notifications untuk due date
- [ ] Recurring todos (daily, weekly, monthly)
- [ ] Search/filter by text
- [ ] Export to PDF/CSV
- [ ] Subtasks support
- [ ] Tags/Labels
- [ ] Time-based reminders
- [ ] Widget untuk home screen
- [ ] Backup & restore
- [ ] Multi-language support

---

## 📝 Notes

- Semua data disimpan di **SQLite database** lokal
- Tidak perlu internet connection
- Database file tersimpan di internal storage
- Saat uninstall, data akan terhapus (gunakan backup jika perlu)

---

## 🐛 Troubleshooting

**Q: App tidak bisa di-run?**
A: Pastikan Gradle sync sudah selesai dan semua dependencies ter-install

**Q: Data hilang setelah app ditutup?**
A: Data seharusnya tersimpan. Cek logcat untuk error database

**Q: Emulator error?**
A: Coba gunakan device fisik atau reset emulator

---

## 📧 Support

Jika ada issue atau pertanyaan, silakan buka issue di repository ini.

---

**Dibuat dengan ❤️ untuk produktivitas yang lebih baik**

*Version: 1.0.0*
*Last Updated: 2024*
