# Final_Evalution
Project Submission Link:
https://docs.google.com/spreadsheets/d/1Osa-OrIv0MRbPVfzT7AUSDGdhWDSIdyR5AXXV5ctXDk/edit?usp=sharing



AssignMent Submission Link:
https://docs.google.com/spreadsheets/d/1y3r3tBHxI03YFnRKn8o466GItJUHp_WxKIZW5rmgrZk/edit?gid=0#gid=0



reference for design


Frontend degign:


| **Route**    | **Purpose**                     | **Logic**                                                                                                 | **Packages Used**                                                                 |
| ------------ | ------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `/register`  | Registration page               | - Show a form to collect name, email, and password.<br>- On submit → send POST request to backend API.    | `react-router-dom`, `axios`,  |
| `/login`     | Login page                      | - Show a form for email & password.<br>- On submit → POST to backend API.<br>- Save JWT token in storage. | `react-router-dom`, `axios`, `                                  |
| `/dashboard` | Protected user dashboard        | - Check if user token exists.<br>- If yes, fetch user data.<br>- If no, redirect to `/login`.             | `react-router-dom`, `axios`,                             |
| `/forgot`    | Forgot password page (optional) | - Collect email.<br>- Send POST request to trigger password reset flow.                                   | `axios`, `react-router-dom`                                                       |
| `/`          | Landing or Home page            | - Public page anyone can see.                                                                             | `react-router-dom`                                                                |




Backend Design:

| **Route**       	 | **Purpose**                          | **Logic**                                                                                               | **Packages Used**                                 |
| ---------------	 | ------------------------------------ | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------- |
| `/api/auth/register`   | Register a new user                  | - Check if email already exists.<br>- Hash password.<br>- Save user to DB.<br>- Return success message. | `express`, `bcryptjs`, `mongoose`, `jsonwebtoken` |
| `/api/auth/login`    	 | Authenticate user                    | - Check if user exists.<br>- Compare hashed password.<br>- Return JWT token if valid.                   | `express`, `bcryptjs`, `mongoose`, `jsonwebtoken` |
| `/api/profile` 	 | Get user profile (protected route)   | - Verify JWT token.<br>- Fetch user data from DB.<br>- Return user info.                                | `express`, `jsonwebtoken`, `mongoose`             |     |
| `/api/forgot`   	 | Send reset password email (optional) | - Verify email exists.<br>- Generate reset token.<br>- Send email with reset link.                      | `express`, `nodemailer`, `crypto`                 |











