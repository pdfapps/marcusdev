# 👋 Hi, I'm Marcus

Full-stack engineer building developer tools and mobile apps. Founder of **[MockMyData.io](https://mockmydata.io)** 

## 🔗 See it running

- 📱 **[Field service app template](https://github.com/mockmydata/field-service-app)** — sample mobile app for field techs, built with React Native + TypeScript on MockMyData.io. Clone it, `npm install`, `npx expo start` — runs immediately against a live demo workspace, no signup or config.
- 🧪 **[MockMyData playground](https://app.mockmydata.io/playground)** — try the platform itself in the browser.

## 🚀 Current Project

### [MockMyData.io](https://mockmydata.io)

SaaS platform that generates realistic mock REST APIs for frontend testing. Built and operated solo — live in production with paying-customer infrastructure.

**🛠️ Tech Deep Dive:**
- **Backend:** Django REST Framework with PostgreSQL for data persistence
- **Request pipeline:** Four-guard middleware — subdomain tenant resolution → three-path API key auth → atomic Redis quota enforcement → Redis health circuit breaker. Tenant isolation is enforced once in middleware rather than per-query, so a forgotten `WHERE` clause can never leak one customer's data to another.
- **Caching & quotas:** Redis for response caching and per-plan rate limiting, with quota state surfaced to clients via `X-Plan` / `X-Requests-*` headers
- **Frontend:** React + TypeScript dashboard with built-in API testing and backend code export
- **Payments:** Stripe webhooks for subscription lifecycle management
- **Security:** AI-powered subdomain validation to prevent brand impersonation

## 📦 Shipped Projects

### [Quick PDF Editor](https://play.google.com/store/apps/details?id=com.pdfapps.quickpdfeditor&hl)
Mobile PDF editing and merging app on Google Play — 📊 1,000+ downloads

**✨ Features:**
- Merge PDFs & images into single documents
- Scan documents with camera
- Edit pages: rotate, crop, reorder, delete, and draw
- Dark mode support

**🛠️ Tech Deep Dive:**
- **Framework:** React Native with custom native modules
- **Core innovation:** Modified react-native-pdf library to support advanced editing features
- **Performance:** Rotation, cropping, deletion, and drawing without re-rendering or flickering
- **Challenge solved:** Coordinate transformation system for real-time PDF manipulation
- **Native integration:** Custom Android modules in Kotlin using PDFBox

## 💻 Tech Stack

- **Backend:** Python • Django • Django REST Framework
- **Frontend:** React • TypeScript • JavaScript
- **Mobile:** React Native • Expo • Android • Kotlin
- **Cloud & Data:** Render • PostgreSQL • Redis
- **Payments:** Stripe

## 🔗 Connect

- 🐦 Twitter: [@mockdatas](https://twitter.com/mockdatas)
- 🌐 Website: [MockMyData.io](https://mockmydata.io)
