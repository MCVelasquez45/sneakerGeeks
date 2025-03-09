# Week 07: Bootstrap Lesson - Sneaker Blog Project

## Learning Objectives
By the end of this lesson, students will be able to:

- Understand the core concepts of Bootstrap 5.
- Implement a responsive navigation bar, hero section, and card-based layout using Bootstrap.
- Apply the Bootstrap grid system and components to structure a sneaker blog.

---

## Glossary
### **Bootstrap**
A popular front-end framework that helps developers build responsive and mobile-friendly websites quickly.

### **Navbar**
A Bootstrap component used to create responsive navigation menus.

### **Jumbotron**
A large, attention-grabbing section typically used for headers or introductions.

### **Card**
A flexible content container in Bootstrap used to display images, text, and links in an organized manner.

### **Sneaker Deals Section**

A section that highlights current sneaker deals using Bootstrap utilities such as alerts and text formatting for emphasis.

### **Community Discussions Section**

A discussion section using Bootstrap form controls, allowing users to submit and interact through a comment box.

### **Footer Section**

A Bootstrap-styled footer that includes copyright information and can be enhanced with social media links and icons.


---

## Code Walkthrough

### 1️⃣ Setting Up the Bootstrap Navbar
The navbar provides easy navigation throughout the sneaker blog.

```html
<!-- Navbar -->
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container">
        <a class="navbar-brand" href="#">Sneaker Geeks Blog</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav ms-auto">
                <li class="nav-item"><a class="nav-link" href="#reviews">Reviews</a></li>
                <li class="nav-item"><a class="nav-link" href="#deals">Sneaker Deals</a></li>
                <li class="nav-item"><a class="nav-link" href="#community">Community</a></li>
            </ul>
        </div>
    </div>
</nav>
```

#### **Explanation:**
- `navbar-expand-lg` makes the navbar responsive and collapsible on smaller screens.
- `navbar-dark bg-dark` applies a dark-themed background to the navbar.
- `ms-auto` aligns the navigation links to the right.
- The button toggles the menu in mobile view using `data-bs-toggle`.

---

### 2️⃣ Creating a Hero Section (Jumbotron)
The hero section introduces the sneaker blog with a prominent heading and call-to-action button.

```html
<!-- Hero Section -->
<header class="jumbotron text-center text-white d-flex align-items-center justify-content-center">
    <div class="container">
        <div class="bg-dark bg-opacity-75 p-4 rounded d-inline-block">
            <h1 class="fw-bold">Welcome to the Sneaker Geek Blog</h1>
            <p class="lead">The go-to place for sneaker reviews, discussions, and deals.</p>
            <a href="#reviews" class="btn btn-light btn-lg">Explore Reviews</a>
        </div>
    </div>
</header>
```

#### **Explanation:**
- `text-center` centers the text (X-axis alignment).
- `text-white` ensures high contrast for readability.
- `d-flex align-items-center justify-content-center` centers content within the hero section both **vertically (Y-axis)** and **horizontally (X-axis)**.
- `bg-dark bg-opacity-75` provides a semi-transparent background for better readability.

---

### 3️⃣ Implementing Sneaker Review Cards with Bootstrap Grid
This section displays a grid of sneaker reviews using Bootstrap cards.

```html
<!-- Sneaker Reviews Section -->
<div class="container my-5">
    <h2 class="text-center mb-4">Latest Sneaker Reviews</h2>
    <div id="reviews" class="row row-cols-1 row-cols-md-4 g-4">
        <!-- Sneaker Cards -->
        <div class="col">
            <div class="card shadow">
                <img src="/assets/jordan-kicks.jpg" class="card-img-top sneaker-img" alt="Jordan Kicks">
                <div class="card-body">
                    <h5 class="card-title">Jordan Kicks</h5>
                    <p class="card-text">A classic sneaker with premium comfort and style.</p>
                    <button class="btn btn-outline-primary" data-bs-toggle="modal" data-bs-target="#reviewModal">Read Reviews</button>
                </div>
            </div>
        </div>
    </div>
</div>
```

#### **Explanation:**
- `container my-5` ensures spacing around the review section.
- `row row-cols-1 row-cols-md-4 g-4` structures the grid for responsiveness along the **X-axis**.
- `card shadow` applies Bootstrap card styling and adds a shadow effect.
- `btn btn-outline-primary` styles the button for readability and contrast.

---

### 4️⃣ Sneaker Deals Section
This section highlights current sneaker deals available.

```html
<!-- Sneaker Deals Section -->
<div class="container my-5" id="deals">
    <h2 class="text-center">Latest Sneaker Deals</h2>
    <p class="text-center">Find and share the best places to buy your favorite sneakers.</p>
    <div class="alert alert-success text-center">
        New Deal: 20% off Air Jordans at Footlocker! <a href="#">Check it out</a>
    </div>
</div>
```

#### **Explanation:**
- `container my-5` centers and spaces the deals section (Y-axis margin control).
- `alert alert-success` creates a Bootstrap-styled alert box with a success message that spans the **X-axis**.
- The `<a>` tag inside the alert allows users to check out the deal.

---

### 5️⃣ Community Discussions Section
This section allows users to participate in sneaker-related discussions.

```html
<!-- Community Discussions Section -->
<div class="container my-5" id="community">
    <h2 class="text-center">Community Discussions</h2>
    <p class="text-center">Join the conversation and share your sneaker knowledge!</p>
    <textarea class="form-control" rows="3" placeholder="Leave a comment..."></textarea>
    <button class="btn btn-primary mt-2">Post Comment</button>
</div>
```

#### **Explanation:**
- `form-control` ensures the text area spans **horizontally (X-axis)** while remaining responsive.
- `btn btn-primary` ensures a Bootstrap-styled primary button for submitting comments, aligned **along the Y-axis**.

---

### 6️⃣ Footer Section
The footer section includes site-wide copyright information.

```html
<!-- Footer Section -->
<footer class="footer bg-dark text-white text-center py-3">
    <div class="container">
        <p>&copy; 2025 Sneaker Blog. All rights reserved.</p>
    </div>
</footer>
```

#### **Explanation:**
- `bg-dark text-white` creates a dark-themed footer with white text.
- `text-center` centers the footer content **along the X-axis**.
- `py-3` ensures sufficient padding **along the Y-axis** for visual spacing.

---

## 📌 **Check for Understanding Questions**
1️⃣ What Bootstrap class is used to make the navbar collapse on smaller screens?  
2️⃣ How does the Bootstrap grid system help organize the sneaker cards?  
3️⃣ What is the purpose of the `card-img-top` class in the sneaker card component?  
4️⃣ How does `btn btn-outline-primary` differ from `btn-primary`?  
5️⃣ Why do we use `container` and `row` classes when structuring the layout?  

---

## Summary
This lesson introduced key Bootstrap 5 concepts, focusing on:

✅ Building a responsive **navbar**.  
✅ Implementing a **hero section**.  
✅ Creating a responsive grid of **sneaker cards** using Bootstrap components.  
✅ Adding sections for **sneaker deals**, **community discussions**, and **a footer**.  

Students should now be able to **structure a sneaker blog using Bootstrap efficiently**. In the next lesson, we will focus on **adding dynamic functionality using JavaScript and event handling**.  

🚀 **Great job! Keep practicing, and let’s continue building!**

