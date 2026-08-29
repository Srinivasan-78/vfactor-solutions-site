<!--
  @authormark v1 -- do not remove (authorship watermark)⁠​‌‌​​‌​‌​‌​​​​‌​​‌‌​‌​​‌​‌​‌​​​‌​‌‌​‌​‌‌​‌‌​‌‌‌​​‌​‌‌​​‌​‌​​‌‌‌​​‌‌​​​‌‌​‌‌​‌‌​‌​‌‌​‌​​‌​‌​​​​‌​​‌​‌​​‌‌​‌​‌​​​‌​‌‌‌​​‌‌​‌‌​‌​​‌​‌‌​‌​​​​‌​‌‌​‌​​‌‌‌​‌‌​​‌​‌‌​​​​‌‌‌​‌​‌​‌​‌‌​‌​⁠
  Copyright (c) 2026 Srinivasan Vijayaraghavan <srinivasan.shyam2000@gmail.com>
  Author: https://github.com/Srinivasan-78
  SPDX-License-Identifier: MIT
  Fingerprint: AMK1.eBiQknYNcmiBSQsihZvXuZ
-->
# vFactor Solutions — The Whole Website, Explained Simply

![vFactor Solutions social preview](docs/assets/img/og.png)

Imagine a shop. But instead of selling toys or ice cream, this shop helps
companies **find the right people to hire**, and helps people **find a job**.
The shop is called **vFactor Solutions**, and it is run by one person,
**Vijay Purushothaman**, from Chennai in India.

This repository is not the shop itself — it is the **shop window**: the website
that tells the world what vFactor does, and gives visitors a way to get in touch.

Everything here is a *static* website. That means there is no big computer
program running in the background thinking hard. There are only a few files —
some text, some styling, a little bit of JavaScript — and a web browser reads
them and draws the page. Nothing to build, nothing to install, nothing to
deploy by hand.

---

## Table of contents

