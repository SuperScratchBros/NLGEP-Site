<div align="center">

# NLGEP, by Infinet, Infinity Network
Next Learning Generation Education Program-Next Level Games Entertainment & Proxies

![version](https://img.shields.io/badge/version-2.0-blue?style=flat-square)
![license](https://img.shields.io/badge/license-AGPLv3-green?style=flat-square)
![no service workers](https://img.shields.io/badge/service%20workers-absolutely%20not-red?style=flat-square)
![totally working svg](https://img.shields.io/badge/svg%20functionality-gorgeous%20and%20beautiful-blue?style=flat-square)

</div>

---

## Links

- https://cdn.jsdelivr.net/gh/nautilus-os/GUST@latest/svg/site.svg
- https://gust-browser.vercel.app

---
## What is this?

NLGEP is a full-featured web proxy, game collection, chat that lives entirely inside a single HTML file, allowing you to use it without any setup, hosting, or terminal access. It was built by the Infinet.

---

## Why schools can't block it 

Every single web proxy out there relies on something called a **Service Worker**, a background script that intercepts network requests before they reach the browser. It's an integral part of any other web proxy you use, allowing the proxy to communicate with its server and proxy your requests, but Service Workers ALWAYS require a live server to function. That means traditional proxies only work when hosted at a specific URL. Block that URL, and the proxy is dead. You're probably already familiar with the cat-and-mouse game between you and your admin, where someone makes a link, it gets used for a day or two, then gets blocked.

School network filters, admin installed extensions (think Securly,  Lightspeed Systems, Securly, Linewize, Blocksi, etc.) and admin-controlled browsers (like Chromebook MDM policies) are very good at exactly this. Your school maintains blocklists, with specific sites added every day to this list of sites you can't access. Many filtering extensions also have more advanced features, where they read a links metadata to detect proxy patterns and automatically add them to the blocklist. An even higher number of these extensions control what can run in the background, which is a big achilles heel for every single current proxy site available. 
GUST doesn't use Service Workers at all. Heres what we came up with instead:

<img width="1440" height="1040" alt="image" src="https://github.com/user-attachments/assets/f5403020-c0b4-4d89-b795-cfa11b898c78" /><br>

Instead, it uses **libcurl.js**, a full HTTP library compiled to WebAssembly, to make requests directly through a WebSocket tunnel called the WISP protocol. (Thanks to Mercury Workshop for these) The entire proxy engine runs as plain JavaScript inside a single HTML file. This means:

- ✅ **It can run as a local file** (`file://`), with no server and no domain to block
- ✅ **It can be hosted anywhere static files work**: GitHub Pages, Vercel, Netlify, a USB drive, a Google Doc, a Google Site, etc.
- ✅ **It can be hosted on JSDelivr or CDN sites**, because the site can be loaded through one SVG file
- ✅ **It has no Service Worker to kill**, because it never registered one
- ✅ **It can be renamed, embedded in an iframe, or wrapped in another HTML file**, giving the filter nothing to latch onto
- ✅ **It can be copy-pasted into any WYSIWYG HTML editor on the web**, because again, it's just HTML with CSS and JS inlined
- ✅ **It can be compiled into a blob: or data: url and opened that way**, again, HTML
- ✅ **It can be written to an about:blank page and used from there**, need I repeat why?

The short version: most blockers can only block URLs. NLGEP is a file. You can't block a file without obliterating a cruical part of the student user experience, and even if they take that drastic step, well, HTML can be hosted or opened in litrally anything. It's the frame of the world wide web. no more whack-a-mole, cat-and-mouse game of finding unblocked links and your school blocking them!

</div>
