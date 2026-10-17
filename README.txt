KESTREL K1 — LOSSLESS PERFORMANCE OPTIMIZATION

1. Put index.html at the root of the existing Vercel/GitHub project.
2. Copy the supplied assets/kestrel-static/ directory into the existing assets directory.
3. Keep your EXISTING assets/frame_000.jpg through frame_079.jpg as-is.
   These 80 frame files were not provided and are NOT included in this package.
4. Put vercel.json at your project root if you deploy directly to Vercel
   (merge its headers configuration with your existing vercel.json if any).
5. Deploy and use Lighthouse on MOBILE and DESKTOP, at least three runs each.

WHAT REMAINS IDENTICAL:
- All original CSS, including animations, durations, fonts, colors and layout.
- Exact original image bytes: all embedded PNG/WebP assets extracted without recompression.
- All 80 car-assembly frames, their order and the original rendering/masking code.
- The scrolling hanging "Build by Anshu" board and fixed DeLorean.
- Interactive controls and navigation, unchanged.

WHAT IS CHANGED UNDER THE HOOD:
- Heavy inline images moved into separately cacheable assets.
- The initial hero car image is preloaded with high priority.
- Press artwork / heritage picture load on demand (native loading=lazy).
- The 80-frame sequence only begins downloading when approaching the section.
- Static hashed assets get long-lived cache headers on Vercel.

The goal is improving all four Lighthouse scores, NOT a guarantee of 100/100.
The 2.5-second preloader, image transitions and animated design are deliberately
unchanged. They may limit possible mobile scores. A real deployed report is
needed to diagnose remaining accessibility, SEO and performance audits.
