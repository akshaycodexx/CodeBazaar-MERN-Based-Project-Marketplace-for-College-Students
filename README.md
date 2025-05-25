# CodeBazaar – MERN-Based Project Marketplace for College Students

CodeBazaar is a full-stack MERN web application designed for Indian college students to **upload, showcase, and sell coding projects**. It also supports hackathon hosting, paid setup video tutorials, affiliate earnings, verified badges, and recruiter access for hiring.

## 🚀 Features

- Student project uploads with GitHub & live demo links
- Paid/Free setup video tutorials with revenue sharing
- Hackathon creation, project submission & voting system
- Recruiter panel for hiring and project shortlisting
- Affiliate referral system for passive income
- Premium memberships and verified badges
- In-app notifications and real-time updates
- Admin panel for full platform control

## 🎯 Schemas Models


### 👤 User Model – Manages All Platform Users

- 🎯 Purpose:

Stores basic user information like name, email, password, profile, role (student, recruiter, admin), premium status, skills, earnings, referral info, and more.

## 💡 Functionality:

- When a user signs up, their data is stored here.

- Handles different user roles: student (uploads projects), recruiter (hires), and admin (manages platform).

- Tracks premium membership, total downloads, referral code, and earnings.


---


### 🧑‍💻 Project Model – Handles Uploaded Coding Projects

- 🎯 Purpose:

Stores details of all coding projects uploaded by students, including title, description, technologies used, GitHub/demo links, paid/free status, price, views/downloads, and creator info.

## 💡Functionality:

- When a user uploads a project, it’s saved here.

- Connects to the User model to show who uploaded it.

- Includes pricing and video URL if the project is paid.

- Tracks project performance with views/downloads.
  

---


### 🧑‍💻 Transaction Model – Tracks Purchases and Payments

- 🎯 Purpose:

Logs all financial transactions such as project downloads, video purchases, and premium membership payments.

## 💡Functionality:

- Every time a user pays for something, a transaction entry is created.

- Contains the transaction type (download, video, membership) and status (success, failed).

- Links the transaction to both user and project.


---


### 🏆Hackathon Model – Stores Hackathon Details

- 🎯 Purpose:

Keeps data related to hackathons hosted on the platform: title, description, dates, host, participants, and submitted projects.

## 💡 Functionality:

- Admins or recruiters can host hackathons.

- Students can participate, and submitted projects are tracked.

- Hackathons can be filtered by active/inactive.


---


### 🌟 Submission Model – Manages Project Submissions to Hackathons

- 🎯 Purpose:

Links submitted projects to their respective hackathons, showing which user submitted what project.

## 💡 Functionality:

- Every submission is tied to a user, hackathon, and project.

- Used to calculate votes and display leaderboards.



---


### 💰 Affiliate Model – Supports Referral Earnings System

- 🎯 Purpose:

Manages affiliate program where users can earn by referring others using unique codes.

## 💡 Functionality:

- Every user can have an affiliate code.

- Tracks how many users they referred and total referral earnings.

- Helpful for marketing and platform growth.


---

### 🌟 Rating Model – Stores Project Ratings and Reviews

- 🎯 Purpose:

Allows users to rate and review projects they’ve purchased or downloaded.

## 💡 Functionality:

- Saves the user’s rating (1–5 stars) and optional written review.

- Connects to both User and Project.

- Helps display average rating on project listings.



---


### 🌟 Badge Model – Handles Special Badges (e.g., Verified, Top Contributor)

- 🎯 Purpose:

Stores and manages badges awarded to users based on achievements or admin decisions.

## 💡Functionality:

- Admins can award badges to users.

- Badges are shown on user profiles for credibility.

- Badges have icons, names, and descriptions.



---


### 🧭 Notification Model – In-App Notifications for Users

- 🎯 Purpose:

Stores messages sent to users, such as hackathon updates, new badges, payment confirmations, etc.

## 💡 Functionality:

- Sends messages to users when certain events happen.

- isRead flag is used to manage unread/read states.

- Shown on user dashboards for real-time updates.



---


### 🛡️ Admin Model – Super Admin Control

- 🎯 Purpose:

Stores admin credentials to manage the platform backend securely.

## 💡Functionality:

- Admins can log in and access a special dashboard.

- They can approve projects, manage users, assign badges, and more.

- Separate from regular users for higher security.



---

## **🎨 ER-Diagram **

ER-Diagram

![ER-Diagram](./img/ERDiagram.png)

# 🚀 Model Relationships Summary

### 🌟 Model	Related To	Purpose of Relationship

User	Projects, Transactions, Ratings, Affiliates	Who created what, who paid what, who referred who
Project	User, Transactions, Ratings	Who uploaded, who paid, who rated
Transaction	User, Project	Who paid for what
Hackathon	User, Project (via Submission)	Who hosted/joined/submitted what
Submission	User, Hackathon, Project	Track who submitted what and when
Affiliate	User	Who referred whom
Rating	User, Project	Who reviewed what
Badge	User	Who owns what badge
Notification	User	Who received what alert
Admin	Independent	Platform control



---


## 🛠️ Tech Stack

| Layer        | Technologies                             |
|--------------|------------------------------------------|
| Frontend     | React.js, TailwindCSS, Redux Toolkit     |
| Backend      | Node.js, Express.js, MongoDB             |
| Auth         | JWT, Google OAuth                        |
| Real-Time    | Socket.io                                |
| File Upload  | Cloudinary                               |
| Notifications| Firebase                                 |
| Payments     | Stripe API / Paytm SDK                   |
| DevOps       | Git, GitHub, Postman, Render/Vercel      |

---

## 📸 Screenshots

![Landing Page](https://your-image-url.com)
![Dashboard](https://your-image-url.com)
![Project Upload](https://your-image-url.com)

---
🧠 Why This Project Stands Out
✅ Real-world use case: Monetization + Mentorship + Hackathons
✅ Covers full-stack depth: REST APIs, JWT, OAuth, Websockets, Payments
✅ Highly scalable & startup-worthy architecture
✅ Perfect for resumes, internships, or open-source contribution

🙌 Contributing
Pull requests are welcome! If you'd like to collaborate, reach out via GitHub or drop an email.

📄 License
MIT License © 2025 Your Name

🔗 Connect With Me
LinkedIn: Akshay Kumar Mandal

GitHub: @akshaycodexx


