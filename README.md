# Lovey Bal Niketan School Website
## ✅ FIXED VERSION - Separate Header & Footer

## 🎯 What Was Fixed
- ✅ CSS class naming conflicts resolved (changed `.dropdown` to `.nav-dropdown`)
- ✅ Header and footer separated into individual files
- ✅ Automatic include system with `include.js`
- ✅ All navigation dropdown menus working properly
- ✅ Easy to add new pages - just copy the template!

## 📁 File Structure

### Core Files (Required for all pages)
```
website/
├── header.html          ← Navigation menu (used on ALL pages)
├── footer.html          ← Footer content (used on ALL pages)
├── styles.css           ← All styling
├── script.js            ← Main functionality
└── include.js           ← Loads header & footer automatically
```

### Pages
```
├── index.html                 (Homepage)
├── about-school.html         (About section)
├── director.html
├── principles.html
├── curricular.html           (Academics section)
├── achievements.html
├── board-results.html
├── admission-process.html    (Admission section)
├── book-list.html
├── uniform.html
├── fee-structure.html
├── facilities.html
├── contact.html
```

## 🚀 How It Works

### Header & Footer Auto-Loading
Every page has these two lines:
```html
<!-- Header will be loaded here -->
<div id="header-placeholder"></div>

... page content ...

<!-- Footer will be loaded here -->
<div id="footer-placeholder"></div>
```

The `include.js` file automatically:
1. Loads `header.html` into the header placeholder
2. Loads `footer.html` into the footer placeholder
3. Sets the active page in navigation
4. Initializes all dropdown menus

### Adding a New Page - SUPER EASY!

**Just 5 steps:**
1. Copy any page (e.g., `about-school.html`)
2. Rename it (e.g., `new-page.html`)
3. Change the `<title>` tag
4. Change page header title/subtitle
5. Add your content - Done!

Header and footer load automatically! No need to copy/paste navigation code.

## 📝 Editing Header & Footer

### To Update Navigation
Edit `header.html` - changes apply to ALL pages automatically!

**Add a new menu item:**
```html
<li><a href="new-page.html" class="nav-link">New Page</a></li>
```

**Add a new dropdown:**
```html
<li class="nav-dropdown">
    <a href="#" class="nav-link dropdown-toggle">Menu Name <span class="arrow">▾</span></a>
    <ul class="dropdown-menu">
        <li><a href="page1.html">Sub Page 1</a></li>
        <li><a href="page2.html">Sub Page 2</a></li>
    </ul>
</li>
```

### To Update Footer
Edit `footer.html` - changes apply to ALL pages automatically!

## 🎨 Customization

### Change Logo
In `header.html`, replace:
```html
<div class="logo-placeholder">
    <span class="logo-text">LBN</span>
</div>
```
With:
```html
<img src="your-logo.png" alt="LBN Logo" style="width: 60px; height: 60px;">
```

### Change Colors
Edit `styles.css` variables (top of file):
```css
:root {
    --primary-purple: #5E35B1;
    --accent-gold: #FFB300;
}
```

### Add Images
Replace placeholder divs with:
```html
<img src="your-image.jpg" alt="Description">
```

## ⚙️ Navigation Features

### Desktop
- Hover over "About", "Academics", or "Admission" to see dropdowns
- Smooth animations
- Active page highlighted

### Mobile
- Click hamburger menu
- Click dropdown items to expand
- Fully touch-optimized

## 📱 Testing Locally

**⚠️ IMPORTANT:** Must use a web server (not direct file opening)

### Option 1: Python
```bash
python -m http.server 8000
# Visit: http://localhost:8000
```

### Option 2: Node.js
```bash
npx http-server
```

### Option 3: VS Code
Install "Live Server" extension → Click "Go Live"

## 🌐 Deployment

Upload ALL files to your web hosting - that's it!

Required files:
- All `.html` files
- `styles.css`
- `script.js`
- `include.js`
- Your images

## 🆘 Troubleshooting

**Header/Footer not showing?**
→ Use a web server, not direct file opening

**Dropdowns not working?**
→ Clear browser cache, check console (F12)

**Mobile menu stuck?**
→ Refresh page, verify all JS files loaded

---

**Created for Lovey Bal Niketan School**
✅ Fixed navigation system  
✅ Separate header/footer for easy updates  
✅ Production-ready and fully responsive
