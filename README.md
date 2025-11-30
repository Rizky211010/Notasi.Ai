<div align="center">

# 🎵 Notasi.AI - Music Notation Converter

### Ubah Notasi Musik dalam Hitungan Detik dengan AI

[![Next.js](https://img.shields.io/badge/Next.js-16-black?style=for-the-badge&logo=next.js)](https://nextjs.org/)
[![React](https://img.shields.io/badge/React-19-61DAFB?style=for-the-badge&logo=react)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?style=for-the-badge&logo=typescript)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-4-38B2AC?style=for-the-badge&logo=tailwind-css)](https://tailwindcss.com/)
[![Express](https://img.shields.io/badge/Express-4-000000?style=for-the-badge&logo=express)](https://expressjs.com/)

<p align="center">
  <img src="public/demo.gif" alt="Notasi.AI Demo" width="600">
</p>

[Demo Langsung](https://notasi.ai) · [Laporkan Bug](https://github.com/username/notasi-ai/issues) · [Minta Fitur](https://github.com/username/notasi-ai/issues)

</div>

---

## ✨ Fitur Utama

| Fitur | Deskripsi |
|-------|-----------|
| 🔄 **Konversi Dua Arah** | Not Balok ↔ Not Angka dengan akurasi tinggi |
| 🤖 **AI-Powered** | Menggunakan GPT-4 Vision untuk pengenalan notasi musik |
| 📄 **Multi-Format** | Support PDF, PNG, JPG, XML, dan MIDI |
| ⚡ **Super Cepat** | Proses konversi < 5 detik |
| 🎨 **Modern UI** | Interface bersih dengan dark/light mode |
| 🔐 **Autentikasi** | Sistem login dengan JWT & Supabase |
| 📱 **Responsive** | Optimal di desktop, tablet, dan mobile |

## 🎯 Untuk Siapa?

- 🎹 **Arranger Musik** - Konversi partitur dengan cepat
- 🎤 **Paduan Suara** - Ubah format notasi sesuai kebutuhan
- 📚 **Pendidik Musik** - Buat materi pembelajaran
- 🎵 **Musisi** - Baca notasi dalam format yang familiar

## 🛠️ Tech Stack

### Frontend
- **Framework:** Next.js 16 dengan Turbopack
- **UI:** React 19 + Tailwind CSS 4
- **Icons:** Lucide React
- **Language:** TypeScript 5

### Backend
- **Runtime:** Node.js + Express.js
- **Database:** Supabase (PostgreSQL)
- **AI Engine:** OpenRouter API (GPT-4 Vision)
- **Auth:** JWT + bcrypt
- **File Processing:** Sharp, Multer, PDF-Poppler

## 📂 Struktur Proyek

```
notasi-ai/
├── 📁 app/                    # Next.js App Router
│   ├── 📁 components/         # Komponen React
│   │   ├── 📁 ui/             # Komponen UI dasar
│   │   ├── AIProcessingModal  # Modal proses AI
│   │   ├── AudioPlayer        # Pemutar audio
│   │   ├── ScoreViewer        # Penampil partitur
│   │   └── UploadArea         # Area upload file
│   ├── 📁 context/            # React Context
│   ├── 📁 lib/                # Utility functions
│   ├── 📁 pages/              # Halaman aplikasi
│   ├── layout.tsx             # Layout utama
│   └── page.tsx               # Halaman utama
│
├── 📁 backend/                # Backend API
│   └── 📁 src/
│       ├── 📁 config/         # Konfigurasi
│       ├── 📁 controllers/    # Request handlers
│       ├── 📁 middleware/     # Express middleware
│       ├── 📁 models/         # Data models
│       ├── 📁 routes/         # API routes
│       ├── 📁 services/       # Business logic
│       └── app.ts             # Entry point
│
└── 📁 public/                 # Static assets
```

## 🚀 Instalasi & Setup

### Prerequisites

- Node.js 18+ 
- npm atau yarn
- Akun Supabase (untuk database)
- OpenRouter API Key (untuk AI)

### 1. Clone Repository

```bash
git clone https://github.com/username/notasi-ai.git
cd notasi-ai
```

### 2. Install Dependencies

```bash
# Frontend
npm install

# Backend
cd backend
npm install
```

### 3. Konfigurasi Environment

Buat file `.env` di folder `backend/`:

```env
# Server
PORT=5000
NODE_ENV=development

# Database (Supabase)
SUPABASE_URL=your_supabase_url
SUPABASE_ANON_KEY=your_supabase_anon_key

# AI Service (OpenRouter)
OPENROUTER_API_KEY=your_openrouter_api_key
OPENROUTER_BASE_URL=https://openrouter.ai/api/v1
OPENROUTER_MODEL=openai/gpt-4o-mini

# JWT
JWT_SECRET=your_jwt_secret
JWT_EXPIRES_IN=7d
```

### 4. Jalankan Aplikasi

```bash
# Terminal 1 - Frontend
npm run dev

# Terminal 2 - Backend
cd backend
npm run dev
```

Buka [http://localhost:3000](http://localhost:3000) untuk melihat aplikasi.

## 📡 API Endpoints

### Authentication
| Method | Endpoint | Deskripsi |
|--------|----------|-----------|
| POST | `/api/auth/register` | Registrasi user baru |
| POST | `/api/auth/login` | Login user |
| GET | `/api/auth/me` | Get current user |

### Conversion
| Method | Endpoint | Deskripsi |
|--------|----------|-----------|
| POST | `/api/conversion/balok-to-angka` | Konversi not balok ke angka |
| POST | `/api/conversion/angka-to-balok` | Konversi not angka ke balok |
| GET | `/api/conversion/history` | Riwayat konversi |

### File
| Method | Endpoint | Deskripsi |
|--------|----------|-----------|
| POST | `/api/file/upload` | Upload file |
| GET | `/api/file/:id` | Download file |

## 🎨 Screenshots

<div align="center">
<table>
  <tr>
    <td><img src="public/screenshots/home.png" alt="Home" width="400"></td>
    <td><img src="public/screenshots/converter.png" alt="Converter" width="400"></td>
  </tr>
  <tr>
    <td align="center"><b>Halaman Utama</b></td>
    <td align="center"><b>Halaman Konversi</b></td>
  </tr>
</table>
</div>

## 🔮 Roadmap

- [ ] Export ke MusicXML
- [ ] Playback audio MIDI
- [ ] Transpose otomatis
- [ ] Kolaborasi real-time
- [ ] Mobile app (React Native)
- [ ] Plugin untuk MuseScore

## 🤝 Kontribusi

Kontribusi sangat diterima! Silakan buka issue atau pull request.

1. Fork repository
2. Buat branch fitur (`git checkout -b feature/FiturBaru`)
3. Commit perubahan (`git commit -m 'Menambah FiturBaru'`)
4. Push ke branch (`git push origin feature/FiturBaru`)
5. Buka Pull Request

## 📄 Lisensi

Didistribusikan di bawah Lisensi MIT. Lihat `LICENSE` untuk informasi lebih lanjut.

## 📞 Kontak

**Developer:** [Nama Anda]

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/username)
[![Twitter](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/username)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:email@example.com)

---

<div align="center">

**⭐ Jika proyek ini membantu, berikan bintang di GitHub! ⭐**

Made with ❤️ in Indonesia

</div>