1. [The one-minute version](#1-the-one-minute-version)
2. [Who the website is talking to](#2-who-the-website-is-talking-to)
3. [The pages, one by one](#3-the-pages-one-by-one)
4. [A tour down the front page](#4-a-tour-down-the-front-page)
5. [What happens when you open the site](#5-what-happens-when-you-open-the-site)
6. [What happens when you fill in a form](#6-what-happens-when-you-fill-in-a-form)
7. [The cookie banner and why it exists](#7-the-cookie-banner-and-why-it-exists)
8. [Dark mode, menus, and the other moving parts](#8-dark-mode-menus-and-the-other-moving-parts)
9. [How the files fit together](#9-how-the-files-fit-together)
10. [How the site gets onto the internet](#10-how-the-site-gets-onto-the-internet)
11. [How to run it on your own computer](#11-how-to-run-it-on-your-own-computer)
12. [Making changes without breaking anything](#12-making-changes-without-breaking-anything)
13. [Things still to fill in before launch](#13-things-still-to-fill-in-before-launch)
14. [Words you might not know](#14-words-you-might-not-know)

---

## 1. The one-minute version

```mermaid
flowchart LR
    A["A company needs<br/>to hire someone"] --> B["They visit<br/>vfactorsolutions.com"]
    C["A person needs<br/>a job"] --> B
    B --> D["They read what<br/>vFactor does"]
    D --> E["They send an email,<br/>call, or fill in a form"]
    E --> F["Vijay replies within<br/>one business day"]

    style B fill:#2E5C40,color:#ffffff
    style F fill:#2E5C40,color:#ffffff
```

That is the entire job of this website. Every single thing in this repository
exists to move a visitor from box **B** to box **E**.

---

## 2. Who the website is talking to

A website that tries to talk to everybody ends up talking to nobody. This one
has three very specific visitors in mind, and the front page asks the visitor
to pick which one they are, right at the top, using three buttons.

```mermaid
flowchart TD
    H["Front page<br/>“I'm here to…”"]
    H --> H1["🏢 Hire for my team<br/><i>a company with an empty desk</i>"]
    H --> H2["🧑‍💻 Find a role<br/><i>a person looking for a job</i>"]
    H --> H3["📋 Build a lead list<br/><i>a sales team wanting<br/>a list of possible customers</i>"]

    H1 --> P1["Jumps to<br/>“How we work”"]
    H2 --> P2["Jumps to<br/>“Submit your profile”"]
    H3 --> P3["Jumps to<br/>“What we do”"]
```

Clicking a button does two things: it slides the page down to the part that
person cares about, and it quietly makes a note (only if analytics were
allowed — more on that later) that somebody of that type visited.

---

## 3. The pages, one by one

The whole site is only **five** pages. Think of them as five sheets of paper.

| Page | File | What it is for |
|---|---|---|
| **Home** | `docs/index.html` | The whole story on one long page: services, process, prices, founder, reviews, forms, contact |
| **Privacy notice** | `docs/privacy.html` | The honest explanation of what information the site collects and why |
| **Terms of use** | `docs/terms.html` | The rules for using the site — what vFactor promises and what it does not |
| **Thank you** | `docs/thank-you.html` | The "we got your message" page you land on after sending a form |
| **Not found** | `docs/404.html` | The friendly page shown when you type a web address that does not exist |

Two of them — *Thank you* and *Not found* — are marked `noindex`. That is a
polite instruction to Google saying *"please don't put this page in search
results"*, because nobody searching the internet wants to land on somebody
else's thank-you page.

---

## 4. A tour down the front page

The home page is one long scroll. Here is every section, in order, top to
bottom, and what each one is trying to achieve.

```mermaid
flowchart TD
    S0["🔝 <b>Header</b><br/>logo, menu, dark-mode switch"]
    S1["🎯 <b>Hero</b><br/>the big headline + the three<br/>“I'm here to…” buttons + a target drawing"]
    S2["📊 <b>Stat strip</b><br/>35+ yrs · 22 yrs · 16 yrs · 6 yrs"]
    S3["🛠️ <b>Services</b><br/>the four things vFactor sells"]
    S4["🪜 <b>Process</b><br/>the five stages of a hire"]
    S5["💷 <b>Engagement models</b><br/>the three ways to pay"]
    S6["⭐ <b>Why vFactor</b><br/>four reasons to choose it"]
    S7["👤 <b>Founder</b><br/>photo, bio and career timeline"]
    S8["💬 <b>Reviews</b><br/>what people said + a form to add one"]
    S9["📄 <b>Candidates</b><br/>a form for job-seekers"]
    S10["📞 <b>Contact</b><br/>email, phone, LinkedIn"]
    S11["🦶 <b>Footer</b><br/>links, legal, copyright"]

    S0 --> S1 --> S2 --> S3 --> S4 --> S5 --> S6 --> S7 --> S8 --> S9 --> S10 --> S11
```

**Services — the four things vFactor sells**

1. **Recruitment** — finding people to hire, from brand-new graduates all the
   way up to bosses, for companies in IT, factories, telecom, engineering and
   logistics.
2. **Lead generation** — building a checked, verified list of companies that
   might want to buy what a client sells.
3. **Recruiter training** — teaching a company's *own* hiring team to do the
   job better.
4. **EdTech and campus operations** — running student enrollment, college
   counselling and career-guidance programs.

**Process — the five stages, and this is the heart of the pitch**

```mermaid
flowchart LR
    P1["<b>01 Intake</b><br/>Talk about the job.<br/>👉 You get a written brief"]
    P2["<b>02 Sourcing</b><br/>Go looking for people.<br/>👉 You get a live pipeline"]
    P3["<b>03 Validation</b><br/>Actually talk to each one.<br/>👉 You get screened profiles"]
    P4["<b>04 Shortlist</b><br/>Rank the best few.<br/>👉 You get a ranked list"]
    P5["<b>05 Offer &amp; joining</b><br/>Stay until they start.<br/>👉 You get follow-through"]

    P1 --> P2 --> P3 --> P4 --> P5

    style P3 fill:#2E5C40,color:#ffffff
    style P5 fill:#2E5C40,color:#ffffff
```

Stages **03** and **05** are highlighted because they are the two the site
argues most agencies skip. Lots of agencies forward a pile of CVs they have
never read (skipping 03), and disappear the moment an offer letter is signed
(skipping 05). The whole sales argument of this website is: *we do those two.*

**Engagement models — the three ways to pay**

| Model | Plain English | Best for |
|---|---|---|
| **Contingency** | You pay nothing until somebody actually joins your company | One urgent role |
| **Retained** | You pay in stages across the search, because the search is long and serious | Bosses, secret searches, rare skills |
| **RPO** | A flat fee every month; vFactor acts like your own hiring department | Companies hiring lots of people, all the time |

*RPO* stands for **Recruitment Process Outsourcing**. "Outsourcing" just means
paying somebody outside your company to do a job your company would otherwise
do itself.

---

## 5. What happens when you open the site

Between typing the address and seeing the page, a fair amount happens in under
a second. Here it is in order.

```mermaid
sequenceDiagram
    participant You as 🧑 You
    participant B as 🌐 Browser
    participant GH as ☁️ GitHub Pages

    You->>B: type vfactorsolutions.com
    B->>GH: please send me the home page
    GH-->>B: index.html
    Note over B: A tiny script runs first and<br/>picks light or dark mode,<br/>BEFORE anything is drawn —<br/>so there is no white flash
    B->>GH: send style.css and main.js
    GH-->>B: here they are
    B-->>You: page appears
    Note over B: main.js wakes up the menu,<br/>the scroll animations,<br/>the forms and the banner
    B-->>You: cookie banner slides in
```

The important trick is that theme script. It sits directly inside
`index.html`, before the styling loads, and it checks two things: did you
choose a theme here before (stored in your own browser), and if not, does your
computer prefer dark mode? It answers that question *before the first pixel is
painted*, so a dark-mode visitor never gets blinded by a flash of white.

---

## 6. What happens when you fill in a form

There are two forms on the site: **leave a review** and **submit your profile**
(for job-seekers). They both behave the same way.

```mermaid
flowchart TD
    A["You type your details<br/>and press Send"] --> B{"Is the hidden<br/>trap field filled in?"}
    B -- "yes — you are a robot" --> Z["Pretend it worked.<br/>Send nothing."]
    B -- "no — you are a person" --> C{"Are all the<br/>required boxes filled<br/>in correctly?"}
    C -- no --> D["Show a red message<br/>under the wrong box.<br/>Nothing is sent."]
    D --> A
    C -- yes --> E["Button shows a spinner<br/>and locks so you<br/>cannot double-send"]
    E --> F["Message is sent to<br/>Formspree, an email service"]
    F --> G{"Did Formspree<br/>accept it?"}
    G -- yes --> H["You are taken to<br/>thank-you.html"]
    G -- no --> I["Show an error and<br/>unlock the button<br/>so you can retry"]
    H --> J["📧 Vijay gets an email"]

    style Z fill:#7a2020,color:#ffffff
    style J fill:#2E5C40,color:#ffffff
```

Three details worth understanding:

**The trap field (a "honeypot").** There is an invisible text box on each form
called `_gotcha`. A human never sees it, so a human never types in it. Automatic
spam robots fill in *every* box they can find — so if that box has anything in
it, the site quietly throws the message away. The robot is told "sent!" and goes
away happy, and no spam reaches the inbox.

**It works even with JavaScript switched off.** If for any reason `main.js`
never loads, the form is still a plain old HTML form. The browser's own built-in
checking takes over (that is what the `required` word in the markup is for), and
a hidden `_next` field tells Formspree where to send the visitor afterwards —
the same thank-you page. The fancy version is an upgrade, not a requirement.

**Formspree is the postman.** A static website cannot send email by itself —
there is no program running to do it. So the form hands the message to
Formspree, an outside service, and Formspree emails it on to Vijay.

---

## 7. The cookie banner and why it exists

vFactor would like to know how many people visit the site. Counting visitors is
normal and useful. But *how* you count matters.

```mermaid
flowchart TD
    A["Page loads"] --> B{"Have you answered<br/>the banner before?"}
    B -- "no" --> C["Show the banner"]
    C --> D{"Your choice"}
    D -- "Allow analytics" --> E["Remember 'granted'<br/>in your browser"]
    D -- "No thanks" --> F["Remember 'denied'<br/>in your browser"]
    E --> G["Load GoatCounter<br/>and count this visit"]
    F --> H["Load nothing at all"]
    B -- "yes: granted" --> G
    B -- "yes: denied" --> H

    style G fill:#2E5C40,color:#ffffff
    style H fill:#3a3a3a,color:#ffffff
```

The counting tool is **GoatCounter**. It is a deliberately gentle one: it sets
no cookies and does not try to work out who you are. Even so, **nothing is
requested until you say yes.** Not the script, not a single hidden pixel. If
you say no, the browser never contacts GoatCounter at all.

Your answer lives in `localStorage` — a small notebook that belongs to your own
browser, on your own device. It never travels anywhere. And if you change your
mind, the privacy page has a button that rubs out the answer, so the banner
asks you again next time.

---

## 8. Dark mode, menus, and the other moving parts

Small things, but they are the difference between a page that feels finished
and one that does not.

- **Dark-mode switch.** The 🌙/☀️ button in the header flips the whole site
  between light and dark and writes your choice into `localStorage`, so the
  site remembers next time.
- **Mobile menu.** On a narrow phone screen the navigation links collapse
  behind a menu button. Tapping a link closes it, pressing `Escape` closes it,
  and turning your phone sideways to a wide screen closes it too.
- **Scroll reveal.** Sections fade gently upward as they come into view. If
  your device is set to *reduce motion* — a setting some people need, because
  animation can cause dizziness or headaches — everything simply appears
  instantly instead.
- **Active link highlighting.** As you scroll, the header quietly underlines
  whichever section you are currently looking at.
- **Sticky mobile button.** On phones, a "Get candidates, not resumes" bar
  slides up from the bottom once the big top button has scrolled out of sight —
  and politely hides itself again over the contact section, over the footer,
  when the menu is open, and while the cookie banner is showing. It never
  covers up something else you are trying to read.
- **Skip link.** Press `Tab` the moment the page loads and a "Skip to content"
  link appears. Somebody using a keyboard or a screen reader can jump straight
  past the navigation instead of hearing every link read out on every page.
- **The target drawing.** The archery target beside the headline is not a
  picture file — it is drawn with SVG, meaning it is described in code as
  circles and lines. It stays perfectly crisp at any size and weighs almost
  nothing.

---

## 9. How the files fit together

```mermaid
flowchart TD
    subgraph repo["📁 the repository"]
        R["README.md<br/><i>this file</i>"]
        subgraph docs["📁 docs/ — everything the public sees"]
            IDX["index.html"]
            PRV["privacy.html"]
            TRM["terms.html"]
            TY["thank-you.html"]
            E404["404.html"]
            CSS["assets/css/style.css"]
            JS["assets/js/main.js"]
            IMG["assets/img/<br/><i>icons, photo, social preview</i>"]
            MISC["robots.txt · sitemap.xml<br/>site.webmanifest · CNAME"]
        end
    end

    IDX --> CSS
    PRV --> CSS
    TRM --> CSS
    TY  --> CSS
    E404 --> CSS
    IDX --> JS
    PRV --> JS
    TRM --> JS
    TY  --> JS
    E404 --> JS
    IDX --> IMG

    style CSS fill:#2E5C40,color:#ffffff
    style JS fill:#2E5C40,color:#ffffff
```

Notice that **all five pages point at the same two files** for their look and
their behaviour. That is the single most important rule in this project: fix
the menu once in `main.js`, and it is fixed on all five pages. Change a colour
once in `style.css`, and it changes everywhere. There is no copy of the styling
hiding inside any page.

The odd-looking files in the corner do small jobs:

| File | Job |
|---|---|
| `CNAME` | Tells GitHub "this site lives at vfactorsolutions.com", not at a github.io address |
| `robots.txt` | Tells search engines what they may look at, and points them at the sitemap |
| `sitemap.xml` | A list of the three pages worth putting in search results |
| `site.webmanifest` | Lets a phone "install" the site to the home screen with a proper icon |
| `favicon.ico` | The tiny icon in the browser tab |
| `assets/founder.png` | The big master photo. Never sent to visitors — it is only the source the small versions are made from |

**About that photo.** The founder's picture is served in four versions: WebP
and JPEG, each at 216 and 432 pixels wide. The browser looks at the list,
notices what it can handle and how sharp its screen is, and downloads exactly
one of them — a small one on an ordinary phone, a sharper one on a retina
laptop. The multi-megabyte original never leaves the repository.

---

## 10. How the site gets onto the internet

There is no deploy button, no build server, no upload step.

```mermaid
sequenceDiagram
    participant Dev as 🧑‍💻 You
    participant Git as 📦 GitHub repo
    participant Pages as ☁️ GitHub Pages
    participant Visitor as 🌍 A visitor

    Dev->>Git: git push to main
    Note over Git,Pages: Pages is watching the<br/>docs/ folder on main
    Git->>Pages: new files
    Pages-->>Pages: publishes them (about a minute)
    Visitor->>Pages: vfactorsolutions.com
    Pages-->>Visitor: the new version
```

That is the entire pipeline. Push to `main`, wait about a minute, refresh.
The `CNAME` file is what makes the custom domain stick, so **do not delete it** —
if it disappears, the custom domain quietly stops working.

---

## 11. How to run it on your own computer

You cannot simply double-click `index.html`. The pages link to their styling as
`/assets/css/style.css` — that leading slash means "from the root of the
website", and when you open a file directly there is no website root, so
nothing loads and the page looks broken.

Start a tiny local web server instead. From the project folder:

```bash
cd docs
python3 -m http.server 8000
```

Then open <http://localhost:8000> in a browser. Press `Ctrl+C` in the terminal
to stop it.

If you prefer Node:

```bash
npx serve docs
```

Either way there is nothing to install, nothing to compile, and no
`node_modules` folder. What you see locally is what visitors get.

---

## 12. Making changes without breaking anything

A short checklist, worth reading before the first edit.

- **Change styling in `style.css` only.** Never paste CSS back into a page.
- **Change behaviour in `main.js` only.** Same reason.
- **Check both themes.** A colour that looks right in light mode can vanish in
  dark mode. Flip the switch and look.
- **Check a narrow window.** Squash the browser below 860 pixels wide and make
  sure the sticky bottom bar is not covering something important.
- **Never link the big PNG directly.** If you add a photo, make the small WebP
  and JPEG versions the same way the founder photo was done.
- **Keep the email address consistent.** `vijay@vfactorsolutions.com` appears in
  many places across the pages. If it changes, it has to change in all of them —
  the contact section, the footer, the founder card, the legal pages and the
  structured data at the top of `index.html`.
- **If you add a real page, add it to `sitemap.xml`** so search engines find it.
- **Leave the `noindex` on** `thank-you.html` and `404.html`.

There is a second, shorter README at `docs/README.md` written for developers.
This file explains *what the site is*; that one is a quick technical reference.

---

## 13. Things still to fill in before launch

The pages contain `TODO` comments marking places where placeholder text is
standing in for real information. Search the HTML for `TODO` to find them all.
The main ones:

- [ ] **Registered company details** — legal entity name, address and GSTIN, in
      the footer and on both legal pages. An Indian services business with none
      of these on its site looks informal to a client's purchasing team.
- [ ] **Real results instead of years of experience.** "35+ years" is weaker
      proof than "22 roles closed, 5-week median time to fill". Swap the stat
      strip as soon as there are numbers to swap in.
- [ ] **Time commitments on each of the five process stages** — for example
      "first shortlist within 5 working days". A promise you actually keep is
      the strongest trust signal a recruitment site can carry.
- [ ] **Real commercials in the three engagement cards** — the percentage, the
      retainer split, the monthly rate, the replacement guarantee window.
      Visitors decide for themselves from this section; leaving it vague loses
      serious enquiries.
- [ ] **At least two more reviews**, and ideally from *clients* rather than
      colleagues. One lone testimonial can read as "he could only find one
      person willing to say something".
- [ ] **Two case studies.** The markup is already written and commented out in
      `index.html`, waiting for two real engagements to describe. Anonymise the
      client if you must, but keep the numbers honest.
- [ ] **A real data-retention period** in the privacy notice — one you will
      genuinely honour.
- [ ] **A second Formspree form**, so candidate CVs do not land in the same
      inbox thread as public reviews. Both forms currently post to the same
      endpoint.
- [ ] **A lawyer's read of `terms.html`** before relying on it.
- [ ] **The mailbox itself.** `vijay@vfactorsolutions.com` is used across every
      page. It must exist on the domain before the site goes live, or every
      enquiry bounces.

---

## 14. Words you might not know

| Word | What it means |
|---|---|
| **Static site** | A website made of ready-made files. Nothing is calculated when you visit; the files are simply handed over as they are. |
| **HTML** | The words and structure of a page — the skeleton. |
| **CSS** | The colours, spacing and fonts — the clothes. |
| **JavaScript** | The behaviour — menus opening, forms checking themselves. The muscles. |
| **SVG** | A picture described in code as shapes rather than dots, so it stays sharp at any size. |
| **RPO** | Recruitment Process Outsourcing — paying an outside expert to run your hiring. |
| **CTC** | Cost To Company — an Indian term for a salary package including every benefit. |
| **ATS** | Applicant Tracking System — the software a company uses to keep track of job applicants. |
| **JD** | Job Description — the written advert for a role. |
| **Shortlist** | The small group of best candidates picked out of a big pile. |
| **Passive candidate** | Someone good at their job who is not looking to move — and therefore not applying anywhere. Finding them is the hard part of recruiting. |
| **Contingency** | Pay only if it works. |
| **Retainer** | Pay along the way, because the work is committed. |
| **Lead** | A company or person who *might* become a customer. |
| **localStorage** | A small notebook inside your own browser where a site can leave itself a note. It never leaves your device. |
| **Formspree** | An outside service that receives web forms and emails them onward. |
| **GoatCounter** | A privacy-respecting visitor counter — no cookies, no identifying anyone. |
| **noindex** | An instruction asking search engines not to list a page. |
| **Sitemap** | A list of a site's pages, handed to search engines. |
| **Favicon** | The tiny icon on a browser tab. |
| **WebP** | A modern image format — same picture, smaller file. |
| **Honeypot** | A hidden trap field that catches spam robots, because robots fill in everything and people cannot see it. |

---

**Contact:** vijay@vfactorsolutions.com · +91 91504 62580 · Chennai, Tamil Nadu,
India · [LinkedIn](https://www.linkedin.com/in/vijay-purushothaman-9503b810)
