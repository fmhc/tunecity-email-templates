# Tunecity Email Templates

Beautiful, responsive email templates for Supabase Authentication flows, optimized for the Tunecity music discovery platform.

## 🎵 Overview

This repository contains professionally designed HTML email templates for all Supabase authentication flows:

- **Confirm Signup** - Welcome new users to Tunecity
- **Invite User** - Team invitations and user referrals  
- **Magic Link** - Passwordless authentication
- **Password Recovery** - Secure password reset
- **Email Change** - Email address confirmation

## 🚀 Features

- ✨ Modern, music-themed design
- 📱 Fully responsive (mobile-first)
- 🎨 Consistent branding with Tunecity
- 🔒 Secure token handling (uses TokenHash instead of direct links)
- 🌐 Multiple language support ready
- ♿ Accessibility optimized
- 📧 Email client compatibility tested

## 📋 Available Templates

### 1. Confirm Signup (`confirm-signup.html`)
**Variables:** `{{ .ConfirmationURL }}`, `{{ .Token }}`, `{{ .TokenHash }}`, `{{ .SiteURL }}`, `{{ .Email }}`

Welcome new users with a warm, music-themed confirmation email.

### 2. Invite User (`invite.html`) 
**Variables:** `{{ .ConfirmationURL }}`, `{{ .Token }}`, `{{ .TokenHash }}`, `{{ .SiteURL }}`, `{{ .Email }}`

Invite friends to join your music discovery journey.

### 3. Magic Link (`magic-link.html`)
**Variables:** `{{ .ConfirmationURL }}`, `{{ .Token }}`, `{{ .TokenHash }}`, `{{ .SiteURL }}`, `{{ .Email }}`

Secure, passwordless login for returning users.

### 4. Password Recovery (`password-recovery.html`)
**Variables:** `{{ .ConfirmationURL }}`, `{{ .Token }}`, `{{ .TokenHash }}`, `{{ .SiteURL }}`, `{{ .Email }}`

Help users securely reset their passwords.

### 5. Email Change (`email-change.html`)
**Variables:** `{{ .ConfirmationURL }}`, `{{ .Token }}`, `{{ .TokenHash }}`, `{{ .SiteURL }}`, `{{ .Email }}`, `{{ .NewEmail }}`

Confirm email address changes securely.

## 🔧 Configuration

### For Self-Hosted Supabase (Coolify)

Set these environment variables in your Supabase configuration:

```bash
GOTRUE_MAILER_TEMPLATES_CONFIRMATION=https://your-username.github.io/tunecity-email-templates/confirm-signup.html
GOTRUE_MAILER_TEMPLATES_INVITE=https://your-username.github.io/tunecity-email-templates/invite.html
GOTRUE_MAILER_TEMPLATES_MAGIC_LINK=https://your-username.github.io/tunecity-email-templates/magic-link.html
GOTRUE_MAILER_TEMPLATES_RECOVERY=https://your-username.github.io/tunecity-email-templates/password-recovery.html
GOTRUE_MAILER_TEMPLATES_EMAIL_CHANGE=https://your-username.github.io/tunecity-email-templates/email-change.html
```

### For Hosted Supabase

1. Copy the HTML content from each template
2. Paste into your Supabase Dashboard → Authentication → Email Templates
3. Save each template

## 🌐 GitHub Pages Setup

1. Fork this repository
2. Go to repository Settings → Pages
3. Set Source to "Deploy from a branch"
4. Select branch: `main`, folder: `/ (root)`
5. Your templates will be available at: `https://your-username.github.io/tunecity-email-templates/`

## 🔒 Security Features

- Uses `{{ .TokenHash }}` for secure verification
- Includes both click-to-verify buttons and OTP codes
- Email prefetch protection via custom confirmation pages
- Follows OWASP email security guidelines

## 🎨 Customization

### Colors
- Primary: `#1DB954` (Spotify Green)
- Secondary: `#191414` (Dark Background)
- Accent: `#FFA500` (Orange)
- Text: `#FFFFFF` (White) / `#191414` (Dark)

### Fonts
- Headlines: Inter, system-ui
- Body: -apple-system, BlinkMacSystemFont, Segoe UI

### Brand Elements
- Music note icons (🎵, 🎶)
- Tunecity logo placement
- Consistent button styling
- Music-themed imagery

## 📱 Testing

Templates tested on:
- Gmail (Web, iOS, Android)
- Outlook (Web, Desktop, Mobile)
- Apple Mail (macOS, iOS)
- Yahoo Mail
- Thunderbird

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch
3. Test templates across email clients
4. Submit a pull request

## 📄 License

MIT License - feel free to customize for your own projects!

## 🎵 About Tunecity

Tunecity is a social music discovery platform that helps you find new music through your location and social connections. Discover what's playing around you and connect with fellow music lovers! 