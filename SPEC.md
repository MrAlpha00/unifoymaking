# UniFoy Making - Service Marketplace Website Specification

## Project Overview
- **Project Name**: UniFoy Making
- **Type**: Service Marketplace Website
- **Core Functionality**: A platform connecting users with custom service providers
- **Target Users**: Customers seeking services and service providers offering services

---

## UI/UX Specification

### Color Palette
- **Primary**: `#0D1B2A` (Deep Navy)
- **Secondary**: `#1B263B` (Dark Blue)
- **Accent**: `#E94560` (Vibrant Coral Red)
- **Accent Secondary**: `#00D9FF` (Electric Cyan)
- **Surface**: `#162032` (Card Background)
- **Surface Light**: `#1F2D40` (Hover states)
- **Text Primary**: `#FFFFFF`
- **Text Secondary**: `#A0AEC0` (Muted gray)
- **Success**: `#10B981`
- **Warning**: `#F59E0B`

### Typography
- **Primary Font**: 'Outfit', sans-serif (Google Fonts)
- **Heading Sizes**:
  - H1: 4rem (64px) - Hero title
  - H2: 2.5rem (40px) - Section titles
  - H3: 1.5rem (24px) - Card titles
  - H4: 1.25rem (20px) - Subheadings
- **Body**: 1rem (16px)
- **Small**: 0.875rem (14px)

### Layout
- **Max Width**: 1280px
- **Spacing Scale**: 4px, 8px, 16px, 24px, 32px, 48px, 64px, 96px
- **Border Radius**: 12px (cards), 8px (buttons), 50% (avatars)
- **Glass Effect**: `background: rgba(22, 32, 50, 0.8); backdrop-filter: blur(20px);`

### Responsive Breakpoints
- **Mobile**: < 768px
- **Tablet**: 768px - 1024px
- **Desktop**: > 1024px

### Visual Effects
- **Card Hover**: translateY(-8px) with glow shadow
- **Button Hover**: Scale(1.02) with brightness increase
- **Gradient Backgrounds**: Diagonal from primary to secondary
- **Accent Glow**: box-shadow with accent color at 30% opacity
- **Glass Morphism**: Backdrop blur on header and cards
- **Transitions**: All 0.3s cubic-bezier(0.4, 0, 0.2, 1)

---

## Page Structure

### 1. Homepage (index.html)

#### Header (Fixed)
- Logo (left): "UniFoy Making" text logo with accent color
- Navigation (center): Home, Services, About, Blog, Contact
- Auth Buttons (right): Sign In (outline), Sign Up (filled accent)

#### Hero Section
- Full viewport height (100vh)
- Centered content
- H1: "Find Your Perfect Service"
- Subtitle: "Connect with expert professionals for all your needs"
- Search Bar (centered):
  - Large input with placeholder "Search for services..."
  - Search icon button
  - Glass morphism styling

#### Products/Services Section
- Section Title: "Our Services"
- Grid of 3 service cards (3 columns desktop, 1 mobile):
  - **Web Development** - Icon: code, Description: "Custom websites & web apps"
  - **Mobile Apps** - Icon: phone, Description: "iOS & Android applications"
  - **UI/UX Design** - Icon: palette, Description: "Beautiful user interfaces"
- Each card has:
  - Icon in accent color
  - Title
  - Description
  - "Learn More" button
  - Glass card effect with hover animation

#### Info Section
- Title: "Why Choose Us"
- 3 feature cards:
  - Expert Professionals: "Verified experts in every field"
  - Secure Payments: "Protected transactions & refunds"
  - 24/7 Support: "Round-the-clock assistance"

#### Blog Section
- Title: "Latest from Our Blog"
- Grid of 3 blog post cards:
  - Blog 1: "Getting Started with Web Development"
  - Blog 2: "The Future of Mobile Apps"
  - Blog 3: "UX Design Best Practices"
- Each card: Image placeholder, Title, Excerpt, "Read More" link

#### Newsletter Section
- Title: "Stay Updated"
- Subtitle: "Subscribe to get the latest services and offers"
- Email input + Subscribe button
- Background: Gradient with accent glow

#### Footer
- 4 columns:
  - **Company**: Logo, description, social icons
  - **Quick Links**: Home, Services, About, Blog
  - **Support**: Help Center, Contact Us, FAQ, Privacy Policy
  - **Legal**: Terms & Conditions, Privacy Policy, Refund Policy
- Bottom bar: Copyright, social links

#### Sign In/Sign Up CTA at bottom
- Repeat auth buttons

---

### 2. Login Page (login.html)

#### Centered Card
- Title: "Welcome Back"
- Subtitle: "Sign in to continue"
- Form:
  - Email input
  - Password input
  - "Forgot Password?" link
  - Sign In button
- Divider: "or continue with"
- OAuth Buttons:
  - Google Sign In (icon + text)
  - GitHub Sign In (icon + text)
- Footer: "Don't have an account? Sign Up"

---

### 3. Sign Up Page (signup.html)

#### Centered Card
- Title: "Create Account"
- Subtitle: "Join us today"
- Form:
  - Full Name input
  - Email input
  - Password input
  - Confirm Password input
  - Terms checkbox
  - Sign Up button
- Divider: "or sign up with"
- OAuth Buttons:
  - Google Sign Up
  - GitHub Sign Up
- Footer: "Already have an account? Sign In"

---

### 4. User Account Page (account.html)

#### Header
- Logo + Auth (logged in state)

#### Main Content
- Title: "Complete Your Profile"
- Subtitle: "Tell us about your requirements to help us serve you better"

#### Requirements Form
- Form fields:
  - Service Type (dropdown): Web Development, Mobile App, UI/UX Design, Other
  - Project Description (textarea)
  - Budget Range (dropdown)
  - Timeline (dropdown)
  - Contact Number
  - Company/Organization (optional)
- Buttons: "Save for Later", "Continue"

#### Skip Option
- "Skip for now" link

---

### 5. Service Pages

#### service-web.html - Web Development
- Hero with title and description
- Features list
- Pricing packages (Basic, Standard, Premium)
- Process steps
- CTA: "Get Started"

#### service-mobile.html - Mobile Apps
- Same structure as web

#### service-design.html - UI/UX Design
- Same structure as web

---

### 6. Policy Pages

#### terms.html - Terms & Conditions
- Full page content with terms text

#### privacy.html - Privacy Policy
- Full page content with policy text

#### refund.html - Refund Policy
- Full page content with refund terms

---

## Functionality Specification

### Navigation
- Fixed header with glass effect
- Smooth scroll to sections
- Mobile hamburger menu

### Search
- Centered search bar with icon
- Placeholder styling

### Authentication
- Form validation
- OAuth button placeholders (link to auth endpoints)
- Redirect to account after login

### User Account
- Form with all required fields
- "Save for Later" stores data
- "Continue" proceeds (mock)

### Forms
- All inputs with proper validation
- Error states
- Success states

---

## Acceptance Criteria

1. ✓ Homepage loads with hero, search, services, info, blog, newsletter, footer
2. ✓ Header is fixed with glass effect
3. ✓ Sign In/Sign Up buttons visible in header and at bottom of homepage
4. ✓ All 3 service cards display with hover effects
5. ✓ Search bar is centered in hero
6. ✓ Login page has email, password, Google, GitHub options
7. ✓ Sign up page has all fields plus OAuth
8. ✓ Account page has complete requirements form
9. ✓ All 3 service pages exist with content
10. ✓ Terms, Privacy, Refund pages exist
11. ✓ Responsive on all devices
12. ✓ Beautiful modern UI with animations