# Next.js 15/16 App Router Technical SEO & AI Visibility Checklist (2026)

A practical, copy-and-paste reference for configuring **Next.js App Router (`Metadata` API)**, **JSON-LD structured data**, **AI crawler `robots.txt` rules (`OAI-SearchBot` vs `GPTBot`)**, **`/llms.txt` markdown indexes**, and **Google Search Console RE2 regex filters**.

## Live Interactive Generators (Free, No Signup)

- **[Next.js Metadata API Code Generator](https://www.nitroserp.com/tools/nextjs-metadata-generator)** — Generate typed `export const metadata: Metadata` and `generateMetadata()` TypeScript snippets.
- **[Free `/llms.txt` Generator for AI Search](https://www.nitroserp.com/tools/llms-txt-generator)** — Create a spec-compliant `/llms.txt` file for ChatGPT, Claude, and Perplexity discovery.
- **[Google Search Console (GSC) RE2 Regex Generator](https://www.nitroserp.com/tools/gsc-regex-generator)** — Build RE2 regular expressions for question queries, 4+ word long-tail keywords, and brand exclusions.
- **[JSON-LD Schema Markup Generator](https://www.nitroserp.com/tools/schema-markup-generator)** — Generate validated `Article`, `BreadcrumbList`, and `FAQPage` JSON-LD scripts.
- **[AI Crawler `robots.txt` Generator](https://www.nitroserp.com/tools/robots-txt-generator)** — Configure `Googlebot`, `OAI-SearchBot`, `PerplexityBot`, and `GPTBot`.
- **[Google SERP Snippet Simulator](https://www.nitroserp.com/tools/serp-preview)** — Preview desktop truncation and check title/description lengths.
- **[HTML & Live HTTP Status Link Checker](https://www.nitroserp.com/tools/broken-link-finder)** — Audit `<a href>` attributes and check live 200/301/404 responses.

---

## 1. Next.js App Router `Metadata` Boilerplate (`app/page.tsx`)

Use the [Next.js Metadata Generator](https://www.nitroserp.com/tools/nextjs-metadata-generator) to customize this block:

```tsx
import type { Metadata } from "next";

export const metadata: Metadata = {
  metadataBase: new URL("https://www.nitroserp.com"),
  title: "Free Next.js Metadata Generator | NitroSERP",
  description:
    "Generate strongly-typed Next.js App Router Metadata objects with canonical URLs, Open Graph images, and Twitter cards.",
  alternates: {
    canonical: "/tools/nextjs-metadata-generator",
  },
  openGraph: {
    title: "Free Next.js Metadata Generator | NitroSERP",
    description:
      "Generate strongly-typed Next.js App Router Metadata objects with canonical URLs, Open Graph images, and Twitter cards.",
    url: "https://www.nitroserp.com/tools/nextjs-metadata-generator",
    siteName: "NitroSERP",
    type: "website",
  },
  twitter: {
    card: "summary_large_image",
    title: "Free Next.js Metadata Generator | NitroSERP",
  },
};
```

---

## 2. Allow ChatGPT Search (`OAI-SearchBot`) While Blocking AI Training (`GPTBot`)

Read the full [OAI-SearchBot vs. GPTBot guide](https://www.nitroserp.com/blog/oai-searchbot-vs-gptbot-robots-txt) or build your file in the [robots.txt generator](https://www.nitroserp.com/tools/robots-txt-generator):

```txt
User-agent: *
Disallow: /api/

User-agent: OAI-SearchBot
Allow: /

User-agent: PerplexityBot
Allow: /

User-agent: GPTBot
Disallow: /

User-agent: Google-Extended
Disallow: /

Sitemap: https://www.nitroserp.com/sitemap.xml
```

---

## 3. Useful Google Search Console RE2 Regex Filters

Generate custom filters in the [GSC Regex Generator](https://www.nitroserp.com/tools/gsc-regex-generator):

| Filter Goal | RE2 Pattern |
|---|---|
| **Question Queries** | `(?i)^(who|what|where|when|why|how|can|does|is|are|should)\b` |
| **4+ Word Long-Tail Queries** | `^(\S+\s+){3,}\S+$` |
| **Commercial & Tool Intent** | `(?i)\b(best|vs|alternative|review|pricing|free|tool|generator|checker)\b` |

---

## More Technical SEO Guides

- [YouTube SEO Checklist 2026: Titles, Descriptions & Tags](https://www.nitroserp.com/blog/youtube-seo-titles-descriptions-tags-2026)
- [FAQ Schema in 2026: What Still Works](https://www.nitroserp.com/blog/faq-schema-2026-what-still-works)
- [Fix Breadcrumb Schema Missing Field `item` Error](https://www.nitroserp.com/blog/breadcrumb-schema-missing-field-item)
- [ChatGPT Brand Visibility Audit Guide](https://www.nitroserp.com/blog/ai-visibility-checker-chatgpt-2026)
- [Fix "Sitemap Could Not Be Read" & "Couldn't Fetch" in GSC](https://www.nitroserp.com/blog/fix-sitemap-could-not-be-read-gsc) — Next.js `app/sitemap.ts`, Cloudflare Bot Fight Mode, and XML namespace debugging
- [Next.js App Router Metadata API, OpenGraph & JSON-LD Guide (2026)](https://www.nitroserp.com/blog/nextjs-app-router-metadata-guide-2026)
- [12 Google Search Console Regex Filters (RE2 Copy-Paste Guide 2026)](https://www.nitroserp.com/blog/google-search-console-regex-filters-2026)
