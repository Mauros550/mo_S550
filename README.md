__Mo_s550_

An immersive, sponsor-ready website showcasing my 2021 Mustang GT. Explore a 3D walk-through, hear exhaust clips, view the full mod list, and request partnerships — all in one clean, fast experience.

✨ What makes it different

3D Walk-Through: Glide around the car using a WebGL scene (react-three-fiber). Hotspots pop up specs, parts, and stories.

360° Cabin & Exterior: Tap to enter 360 photos from the Insta360 (Pannellum/React 360 viewer).

Live Mod Timeline: Interactive timeline with before/after sliders.

Soundboard: Exhaust clips (idle, 3k, redline, drive-bys) with spectrogram visual.

Build Sheet: Filterable parts list with vendors, prices, and install notes.

Sponsor Hub: One-click Media Kit + Partnership Request (email form + auto-generated PDF).

Performance First: Progressive loading, image optimization, Lighthouse ≥90.

Demo/GIF Placeholder: docs/demo.gif (add later)

🧠 Tech Stack

Frontend: Next.js (App Router), React 18, TypeScript

3D: Three.js via react-three-fiber + drei; optional GLTF models (photogrammetry or CAD)

Animations: Framer Motion, GSAP (optional)

360 Viewer: Pannellum or react-360-view

Styling/UI: Tailwind CSS + shadcn/ui

Forms: React Hook Form + Zod; email via Resend/SendGrid or Vercel Serverless

Assets: Next/Image, sharp, next-sitemap for SEO

Analytics: Vercel Analytics or Plausible

Deployment: Vercel (Preview → Production)

🗺️ Site Map

/ — Hero + 3D car reveal + quick stats

/build — Parts, install notes, brands, receipts (optional)

/gallery — 360s, photo sets, reels

/sound — Exhaust board + dyno graph (static or simulated)

/timeline — Mod history + before/after sliders

/about — Who I am, what I stand for

/sponsor — Media kit + partnership form

/contact — Direct message form + socials
📁 Project Structure
/src
  /app
    /(marketing)
      page.tsx
      about/page.tsx
      sponsor/page.tsx
      contact/page.tsx
    /build/page.tsx
    /gallery/page.tsx
    /sound/page.tsx
    /timeline/page.tsx
    /api/contact/route.ts
    /api/partner/route.ts
  /components
    CanvasScene.tsx
    Hotspot.tsx
    PartCard.tsx
    SoundPlayer.tsx
    BeforeAfter.tsx
    MediaKit.tsx
  /lib
    content.ts            # content model + helpers
    seo.ts
    analytics.ts
  /data
    build.json            # parts list
    clips.json            # audio metadata
    hotspots.json         # 3D hotspot data
/public
  /models                 # GLTF/GLB
  /images                 # optimized images
  /360                    # equirectangular 360s
