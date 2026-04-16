# Multica New - Next.js 16 Projesi

Bu proje Next.js 16, Tailwind CSS, shadcn/ui ve Prisma ile oluşturulmuş modern bir web uygulamasıdır.

## Teknolojiler

- **Next.js 16** (App Router)
- **TypeScript**
- **Tailwind CSS**
- **shadcn/ui** (Radix UI bileşenleri)
- **Prisma** (PostgreSQL ORM)
- **PostgreSQL**

## Kurulum

### Gereksinimler

- Node.js 20.9.0 veya üzeri
- PostgreSQL veritabanı

### Adımlar

1. Depoyu klonlayın:
```bash
git clone git@github.com:mbahadirs/multica_new.git
cd multica_new
```

2. Bağımlılıkları yükleyin:
```bash
npm install
```

3. `.env` dosyasını oluşturun ve veritabanı bağlantı bilgilerinizi ekleyin:
```env
DATABASE_URL="postgresql://kullanici:sifre@localhost:5432/veritabani_adi?schema=public"
NEXT_PUBLIC_API_URL="http://localhost:3000"
```

4. Prisma migrasyonlarını çalıştırın:
```bash
npx prisma migrate dev --name init
```

5. Geliştirme sunucusunu başlatın:
```bash
npm run dev
```

Uygulama [http://localhost:3000](http://localhost:3000) adresinde çalışacaktır.

## Proje Yapısı

```
multica_new/
├── app/                    # Next.js App Router sayfaları
├── components/             # React bileşenleri
├── lib/                    # Yardımcı fonksiyonlar ve Prisma client
├── prisma/                 # Prisma schema ve migrasyonlar
├── public/                 # Statik dosyalar
└── ...
```

## Prisma

Veritabanı şeması `prisma/schema.prisma` dosyasında tanımlanmıştır. Şu anda örnek bir `User` modeli içermektedir.

### Prisma Komutları

- Prisma Client'ı yeniden oluştur: `npx prisma generate`
- Yeni migrasyon oluştur: `npx prisma migrate dev --name migration_adi`
- Prisma Studio'yu aç: `npx prisma studio`

## Geliştirme

- `npm run dev` - Geliştirme sunucusunu başlatır
- `npm run build` - Production build oluşturur
- `npm run start` - Production sunucusunu başlatır
- `npm run lint` - ESLint kontrolü yapar

## shadcn/ui Bileşenleri

Yeni bileşenler eklemek için:

```bash
npx shadcn@latest add button
npx shadcn@latest add card
# vb.
```

## Lisans

MIT
