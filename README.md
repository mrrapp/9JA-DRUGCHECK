<div align="center">

# 💊 DrugCheck NG
*https://f34ea4a0.mydala.app*

### Verify Before You Buy.

An AI-ready digital health platform helping Nigerians verify medicines, spot counterfeit drugs, report suspicious products, and locate licensed pharmacies.

*Built for the 3MTT Product Showcase*

</div>

---

## 📖 About The Project

Counterfeit and substandard medicines remain a major public health risk in Nigeria. Many people:

- Have no easy way to verify a medicine before buying it
- Unknowingly purchase fake or substandard drugs
- Don't know where to report suspicious products
- Lack access to trusted, plain-language medicine information
- Struggle to find licensed pharmacies nearby

**DrugCheck NG** is a mobile-first Progressive Web App (PWA) built to close that gap — giving patients, parents, students, healthcare workers, pharmacists, and vendors a simple way to check what they're taking, report what's suspicious, and find help nearby.

>  **Disclaimer:** DrugCheck NG provides educational information only and does not verify the physical authenticity of any medicine. It is not a substitute for professional medical advice. Always consult a licensed pharmacist or doctor for medical decisions.

---

##  Target Users

Patients · Parents · Students · Healthcare Workers · Pharmacists · Hospitals · Patent Medicine Vendors · NGOs · Government Agencies

---

##  Core Features

| Feature | Description |
|---|---|
|  **Authentication** | Email, phone, and Google sign-in with secure profile management |
|  **Dashboard** | Quick actions, recent activity, safety alerts, and usage stats at a glance |
|  **Medicine Search** | Search by brand, generic name, manufacturer, NAFDAC number, or barcode |
|  **Barcode/QR Scanner** | Instantly pull up medicine details by scanning packaging |
|  **AI Packaging Checker** | Upload product images for future AI-based verification *(placeholder in MVP)* |
|  **Expiry Checker** | Enter batch/manufacturing/expiry dates to check validity status |
|  **Fake Drug Reporting** | Report suspicious products with photos, location, and description |
|  **Pharmacy Locator** | Find nearby licensed pharmacies with directions and open/closed status |
|  **Safety Alerts** | Recalls, advisories, and shortage notifications with severity indicators |
|  **Admin Dashboard** | Manage users, medicines, reports, pharmacies, and alerts |

---

##  Screenshots

> _Add screenshots or a demo GIF here once available._

| Home | Medicine Detail | Scanner | Pharmacy Locator |
|---|---|---|---|
| ![home](docs/screenshots/home.png) | ![detail](docs/screenshots/detail.png) | ![scanner](docs/screenshots/scanner.png) | ![pharmacy](docs/screenshots/pharmacy.png) |

---

##  Tech Stack

> _Update this section to reflect your actual implementation._

| Layer | Technology |
|---|---|
| Frontend | React / Next.js (PWA) |
| Styling | Tailwind CSS |
| Backend | Node.js / Express |
| Database | PostgreSQL |
| Auth | Firebase Auth / JWT |
| Maps | Google Maps API |
| Hosting | Vercel / Render |
| Future AI | Vision API for packaging analysis (planned) |

---

##  Project Structure

```
drugcheck-ng/
├── client/                 # Frontend application
│   ├── components/         # Reusable UI components
│   ├── pages/               # App routes/screens
│   ├── assets/              # Images, icons
│   └── styles/               # Design tokens, global styles
├── server/                 # Backend API
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   └── middleware/
├── database/
│   └── schema.sql
├── docs/
│   └── screenshots/
└── README.md
```

---

##  Database Overview

<details>
<summary>Click to expand schema summary</summary>

**Users** — id, name, email, phone, photo, role, created_at
**Medicines** — id, brand_name, generic_name, manufacturer, strength, dosage_form, description, uses, warnings, side_effects, interactions, storage, registration_number, barcode, image, created_at
**Reports** — id, user_id, medicine_id, manufacturer, batch_number, description, images, location, status, created_at
**Pharmacies** — id, name, address, latitude, longitude, phone, license_status, opening_hours
**Alerts** — id, title, description, severity, date
**Notifications** — id, title, body, recipient, status

</details>

---

##  User Roles

- **Guest** — browse limited public info
- **Registered User** — full search, scan, report, and profile access
- **Admin** — manage platform content and moderate reports

---

##  Getting Started

### Prerequisites
- Node.js (v18+)
- npm or yarn
- PostgreSQL (or your configured database)

### Installation

```bash
# Clone the repository
git clone https://github.com/<your-username>/drugcheck-ng.git
cd drugcheck-ng

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env
# Fill in your database, auth, and API keys

# Run database migrations
npm run migrate

# Start the development server
npm run dev
```

The app should now be running at `http://localhost:3000`.

### Environment Variables

```env
DATABASE_URL=
JWT_SECRET=
GOOGLE_CLIENT_ID=
GOOGLE_CLIENT_SECRET=
GOOGLE_MAPS_API_KEY=
```

---

##  Design System

| Token | Value |
|---|---|
| Primary | `#00695C` |
| Secondary | `#00A896` |
| Accent | `#FFC107` |
| Background | `#F8FAFC` |

- Rounded cards with soft shadows
- Clean, readable typography with generous spacing
- Mobile-first, fully responsive (mobile / tablet / desktop breakpoints)
- Accessible: large touch targets, strong contrast, screen-reader friendly

---

##  Roadmap

- [x] Core MVP: search, scan, report, pharmacy locator, alerts
- [x] Admin dashboard
- [ ] AI-powered packaging verification (OCR + image recognition)
- [ ] AI chatbot for medicine questions
- [ ] Voice search
- [ ] Drug interaction checker
- [ ] SMS/USSD access for low-connectivity users
- [ ] Integration with NAFDAC's official verification systems

---

##  Contributing

Contributions are welcome!

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add some feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

---

##  Team / Author

Built by **Rapp Jeremiah** as part of the **3MTT Product Showcase**.

---

##  Acknowledgements

- [3MTT (3 Million Technical Talent)](https://3mtt.nitda.gov.ng/) Programme
- NAFDAC — for the inspiration behind medicine safety verification in Nigeria
- Icons: [Lucide](https://lucide.dev/)

---

<div align="center">

**DrugCheck NG** — because everyone deserves to know what they're taking.

</div>
