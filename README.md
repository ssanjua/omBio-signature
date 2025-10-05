## OmBio Email Signatures

Have questions or need help? ✉️ Email me: ppaupallares@gmail.com 

### Which file should I use?

- AF: for Ahmed Rarag (Co-founder)
- BC: for Berkan Çokdeğerli (Co-founder)

### Quick start (most people only need this)

- Pick the right file (AF or BC) above.
- Open the `.html` file in your web browser.
- Select all (Ctrl/Cmd+A) and copy (Ctrl/Cmd+C).
- Open your email app's signature settings and paste. Save. Done!

Two ready-to-use HTML signatures for email clients:

- `om-bio_signature_AF.html`
- `om-bio_signature_BC.html`

Assets (logo and icons) use absolute HTTPS URLs so no attachments are required.

### Quick preview

- Open either `.html` in a browser to preview.
- Copy the full HTML and paste it into your email client's signature editor (see client-specific steps below).

## Compatibility and technical approach

- Table-based layout with inline styles (best practice for HTML email).
- Images hosted over HTTPS via `raw.githubusercontent.com` under `assets/`.
- Mobile media queries included; supported in Apple Mail/iOS and most modern apps. Outlook for Windows ignores media queries.
- Fonts: `Montserrat, Arial, Helvetica, sans-serif` fallback chain. If webfonts are blocked, a system sans-serif will be used.

## Client-specific instructions

### Outlook (Windows, desktop)

Recommended (simple) method:
1. Outlook > File > Options > Mail > Signatures.
2. Create a new signature (give it a name).
3. Open `om-bio_signature_*.html` in a browser, Select All and Copy.
4. Paste into the Outlook signature editor (Ctrl+V) keeping formatting.
5. Set as default for New messages and/or Replies.

Advanced (Signatures folder) method:
1. Create a signature from Outlook (as above) and close Outlook.
2. Open `%APPDATA%\\Microsoft\\Signatures`.
3. Edit the corresponding `.htm` and replace its body with the HTML from `om-bio_signature_*.html`.
4. Reopen Outlook.

Notes for Outlook Windows:
- Outlook may ignore `max-width` and media queries; this signature uses tables and fixed widths for robustness.
- If images are not visible, enable “Download pictures automatically” or add the asset domain as a safe sender.

### Outlook (Mac, desktop)
1. Outlook > Settings > Signatures.
2. Create a new signature.
3. Open the `.html` in a browser, copy all, and paste into the signature editor (keep formatting).
4. Set as default if desired.

### Outlook Web (OWA)
1. Settings (gear) > Mail > Compose and reply > Email signature.
2. Paste the contents of the `.html` (OWA may simplify advanced styles).
3. Save and set as default.

### Gmail (Web)
1. Settings > See all settings > General tab > Signature.
2. “Create new”, give it a name.
3. Open the `.html` in a browser, copy all, and paste into Gmail's signature editor.
4. Save at the bottom of the page.

Gmail notes:
- Gmail strips external `<style>`; this signature relies on inline CSS for compatibility.
- Media queries are not applied; layout remains readable.

### Apple Mail (macOS)

Simple method:
1. Mail > Settings > Signatures.
2. Create a new signature.
3. Copy from the browser the contents of the `.html` and paste into the signature.
4. Uncheck “Always match my default message font” to preserve styles.

Advanced method (if paste loses formatting):
1. Create a signature, then quit Mail.
2. Open `~/Library/Mail/V*/MailData/Signatures/` (V number varies with macOS).
3. Find the most recent `.mailsignature` and replace its body with the `.html` content (keep the file's headers intact).
4. Mark the file as Locked (Get Info) and reopen Mail.

### iOS Mail (iPhone/iPad)
1. Email yourself from desktop with the signature applied.
2. On iOS, open the email, long-press the signature > Copy.
3. Settings > Mail > Signature, paste the copied signature.

Mobile limitations:
- Gmail for iOS/Android and Outlook Mobile often support only plain-text signatures in settings; pasted HTML may be simplified.
- iOS Mail preserves HTML when pasted from a received email.

### Thunderbird
1. Account Settings > Signature.
2. Check “Use HTML”.
3. Paste the `.html` contents or choose “Attach the signature from a file” and point to the `.html`.

## Customization

- Two variants: `AF` and `BC`, each with a specific header image.
- To change data (phone, email, role), edit the links and text within the info cell of the respective file.
- Phone/email/web/instagram/tiktok icons live in `assets/`. If replacing icons, keep consistent sizes (20px) and add `width`/`height` attributes to avoid layout shifts.

## Best practices and compatibility notes

- Keep CSS inline; avoid advanced CSS, `position`, `float`, and image backgrounds.
- Use tables for layout. Avoid relying solely on `max-width` for Outlook Windows; keep fixed widths on tables/cells where needed.
- Add `width` and ideally `height` to `<img>` to reserve space. All images should include `alt`.
- Prefer absolute `https://` links to static assets; some corporate environments block `raw.githubusercontent.com`.
- Font stack: `Montserrat, Arial, Helvetica, sans-serif`. Properties like `font-optical-sizing` may be ignored by some clients.

## Image hosting

Currently using `raw.githubusercontent.com` URLs. Consider alternatives for maximum deliverability:

- Own subdomain: `https://assets.myombio.com/signature/...`
- CDN (Cloudflare, Amazon S3 + CloudFront, Vercel static hosting)
- GitHub Pages with custom domain

Benefits:
- Fewer corporate proxy blocks, better cache headers and performance.

## QA checklist before delivery

- Send a test email to: Gmail Web, Outlook Windows, Outlook Mac, Apple Mail.
- Verify image loading, `tel:` and `mailto:` links, and mobile rendering.
- Test dark mode in Apple Mail/iOS (design uses flat colors; should render well).

## FAQ

- Why does it look different in Outlook Windows?
  - Outlook uses Word's rendering engine, which ignores parts of modern CSS. The signature is built to degrade gracefully.

- Why don't images load?
  - Many clients block remote images by default. Users can enable image download for the sender or IT can allowlist the asset domain.

## Credits

- Base design by OmBio graphic design. HTML implementation and multi-client compatibility adjustments made made with ❤️ by ssanjua


