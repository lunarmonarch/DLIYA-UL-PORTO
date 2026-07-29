# Portofolio — Muhammad Dliya'ul Haq

Project ini dibangun mengikuti **Blueprint-Portofolio-Muhammad-Dliyaul-Haq.md** (Milestone M1: Setup & Design System).

## Menjalankan di Komputer Anda

Karena environment ini tidak punya akses internet untuk instalasi package, jalankan langkah berikut **di komputer Anda sendiri** (pastikan Node.js 18+ sudah terpasang):

```bash
# 1. Masuk ke folder project
cd portfolio

# 2. Install dependencies
npm install

# 3. Jalankan development server
npm run dev
```

Lalu buka `http://localhost:3000` — Anda akan melihat halaman **Design System Preview** yang menampilkan palet warna, tipografi, button, badge, dan card sesuai Blueprint.

## Struktur Project

```
portfolio/
├── app/
│   ├── layout.tsx      # Root layout + setup font (Plus Jakarta Sans & Inter)
│   ├── page.tsx         # Style-guide preview (sementara, akan diganti Home di M2)
│   └── globals.css      # Base styles, focus ring, reduced-motion support
├── components/
│   └── ui/
│       ├── Button.tsx    # Button (primary/secondary/outline) + micro-interaction
│       ├── Badge.tsx     # Badge/chip untuk skill tags & status
│       └── Card.tsx      # Card + varian ComingSoonCard (shimmer effect)
├── lib/
│   └── data.ts           # Data profil, skill, sertifikasi (sumber tunggal konten)
├── tailwind.config.ts    # Design tokens: warna, font, spacing, shadow
└── package.json
```

## Design Tokens yang Sudah Diimplementasikan

- **Warna**: `primary` (#1E3A8A), `primary-light` (#3B82F6), `ink`, `surface`, `success`, `pending` — lihat `tailwind.config.ts`
- **Font**: `font-heading` (Plus Jakarta Sans) untuk judul, `font-body` (Inter) untuk teks — di-load via `next/font` agar tidak ada layout shift
- **Aksesibilitas**: focus ring terlihat untuk navigasi keyboard, dan seluruh animasi menghormati `prefers-reduced-motion`

## Langkah Selanjutnya (M2)

Setelah Anda menjalankan project ini dan mengonfirmasi tampilan design system sudah sesuai, kita lanjut ke **M2: Home Page** — Hero section, highlight skill, preview pengalaman, dan project card dengan animasi scroll-reveal penuh, menggantikan halaman style-guide ini.

## Deploy ke Vercel (Gratis)

1. Push project ini ke GitHub.
2. Buka [vercel.com](https://vercel.com), sign in dengan akun GitHub.
3. Klik "New Project", pilih repo ini, klik Deploy.
4. Website otomatis online di `nama-project.vercel.app`.
