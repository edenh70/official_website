# Curious Explorer App Redirect Setup

## Overview
This configuration redirects `https://edencuriosity.co.il/curiousexplorer` to your Vercel app at `https://frontend-eight-ashy-13.vercel.app/`.

## Files Created

### 1. `/curiousexplorer/index.html` (✅ Works Everywhere)
- **Purpose**: Client-side HTML redirect page
- **How it works**: When users visit `/curiousexplorer`, they'll see a loading spinner and be automatically redirected
- **Status**: ✅ Ready to use - No server configuration needed!
- **Pros**: Works on any hosting platform, simple, immediate
- **Cons**: Slight delay before redirect, less SEO-friendly

### 2. `_redirects` (Netlify)
- **Purpose**: Server-side redirect for Netlify hosting
- **How to use**: If your domain is hosted on Netlify, this file will automatically work
- **Status**: 🔄 Only use if hosted on Netlify
- **Pros**: Instant redirect, SEO-friendly (301 redirect)

### 3. `vercel.json` (Vercel)
- **Purpose**: Server-side redirect for Vercel hosting
- **How to use**: If your domain is hosted on Vercel, this file will automatically work
- **Status**: 🔄 Only use if hosted on Vercel
- **Pros**: Instant redirect, SEO-friendly

### 4. `.htaccess` (Apache)
- **Purpose**: Server-side redirect for Apache servers
- **How to use**: If your domain is hosted on an Apache server, upload this file
- **Status**: 🔄 Only use if hosted on Apache
- **Pros**: Instant redirect, SEO-friendly

## Recommended Next Steps

1. **Upload all files** to your hosting provider:
   - Upload the entire `curiousexplorer/` folder
   - Upload the config file for your hosting platform (if applicable)

2. **Test the redirect**:
   - Visit `https://edencuriosity.co.il/curiousexplorer`
   - You should be redirected to your Vercel app

3. **Clean up** (optional):
   - If using a server-side config (_redirects, vercel.json, or .htaccess), you can remove the HTML redirect
   - Keep the HTML redirect if you're unsure about your hosting platform

## Which Configuration to Use?

**Not sure which hosting platform you're using?**
- The HTML redirect (`/curiousexplorer/index.html`) will work regardless of hosting
- Just upload the `curiousexplorer` folder to your server and you're done!

**Know your hosting platform?**
- **Netlify**: Use `_redirects` (delete others)
- **Vercel**: Use `vercel.json` (delete others)
- **Apache Server**: Use `.htaccess` (delete others)
- **Other/Unknown**: Use the HTML redirect in `/curiousexplorer/index.html`

## Testing Locally
To test locally, you can use a simple HTTP server:
```bash
cd /Users/eden/PycharmProjects/website
python3 -m http.server 8000
# Then visit: http://localhost:8000/curiousexplorer
```

## Need Help?
If the redirect doesn't work after uploading:
1. Check that the `curiousexplorer` folder is at the root of your website
2. Ensure your hosting platform supports the config file you're using
3. Clear your browser cache and try again
