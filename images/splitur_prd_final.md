# Product Requirements Document (PRD)
## Splitur - Modern Expense Splitting App

**Version:** 2.0  
**Last Updated:** February 7, 2026  
**Document Owner:** Product Team

---

## Table of Contents
1. [Executive Summary](#executive-summary)
2. [Product Vision & Goals](#product-vision--goals)
3. [Feature Breakdown](#feature-breakdown)
4. [User Personas & Flows](#user-personas--flows)
5. [Design System](#design-system)
6. [Information Architecture](#information-architecture)
7. [Technical Architecture](#technical-architecture)
8. [Screen & Page Specifications](#screen--page-specifications)
9. [Data Models](#data-models)
10. [Security & Compliance](#security--compliance)
11. [Success Metrics](#success-metrics)
12. [Roadmap & Phases](#roadmap--phases)

---

## 1. Executive Summary

**Product Name:** Splitur

**Tagline:** "Split expenses, settle debts, stay organized"

**Overview:**  
Splitur is a modern, minimalist expense-splitting platform that helps users track shared expenses, settle debts, and manage group finances effortlessly. Built with clean design principles inspired by the best SaaS applications, it provides an intuitive, beautiful experience across web and mobile platforms.

**Brand Colors:**
- **Primary Black:** `#080808` - Near-black for text, headings, primary elements
- **White:** `#FFFFFF` - Backgrounds, cards, surfaces
- **Accent Blue:** `#2A67F4` - Primary actions, highlights, brand accent

**Key Differentiators:**
- Ultra-clean, minimal design aesthetic
- Receipt scanning with smart field extraction (Tesseract OCR)
- Intelligent debt simplification algorithm
- Real-time activity feed
- Multi-currency support with live exchange rates
- Recurring expense automation
- Advanced analytics and spending insights
- 100% open-source stack
- Works beautifully on both web and mobile

---

## 2. Product Vision & Goals

### Vision
To become the most beautiful and intuitive way for people to manage shared finances, eliminating the friction of money discussions among friends, family, and colleagues.

### Primary Goals
1. **Simplicity:** Make expense splitting intuitive and delightful
2. **Accuracy:** Ensure 100% mathematical accuracy in debt calculations
3. **Clarity:** Provide instant visibility into who owes what
4. **Beauty:** Create a visually stunning, Apple-like experience
5. **Speed:** Enable expense entry in under 30 seconds

### Success Criteria
- User onboarding completion rate > 85%
- Weekly active user retention > 60%
- Average expense entry time < 30 seconds
- Receipt scan accuracy > 90%
- Net Promoter Score (NPS) > 50

---

## 3. Feature Breakdown

### 3.1 Core Features (MVP)

#### Authentication & Onboarding
- Email/password registration
- Social login (Google, Apple, Facebook)
- Phone number verification (OTP)
- Multi-step onboarding wizard
- Profile setup (name, photo, default currency, preferred language)
- Friend invitation system

#### Expense Management
- **Add Expense:**
  - Manual entry with description, amount, date, category
  - Receipt photo upload
  - Split types: Equal, Exact amounts, Percentages, Shares
  - Multiple payers support
  - Category tagging (15 predefined + custom)
  - Note/description field
  - Attachment support (up to 5 files)
  
- **Edit/Delete Expense:**
  - Full edit history with audit trail
  - Notifications to affected participants
  - Soft delete with restore option (30 days)

- **Expense List Views:**
  - All expenses (chronological)
  - By group
  - By friend
  - By category
  - By date range
  - Unsettled only filter

#### Groups
- Create groups (name, photo, category)
- Add/remove members
- Group settings (simplify debts, default split method)
- Group expense summary
- Group balances overview
- Archive/delete groups

#### Friends
- Add friends (email, phone, username)
- Friend requests system
- Friend list with balance summary
- Individual friend expense history
- Remove friends (with debt settlement requirement)

#### Balances & Settlement
- **Dashboard Overview:**
  - Total you owe (aggregated)
  - Total owed to you (aggregated)
  - Net balance
  - Per-person breakdown
  - Per-group breakdown

- **Debt Simplification:**
  - Smart algorithm to minimize transactions
  - "Settle All Debts" feature
  - Partial payment recording
  - Payment confirmation flow

- **Payment Methods:**
  - Cash payment recording
  - Payment app integration markers (Venmo, PayPal, UPI, etc.)
  - Bank transfer details
  - Payment notes

#### Activity Feed
- Real-time updates on:
  - New expenses added
  - Expenses edited/deleted
  - Payments made
  - Group changes
  - Friend activity
- Contextual insights (spending trends, unusual expenses)
- Filter by type, person, group, date

### 3.2 Premium Features (All Included)

#### Receipt Scanning
- Open-source OCR technology (Tesseract.js)
- Automatic field extraction:
  - Merchant name
  - Total amount
  - Date
  - Individual line items
  - Tax breakdown
- Item-level splitting
- Manual correction interface
- Support for multiple image formats

#### Advanced Analytics
- **Spending Dashboard:**
  - Monthly/quarterly/yearly spending trends
  - Category breakdown with visualizations
  - Top expenses
  - Spending by person/group
  - Budget vs actual comparison
  
- **Insights:**
  - Spending patterns
  - Category trends over time
  - Unusual expense alerts
  - Monthly spending reports
  - Year-end summary

#### Charts & Visualizations
- Pie charts (spending by category)
- Bar charts (spending over time)
- Line graphs (trends)
- Heatmaps (spending density)
- Comparison charts (this month vs last month)

#### Export & Integration
- Export to CSV/Excel/PDF
- Date range selection
- Custom field selection
- Tax-ready exports (itemized with categories)
- Integration with accounting software APIs:
  - QuickBooks
  - Xero
  - FreshBooks
  - Wave

#### Recurring Expenses
- Set up recurring bills:
  - Frequency (daily, weekly, monthly, yearly, custom)
  - End date or indefinite
  - Auto-add or notification reminder
- Edit/pause recurring templates
- History of recurring expense instances

#### Currency Conversion
- Multi-currency expense support
- Live exchange rate updates (hourly)
- Historical rates for past expenses
- Default currency per user
- Per-expense currency override
- Automatic conversion in balances

#### Search & Filters
- Advanced search:
  - Full-text search across descriptions, notes
  - Filter by amount range
  - Filter by date range
  - Filter by category
  - Filter by person
  - Filter by group
  - Filter by settlement status
  - Saved search presets

### 3.3 Enhanced Features

#### Smart Notifications
- Customizable notification preferences
- Digest mode (daily/weekly summaries)
- Contextual notifications:
  - "John owes you for 3 expenses totaling $45"
  - "Your Netflix subscription was added automatically"
  - "Settle up before the month ends!"

#### Budget Tracking
- Set personal monthly budgets by category
- Group budget tracking
- Budget alerts (50%, 75%, 90%, 100%)
- Budget vs actual visualization
- Rollover budget options

#### Payment Reminders
- Gentle automated reminders
- Customizable frequency
- One-click payment initiation
- Reminder templates with personalization

#### Offline Mode
- Full read access offline
- Queue expense additions offline
- Sync when back online
- Conflict resolution UI

#### Data Privacy & Control
- Granular privacy settings
- Download all personal data
- Delete account with data purge
- Activity log (who viewed what)
- Two-factor authentication

---

## 4. User Flows

### 4.1 Core User Flows

#### Flow 1: New User Onboarding
```
1. Landing page → Sign up button
2. Choose sign-up method (Email/Google/Apple)
3. Enter basic info (name, email, password)
4. Verify email/phone (OTP)
5. Onboarding wizard:
   - Step 1: Upload profile photo (optional)
   - Step 2: Set default currency
   - Step 3: Add first friend (optional, can skip)
   - Step 4: Join/create first group (optional, can skip)
   - Step 5: Tutorial highlights (interactive tooltips)
6. Land on Dashboard
```

#### Flow 2: Adding an Expense (Manual)
```
1. Dashboard → "+" button (prominent FAB on mobile, header button on web)
2. Add Expense screen:
   - Enter description
   - Enter amount
   - Select category (dropdown with icons)
   - Select date (default: today)
   - Choose "With you and" → select friends/group
   - Choose split method:
     * Equal (default)
     * Exact amounts
     * Percentages
     * Shares
   - Paid by: Select payer(s)
   - Add note (optional)
   - Attach files (optional)
3. Preview split breakdown
4. Confirm → Expense added
5. Redirect to expense detail page
6. Show success toast with "Undo" option (5 seconds)
```

#### Flow 3: Adding an Expense (Receipt Scan)
```
1. Dashboard → "+" button → "Scan Receipt" tab
2. Camera interface opens
3. Capture receipt photo OR upload from gallery
4. AI processes image (loading state: 2-5 seconds)
5. Auto-populated expense form:
   - Merchant name (editable)
   - Total amount (editable)
   - Date (editable)
   - Line items shown (can select items to split)
6. Select participants
7. Choose split method:
   - Split entire receipt equally
   - Split by line items (each person selects their items)
8. Review & confirm
9. Expense added with receipt attached
```

#### Flow 4: Settling Up
```
1. Dashboard → "Settle Up" button (visible when debts exist)
2. Settle Up page shows:
   - List of people you owe
   - List of people who owe you
   - Simplified debts (algorithm-optimized)
3. Select person to settle with
4. Shows amount owed/owing
5. Record payment:
   - Choose payment method (Cash, Venmo, PayPal, UPI, etc.)
   - Can settle partial amount or full amount
   - Add payment note
   - Upload payment proof (optional)
6. Confirm settlement
7. Both parties receive notification
8. Balances update immediately
```

#### Flow 5: Viewing Analytics
```
1. Dashboard → "Insights" tab (web) or bottom nav (mobile)
2. Analytics overview:
   - Time period selector (This month, Last month, Custom range)
   - Total spent
   - Category breakdown (pie chart)
   - Spending trend (line graph)
   - Top expenses (list)
3. Tap any category → Detailed category view:
   - All expenses in that category
   - Trend over time
   - Compare to previous period
4. Export options:
   - Download PDF report
   - Export to CSV
   - Share insights
```

#### Flow 6: Managing Groups
```
1. Dashboard → "Groups" section → Select group
2. Group detail page:
   - Group name & photo
   - Member list with balances
   - Group expenses (chronological)
   - Balances summary
   - Settings icon
3. Add expense → scoped to this group
4. Group settings:
   - Edit group name/photo
   - Add/remove members
   - Toggle debt simplification
   - Set default split method
   - Archive group
   - Delete group (if no unsettled balances)
```

---

## 5. Design System

### 5.1 Color Palette

**Design Philosophy:** Ultra-minimal, clean aesthetic with purposeful use of color

#### Brand Colors (Splitur)

**Primary Colors:**
- **Near Black:** `#080808` - Primary text, headings, important UI elements
- **White:** `#FFFFFF` - Main backgrounds, cards, surfaces  
- **Accent Blue:** `#2A67F4` - Primary actions, active states, brand highlights

**Usage Philosophy:**
- 90% of interface uses Near Black (#080808) and White (#FFFFFF)
- Blue (#2A67F4) used sparingly for primary actions and key highlights (10%)
- Color draws attention - use it purposefully
- Clean, uncluttered, professional aesthetic

#### Extended Palette (Grays for depth)

**Gray Scale:**
- **Gray 50:** `#FAFAFA` - Subtle background variations
- **Gray 100:** `#F5F5F5` - Card backgrounds, hover states
- **Gray 200:** `#E5E5E5` - Borders, dividers
- **Gray 300:** `#D4D4D4` - Disabled states
- **Gray 400:** `#A3A3A3` - Placeholder text, inactive icons
- **Gray 500:** `#737373` - Secondary text
- **Gray 600:** `#525252` - Body text
- **Gray 700:** `#404040` - Strong emphasis
- **Gray 800:** `#262626` - Alternative to near-black
- **Gray 900:** `#171717` - Deepest gray
- **Near Black:** `#080808` - Primary text, headings

#### Semantic Colors (Functional use only)

- **Success Green:** `#10B981` - "Owed to you" amounts, successful actions
- **Alert Red:** `#EF4444` - "You owe" amounts, errors, deletions
- **Warning Amber:** `#F59E0B` - Warnings, pending actions
- **Info Cyan:** `#06B6D4` - Informational messages, tips

#### Color Usage Guidelines

**Backgrounds:**
- Primary: White (#FFFFFF) - 85%
- Secondary: Gray 50 (#FAFAFA) - 10%
- Accent backgrounds: Gray 100 (#F5F5F5) - 5%

**Text:**
- Primary headings: Near Black (#080808)
- Body text: Gray 600 (#525252)
- Secondary text: Gray 500 (#737373)
- Disabled: Gray 400 (#A3A3A3)

**Interactive Elements:**
- Primary buttons: Blue (#2A67F4) background, White text
- Secondary buttons: White background, Near Black border and text
- Text buttons: Blue (#2A67F4) text only
- Links: Blue (#2A67F4)
- Hover states: Lighten/darken by 10%

**Borders & Dividers:**
- Default: Gray 200 (#E5E5E5)
- Strong: Gray 300 (#D4D4D4)
- Subtle: Gray 100 (#F5F5F5)

**Do's:**
✅ Use Near Black and White for 90% of interface  
✅ Reserve Blue for primary actions and brand moments  
✅ Use semantic colors only for meaningful data (amounts, status)  
✅ Rely on typography and spacing for hierarchy  
✅ Keep backgrounds white or very light gray  

**Don'ts:**
❌ Don't use multiple bright colors  
❌ Don't color every element  
❌ Don't use colored backgrounds for large areas  
❌ Don't overuse the blue accent  
❌ Don't use gradients (except very subtle ones)

### 5.2 Typography

**Design Philosophy:** Clean, readable, professional typography

#### Font Family
- **Primary Font:** "Inter", -apple-system, BlinkMacSystemFont, "Segoe UI", "Roboto", system-ui, sans-serif
  - Inter (Google Fonts) - modern, clean, excellent readability
  - System fonts as fallback for optimal performance
- **Mono Font:** "Roboto Mono", "SF Mono", "Courier New", monospace - For amounts and numbers

**Why Inter:**
- Professional and modern
- Excellent readability at all sizes
- Free and open-source
- Wide character support
- Optimized for screens
- Popular in modern SaaS apps

#### Font Sizes (Mobile)
- **H1:** 32px / 700 weight - Page titles
- **H2:** 24px / 600 weight - Section headers
- **H3:** 20px / 600 weight - Card titles
- **H4:** 18px / 500 weight - Subsections
- **Body Large:** 17px / 400 weight - Primary content
- **Body:** 15px / 400 weight - Standard text
- **Body Small:** 13px / 400 weight - Captions, meta info
- **Button:** 15px / 500 weight - Button labels
- **Amount Large:** 36px / 700 weight / Mono - Dashboard balances
- **Amount Medium:** 24px / 600 weight / Mono - Expense amounts
- **Amount Small:** 17px / 500 weight / Mono - Small amounts

#### Font Sizes (Web/Desktop)
- **H1:** 48px / 700 weight - Hero titles
- **H2:** 36px / 600 weight - Page headers
- **H3:** 28px / 600 weight - Section headers
- **H4:** 20px / 500 weight - Subsections
- **Body Large:** 19px / 400 weight - Emphasized content
- **Body:** 17px / 400 weight - Standard text
- **Body Small:** 15px / 400 weight - Secondary text
- **Button:** 17px / 500 weight - Button labels
- **Amount Large:** 56px / 700 weight / Mono - Large balances
- **Amount Medium:** 36px / 600 weight / Mono - Medium amounts
- **Amount Small:** 20px / 500 weight / Mono - Small amounts

#### Line Height
- Headings: 1.2 (tight, clean)
- Body text: 1.6 (comfortable reading)
- Buttons: 1.2

#### Letter Spacing
- Headings: -0.02em (slightly tighter)
- Body: 0 (default)
- All caps: 0.05em (slightly wider)
- Amounts: -0.01em (tight, clean)

### 5.3 Spacing System (Apple-inspired: 4pt grid)
- **2px** - xxxs (minimal spacing)
- **4px** - xxs (icon padding, tight spacing)
- **8px** - xs (compact spacing)
- **12px** - sm (comfortable spacing)
- **16px** - md (standard spacing) - Most common
- **24px** - lg (section spacing)
- **32px** - xl (large gaps)
- **48px** - 2xl (page sections)
- **64px** - 3xl (hero spacing)

### 5.4 Border Radius (Soft, Apple-like)
- **Small:** 8px - Buttons, inputs, tags
- **Medium:** 12px - Cards, smaller containers
- **Large:** 16px - Feature cards, modals
- **XLarge:** 20px - Hero sections, large images
- **XXLarge:** 24px - Special highlight containers
- **Full:** 9999px - Pills, avatars, circular elements

### 5.5 Shadows (Subtle, Layered)
- **None:** No shadow - Flat elements
- **XSmall:** `0 1px 2px rgba(0, 0, 0, 0.04)` - Subtle lift
- **Small:** `0 2px 4px rgba(0, 0, 0, 0.06)` - Slight elevation
- **Medium:** `0 4px 12px rgba(0, 0, 0, 0.08)` - Cards (default)
- **Large:** `0 8px 24px rgba(0, 0, 0, 0.12)` - Modals, dropdowns
- **XLarge:** `0 16px 48px rgba(0, 0, 0, 0.16)` - Overlays, popovers

**Apple Principle:** Use very subtle shadows. Prefer lighter shadows over dark.

### 5.6 Iconography
- **Library:** Lucide Icons or SF Symbols (Apple-style)
- **Size:** 24px default, 20px small, 28px large
- **Style:** Outlined (2px stroke weight)
- **Color:** Inherits from parent or Gray 600 default

### 5.7 Components (Splitur Design System)

#### Buttons

**Primary Button:**
- Background: Blue (#2A67F4)
- Text: White (#FFFFFF)
- Padding: 12px 24px (mobile), 14px 28px (desktop)
- Border Radius: 10px
- Font: 15px / 500 weight (mobile), 17px / 500 weight (desktop)
- Shadow: Small
- Transition: all 0.2s ease
- States:
  - Hover: Background Blue (#1E54E0) (10% darker), shadow Medium
  - Active: Background Blue (#123AA0) (20% darker), shadow XSmall
  - Disabled: Gray 300 background, Gray 500 text, no shadow

**Secondary Button:**
- Background: White (#FFFFFF)
- Text: Near Black (#080808)
- Border: 1.5px solid Near Black (#080808)
- Padding: 12px 24px
- Border Radius: 10px
- States:
  - Hover: Background Gray 50 (#FAFAFA)
  - Active: Background Gray 100 (#F5F5F5)
  - Disabled: Gray 200 border, Gray 400 text

**Text Button:**
- Background: Transparent
- Text: Blue (#2A67F4)
- No border, no background
- Padding: 8px 12px
- Hover: Background Gray 50 (#FAFAFA), border-radius 8px
- Active: Background Gray 100 (#F5F5F5)

**Ghost Button:**
- Background: Transparent
- Text: Near Black (#080808)
- Border: 1.5px solid Gray 300 (#D4D4D4)
- Padding: 12px 24px
- Border Radius: 10px
- Hover: Border Gray 400, Background Gray 50

#### Input Fields

- Background: White (#FFFFFF)
- Border: 1.5px solid Gray 200 (#E5E5E5)
- Border Radius: 10px
- Padding: 14px 16px
- Font: Body (15px mobile, 17px desktop)
- Text: Near Black (#080808)
- Placeholder: Gray 400 (#A3A3A3)
- States:
  - Focus: Border Blue (#2A67F4), shadow Small with blue tint (0 0 0 3px rgba(42,103,244,0.1))
  - Error: Border Red (#EF4444), background Red 50 (#FEF2F2)
  - Disabled: Background Gray 100, Border Gray 200, Text Gray 400

#### Cards

- Background: White (#FFFFFF)
- Border: None (or 1px solid Gray 100 for subtle definition)
- Border Radius: 16px
- Shadow: Medium (0 4px 12px rgba(0,0,0,0.08))
- Padding: 20px (mobile), 24px (desktop)
- Hover (if interactive): Shadow Large, translateY(-2px)
- Transition: all 0.2s ease

#### Balance Cards (Dashboard)

**You Owe Card:**
- Background: White (#FFFFFF)
- Border: 1.5px solid Red 200 (#FECACA)
- Border Radius: 16px
- Shadow: Medium
- Icon: Arrow down circle (Red 500 #EF4444)
- Amount Color: Red 500 (#EF4444)
- Label: Gray 600 (#525252)

**You're Owed Card:**
- Background: White (#FFFFFF)
- Border: 1.5px solid Green 200 (#BBF7D0)
- Border Radius: 16px
- Shadow: Medium
- Icon: Arrow up circle (Green 500 #10B981)
- Amount Color: Green 500 (#10B981)
- Label: Gray 600 (#525252)

**Design Note:** Keep backgrounds white. Use color only for icons, amounts, and subtle borders.

#### Avatars

- Size: 40px (standard), 32px (small), 56px (large), 24px (tiny)
- Border Radius: Full (circular)
- Border: 2px solid White (on colored backgrounds)
- Fallback: Initials on blue gradient background
  - Background: Linear gradient from Blue (#2A67F4) to lighter blue
  - Text: White, bold, centered
  - Algorithm: Use first letter of first and last name

#### Badges & Tags

**Default Tag:**
- Border Radius: 6px (rounded rectangle)
- Padding: 4px 10px
- Font: 13px / 500 weight
- Background: Gray 100 (#F5F5F5)
- Text: Gray 700 (#404040)

**Colored Tags (for categories):**
- Background: Color at 10% opacity (e.g., Blue #2A67F4 at 10%)
- Text: Darker shade of same color
- Border: 1px solid color at 20% opacity

**Status Badges:**
- Pill-shaped (border-radius: 999px)
- Padding: 4px 12px
- Font: 12px / 600 weight
- Examples:
  - Settled: Green 100 bg, Green 700 text
  - Pending: Amber 100 bg, Amber 700 text
  - Overdue: Red 100 bg, Red 700 text

#### Lists

**List Items:**
- Background: White
- Padding: 16px
- Border-bottom: 1px solid Gray 100
- Hover: Background Gray 50
- Active/Selected: Background Blue at 5% opacity, left border 3px solid Blue

#### Empty States

- Icon: Gray 300, large (64px)
- Heading: Gray 700, H3 size
- Description: Gray 500, Body size
- CTA Button: Primary blue button
- Illustration: Optional, subtle, gray tones only

---

## 6. Information Architecture

### 6.1 Mobile App Navigation (Bottom Tab Bar)

**5 Main Tabs:**

1. **Dashboard** (Icon: Home)
   - Overview/Home screen
   
2. **Activity** (Icon: List)
   - Activity feed
   
3. **Add** (Icon: Plus Circle - larger, prominent)
   - Quick add expense
   
4. **Groups** (Icon: Users)
   - Groups list
   
5. **Profile** (Icon: User)
   - Profile & settings

### 6.2 Web App Navigation (Sidebar + Top Bar)

**Left Sidebar (Fixed, 240px width):**
- Logo
- Dashboard
- Activity
- Groups
- Friends
- Insights
- Settings
- Help & Support

**Top Navigation Bar:**
- Search bar (global)
- Add Expense button (prominent)
- Notifications icon (with badge)
- Profile dropdown

### 6.3 Site Map

```
Splitur
│
├── Authentication
│   ├── Login
│   ├── Sign Up
│   ├── Forgot Password
│   ├── Reset Password
│   └── Email Verification
│
├── Onboarding
│   ├── Welcome
│   ├── Profile Setup
│   ├── Add Friends
│   └── Tutorial
│
├── Dashboard (Home)
│   ├── Balance Summary
│   ├── Recent Activity (top 5)
│   ├── Quick Actions
│   └── Groups Overview
│
├── Activity Feed
│   ├── All Activity
│   ├── Filtered Views
│   └── Activity Detail
│
├── Expenses
│   ├── All Expenses
│   ├── Add Expense
│   │   ├── Manual Entry
│   │   └── Scan Receipt
│   ├── Expense Detail
│   ├── Edit Expense
│   └── Delete Expense
│
├── Groups
│   ├── Groups List
│   ├── Create Group
│   ├── Group Detail
│   │   ├── Group Expenses
│   │   ├── Group Balances
│   │   ├── Group Members
│   │   └── Group Settings
│   ├── Edit Group
│   └── Delete Group
│
├── Friends
│   ├── Friends List
│   ├── Add Friend
│   ├── Friend Detail
│   │   ├── Friend Expenses
│   │   └── Friend Balance
│   ├── Friend Requests
│   └── Remove Friend
│
├── Balances
│   ├── Overview
│   ├── Settle Up
│   └── Payment History
│
├── Insights
│   ├── Spending Dashboard
│   ├── Category Analysis
│   ├── Trends
│   ├── Reports
│   └── Export Data
│
├── Profile
│   ├── View Profile
│   ├── Edit Profile
│   ├── Preferences
│   ├── Notification Settings
│   └── Privacy Settings
│
├── Settings
│   ├── Account Settings
│   ├── Currency Settings
│   ├── Notification Preferences
│   ├── Connected Accounts
│   ├── Security (2FA)
│   ├── Data & Privacy
│   └── About
│
└── Help & Support
    ├── FAQ
    ├── Contact Support
    └── Feature Requests
```

---

## 7. Technical Architecture

### 7.1 Tech Stack (100% Open Source & Free)

#### Frontend - Web
- **Framework:** Next.js 14+ (React 18+) - Open source
  - Server-side rendering (SSR)
  - App Router for modern routing
  - Server components
  
- **Language:** TypeScript (strict mode) - Open source
  
- **Styling:** Tailwind CSS v4 - Open source
  - Custom design tokens
  - Apple-inspired theme
  
- **State Management:** 
  - Zustand - Open source, lightweight
  - TanStack Query (React Query) - Open source, server state
  
- **Forms:** React Hook Form + Zod - Open source
  
- **Charts:** Recharts - Open source, built on D3.js
  - Alternative: Chart.js - Open source
  
- **UI Components:** 
  - Radix UI - Open source, headless, accessible
  - shadcn/ui - Open source component library
  
- **Animation:** Framer Motion - Open source
  
- **Icons:** Lucide React - Open source

#### Frontend - Mobile
- **Framework:** React Native (Expo) - Open source
  - Cross-platform iOS & Android
  - Expo managed workflow
  
- **Language:** TypeScript - Open source
  
- **Navigation:** React Navigation v6 - Open source
  
- **Styling:** NativeWind (Tailwind for React Native) - Open source
  
- **State Management:** Zustand + TanStack Query - Open source
  
- **Camera/OCR:** 
  - Expo Camera - Open source
  - Expo Image Picker - Open source
  - **Tesseract.js** - Open source OCR engine (FREE)
  
- **Local Storage:** Async Storage - Open source
  
- **Offline:** WatermelonDB - Open source, reactive database

#### Backend
- **Runtime:** Node.js 20+ LTS - Open source
  
- **Framework:** Fastify - Open source (faster than Express)
  
- **Language:** TypeScript - Open source
  
- **API Style:** RESTful API
  
- **Real-time:** Socket.io - Open source
  
- **Database:** 
  - PostgreSQL 15+ - Open source
  - Redis - Open source (caching, sessions)
  
- **ORM:** Prisma - Open source
  
- **File Storage:** 
  - MinIO - Open source S3-compatible storage
  - Alternative: Local file system + Nginx
  
- **OCR Engine:** 
  - **Tesseract OCR** - Open source, FREE
  - Wrapper: tesseract.js (for web) or react-native-tesseract-ocr
  
- **Authentication:** 
  - JWT (JSON Web Tokens) - Open source
  - Passport.js - Open source
  
- **Email Service:** 
  - Nodemailer - Open source
  - SMTP (free tier from Gmail/Outlook)
  
- **Currency Exchange:** 
  - **Fixer.io FREE tier** (1000 requests/month)
  - Alternative: **ExchangeRate-API FREE tier**
  - Alternative: **Frankfurter API** (completely FREE, no key needed)
  
- **PDF Generation:**
  - **jsPDF** - Open source
  - **PDFKit** - Open source
  - **Puppeteer** - Open source (for complex PDFs)
  
- **Excel Generation:**
  - **ExcelJS** - Open source
  - **SheetJS (xlsx)** - Open source (community edition)
  
- **Background Jobs:** 
  - BullMQ - Open source (Redis-based)
  - node-cron - Open source (cron jobs)
  
- **Monitoring:** 
  - **Sentry** - Open source (self-hosted option)
  - **Winston** - Open source (logging)
  
- **Testing:** 
  - Jest - Open source
  - Supertest - Open source
  - Playwright - Open source

#### DevOps & Infrastructure (Free Tier Options)
- **Hosting:** 
  - Vercel FREE tier (Next.js frontend)
  - Render FREE tier (backend)
  - Railway FREE tier (alternative)
  - Expo Application Services FREE tier (mobile builds)
  
- **Database Hosting:** 
  - **Supabase FREE tier** (PostgreSQL + 500MB storage)
  - **Neon FREE tier** (PostgreSQL serverless)
  - **ElephantSQL FREE tier** (PostgreSQL 20MB)
  
- **Redis Hosting:**
  - **Upstash FREE tier** (Redis 10K commands/day)
  - **Redis Cloud FREE tier** (30MB)
  
- **File Storage:**
  - **Cloudflare R2 FREE tier** (10GB storage)
  - **Backblaze B2 FREE tier** (10GB storage)
  
- **CI/CD:** 
  - GitHub Actions - FREE for public repos
  
- **Version Control:** Git + GitHub - FREE
  
- **Documentation:** 
  - Swagger/OpenAPI - Open source
  - Storybook - Open source

#### Recommended FREE OCR API
**Option 1: Tesseract.js (Best for this project)**
- Completely FREE
- No API key needed
- Runs client-side (no server cost)
- 100+ languages
- Accuracy: 85-95% (good for receipts)

**Option 2: OCR.space API**
- FREE tier: 25,000 requests/month
- API key required (free)
- Server-side processing
- Accuracy: 90-95%

**Recommendation:** Use Tesseract.js for MVP, upgrade to OCR.space if needed

### 7.2 System Architecture Diagram

```
┌─────────────────────────────────────────────────────────────┐
│                         CLIENT LAYER                         │
├──────────────────────────────┬──────────────────────────────┤
│      Web App (Next.js)       │   Mobile App (React Native)  │
│         (TypeScript)         │        (TypeScript)          │
└──────────────┬───────────────┴──────────────┬───────────────┘
               │                              │
               │        HTTPS/WSS             │
               │                              │
┌──────────────┴──────────────────────────────┴───────────────┐
│                    API GATEWAY / LOAD BALANCER               │
│                     (Nginx / AWS ALB)                        │
└──────────────┬──────────────────────────────────────────────┘
               │
┌──────────────┴──────────────────────────────────────────────┐
│                   APPLICATION LAYER                          │
├──────────────────────────────────────────────────────────────┤
│                  Backend API (Node.js/Express)               │
│                      (TypeScript)                            │
│                                                              │
│  ┌─────────────┐  ┌──────────────┐  ┌──────────────┐       │
│  │   Auth      │  │   Expense    │  │   Balance    │       │
│  │   Service   │  │   Service    │  │   Service    │       │
│  └─────────────┘  └──────────────┘  └──────────────┘       │
│                                                              │
│  ┌─────────────┐  ┌──────────────┐  ┌──────────────┐       │
│  │   Group     │  │   Friend     │  │   OCR        │       │
│  │   Service   │  │   Service    │  │   Service    │       │
│  └─────────────┘  └──────────────┘  └──────────────┘       │
│                                                              │
│  ┌─────────────┐  ┌──────────────┐  ┌──────────────┐       │
│  │  Analytics  │  │ Notification │  │   Payment    │       │
│  │   Service   │  │   Service    │  │   Service    │       │
│  └─────────────┘  └──────────────┘  └──────────────┘       │
└──────────────┬──────────────────────────────────────────────┘
               │
┌──────────────┴──────────────────────────────────────────────┐
│                      DATA LAYER                              │
├──────────────┬──────────────┬───────────────┬───────────────┤
│  PostgreSQL  │    Redis     │   S3/R2       │  External APIs│
│  (Primary DB)│   (Cache)    │ (File Storage)│               │
│              │              │               │  - Google     │
│  - Users     │  - Sessions  │  - Receipts   │    Vision API │
│  - Expenses  │  - Temp Data │  - Avatars    │  - Exchange   │
│  - Groups    │  - Job Queue │  - Exports    │    Rate API   │
│  - Balances  │              │               │  - SendGrid   │
└──────────────┴──────────────┴───────────────┴───────────────┘

┌──────────────────────────────────────────────────────────────┐
│                   BACKGROUND JOBS LAYER                       │
├──────────────────────────────────────────────────────────────┤
│  - Recurring expense processor (cron: daily)                 │
│  - Email digest sender (cron: configurable)                  │
│  - Currency rate updater (cron: hourly)                      │
│  - Analytics aggregator (cron: daily)                        │
│  - Receipt processing queue (BullMQ)                         │
│  - Notification queue (BullMQ)                               │
└──────────────────────────────────────────────────────────────┘
```

### 7.3 Database Schema (Core Tables)

#### Users Table
```sql
CREATE TABLE users (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  email VARCHAR(255) UNIQUE NOT NULL,
  phone VARCHAR(20) UNIQUE,
  password_hash VARCHAR(255),
  username VARCHAR(50) UNIQUE,
  full_name VARCHAR(100) NOT NULL,
  avatar_url TEXT,
  default_currency VARCHAR(3) DEFAULT 'USD',
  preferred_language VARCHAR(10) DEFAULT 'en',
  email_verified BOOLEAN DEFAULT FALSE,
  phone_verified BOOLEAN DEFAULT FALSE,
  created_at TIMESTAMP DEFAULT NOW(),
  updated_at TIMESTAMP DEFAULT NOW(),
  last_login TIMESTAMP,
  is_active BOOLEAN DEFAULT TRUE
);
```

#### Expenses Table
```sql
CREATE TABLE expenses (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  description VARCHAR(255) NOT NULL,
  amount DECIMAL(12, 2) NOT NULL,
  currency VARCHAR(3) NOT NULL,
  category VARCHAR(50),
  expense_date DATE NOT NULL,
  created_by_user_id UUID REFERENCES users(id),
  group_id UUID REFERENCES groups(id),
  notes TEXT,
  receipt_url TEXT,
  is_recurring BOOLEAN DEFAULT FALSE,
  recurring_template_id UUID REFERENCES recurring_expenses(id),
  created_at TIMESTAMP DEFAULT NOW(),
  updated_at TIMESTAMP DEFAULT NOW(),
  deleted_at TIMESTAMP,
  is_settled BOOLEAN DEFAULT FALSE
);
```

#### Expense Participants Table (Join)
```sql
CREATE TABLE expense_participants (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  expense_id UUID REFERENCES expenses(id) ON DELETE CASCADE,
  user_id UUID REFERENCES users(id),
  paid_amount DECIMAL(12, 2) DEFAULT 0,
  owed_amount DECIMAL(12, 2) NOT NULL,
  is_payer BOOLEAN DEFAULT FALSE,
  created_at TIMESTAMP DEFAULT NOW()
);
```

#### Groups Table
```sql
CREATE TABLE groups (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  name VARCHAR(100) NOT NULL,
  description TEXT,
  avatar_url TEXT,
  category VARCHAR(50),
  created_by_user_id UUID REFERENCES users(id),
  simplify_debts BOOLEAN DEFAULT TRUE,
  default_split_method VARCHAR(20) DEFAULT 'equal',
  created_at TIMESTAMP DEFAULT NOW(),
  updated_at TIMESTAMP DEFAULT NOW(),
  is_archived BOOLEAN DEFAULT FALSE
);
```

#### Group Members Table (Join)
```sql
CREATE TABLE group_members (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  group_id UUID REFERENCES groups(id) ON DELETE CASCADE,
  user_id UUID REFERENCES users(id) ON DELETE CASCADE,
  role VARCHAR(20) DEFAULT 'member', -- admin, member
  joined_at TIMESTAMP DEFAULT NOW(),
  UNIQUE(group_id, user_id)
);
```

#### Friendships Table
```sql
CREATE TABLE friendships (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  user_id UUID REFERENCES users(id) ON DELETE CASCADE,
  friend_id UUID REFERENCES users(id) ON DELETE CASCADE,
  status VARCHAR(20) DEFAULT 'pending', -- pending, accepted, blocked
  created_at TIMESTAMP DEFAULT NOW(),
  accepted_at TIMESTAMP,
  UNIQUE(user_id, friend_id),
  CHECK (user_id != friend_id)
);
```

#### Balances Table (Computed/Cached)
```sql
CREATE TABLE balances (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  user_id UUID REFERENCES users(id) ON DELETE CASCADE,
  friend_id UUID REFERENCES users(id) ON DELETE CASCADE,
  group_id UUID REFERENCES groups(id) ON DELETE CASCADE,
  amount DECIMAL(12, 2) NOT NULL,
  currency VARCHAR(3) NOT NULL,
  updated_at TIMESTAMP DEFAULT NOW(),
  UNIQUE(user_id, friend_id, group_id)
);
```

#### Payments Table
```sql
CREATE TABLE payments (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  from_user_id UUID REFERENCES users(id),
  to_user_id UUID REFERENCES users(id),
  amount DECIMAL(12, 2) NOT NULL,
  currency VARCHAR(3) NOT NULL,
  payment_method VARCHAR(50),
  payment_date DATE NOT NULL,
  notes TEXT,
  proof_url TEXT,
  created_at TIMESTAMP DEFAULT NOW(),
  confirmed_by_recipient BOOLEAN DEFAULT FALSE
);
```

#### Recurring Expenses Table
```sql
CREATE TABLE recurring_expenses (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  description VARCHAR(255) NOT NULL,
  amount DECIMAL(12, 2) NOT NULL,
  currency VARCHAR(3) NOT NULL,
  category VARCHAR(50),
  frequency VARCHAR(20) NOT NULL, -- daily, weekly, monthly, yearly, custom
  interval_count INT DEFAULT 1,
  start_date DATE NOT NULL,
  end_date DATE,
  next_occurrence DATE,
  created_by_user_id UUID REFERENCES users(id),
  group_id UUID REFERENCES groups(id),
  is_active BOOLEAN DEFAULT TRUE,
  auto_add BOOLEAN DEFAULT FALSE,
  created_at TIMESTAMP DEFAULT NOW(),
  updated_at TIMESTAMP DEFAULT NOW()
);
```

#### Activity Log Table
```sql
CREATE TABLE activity_log (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  user_id UUID REFERENCES users(id),
  activity_type VARCHAR(50) NOT NULL, -- expense_added, expense_edited, payment_made, etc.
  entity_type VARCHAR(50), -- expense, group, friend, payment
  entity_id UUID,
  metadata JSONB,
  created_at TIMESTAMP DEFAULT NOW()
);
```

#### Notifications Table
```sql
CREATE TABLE notifications (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  user_id UUID REFERENCES users(id) ON DELETE CASCADE,
  type VARCHAR(50) NOT NULL,
  title VARCHAR(255) NOT NULL,
  message TEXT,
  related_entity_type VARCHAR(50),
  related_entity_id UUID,
  is_read BOOLEAN DEFAULT FALSE,
  created_at TIMESTAMP DEFAULT NOW()
);
```

### 7.4 Modular Code Structure

#### Backend Structure
```
backend/
├── src/
│   ├── config/
│   │   ├── database.ts
│   │   ├── redis.ts
│   │   ├── env.ts
│   │   └── constants.ts
│   ├── modules/
│   │   ├── auth/
│   │   │   ├── auth.controller.ts
│   │   │   ├── auth.service.ts
│   │   │   ├── auth.validation.ts
│   │   │   ├── auth.routes.ts
│   │   │   └── auth.types.ts
│   │   ├── users/
│   │   │   ├── users.controller.ts
│   │   │   ├── users.service.ts
│   │   │   ├── users.validation.ts
│   │   │   ├── users.routes.ts
│   │   │   └── users.types.ts
│   │   ├── expenses/
│   │   │   ├── expenses.controller.ts
│   │   │   ├── expenses.service.ts
│   │   │   ├── expenses.validation.ts
│   │   │   ├── expenses.routes.ts
│   │   │   ├── expenses.types.ts
│   │   │   └── split-logic.service.ts
│   │   ├── groups/
│   │   │   └── ... (similar structure)
│   │   ├── balances/
│   │   │   ├── balances.controller.ts
│   │   │   ├── balances.service.ts
│   │   │   ├── debt-simplification.service.ts
│   │   │   └── ...
│   │   ├── ocr/
│   │   │   ├── ocr.controller.ts
│   │   │   ├── ocr.service.ts (Tesseract.js integration)
│   │   │   └── receipt-parser.service.ts
│   │   ├── analytics/
│   │   │   └── ...
│   │   └── notifications/
│   │       └── ...
│   ├── shared/
│   │   ├── middleware/
│   │   │   ├── auth.middleware.ts
│   │   │   ├── error-handler.middleware.ts
│   │   │   ├── validation.middleware.ts
│   │   │   └── rate-limit.middleware.ts
│   │   ├── utils/
│   │   │   ├── logger.ts
│   │   │   ├── response.ts
│   │   │   └── helpers.ts
│   │   └── types/
│   │       └── common.types.ts
│   ├── jobs/
│   │   ├── recurring-expenses.job.ts
│   │   ├── email-digest.job.ts
│   │   └── currency-update.job.ts
│   ├── prisma/
│   │   ├── schema.prisma
│   │   └── migrations/
│   ├── app.ts
│   └── server.ts
├── tests/
│   ├── unit/
│   ├── integration/
│   └── e2e/
├── package.json
├── tsconfig.json
└── .env.example
```

#### Frontend (Web) Structure
```
web/
├── src/
│   ├── app/
│   │   ├── (auth)/
│   │   │   ├── login/
│   │   │   │   └── page.tsx
│   │   │   └── signup/
│   │   │       └── page.tsx
│   │   ├── (dashboard)/
│   │   │   ├── layout.tsx (sidebar layout)
│   │   │   ├── page.tsx (dashboard home)
│   │   │   ├── activity/
│   │   │   │   └── page.tsx
│   │   │   ├── groups/
│   │   │   │   ├── page.tsx
│   │   │   │   └── [groupId]/
│   │   │   │       └── page.tsx
│   │   │   ├── expenses/
│   │   │   │   ├── page.tsx
│   │   │   │   ├── new/
│   │   │   │   │   └── page.tsx
│   │   │   │   └── [expenseId]/
│   │   │   │       └── page.tsx
│   │   │   ├── insights/
│   │   │   │   └── page.tsx
│   │   │   └── settings/
│   │   │       └── page.tsx
│   │   ├── layout.tsx
│   │   └── globals.css
│   ├── components/
│   │   ├── ui/ (Radix-based primitives)
│   │   │   ├── button.tsx
│   │   │   ├── input.tsx
│   │   │   ├── card.tsx
│   │   │   ├── modal.tsx
│   │   │   └── ...
│   │   ├── layout/
│   │   │   ├── Sidebar.tsx
│   │   │   ├── Topbar.tsx
│   │   │   └── Layout.tsx
│   │   ├── dashboard/
│   │   │   ├── BalanceCard.tsx
│   │   │   ├── RecentActivity.tsx
│   │   │   └── QuickActions.tsx
│   │   ├── expenses/
│   │   │   ├── ExpenseCard.tsx
│   │   │   ├── ExpenseForm.tsx
│   │   │   └── SplitCalculator.tsx
│   │   └── charts/
│   │       ├── SpendingPieChart.tsx
│   │       └── TrendLineChart.tsx
│   ├── lib/
│   │   ├── api/
│   │   │   ├── client.ts
│   │   │   ├── auth.ts
│   │   │   ├── expenses.ts
│   │   │   └── ...
│   │   ├── hooks/
│   │   │   ├── useAuth.ts
│   │   │   ├── useExpenses.ts
│   │   │   └── ...
│   │   ├── store/
│   │   │   ├── authStore.ts
│   │   │   └── uiStore.ts
│   │   └── utils/
│   │       ├── formatters.ts
│   │       └── validators.ts
│   ├── types/
│   │   ├── expense.types.ts
│   │   ├── user.types.ts
│   │   └── ...
│   └── styles/
│       └── tailwind.config.ts
├── public/
├── package.json
└── tsconfig.json
```

#### Mobile App Structure
```
mobile/
├── src/
│   ├── navigation/
│   │   ├── AppNavigator.tsx
│   │   ├── AuthNavigator.tsx
│   │   └── TabNavigator.tsx
│   ├── screens/
│   │   ├── auth/
│   │   │   ├── LoginScreen.tsx
│   │   │   └── SignupScreen.tsx
│   │   ├── dashboard/
│   │   │   └── DashboardScreen.tsx
│   │   ├── activity/
│   │   │   └── ActivityScreen.tsx
│   │   ├── expenses/
│   │   │   ├── ExpenseListScreen.tsx
│   │   │   ├── AddExpenseScreen.tsx
│   │   │   ├── ScanReceiptScreen.tsx
│   │   │   └── ExpenseDetailScreen.tsx
│   │   ├── groups/
│   │   │   └── ...
│   │   └── profile/
│   │       └── ProfileScreen.tsx
│   ├── components/
│   │   ├── ui/
│   │   ├── dashboard/
│   │   ├── expenses/
│   │   └── ...
│   ├── services/
│   │   ├── api/
│   │   ├── storage/
│   │   └── camera/
│   ├── store/
│   ├── hooks/
│   ├── utils/
│   ├── types/
│   └── constants/
├── app.json
├── package.json
└── tsconfig.json
```

### 7.5 API Endpoints

#### Authentication Endpoints
```
POST   /api/v1/auth/register
POST   /api/v1/auth/login
POST   /api/v1/auth/logout
POST   /api/v1/auth/refresh-token
POST   /api/v1/auth/forgot-password
POST   /api/v1/auth/reset-password
POST   /api/v1/auth/verify-email
POST   /api/v1/auth/resend-verification
POST   /api/v1/auth/oauth/google
POST   /api/v1/auth/oauth/apple
```

#### User Endpoints
```
GET    /api/v1/users/me
PUT    /api/v1/users/me
DELETE /api/v1/users/me
PUT    /api/v1/users/me/avatar
GET    /api/v1/users/search?q={query}
```

#### Expense Endpoints
```
GET    /api/v1/expenses
GET    /api/v1/expenses/:id
POST   /api/v1/expenses
PUT    /api/v1/expenses/:id
DELETE /api/v1/expenses/:id
GET    /api/v1/expenses/:id/history
POST   /api/v1/expenses/scan-receipt (multipart/form-data)
```

#### Group Endpoints
```
GET    /api/v1/groups
GET    /api/v1/groups/:id
POST   /api/v1/groups
PUT    /api/v1/groups/:id
DELETE /api/v1/groups/:id
GET    /api/v1/groups/:id/members
POST   /api/v1/groups/:id/members
DELETE /api/v1/groups/:id/members/:userId
GET    /api/v1/groups/:id/expenses
GET    /api/v1/groups/:id/balances
```

#### Friend Endpoints
```
GET    /api/v1/friends
POST   /api/v1/friends/request
PUT    /api/v1/friends/:friendshipId/accept
PUT    /api/v1/friends/:friendshipId/reject
DELETE /api/v1/friends/:friendId
GET    /api/v1/friends/:friendId/expenses
GET    /api/v1/friends/:friendId/balance
```

#### Balance Endpoints
```
GET    /api/v1/balances
GET    /api/v1/balances/summary
GET    /api/v1/balances/simplified
POST   /api/v1/balances/settle
GET    /api/v1/balances/settle-up-suggestions
```

#### Payment Endpoints
```
GET    /api/v1/payments
GET    /api/v1/payments/:id
POST   /api/v1/payments
PUT    /api/v1/payments/:id/confirm
```

#### Analytics Endpoints
```
GET    /api/v1/analytics/spending-summary?period={month|quarter|year}
GET    /api/v1/analytics/category-breakdown?period={month|quarter|year}
GET    /api/v1/analytics/trends?period={month|quarter|year}
GET    /api/v1/analytics/export?format={csv|pdf}&period={...}
```

#### Activity Endpoints
```
GET    /api/v1/activity?limit={num}&offset={num}
GET    /api/v1/activity/filter?type={...}&userId={...}
```

#### Notification Endpoints
```
GET    /api/v1/notifications
PUT    /api/v1/notifications/:id/read
PUT    /api/v1/notifications/read-all
GET    /api/v1/notifications/preferences
PUT    /api/v1/notifications/preferences
```

---

## 8. Screen & Page Specifications

### 8.1 Mobile Screens (Portrait)

#### Screen 1: Login
**Layout:**
- Logo (centered, top 20%)
- Heading: "Welcome back"
- Email input field
- Password input field (with show/hide toggle)
- "Forgot password?" link
- Login button (primary, full width)
- Divider with "OR"
- Social login buttons (Google, Apple)
- "Don't have an account? Sign up" link

#### Screen 2: Dashboard (Home)
**Layout:**
- Top bar:
  - Greeting: "Hi, [FirstName]" (left)
  - Notification bell icon (right)
  - Avatar (right)
  
- Balance Summary Section:
  - Two cards side-by-side:
    - **You Owe Card** (Coral gradient)
      - Icon: Down arrow
      - Label: "You owe"
      - Amount: $XXX.XX (large, bold)
    - **You're Owed Card** (Mint gradient)
      - Icon: Up arrow
      - Label: "Owed to you"
      - Amount: $XXX.XX (large, bold)
  
- Quick Actions (3 buttons in row):
  - Add Expense
  - Settle Up
  - Scan Receipt
  
- Recent Activity Section:
  - Heading: "Recent Activity"
  - List of 5 recent activities (infinite scroll for more)
  - Each item: Avatar, Name, Action, Amount, Time
  
- Groups Overview Section:
  - Heading: "Your Groups" with "See All" link
  - Horizontal scrollable list of group cards
  - Each card: Group photo, Name, Balance

- Bottom Tab Bar (fixed):
  - Dashboard | Activity | + | Groups | Profile

#### Screen 3: Add Expense
**Layout:**
- Top bar: "Add Expense" with back button, "Save" button (disabled until valid)

- Two tabs:
  - Manual Entry (default)
  - Scan Receipt

- **Manual Entry Tab:**
  - Description input (large)
  - Amount input (numeric keyboard, currency symbol prefix)
  - Category selector (icon grid or dropdown)
  - Date picker (default: today)
  - "With you and:" section
    - Search/select friends or groups
    - Chips showing selected participants
  - "Paid by" section
    - Select who paid (default: current user)
  - Split method selector:
    - Equal (default)
    - Exact amounts
    - Percentages
    - Shares
  - Preview card: Shows split breakdown
  - "Add note" expandable section
  - "Attach files" option
  - Primary button: "Add Expense"

#### Screen 4: Scan Receipt
**Layout:**
- Camera viewfinder (full screen)
- Capture button (bottom center, large circle)
- "Upload from gallery" button (bottom left)
- Flash toggle (top right)
- Back button (top left)

**After capture:**
- Receipt image preview (top half)
- Processing loader
- Auto-filled form (bottom half):
  - Extracted merchant name
  - Extracted amount
  - Extracted date
  - Edit buttons for each field
- "Looks good" button to proceed to split screen

#### Screen 5: Activity Feed
**Layout:**
- Top bar: "Activity" with filter icon
- Filter chips (horizontal scroll):
  - All | Expenses | Payments | Groups | Friends
- Infinite scroll list:
  - Each item:
    - Left: Avatar or group photo
    - Middle: 
      - Name/Group name
      - Action description
      - Timestamp
    - Right: Amount (if applicable)
- Empty state: Illustration + "No activity yet"

#### Screen 6: Groups List
**Layout:**
- Top bar: "Groups" with "+" button
- Search bar
- List of groups (alphabetical):
  - Each item:
    - Group photo
    - Group name
    - Member count
    - Balance (you owe / owed to you)
    - Right arrow
- Empty state: "Create your first group"

#### Screen 7: Group Detail
**Layout:**
- Header:
  - Group photo (large, centered)
  - Group name
  - Member avatars (overlapping circles)
  - Settings icon (top right)
  
- Balance Summary:
  - "Group Balances" heading
  - List of members with their balances
  
- Quick Actions:
  - Add Expense (to this group)
  - Settle Up
  
- Expenses List:
  - "Group Expenses" heading with filter/sort
  - Chronological list of expenses
  - Each expense: Description, Date, Amount, Paid by, Split info

#### Screen 8: Expense Detail
**Layout:**
- Header:
  - Category icon (large, colored)
  - Description (heading)
  - Amount (large)
  - Date
  
- Info cards:
  - Paid by: Name, amount
  - Split among: List of participants with amounts
  
- Receipt section (if exists):
  - Thumbnail of receipt
  - Tap to view full screen
  
- Notes section (if exists):
  - Note text
  
- Actions:
  - Edit button
  - Delete button
  - Share button

#### Screen 9: Settle Up
**Layout:**
- Top bar: "Settle Up" with back button

- Summary card:
  - "You owe in total: $XXX.XX"
  - "You're owed in total: $XXX.XX"
  - "Simplified debts" toggle

- Tabs:
  - You Owe
  - You're Owed

- **You Owe Tab:**
  - List of people/groups you owe
  - Each item:
    - Avatar
    - Name
    - Amount owed (Coral color)
    - "Settle" button
  
- **Settle Payment Modal** (when "Settle" tapped):
  - Person's name and avatar
  - Amount owed
  - "Settle full amount" / "Settle partial" toggle
  - Amount input (if partial)
  - Payment method selector
  - Payment note input
  - "Record Payment" button

#### Screen 10: Insights
**Layout:**
- Top bar: "Insights" with export icon

- Period selector:
  - This Month | Last Month | Custom Range
  
- Summary cards (2x2 grid):
  - Total Spent
  - Largest Expense
  - Most Frequent Category
  - Average Per Day
  
- Spending by Category:
  - Pie chart
  - Legend below
  
- Spending Trend:
  - Line chart (spending over time)
  
- Top Expenses:
  - List of top 5 expenses
  - Each item: Description, Category, Amount

- Export button (bottom)

#### Screen 11: Profile
**Layout:**
- Header:
  - Avatar (large, centered, editable)
  - Name
  - Email
  - "Edit Profile" button
  
- Settings List:
  - Account
    - Personal Information
    - Preferences
    - Currency
  - Security
    - Change Password
    - Two-Factor Authentication
  - Notifications
    - Push Notifications
    - Email Preferences
  - Data & Privacy
    - Download My Data
    - Delete Account
  - About
    - Version
    - Help & Support
    - Terms & Privacy
  - Log Out (red)

### 8.2 Web Pages (Desktop)

#### Common Layout Structure:
```
┌────────────────────────────────────────────────────────────┐
│  Top Bar (fixed, 64px height)                              │
│  Logo | Search | Add Expense Btn | Notifications | Avatar  │
├──────────┬─────────────────────────────────────────────────┤
│          │                                                  │
│ Sidebar  │                 Main Content Area               │
│ (240px)  │                                                  │
│          │                                                  │
│ Nav      │                                                  │
│ Items    │                                                  │
│          │                                                  │
│          │                                                  │
└──────────┴─────────────────────────────────────────────────┘
```

#### Page 1: Dashboard (`/dashboard`)
**Main Content Area:**

- Page heading: "Dashboard"

- Balance Summary (full width):
  - Two large cards side-by-side (50% each):
    - **You Owe Card**
      - Icon, label, large amount
      - List of top 3 people you owe
      - "See All" link
    - **You're Owed Card**
      - Icon, label, large amount
      - List of top 3 people who owe you
      - "See All" link

- Stats Row (3 cards, 33% each):
  - Total Expenses This Month
  - Most Active Group
  - Largest Expense

- Two-column layout:
  
  **Left Column (60%):**
  - Recent Activity
    - Heading with "View All" link
    - List of 10 recent activities
    - Load more button
  
  **Right Column (40%):**
  - Quick Actions (stacked cards):
    - Add Expense
    - Scan Receipt
    - Settle Up
  - Groups Overview:
    - List of groups with balances
    - "See All Groups" link

#### Page 2: Activity Feed (`/activity`)
**Main Content Area:**

- Page heading: "Activity Feed"

- Filter bar:
  - Filter chips: All | Expenses | Payments | Groups | Friends
  - Date range picker
  - Search input
  
- Activity list (card-based):
  - Infinite scroll
  - Each card:
    - Left: Avatar/icon
    - Center: Activity description, timestamp
    - Right: Amount (if applicable), action buttons

#### Page 3: Expenses List (`/expenses`)
**Main Content Area:**

- Page heading: "All Expenses" with "Add Expense" button

- Filter & Sort bar:
  - Search expenses
  - Filter by: Category, Date Range, Group, Person, Status
  - Sort by: Date, Amount, Description
  - View toggle: List / Grid

- Expenses table (or card grid based on view):
  - Columns: Date, Description, Category, Amount, Paid By, Split, Status, Actions
  - Row actions: View, Edit, Delete
  - Pagination or infinite scroll

#### Page 4: Add/Edit Expense (`/expenses/new` or `/expenses/:id/edit`)
**Main Content Area:**

- Page heading: "Add Expense" or "Edit Expense"

- Two-column form:
  
  **Left Column:**
  - Description input
  - Amount input (large, prominent)
  - Category selector (icon grid)
  - Date picker
  - Receipt upload area (drag & drop or click)
  - Notes textarea
  - Attachments
  
  **Right Column:**
  - "With you and:" section
    - Search/select participants
    - Selected participants list
  - "Paid by" section
    - Select payers
  - Split method selector
  - Split preview (live calculation)
    - Table showing each person's share
  
- Bottom actions:
  - Cancel button
  - Save button (primary)

#### Page 5: Expense Detail (`/expenses/:id`)
**Main Content Area:**

- Breadcrumb: Dashboard > Expenses > [Expense Description]

- Header card:
  - Left: Category icon (large)
  - Center: 
    - Description (H1)
    - Amount (large)
    - Date, Category
  - Right:
    - Edit button
    - Delete button
    - More actions dropdown

- Content area (tabs or sections):
  
  **Details Tab:**
  - Paid by: Avatar, Name, Amount
  - Split among: Table of participants with amounts
  - Receipt: Image gallery (if exists)
  - Notes: Text
  - Attachments: Download links
  
  **Activity Tab:**
  - Edit history
  - Related payments

#### Page 6: Groups List (`/groups`)
**Main Content Area:**

- Page heading: "Groups" with "Create Group" button

- Grid of group cards (3 per row):
  - Each card:
    - Group photo
    - Group name
    - Member count
    - Balance summary (visual indicator)
    - "View Details" button
  
- Empty state: Illustration + "Create your first group"

#### Page 7: Group Detail (`/groups/:id`)
**Main Content Area:**

- Breadcrumb: Dashboard > Groups > [Group Name]

- Header:
  - Group photo (left)
  - Group name (H1)
  - Member avatars (horizontal list)
  - Settings button
  - Add Expense button

- Tabs:
  - **Overview Tab:**
    - Group balance summary
    - Quick stats (Total expenses, Member count, etc.)
    - Recent expenses
  
  - **Expenses Tab:**
    - Filter & sort bar
    - Expenses table (same as global expenses page, but filtered to group)
  
  - **Balances Tab:**
    - Table showing balances between all members
    - Settle up options
  
  - **Members Tab:**
    - List of members with actions (remove, change role)
    - Add member button

#### Page 8: Friends List (`/friends`)
**Main Content Area:**

- Page heading: "Friends" with "Add Friend" button

- Tabs:
  - **All Friends:**
    - Search bar
    - List/table of friends:
      - Avatar, Name, Balance (you owe / owed to you), Actions
  
  - **Friend Requests:**
    - Pending received requests
    - Pending sent requests

#### Page 9: Friend Detail (`/friends/:id`)
**Main Content Area:**

- Breadcrumb: Dashboard > Friends > [Friend Name]

- Header:
  - Avatar
  - Name
  - Balance summary
  - Actions: Add Expense, Settle Up, Remove Friend

- Tabs:
  - **Expenses Tab:**
    - All expenses with this friend
  
  - **Activity Tab:**
    - Activity history with this friend

#### Page 10: Balances Overview (`/balances`)
**Main Content Area:**

- Page heading: "Balances & Settlements"

- Summary cards (full width):
  - Total you owe
  - Total owed to you
  - Net balance

- Two-column layout:
  
  **Left Column:**
  - "You Owe" section
    - List of people/groups
    - Amounts
    - Settle buttons
  
  **Right Column:**
  - "You're Owed" section
    - List of people/groups
    - Amounts
    - Request payment buttons

- Simplify Debts section:
  - Toggle: "Use simplified debts"
  - Visualization of optimal settlements
  - "Settle all" button

#### Page 11: Insights & Analytics (`/insights`)
**Main Content Area:**

- Page heading: "Insights & Analytics" with Export button

- Period selector (tabs or dropdown):
  - This Month | Last Month | Last 3 Months | Last Year | Custom

- Stats cards (4 across):
  - Total Spent
  - Avg per Day
  - Largest Expense
  - Most Frequent Category

- Charts section (grid layout):
  
  **Row 1:**
  - Spending by Category (Pie chart, 50% width)
  - Spending Trend (Line chart, 50% width)
  
  **Row 2:**
  - Monthly Comparison (Bar chart, full width)
  
  **Row 3:**
  - Top Expenses (Table, 50% width)
  - Category Breakdown (Table, 50% width)

- Export modal:
  - Format: CSV, PDF, Excel
  - Date range
  - What to include (checkboxes)
  - Download button

#### Page 12: Settings (`/settings`)
**Main Content Area:**

- Page heading: "Settings"

- Tabbed interface (vertical tabs on left, content on right):
  
  **Profile Tab:**
  - Avatar upload
  - Name, Email, Phone
  - Username
  - Bio
  - Save button
  
  **Preferences Tab:**
  - Default currency
  - Language
  - Date format
  - Theme (Light/Dark)
  - Save button
  
  **Notifications Tab:**
  - Email notifications (toggles for each type)
  - Push notifications (toggles)
  - Digest preferences
  - Save button
  
  **Security Tab:**
  - Change password form
  - Two-factor authentication setup
  - Active sessions list
  - Save button
  
  **Privacy Tab:**
  - Who can add me to groups
  - Who can see my expenses
  - Data download
  - Delete account
  
  **Connected Accounts Tab:**
  - List of connected OAuth accounts
  - Payment integrations
  - Disconnect options

---

## 9. Data Models

### 9.1 Split Calculation Logic

#### Equal Split
```
Split Amount per Person = Total Amount / Number of Participants
```

**Example:**
- Total: $100
- Participants: 4 people
- Each owes: $25

#### Exact Amounts
Users manually specify exactly what each person owes.

**Example:**
- Total: $100
- Person A owes: $40
- Person B owes: $35
- Person C owes: $25
- **Validation:** Sum must equal total

#### Percentages
Each person is assigned a percentage of the total.

**Example:**
- Total: $100
- Person A: 40% → owes $40
- Person B: 35% → owes $35
- Person C: 25% → owes $25
- **Validation:** Percentages must sum to 100%

#### Shares
Each person is assigned a number of shares.

**Example:**
- Total: $100
- Person A: 2 shares
- Person B: 2 shares
- Person C: 1 share
- Total shares: 5
- Per-share value: $100 / 5 = $20
- Person A owes: 2 × $20 = $40
- Person B owes: 2 × $20 = $40
- Person C owes: 1 × $20 = $20

### 9.2 Debt Simplification Algorithm

When multiple people owe each other in a group, the algorithm minimizes the number of transactions.

**Example:**
- A owes B: $20
- B owes C: $30
- A owes C: $10

**Without simplification:**
- 3 transactions

**With simplification:**
- A owes C: $30
- B owes C: $10
- 2 transactions

**Algorithm (Greedy approach):**
1. Calculate net balance for each person
2. Create two lists: creditors (net positive) and debtors (net negative)
3. Sort both lists
4. Match largest creditor with largest debtor
5. Settle the minimum of the two amounts
6. Update balances and repeat until all settled

### 9.3 Currency Conversion Logic

**Rules:**
1. Each expense stores its original currency
2. Exchange rates are fetched and cached hourly
3. When displaying in a different currency:
   - Use historical rate for the expense date (if available)
   - Otherwise use current rate
4. Balances are always shown in user's default currency
5. Conversion formula: `Converted Amount = Original Amount × Exchange Rate`

**Example:**
- User's default currency: USD
- Expense: €50 on Jan 1, 2026
- Historical EUR/USD rate on Jan 1: 1.10
- Displayed amount: $55

### 9.4 Balance Calculation

Balances are computed from expense participants:

```sql
-- Calculate balance between User A and User B
SELECT 
  SUM(CASE 
    WHEN ep.user_id = :userA THEN ep.owed_amount 
    ELSE -ep.owed_amount 
  END) as net_balance
FROM expense_participants ep
JOIN expenses e ON e.id = ep.expense_id
WHERE e.deleted_at IS NULL
  AND ep.user_id IN (:userA, :userB)
  AND ep.expense_id IN (
    SELECT expense_id FROM expense_participants 
    WHERE user_id IN (:userA, :userB)
    GROUP BY expense_id
    HAVING COUNT(DISTINCT user_id) = 2
  )
```

**Optimization:** 
- Balances are cached in the `balances` table
- Updated via triggers on expense participant changes
- Recalculated daily for consistency

---

## 10. Security & Compliance

### 10.1 Authentication & Authorization

- **Password Policy:**
  - Minimum 8 characters
  - At least one uppercase, one lowercase, one number
  - Bcrypt hashing (10 rounds)
  
- **JWT Tokens:**
  - Access token: 15-minute expiry
  - Refresh token: 7-day expiry
  - Stored in httpOnly cookies (web) or secure storage (mobile)
  
- **OAuth 2.0:**
  - Google, Apple, Facebook login
  - Only request necessary scopes (email, profile)
  
- **Two-Factor Authentication:**
  - TOTP-based (Google Authenticator, Authy)
  - Backup codes provided

### 10.2 Data Protection

- **Encryption:**
  - In transit: TLS 1.3
  - At rest: AES-256 for sensitive data
  - Database: Encrypted RDS volumes
  
- **PII Handling:**
  - Email, phone numbers stored encrypted
  - Credit card info never stored (if payments added)
  - GDPR compliant: Right to access, right to be forgotten
  
- **File Uploads:**
  - Receipts and attachments scanned for malware
  - Max file size: 10MB
  - Allowed types: PDF, JPEG, PNG, HEIC
  - Stored in S3 with signed URLs (expiry: 1 hour)

### 10.3 API Security

- **Rate Limiting:**
  - Per IP: 100 requests/minute
  - Per user: 1000 requests/hour
  - Stricter limits on auth endpoints (5 login attempts / 15 min)
  
- **Input Validation:**
  - All inputs validated against schemas (Zod)
  - SQL injection prevention (Prisma ORM)
  - XSS prevention (sanitized outputs)
  
- **CORS:**
  - Whitelist allowed origins
  - Credentials allowed only for same-origin

### 10.4 Compliance

- **GDPR:**
  - Data portability (export all data)
  - Right to deletion (soft delete, hard delete after 30 days)
  - Privacy policy, cookie consent
  
- **CCPA:**
  - California residents can request data deletion
  
- **Financial Data:**
  - Not a payment processor (just records)
  - No PCI DSS compliance needed (unless direct payments added)

---

## 11. Success Metrics

### 11.1 User Acquisition Metrics
- **New Sign-ups:** Target 10K/month by Month 6
- **Activation Rate:** % of sign-ups who add first expense (Target: >70%)
- **Referral Rate:** % of users who invite friends (Target: >30%)

### 11.2 Engagement Metrics
- **DAU/MAU Ratio:** Daily Active / Monthly Active (Target: >0.25)
- **Weekly Active Users:** (Target: >60% of total users)
- **Avg Session Duration:** (Target: >3 minutes)
- **Expense Entry Rate:** Avg expenses per user per week (Target: >3)

### 11.3 Feature Adoption Metrics
- **Receipt Scan Usage:** % of expenses via receipt scan (Target: >40%)
- **Group Creation:** % of users in at least one group (Target: >60%)
- **Settlement Rate:** % of debts settled within 30 days (Target: >50%)
- **Analytics View:** % of users viewing insights monthly (Target: >35%)

### 11.4 Retention Metrics
- **D1 Retention:** % of users active day after sign-up (Target: >60%)
- **D7 Retention:** (Target: >40%)
- **D30 Retention:** (Target: >25%)
- **Churn Rate:** Monthly user churn (Target: <10%)

### 11.5 Quality Metrics
- **OCR Accuracy:** Receipt scan field accuracy (Target: >95%)
- **Bug Rate:** Critical bugs per release (Target: <2)
- **Crash Rate:** App crashes per session (Target: <0.5%)
- **API Response Time:** P95 latency (Target: <300ms)

### 11.6 Business Metrics
- **NPS (Net Promoter Score):** (Target: >50)
- **CSAT (Customer Satisfaction):** (Target: >4.5/5)
- **Support Ticket Volume:** Tickets per 1000 users (Target: <20)

---

## 12. Roadmap & Phases

### Phase 1: MVP (Months 1-3)
**Goal:** Launch with core functionality

**Features:**
- User authentication (email, Google, Apple)
- Basic profile management
- Add/edit/delete expenses (manual entry)
- Equal split only
- Friends management
- Basic groups
- Balance calculation
- Simple settlement recording
- Activity feed
- Mobile app (iOS & Android)
- Web app (responsive)

**Deliverables:**
- Functional MVP apps (mobile + web)
- Basic backend API
- PostgreSQL database
- Deployment to production
- Basic analytics tracking

### Phase 2: Premium Features (Months 4-5)
**Goal:** Add advanced features

**Features:**
- Receipt scanning (OCR)
- Multiple split methods (exact, %, shares)
- Recurring expenses
- Multi-currency support
- Advanced search & filters
- Spending insights & analytics
- Charts & visualizations
- Export to CSV/PDF
- Payment reminders
- Offline mode (mobile)

**Deliverables:**
- OCR service integration
- Analytics dashboard
- Background jobs system
- Enhanced mobile features

### Phase 3: Social & Engagement (Months 6-7)
**Goal:** Increase engagement and virality

**Features:**
- Comments on expenses
- Reactions (emojis)
- Expense stories (photo galleries)
- Social sharing
- Friend recommendations
- Group templates (trips, households, etc.)
- Gamification (badges, streaks)
- In-app tutorials & tips

**Deliverables:**
- Social features
- Gamification engine
- Enhanced onboarding

### Phase 4: Optimization & Scale (Months 8-9)
**Goal:** Optimize for performance and scale

**Features:**
- Performance improvements
- Advanced caching
- Database optimizations
- Real-time updates (WebSockets)
- Push notifications (mobile)
- Email digests
- Smart notifications
- A/B testing framework

**Deliverables:**
- Optimized backend
- Real-time infrastructure
- Notification service
- A/B testing platform

### Phase 5: Integrations & Ecosystem (Months 10-12)
**Goal:** Expand ecosystem

**Features:**
- Payment integrations (Venmo, PayPal, UPI, etc.)
- Accounting software exports (QuickBooks, Xero)
- Bank account linking (read-only, auto-import)
- Calendar integrations
- API for third-party apps
- Browser extension
- Slack/Discord bots

**Deliverables:**
- Integration platform
- Public API documentation
- Browser extension
- Chat platform bots

### Future Considerations (12+ months)
- AI-powered expense categorization
- Predictive budgeting
- Bill negotiation service
- Group investment tracking
- Cryptocurrency support
- Tax optimization tools
- Financial education content

---

## 13. Additional Professional Enhancements

### 13.1 Accessibility (a11y)
- **WCAG 2.1 AA Compliance**
- Screen reader support
- Keyboard navigation
- High contrast mode
- Adjustable font sizes
- Alternative text for images
- Focus indicators

### 13.2 Internationalization (i18n)
- Support for 10+ languages initially:
  - English, Spanish, French, German, Hindi, Mandarin, Japanese, Portuguese, Russian, Arabic
- RTL (Right-to-Left) layout support
- Locale-specific number and date formatting
- Currency symbols and formats

### 13.3 Error Handling & User Feedback
- **Graceful Degradation:**
  - Offline mode with queue
  - Fallback UI states
  
- **User-Friendly Error Messages:**
  - No technical jargon
  - Actionable suggestions
  - Retry mechanisms
  
- **Loading States:**
  - Skeleton screens
  - Progress indicators
  - Optimistic UI updates

### 13.4 Onboarding & User Education
- **Interactive Tutorials:**
  - Walkthroughs for key features
  - Tooltips and hints
  - Video tutorials (in-app)
  
- **Sample Data:**
  - Pre-populated demo data for new users
  - "Try it out" mode
  
- **Help Center:**
  - Searchable FAQ
  - Feature documentation
  - Troubleshooting guides

### 13.5 Data Backup & Recovery
- **Automated Backups:**
  - Daily database snapshots
  - Point-in-time recovery
  - 30-day retention
  
- **User-Initiated Exports:**
  - Full data export anytime
  - Multiple formats (JSON, CSV, PDF)

### 13.6 Compliance & Legal
- **Terms of Service**
- **Privacy Policy**
- **Cookie Policy**
- **Acceptable Use Policy**
- **COPPA Compliance** (if allowing users under 13)

### 13.7 User Support & Feedback

**No live customer support initially. Focus on self-service:**

#### FAQ Section
- **In-App FAQ:**
  - Searchable knowledge base
  - Categories: Getting Started, Expenses, Groups, Settlements, Account
  - Video tutorials (optional, links to YouTube)
  - Troubleshooting guides
  
- **Common Questions:**
  - How do I add an expense?
  - How do I split an expense unequally?
  - How do I settle up with someone?
  - How do I create a group?
  - How do I scan a receipt?
  - How do currency conversions work?
  - How do I export my data?
  - How do I delete my account?

#### User Feedback System
- **In-App Feedback Button:**
  - Simple form: "Tell us what you think"
  - Fields: Feedback type (Bug, Feature Request, General), Message, Email (optional)
  - Sends to dedicated email: feedback@splyt.app
  - Auto-reply: "Thanks! We read every message"
  
- **Feature Request Board:**
  - Public roadmap (optional)
  - Users can upvote features
  - Transparency on what's being built
  
- **Bug Reporting:**
  - "Report a Bug" button in settings
  - Auto-includes: Device, OS, App version
  - Screenshot attachment option
  - Email notification when bug is fixed

**Future:** Add live chat support after reaching 10K users

---

## 14. Design Refinements

### 14.1 Micro-interactions
- Button press animations (subtle scale and opacity)
- Swipe gestures (delete expense, mark as settled)
- Pull-to-refresh (mobile)
- Smooth page transitions (fade, slide)
- Loading states with skeleton screens

**Note for Google AI Studio Preview:**
- Keep animations subtle (0.2s duration)
- Use CSS transitions over complex JavaScript animations
- Ensure smooth rendering in both web and mobile preview modes

### 14.2 Empty States
- First-time user states with illustrations
- No data states with clear CTAs
- Error states with retry options

### 14.3 Confirmation Dialogs
- Delete confirmations
- Settlement confirmations
- Edit warnings (if multiple people involved)

### 14.4 Toasts & Notifications
- Success toasts (green, check icon)
- Error toasts (red, X icon)
- Info toasts (blue, i icon)
- Undo actions within toasts (5-second window)

---

## Conclusion

This PRD provides a comprehensive blueprint for building **Splitur**, a modern, beautiful expense-splitting application with a clean, minimal design aesthetic.

**Key Takeaways:**

1. **Brand Identity:**
   - **Name:** Splitur - modern, memorable, unique
   - **Colors:** Near Black (#080808), White (#FFFFFF), Blue (#2A67F4)
   - **Philosophy:** Ultra-minimal, clean, purposeful use of color

2. **Design System:**
   - 90% Near Black and White interface
   - Blue accent used sparingly for primary actions (10%)
   - Inter font family - professional and readable
   - Soft border radius (10-16px) for modern feel
   - Subtle shadows for depth

3. **Technology Stack:**
   - 100% free and open-source technologies
   - Next.js + React Native + TypeScript
   - PostgreSQL + Redis
   - Tesseract.js for OCR (free, open-source)
   - Recharts for visualizations
   - ExcelJS/jsPDF for exports

4. **User Experience:**
   - Simple, intuitive flows
   - Quick expense entry (<30 seconds)
   - Smart debt simplification
   - Real-time updates
   - Works offline

5. **Support Model:**
   - FAQ-based self-service
   - In-app feedback system
   - No live support initially
   - Community-driven feature requests

6. **Development Approach:**
   - Modular, maintainable codebase
   - Open-source libraries only
   - Free hosting tiers (Vercel, Supabase)
   - Optimized for Google AI Studio preview

**Design for Google AI Studio Preview:**
- Responsive layouts render perfectly in web and mobile preview modes
- Clean white backgrounds with minimal colors
- Blue accent (#2A67F4) provides clear visual hierarchy
- Consistent spacing and typography scale beautifully
- Cards and components maintain styling across all viewports
- Near Black text (#080808) ensures excellent readability

**Why This Works:**
✅ Professional and modern aesthetic  
✅ Minimal color palette reduces visual noise  
✅ Clear hierarchy through typography and spacing  
✅ Fast, lightweight, performant  
✅ Easy to maintain and scale  
✅ Looks expensive and premium  
✅ Renders beautifully in any environment  

This document serves as the complete guide for building Splitur with modern, free, and open-source technologies while maintaining professional quality and exceptional user experience.

---

**Document Version History:**
- v1.0 - February 7, 2026 - Initial comprehensive PRD
- v2.0 - February 7, 2026 - Updated with Splitur branding, Near Black/White/Blue color palette, simplified approach
