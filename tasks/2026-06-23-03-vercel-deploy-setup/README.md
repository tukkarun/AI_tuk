# #03 — ตั้งค่า deploy ขึ้น Vercel (ทีม tukkaruns-projects)

- **วันที่สั่ง:** 2026-06-23
- **สถานะ:** ✅ done

## โจทย์

> https://vercel.com/tukkaruns-projects
> ทุกครั้งที่อัพงานขึ้น อัพงานขึ้นที่นี่ทุกครั้ง

## สิ่งที่ทำ

- ติดตั้ง Vercel CLI v54.15.0 (`npm i -g vercel`) — อยู่ที่ `~/.bizdrive-tools/node-v20.20.2-darwin-arm64/bin/vercel`
- Login ผ่าน device flow สำเร็จเป็น `tukkarun` (token เก็บใน `~/Library/Application Support/com.vercel.cli/`)
- ตั้ง default scope เป็นทีม **`tukkaruns-projects`** (`currentTeam`) → deploy ลงทีมนี้ทุกครั้ง

## วิธี deploy งานในอนาคต

```bash
export PATH="$HOME/.bizdrive-tools/node-v20.20.2-darwin-arm64/bin:$PATH"
cd <โฟลเดอร์งาน>
vercel --yes              # preview deploy (ลงทีม tukkaruns-projects อัตโนมัติ)
vercel --prod --yes       # production deploy
```

## หมายเหตุ

- ยังไม่มีงานเว็บที่ deploy ได้ ณ ตอนนี้ (AI_tuk เก็บแค่ task log) — งานนี้คือการตั้งค่าให้พร้อม
- พองานไหนเป็นเว็บ/แอปที่ deploy ได้ → จะ deploy ขึ้น Vercel ทีม tukkaruns-projects ให้ทุกครั้ง
