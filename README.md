# PayLance MVP

A fintech-first marketplace application designed for freelancers in Poland, enabling secure job listings, payments, and invoicing all in one place.

## Overview

**PayLance** is a modern web/PWA application built with **Next.js** and **Supabase**, providing a complete freelance marketplace platform with integrated payment processing, escrow management, and compliance features tailored for Polish freelancers.

### Key Features
- 🔐 Secure authentication and profile management
- 💼 Job marketplace with detailed project descriptions
- 💳 Integrated payment processing and escrow logic
- 📊 Invoice generation and tax compliance tools
- 📱 Progressive Web App (PWA) support
- 🌐 Responsive, mobile-first design

## Architecture

### Authentication (Auth)
- JWT-based authentication via Supabase Auth
- Social login support (Google, GitHub)
- Role-based access control (freelancer, client, admin)
- Session management and security

### Database Schemas
- **Profiles**: User information, portfolio, skills, ratings
- **Jobs**: Project listings, descriptions, budget, timeline
- **Escrow Transactions**: Secure payment holding and release
- **Invoices**: Tax-compliant invoicing system
- **Reviews & Ratings**: Reputation management

### Escrow Logic
- Smart escrow mechanism for payment protection
- Milestone-based fund release
- Dispute resolution system
- Automated payment processing
- Tax calculation and withholding

## Roadmap

### Phase 1 (MVP)
- ✅ User authentication and profiles
- ✅ Job marketplace
- ✅ Basic payment processing
- ⏳ Escrow system

### Phase 2 (Open Source)
We are planning to open-source key modules, particularly:
- **Automated Polish Tax Calculation Module** - Real-time tax computation for freelancers (PIT/VAT)
- Other compliance and financial utilities for the Polish market

## Tech Stack

- **Frontend**: Next.js, React, TailwindCSS
- **Backend**: Supabase (PostgreSQL)
- **Authentication**: Supabase Auth
- **Payments**: Stripe integration (planned)
- **Deployment**: Vercel
- **Database**: PostgreSQL

## Getting Started

### Prerequisites
- Node.js 18+
- npm or yarn
- Supabase account

### Installation

```bash
# Clone the repository
git clone https://github.com/grzywaczz/paylance.git
cd paylance

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env.local

# Run migrations
npm run db:migrate

# Start development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

## Environment Variables

```env
NEXT_PUBLIC_SUPABASE_URL=your_supabase_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_anon_key
SUPABASE_SERVICE_ROLE_KEY=your_service_role_key
```

## Project Structure

```
paylance/
├── app/                    # Next.js app directory
├── components/             # Reusable React components
├── lib/                    # Utility functions and helpers
├── supabase/
│   └── migrations/         # Database migrations
├── public/                 # Static assets
└── package.json
```

## Contributing

We welcome contributions! Please feel free to open issues and pull requests.

## License

MIT License - see LICENSE file for details

## Contact & Support

For questions or feedback, please reach out to the development team.

---

**Made with ❤️ for Polish freelancers**
