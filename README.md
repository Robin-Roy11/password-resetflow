password reset flow README
====================    
This project implements a password reset flow using React for the frontend and Node.js with Express for the backend. It allows users to request a password reset link via email and reset their password securely.
## Features
- User can request a password reset link by entering their email.
- A reset link is sent to the user's email if it exists in the database.
- User can reset their password using the link.
- Passwords are hashed before storing in the database.  
## Technologies Used
- Frontend: React, Axios
- Backend: Node.js, Express, Mongoose
- Database: MongoDB
- Email: Nodemailer
- Authentication: JWT, bcrypt
## Setup Instructions
### Backend
1. Navigate to the `password-reset-backend` directory.
2. Install dependencies:
   ```bash
   npm install
   ```
3. Create a `.env` file with the following variables:
   ```plaintext
   PORT=4000
   MONGO_URI=your_mongodb_uri
   JWT_SECRET=your_jwt_secret
+   EMAIL_USER=your_email_user
+   EMAIL_PASS=your_email_password
   ```          
4. Start the server:
   ```bash
   npm start
   ```
### Frontend
1. Navigate to the `password-reset-client` directory.
2. Install dependencies:
   ```bash
   npm install
   ```
3. Create a `.env` file with the following variable:
   ```plaintext
   VITE_API_URL=http://localhost:4000
   ```
4. Start the development server:
   ```bash
   npm run dev
   ```
## Usage
1. Open the frontend in your browser (usually at `http://localhost:5173`).
2. Navigate to the "Forgot Password" page.
3. Enter your email and submit to receive a password reset link.
4. Click the link in the email to navigate to the reset password page.
5. Enter your new password and submit to reset it.
## Notes
- Ensure your MongoDB instance is running and accessible.
- The email functionality requires a valid email service configuration in the backend `.env` file.
- The frontend and backend should be running simultaneously for the flow to work.
- The reset link is valid for 15 minutes; after that, you will need to request a new link.
- The password must be at least 6 characters long.
## Troubleshooting      
- If you encounter CORS issues, ensure your backend allows requests from the frontend origin.
- Check the console for any errors in both frontend and backend.
- Ensure the email service is correctly configured and the credentials are valid.
- If the reset link does not work, check the token validity and ensure it has not expired.
## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.
## Acknowledgements
- Thanks to the open-source community for the libraries and tools used in this project.
- Special thanks to the contributors who helped improve this project.
