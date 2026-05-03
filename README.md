# Refinance Loan Finders — Deployment Checklist

## Before You Deploy

1. **Replace the redirect URL** in `index.html` and `get-started.html`
   Search for `https://YOUR-PRIMARY-SITE.com` and replace with your actual primary website URL.

2. **Add your NMLS number**
   Search for `[YOUR-NMLS-NUMBER]` in all HTML files and replace with your Oregon NMLS license number.

3. **Verify your sending domain in Resend**
   Log in to resend.com and verify `refinanceloanfinders.com` so `leads@refinanceloanfinders.com` is authorized to send.

4. **Add the Resend API key to Vercel**
   In your Vercel project → Settings → Environment Variables, add:
   - Key: `RESEND_API_KEY`
   - Value: your Resend API key

## Deploy

```bash
npm install
npx vercel --prod
```

## Lead Emails

All leads go to `westlinnhomeloans@gmail.com` with subject:
`🏠 New Lead: [Name] — [Loan Type] — refinanceloanfinders.com`
