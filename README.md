# medibridge-platform
# Medipay Africa

**A Unified Health Wallet Solution for West Africa**  
**Integrating Paystack and Interswitch**  
**Enyata x Interswitch Buildathon 2026 – Health Track**

**Live Demo**: [https://medipay-frontend.vercel.app](https://medipay-frontend.vercel.app)  
**Frontend Repository**: [https://github.com/CeeJay33/medipay-frontend](https://github.com/CeeJay33/medipay-frontend)  
**Backend Repository**: [https://github.com/oluwaseun-Adesina/medipay-backend](https://github.com/oluwaseun-Adesina/medipay-backend)  
**Build Period**: March 23 – 26, 2026

## Problem We Are Solving

In West Africa (especially Nigeria and Ghana), healthcare remains extremely challenging due to:

- **High out-of-pocket (OOP) spending** — 60–70% of health costs are paid directly by patients, often leading to delayed or denied treatment.
- **Fragmented billing** — Patients must run between multiple departments (lab, pharmacy, surgery, admission) to collect and pay separate bills, wasting time and causing drop-offs.
- **Upfront payment barriers** — Public and private centres demand cash before service, even in emergencies.
- **Diaspora funding friction** — Relatives abroad send money via Wise, bank transfers, or cash apps, but the funds are not purpose-bound, often delayed, and families still struggle to confirm payment at the hospital.

**Competitor Analysis**  
While similar-sounding solutions exist, none match MediBridge’s West Africa-first design:  
- **Medipay (South Africa)** offers “Care Now, Pay Later” instalment financing with a repayment app. It is credit-focused and provider-oriented, lacks proactive micro-savings, has no Remita-style public-centre directory, and does not support hybrid Interswitch + Paystack or purpose-bound diaspora links.  
- **Helium Health (Nigeria)** is strong on provider EMR and clinic financing but is backend-heavy and does not give patients a personal savings-first wallet or unified public-centre bill directory.  
- **M-TIBA (East Africa)** is a health wallet with savings and remittances but runs on M-Pesa rails, has no West African gateway integration, and lacks our Remita-style unified bill creation for public hospitals.  

**Our unique standpoint**  
MediBridge is the only platform that combines:  
- A patient-owned **savings-first wallet** (digitising Adashe-style micro-savings)  
- A true **Remita-style unified bill directory** for public and private centres  
- **Hybrid Interswitch + Paystack** payments (mandatory Interswitch for instant provider settlement + Paystack for global cards and Ghana scalability)  
- **Purpose-bound diaspora funding** — relatives pay the exact hospital invoice directly, not loose cash  

This makes MediBridge the complete health-finance infrastructure West Africa has been missing.

Traditional HMOs cover only a small percentage of the population and involve rigid processes with reimbursement delays. There is currently **no single platform** that offers a Remita-style unified bill directory for healthcare, savings-first preparedness, instant provider settlements, and guaranteed diaspora-to-hospital payments.

## Our Solution

**MediBridge Africa** (powered by **MediWallet**) is a mobile-first web app that acts as the **complete healthcare payment infrastructure** for West Africa.

It integrates **Interswitch** (mandatory primary gateway for instant bill settlements via Quickteller) and **Paystack** (secondary gateway for international cards, Ghana mobile money, and recurring payments) to deliver a seamless, stress-free experience.

### How It Works (Remita-Style Unified Bills)

1. **Unified Bill Directory**  
   Open the app → Save, upload provider receipt or bill, pay from wallet or share link for someone to pay for you.  

   The app instantly creates **one single unified invoice**.

2. **Savings-First Payment**  
   Money in your Health Wallet (goal-based micro-savings like daily ₦100 Adashe-style contributions) is automatically deducted first.

3. **One-Tap Payment**  
   Pay the remaining amount once.  
   - **Interswitch** settles funds instantly to the hospital’s account.  
   - **Paystack** handles international cards (from anywhere in the world), Ghana flows, or cheaper routes.  
   The app auto-selects the best gateway.

4. **Diaspora Purpose-Bound Funding**  
   Relatives abroad receive a shareable link, see the exact unified invoice with every service listed, pay with international Visa/Mastercard via Paystack, and the money goes straight to the hospital via Interswitch — guaranteed for health use with full receipt proof.

**Key Benefits**:
- Patients avoid running between buildings for separate bills.
- Providers receive instant payment and better liquidity.
- Diaspora families get peace of mind — money is purpose-bound and traceable.
- No major behaviour change required from hospitals (manual reference entry or simple QR).

## Team Members

- **Backend Developer** — Oluwaseun Adesina (responsible for Interswitch & Paystack integrations, wallet logic, unified invoice engine, and payment webhooks)
- **Frontend Developer** — Joshua (built the responsive UI, directory, invoice builder, and diaspora share flow)
- **UI Designer** — Rebecca Adesina (designed the clean, mobile-first interface focused on simplicity and trust)
- **Product Researcher** — Grace Ghai (conducted user research on OOP barriers, diaspora needs, and hospital workflows across West Africa)

## Tech Stack

- **Frontend**: Next.js / React (deployed on Vercel)
- **Backend**: Node.js / Express
- **Database**: MongoDB (real-time wallet balances and invoices)
- **Payments**: 
  - Interswitch Sandbox (Quickteller Bills Payment API – mandatory)
- **Auth**: JWT 

## Roadmap

**MVP (Built during Buildathon – March 23–26, 2026)**  
- Directory of major centres + unified invoice builder  
- Savings-first wallet  
- Hybrid Interswitch + Paystack payments  
- Diaspora one-tap payment from anywhere  

**Phase 1 (Next 3–6 months)**  
- Expand to 100+ public centres via Interswitch biller partnerships  
- USSD support (*#384*662#)  
- Family sharing & group health pots  

**Phase 2 (6–12 months)**  
- Emergency Micro Health Credit (instant advances when savings are short)  
- Real-time bill pulling from partnered hospitals  

**Phase 3 (Long-term)**  
- Full regional expansion (Ghana, Senegal, Ivory Coast)  
- HMO premium top-ups and telemedicine integration  

## How to Run Locally

```bash
git clone https://github.com/yourusername/medibridge-africa.git
cd medibridge-africa
npm install
npm run dev
