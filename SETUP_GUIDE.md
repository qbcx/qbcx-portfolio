# QBCX Portfolio & Domain Setup Guide

## 🎯 Goal
Create a dark-themed portfolio website + Get free `qbcx.is-a.dev` domain

---

## Phase 1: Backend Setup (Day 1)

### Step 1: Initialize Next.js Project
```bash
# Open your terminal in the project folder
npx create-next-app@latest qbcx-portfolio --typescript --tailwind --eslint --app --src-dir --import-alias "@/*"

# Navigate to project
cd qbcx-portfolio
```

### Step 2: Project Structure Setup
```bash
# Install additional dependencies for animations
npm install framer-motion lucide-react

# Install dev dependencies
npm install --save-dev @types/node
```

### Step 3: Configure Dark Theme
1. Open `tailwind.config.ts`
2. Add dark theme configuration with electric blue accents

### Step 4: Create Basic Portfolio Structure
```
src/
├── app/
│   ├── layout.tsx         # Root layout with dark theme
│   ├── page.tsx          # Home page
│   ├── globals.css       # Global styles
│   └── components/
│       ├── Hero.tsx      # Hero section
│       ├── Skills.tsx    # Skills showcase
│       └── Navbar.tsx    # Navigation
```

### Step 5: Basic Content Setup
1. Update `app/page.tsx` with your info
2. Add your 5 skills: React/Next.js, TypeScript, Node.js, Tailwind CSS, Python
3. Set up "Full-Stack Developer" as your role

### Step 6: Deploy to Vercel
```bash
# Install Vercel CLI
npm install -g vercel

# Login to Vercel
vercel login

# Deploy
vercel

# Note your production URL (will be like: qbcx-portfolio.vercel.app)
```

---

## Phase 2: Domain Registration (Day 2)

### Step 7: Fork is-a-dev Repository
1. Go to: https://github.com/is-a-dev/register
2. Click "Fork" button (top right)
3. This creates: `github.com/YOUR_USERNAME/register`

### Step 8: Create Domain Configuration
1. In your forked repo, go to `domains/` folder
2. Create new file: `domains/qbcx.json`
3. Add this content:

```json
{
  "owner": {
    "username": "YOUR_GITHUB_USERNAME",
    "email": "YOUR_EMAIL"
  },
  "record": {
    "CNAME": "qbcx-portfolio.vercel.app"
  }
}
```

### Step 9: Submit Pull Request
1. Commit your new file:
   ```bash
   git add domains/qbcx.json
   git commit -m "Add qbcx.is-a.dev"
   git push
   ```
2. Go to your fork on GitHub
3. Click "Contribute" → "Open pull request"
4. Wait for approval (usually takes 1-24 hours)

---

## Phase 3: Portfolio Development (Day 2-3)

### Step 10: Add Your Content
1. **Hero Section**: "Hi, I'm QBCX - Full-Stack Developer"
2. **Skills Section**: Your 5 technical skills with progress bars
3. **Projects Section**: "Coming Soon" placeholders
4. **Contact Section**: Email, GitHub, LinkedIn

### Step 11: Add Animations
- Text typing animation in hero
- Smooth scroll between sections
- Hover effects on skill cards
- Section fade-in animations

### Step 12: Final Polish
- Mobile responsiveness
- Electric blue accent colors (#00D4FF)
- Dark theme optimization
- Performance check

---

## 📋 Checklist

### Before Domain Registration:
- [ ] Next.js project created
- [ ] Basic portfolio pages ready
- [ ] Deployed to Vercel
- [ ] Have Vercel production URL

### After Domain Approval:
- [ ] Domain pointing to your Vercel app
- [ ] Update any hardcoded URLs in your code
- [ ] Test all functionality on live domain

---

## 🔧 Useful Commands

```bash
# Development
npm run dev

# Build for production
npm run build

# Start production server
npm run start

# Deploy to Vercel
vercel --prod
```

---

## 📁 Important Files to Create

1. `README.md` - Project documentation
2. `domains/qbcx.json` - Domain configuration
3. `src/app/components/` - React components
4. `src/app/globals.css` - Global styles

---

## ⏰ Timeline

- **Day 1**: Backend setup + Vercel deployment
- **Day 2**: Domain registration + Portfolio development
- **Day 3**: Polish + Final testing

---

## 🆘 Troubleshooting

**Domain not working?**
- Check PR is merged in is-a-dev/register
- Wait up to 24 hours for DNS propagation
- Verify CNAME points to correct Vercel URL

**Build errors?**
- Check TypeScript types
- Verify Tailwind CSS imports
- Ensure all dependencies installed

---

## 🎉 Next Steps After Setup

- Add your real projects
- Implement contact form
- Add blog section
- Set up analytics
- Create dark/light theme toggle

---

*Good luck building your portfolio, QBCX! 🚀*