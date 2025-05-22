
# 📚 **Bookmates** – Share. Discover. Connect.

**Bookmates** is an interactive web platform for book lovers to **share**, **browse**, and **connect** over their favorite reads. Developed with **HTML, CSS, PHP, and MySQL**, it supports user authentication, book uploads, and now includes **search and filter** capabilities to make book discovery even easier.

> ✅ Developed locally with **XAMPP**
> 🌐 Hosted online via **InfinityFree**

---

## 🚀 Features

* 📖 **Browse Books** – Discover titles shared by users, with new search and filter functionality!
* 🔍 **Search & Filter** – Find books by title, author, or genre quickly.
* ➕ **Upload Books** – Share your favorite reads via a user-friendly upload form.
* 🔐 **User Login & Signup** – Secure account system with PHP session management (in progress).
* 🏠 **Home Page** – Introduction and quick navigation.
* ℹ️ **About Page** – Learn the mission behind Bookmates.
* 📞 **Contact Page** – Send questions or suggestions through a form.
* 💬 **Live Chat (Planned)** – Chat feature to enhance community interaction.

---

## 🧰 Tech Stack

| Layer         | Technology/Tools                                   |
| ------------- | -------------------------------------------------- |
| **Frontend**  | HTML, CSS, JavaScript                              |
| **Styling**   | `index.css`, `about.css`, `browse-books.css`, etc. |
| **Backend**   | PHP (`displaybooks.php`, `search.php`)             |
| **Database**  | MySQL via phpMyAdmin                               |
| **Hosting**   | InfinityFree                                       |
| **Local Dev** | XAMPP (Apache + MySQL)                             |

---

## 🗃️ Project Structure

```bash
/bookmates/
├── index.html                # Homepage
├── login.html                # Login form
├── signup.html               # Signup form
├── post-a-book.html          # Upload form
├── displaybooks.php          # Display uploaded books
├── search.php                # Search/filter logic (NEW)
├── about.html
├── contact.html
├── chat.html                 # Chat (optional)
├── /js/                      # JavaScript files
├── /styles/                  # CSS files
├── .htaccess
└── /assets/                  # Images, icons, etc.
```

---

## 🔍 Enhanced: Browse Books with Search & Filter

A new **dynamic search bar and dropdown filters** have been added to `browse-books.html` with a supporting `search.php` backend file.

### Features:

* Search by **Title** or **Author**
* Filter by **Genre**
* Real-time result display using AJAX

### Sample UI (HTML Snippet in `browse-books.html`)

```html
<input type="text" id="searchInput" placeholder="Search by title or author...">
<select id="genreFilter">
  <option value="">All Genres</option>
  <option value="Fiction">Fiction</option>
  <option value="Non-fiction">Non-fiction</option>
  <option value="Sci-Fi">Sci-Fi</option>
</select>
<div id="resultsContainer"></div>
```

### JavaScript Snippet (in `/js/browse.js`)

```javascript
document.getElementById('searchInput').addEventListener('keyup', fetchResults);
document.getElementById('genreFilter').addEventListener('change', fetchResults);

function fetchResults() {
  const query = document.getElementById('searchInput').value;
  const genre = document.getElementById('genreFilter').value;

  fetch(`search.php?query=${query}&genre=${genre}`)
    .then(response => response.text())
    .then(data => document.getElementById('resultsContainer').innerHTML = data);
}
```

---

## 🛠️ Setup Instructions

### ✅ Requirements

* XAMPP (Apache + MySQL)
* Web browser (Chrome, Firefox, etc.)

### 📥 Installation (Local)

1. **Install XAMPP**
   Download from [apachefriends.org](https://www.apachefriends.org)

2. **Move Files**
   Copy `bookmates/` to `C:/xampp/htdocs/`

3. **Start Services**
   Launch Apache and MySQL from XAMPP Control Panel

4. **Setup Database**

   * Open [phpMyAdmin](http://localhost/phpmyadmin)
   * Create database: `bookmates_db`
   * Import SQL file (provided in the repo)

5. **Run in Browser**
   Navigate to: [http://localhost/bookmates](http://localhost/bookmates)

---

## ☁️ Online Hosting

**InfinityFree** hosts the live version of Bookmates.

* 🌐 Live URL: [http://bookmates.ct.ws](http://bookmates.ct.ws)
* 🛠 PHP + MySQL hosting
* 🧰 phpMyAdmin for DB access

---

## 📌 Planned Features

* 🔐 User sessions + Logout support
* 🖼️ Upload book cover images
* 📱 Fully responsive mobile layout
* 💬 Real-time chat/discussion threads
* 📚 Advanced genre-based book filters

---

## 👨‍💻 Created By

**The Bookmates Team**
An academic project aimed at promoting reading and community sharing.

---

## 📄 License

This project is free for **educational** and **non-commercial** use.
Feel free to **contribute**, **adapt**, or **share**.

