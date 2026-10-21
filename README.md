# Maison Amare Studio - Salesforce Agentforce Embedded Messaging Demo

This project is a landing page demo created for showcasing **Salesforce Embedded Messaging (MIAW - Messaging for In-App and Web)** integrated with **Salesforce Agentforce**.

---

## 📌 Project Overview

- **Brand / Theme:** Maison Amare Studio (The First Korean Custom Perfume Bar in Indonesia)
- **Purpose:** Demonstrate how prospective customers interacting with a business landing page can seamlessly connect and chat with a Salesforce Agentforce AI agent / live chat via Salesforce Embedded Messaging.
- **Tech Stack:**
  - HTML5 & Modern Responsive Layout
  - [Tailwind CSS](https://tailwindcss.com/) (CDN)
  - Google Fonts (`Unbounded` & `Lato`)
  - Salesforce Embedded Service Web Bootstrap (Embedded Messaging)

---

## 🤖 Salesforce Agentforce & Embedded Messaging Integration

The embedded chat widget connects to Salesforce Messaging for In-App and Web (MIAW) backed by Salesforce Agentforce:

- **Deployment Name:** `LiveChat`
- **Org ID:** `00DHu00000yv5as`
- **Site URL:** `https://pt1775550561975.my.site.com/ESWLiveChat1792135744669`
- **SCRT 2.0 URL:** `https://pt1775550561975.my.salesforce-scrt.com`

The bootstrap script and initialization logic are integrated at the bottom of [`index.html`](index.html):

```html
<script>
  function initEmbeddedMessaging() {
    try {
      embeddedservice_bootstrap.settings.language = 'en_US';

      embeddedservice_bootstrap.init(
        '00DHu00000yv5as',
        'LiveChat',
        'https://pt1775550561975.my.site.com/ESWLiveChat1792135744669',
        {
          scrt2URL: 'https://pt1775550561975.my.salesforce-scrt.com'
        }
      );
    } catch (err) {
      console.error('Error loading Embedded Messaging: ', err);
    }
  }
</script>
<script 
  type="text/javascript" 
  src="https://pt1775550561975.my.site.com/ESWLiveChat1792135744669/assets/js/bootstrap.min.js" 
  onload="initEmbeddedMessaging()">
</script>
```

---

## 🚀 How to Run the Demo

You can run this project locally using any simple HTTP web server (to ensure the embedded script and site origins operate properly without `file://` protocol restrictions):

### Option 1: Using Python
```bash
# Python 3
python -m http.server 8000
```
Open `http://localhost:8000` in your web browser.

### Option 2: Using Node.js (npx serve or live-server)
```bash
npx serve .
```

### Option 3: VS Code Live Server
Right-click [`index.html`](index.html) and select **"Open with Live Server"**.

---

## 💬 Demo Flow & Testing
1. Open the landing page.
2. Locate the floating chat launcher icon in the bottom corner.
3. Start a conversation to engage with the **Salesforce Agentforce** agent for inquiries regarding perfumes, workshops, booking consultations, or customer support.

