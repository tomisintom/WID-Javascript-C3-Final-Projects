# WID Learn

An online learning platform frontend. You can browse courses, enroll, watch lessons, take quizzes, and track your progress from a dashboard.

This is a frontend-only project. There's no backend. Everything (login, enrollments, progress, quiz scores) is saved in the browser's localStorage.
<br>

## AIM

The aim of this project is:

- To build a fully responsive frontend for an online learning platform (LMS)
- To practice React awhile using tailwind css for styling

## FEATURES

The features of the platform include:

- Home page with hero, categories, and popular courses
- Course catalog with search, filters, and sorting
- Course detail page with curriculum and enroll option
- Lesson player with video, sidebar, and progress tracking
- Quiz system with scoring and results page
- Student dashboard with stats and course progress
- Login/signup and profile page
- Fully responsive navbar and footer with mobile menu
  <br>

## BUILT WITH

- React 19
- Vite
- Tailwind CSS v4
- React Router v7
- React Icons
  <br>

## Project Structure

```
wid-learn/
└─ project_files/
   ├─ public/
   │  └─ favicon.svg
   ├─ src/
   │  ├─ assets/
   │  │  ├─ images/
   │  │  │  ├─ hero-img-7.png
   │  │  │  └─ wid-learn-logo.png
   │  │  └─ desktop-design1.png
   │  ├─ components/
   │  │  ├─ Breadcrumbs.jsx
   │  │  ├─ Button.jsx
   │  │  ├─ CourseCard.jsx
   │  │  ├─ Footer.jsx
   │  │  ├─ Layout.jsx
   │  │  ├─ Logo.jsx
   │  │  ├─ Navbar.jsx
   │  │  ├─ ProgressBar.jsx
   │  │  ├─ ProgressRing.jsx
   │  │  ├─ ProtectedRoute.jsx
   │  │  ├─ RatingStars.jsx
   │  │  └─ StatCard.jsx
   │  ├─ context/
   │  │  ├─ AuthContext.jsx
   │  │  └─ LearningContext.jsx
   │  ├─ data/
   │  │  └─ courses.js
   │  ├─ pages/
   │  │  ├─ CourseDetail.jsx
   │  │  ├─ Courses.jsx
   │  │  ├─ Dashboard.jsx
   │  │  ├─ Home.jsx
   │  │  ├─ LessonPlayer.jsx
   │  │  ├─ Login.jsx
   │  │  ├─ NotFound.jsx
   │  │  ├─ Profile.jsx
   │  │  ├─ Quiz.jsx
   │  │  ├─ QuizResult.jsx
   │  │  └─ Signup.jsx
   │  ├─ App.jsx
   │  ├─ index.css
   │  └─ main.jsx
   ├─ .gitignore
   ├─ index.html
   ├─ package.json
   ├─ package-lock.json
   ├─ README.md
   └─ vite.config.js
```
<br>

## Challenges

Navbar dropdown not responding to clicks
The profile dropdown menu (Dashboard/Profile/Log out) in the navbar looked fine but clicking on any of its options did nothing. The dropdown was being closed by an onBlur event on the toggle button combined with a setTimeout delay, meant to give clicks inside the menu time to register before closing it. In practice, the blur fired and closed the menu right before the click on the link/button underneath could register, so the click was effectively swallowed. Traced the issue back to that onBlur + setTimeout logic, removed it, and replaced it with a click-outside listener attached to the document — the menu now only closes when you click somewhere outside it, so clicks on Dashboard, Profile, and Log out always go through.

Choosing and using React Icons consistently
React Icons bundles several icon sets (Feather, Font Awesome, Material Design, etc.) under one package, and it wasn't immediately obvious which set to standardize on. Mixing icon styles across the navbar, buttons, and cards made the UI look inconsistent early on. Settled on the Feather icon set (react-icons/fi) for a clean, minimal look, and made sure every component that needed an icon imported from the same set instead of picking whichever looked closest at the time.

Structuring the project folders
Deciding how to split the codebase into components, pages, context, and data wasn't obvious at first — some UI pieces (like the navbar and cards) could arguably be pages or components, and state logic (auth, learning progress) needed a clear home separate from the UI. Went through a couple of reworks before settling on: components/ for reusable UI, pages/ for route-level views, context/ for global state (Auth, Learning), and data/ for mock data — a structure that scales cleanly as more routes and features get added.
<br>

## HOW TO ACCESS THE PLATFORM

To Access the Platform, [Click Here](https://wid-learn.vercel.app/)
<br>

## Learning Curve

Learnt a lot of concepts building this project. Such as:

- React Router v7 for nested/dynamic routes
- Tailwind CSS v4's new Vite-plugin-based setup
- Structuring a React project into components, pages, context, and data
- React Hooks
- User Authentication
- Working with icon libraries (React Icons)
  <br>

## Image/Video Demo
<img src="project_files/src/assets/images/desktop-design1.png" alt="WID Learn Desktop Design" width="600">
<!-- ![WID Learn Desktop Design](project_files/src/assets/images/desktop-design1.png) -->

## Project Members

- Oluwatosin
- Oluwatomisin Tomoloju
