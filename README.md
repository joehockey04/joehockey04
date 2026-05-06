<h1 align="center">Hi, I'm Joseph 👋</h1>                                                                                                    
                                                                                                                                               
  <p align="center">                                                                                                                           
   Student Want to be Full-stack engineer building <strong>Quro</strong> — the invisible checkout for dine-in restaurants.<br>                                   
    <em>Scan a QR. Tap to pay. Walk out.</em>                                                                                                  
  </p>

  <p align="center">
    <a href="https://quro.ca/login.html">
      <img alt="Live · Quro merchant console"
  src="https://img.shields.io/badge/Live-quro.ca%2Flogin.html-10b981?style=for-the-badge&logo=googlechrome&logoColor=white">
    </a>
    <a href="https://quro.ca/customer-promo.html">
      <img alt="Customer overview" src="https://img.shields.io/badge/Customer-Overview-0a0a0a?style=for-the-badge&logo=safari&logoColor=white">
    </a>
    <a href="mailto:joseph.picard@picanne.com">
      <img alt="Email" src="https://img.shields.io/badge/Contact-joseph.picard%40picanne.com-6366f1?style=for-the-badge&logo=maildotru&logoColor=white">
    </a>
  </p>

  ---

  ## 🍴 Featured · Quro

  A QR-based **invisible checkout** for restaurants and cafés. Customers scan the QR at their table, pay with Apple Pay or Google Pay in
  seconds, and walk out — no PIN-pad dance, no waiting on a terminal, no commissions to a delivery middleman.

  ### What it does

  - 🪄  **Sub-3-second checkout** at the dine-in table
  - 💸 **Direct Stripe rails** — zero platform commission for the merchant
  - 📊 **Live analytics** — revenue, AOV, tips, KDS prep time, SLA breaches
  - 🔔 **Real-time order queue** with audible ding + green flash on payment
  - 🇨🇦 **EN / FR bilingual**, built for Canadian merchants
  - 🛡️  **Customer checkout isolated** from third-party trackers (privacy-first)

  ### Tech stack

  ![Node.js](https://img.shields.io/badge/Node.js-20_LTS-339933?logo=node.js&logoColor=white)
  ![Express](https://img.shields.io/badge/Express-5-000000?logo=express&logoColor=white)
  ![Socket.io](https://img.shields.io/badge/Socket.io-4-010101?logo=socket.io&logoColor=white)
  ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-16-4169E1?logo=postgresql&logoColor=white)
  ![Knex](https://img.shields.io/badge/Knex.js-3-D26B38?logo=knexdotjs&logoColor=white)
  ![Tailwind](https://img.shields.io/badge/Tailwind-3-06B6D4?logo=tailwindcss&logoColor=white)
  ![Stripe](https://img.shields.io/badge/Stripe-Payments-635BFF?logo=stripe&logoColor=white)
  ![Nginx](https://img.shields.io/badge/Nginx-1.24-009639?logo=nginx&logoColor=white)
  ![PM2](https://img.shields.io/badge/PM2-5-2B037A?logo=pm2&logoColor=white)

  ### Architecture highlights

  - **Two-phase Stripe flow** — the QR creates an empty transaction shell first; the actual Stripe Checkout Session is only opened after the
  customer chooses a tip. Idempotent, refundable, and prevents partial-state ghosts.
  - **Two-brain architecture** — the merchant analytics surface holds deep telemetry; the customer checkout is *strictly* isolated from
  third-party trackers (CSP locked, no GTM, no pixels, no analytics on `/customer-*`).
  - **Server-side recompute on every checkout** — TPS 5% + TVQ 9.975% + tip recalculated server-side from DB prices with a 2¢ tolerance,
  rejecting cross-merchant ID injection.
  - **Real-time via Socket.io rooms** — `merchant_{id}` for dashboard + KDS, with payment events that ding and flash green at the exact table
  number.
  - **Production posture** — JWT in httpOnly cookies, double-submit CSRF, fail-closed Stripe webhook, hardened headers, Stripe-grade payment
  isolation.

  ### Try it

  | Surface | Link | What you'll see |
  |---|---|---|
  | 🔐 **Merchant console** | [quro.ca/login.html](https://quro.ca/login.html) | Sign-in to the operator dashboard (invite-only) |
  | 🎯 **Pitch / overview** | [quro.ca/promo.html](https://quro.ca/promo.html) | The merchant story — why scan-to-pay beats terminals |
  | 📱 **Customer overview** | [quro.ca/customer-promo.html](https://quro.ca/customer-promo.html) | "Skip the line. Scan to leave." |
  | 📚 **Guest guide** | [quro.ca/customer-guide.html](https://quro.ca/customer-guide.html) | 8-chapter how-to for diners |

  > *Source code is private during early-access launch — request a walkthrough by [email](mailto:hello@quro.ca).*

  ---

  ## 📫 Get in touch

  - 🌐 **Website** — [quro.ca](https://quro.ca)
  - 📧 **Email** — [joseph.picard@picanne.com](mailto:joseph.picard@picanne.com)
  - 💼 **Open to** — partnerships, technical interviews, founding-engineer chats
