# kitovu-general-hardware-1
Repository/Deployed link:https://github.com/pandastuart73-jpg/kitovu-general-hardware-website
Accessibility Audit Report — Kitovu General Hardware Website
I reviewed the Kitovu General Hardware website and found the following five accessibility issues:
1. Contact form labels are not connected to their input boxes
Who it affects: People using screen readers
The problem: The contact form (First Name, Last Name, Phone, Email, Subject, Message) has visible labels like "First Name," but in the code these labels aren't actually linked to their input boxes id connection. A screen reader can't tell the user which label belongs to which box, so filling out the form becomes confusing or impossible without sight.
How to fix it: Add a matching id to each input and a for attribute on its label (e.g., <label for="firstName">First Name</label> and <input id="firstName">), so screen readers correctly announce each field.
2. Icon-only buttons and links have no text description
Who it affects: People using screen readers
The problem: The mobile menu button (the hamburger icon in the top navigation) and the social media icons in the footer  WhatsApp are just icons with no text attached. A screen reader either skips it or reads nothing meaningful, so the user doesn't know what the button does or which social network the link goes to.
How to fix it: Add an aria-label to each one, like aria-label="Open menu" on the menu button and aria-label="Visit us on whatsup " on the whatsup icon.
3. Body text color doesn't have enough contrast
Who it affects: People with low vision or color blindness
The problem: Much of the descriptive text on the site (under headings, in product cards, testimonials) uses a grey color (#7f8c8d) on a white background. This only gives a contrast ratio of about 3.9:1, which is below the 4.5:1 minimum needed for normal-sized text to be easily readable.
How to fix it: Darken the grey text color for example to something like #5f6a6a or darker so it meets the 4.5:1 contrast requirement.
4. No "skip to main content" link
Who it affects: People who navigate using only a keyboard, or screen reader users
The problem: The page has a fairly long navigation menu (Home, About, Products, Videos, Services, Contact) at the top. Since there's no skip link, someone using a keyboard has to tab through every single navigation item before reaching the actual page content every time the page loads.
How to fix it: Add a hidden "Skip to main content" link at the very top of the page that becomes visible when focused, letting keyboard users jump straight past the navigation.
5. Embedded videos have no captions or transcript
Who it affects: People who are deaf or hard of hearing
The problem: The two product demonstration videos ("Latest Construction Tools 2026" and "Basic Construction Power Tools Guide") are embedded but there's no caption option or written transcript provided alongside them, so anyone who can't hear the audio misses the spoken information.
How to fix it: Add captions to the videos, or provide a short written transcript/summary of the video content next to each one
