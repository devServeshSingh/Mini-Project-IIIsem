Smart Campus Resource Hub

A single-page web app that puts a college's everyday information in one place: student records, syllabus, notices, class timetables and library resources.

Built with HTML5 and inline CSS only. No JavaScript, no external stylesheet, no database.

Project details
	
Student	Sarvesh Singh
Course	B.Tech, 2nd Semester (CSE)
College	Ashoka Institute of Technology and Management, Varanasi
University	Dr. A.P.J. Abdul Kalam Technical University, Lucknow
Technologies	HTML5, inline CSS
Features
Six screens in one file: Home, Students, Syllabus, Notices, Time table and Library.
One screen at a time: clicking a menu item slides the app to that screen.
Click to open: every card opens its details on a click.
One card open at a time: opening a new card closes the previous one in the same group.
Responsive: works on laptops and mobile phones.
Colour coded: subjects, notice types and book status each have their own colour.
Screens
Screen	What it shows
Home	Student ID card, campus drawing, today's classes, upcoming dates and quick links
Students	8 student profiles with contact details, mentor, CGPA and attendance bar
Syllabus	3 semesters, 17 subjects with credits, faculty, units and textbook
Notices	3 pinned notices on a cork board, plus 15 notices in 8 types
Time table	5 class timetables with room, class teacher and today's row highlighted
Library	Book shelf, 20 items in 4 categories, timings and library rules
How to run
Download index.html.
Double-click it to open it in a browser (Chrome, Edge, Firefox or Safari).

No installation, server or internet connection is needed. Internet is used only to load the Google Fonts; without it, the page falls back to system fonts.

How it works (without JavaScript)

1. Switching screens

All six screens sit side by side in one container that hides everything outside its width. Menu links point to each screen's id, and CSS scroll snap lines the screen up exactly.

html
<div style="display: flex; overflow: hidden; scroll-snap-type: x mandatory;">
  <div id="home" style="flex: 0 0 100%; scroll-snap-align: start;"> ... </div>
  <div id="library" style="flex: 0 0 100%; scroll-snap-align: start;"> ... </div>
</div>

<a href="#library">Library</a>

2. Click to open details

html
<details>
  <summary>Engineering Mathematics – I</summary>
  <p>Faculty: Dr. R. K. Verma</p>
</details>

3. Only one card open at a time

<details> elements that share the same name act as a group, and only one of them can be open.

html
<details name="notice"> <summary>Semester Examination Notice</summary> ... </details>
<details name="notice"> <summary>Diwali Break</summary> ... </details>

Groups used in the project: student-record, semester, subject, notice, class-timetable, library-category, library-item.

Folder structure
smart-campus-app/
├── index.html    # the complete app (all six screens)
└── README.md     # this file
Browser support

Works in the latest versions of Chrome, Edge, Firefox and Safari. The "one card open at a time" feature needs Chrome/Edge 120+, Firefox 130+ or Safari 17.2+. In older browsers, cards still open and close, but more than one can be open together.

Limitations
All data is hard-coded, so changes must be made in the HTML file.
There is no login, so every user sees the same student on the home screen.
There is no search or filter.
Today's date and the current class are fixed in the code.
Future scope
Database and admin panel to update notices, timetables and books
Student login with personal profile and timetable
Search for books and filters for notices
Automatic current date and class
Online book reservation and notifications
Android app or Progressive Web App (PWA)
Note

All student names, notices, timetables and library data in this project are sample data created for demonstration.

© 2026 Sarvesh Singh, Department of Computer Science and Engineering, AITM Varanasi
