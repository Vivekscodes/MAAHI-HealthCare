# MAAHI HealthCare Management System

A comprehensive healthcare management platform that connects patients, doctors, and hospitals for seamless care coordination. Built with modern web technologies to streamline healthcare operations and improve patient care.

## 🏥 Overview

MAAHI HealthCare is a full-stack web application designed to digitize and streamline healthcare management processes. The platform provides separate interfaces for patients, doctors, and hospitals, enabling efficient appointment booking, medical record management, and healthcare service delivery.

## ✨ Features

### For Patients
- **User Registration & Authentication**: Secure signup and login system
- **Medical Records Access**: View and manage personal health records
- **Appointment Booking**: Schedule appointments with healthcare providers
- **Health Journey Tracking**: Monitor health progress over time
- **AI-Powered Health Assistant**: Get medical information and guidance

### For Doctors
- **Professional Dashboard**: Manage practice and patient interactions
- **Patient Record Management**: Access and update patient medical histories
- **Appointment Scheduling**: Manage appointment calendars
- **OPD Management**: Handle outpatient department operations
- **Secure Authentication**: Role-based access control

### For Hospitals
- **Hospital Management Dashboard**: Comprehensive hospital operations overview
- **Bed Management**: Track bed availability and patient admissions
- **Staff Management**: Manage doctors and healthcare staff
- **Patient Management**: Monitor admitted patients and discharge processes
- **OPD Coordination**: Manage multiple outpatient departments
- **Registry Management**: Hospital registration and compliance tracking

### Core Features
- **Multi-Role Authentication**: Separate login systems for patients, doctors, and hospitals
- **Secure Data Management**: Encrypted medical records and user data
- **Real-time Updates**: Live updates for bed availability and appointments
- **AI Integration**: Google Gemini AI for medical assistance and information
- **Responsive Design**: Mobile-friendly interface using Material-UI
- **File Upload Support**: Medical document and image upload capabilities

## 🛠️ Technology Stack

### Frontend
- **React 19.0.0**: Modern React with latest features
- **Material-UI (MUI)**: Professional UI component library
- **React Router DOM**: Client-side routing
- **Tailwind CSS**: Utility-first CSS framework
- **Vite**: Fast build tool and development server
- **Date-fns**: Date manipulation library

### Backend
- **Node.js**: JavaScript runtime environment
- **Express.js**: Web application framework
- **MongoDB**: NoSQL database for data storage
- **Mongoose**: MongoDB object modeling
- **JWT**: JSON Web Tokens for authentication
- **bcryptjs**: Password hashing and security
- **Multer**: File upload handling
- **CORS**: Cross-origin resource sharing
- **Cookie Parser**: HTTP cookie parsing

### AI Integration
- **Google Generative AI**: Gemini 2.0 Flash model for medical assistance
- **Custom AI Agent**: Specialized medical information assistant

## 📁 Project Structure

```
SRM/
├── Backend/
│   ├── AiAgent/              # AI integration and medical assistant
│   ├── Controllers/          # Request handlers
│   │   ├── User Controllers/
│   │   ├── Doctor Controllers/
│   │   └── Hospital Controllers/
│   ├── Database/             # Database connection configuration
│   ├── Middleware/           # Authentication and validation middleware
│   ├── Models/               # MongoDB data models
│   │   ├── user.model.js
│   ��   ├── doctor.model.js
│   │   ├── hopspital.model.js
│   │   ├── patients.model.js
│   │   ├── medHistory.model.js
│   │   └── opd.model.js
│   ├── Routers/              # API route definitions
│   ├── Util/                 # Utility functions
│   ├── uploads/              # File upload storage
│   └── server.js             # Main server file
├── Frontend/
│   ├── public/               # Static assets
│   ├── src/
│   │   ├── assets/           # Images and static resources
│   │   ├── pages/            # React page components
│   │   │   ├── firstpage.jsx
│   │   │   ├── signuppatient.jsx
│   │   │   ├── signupdoctor.jsx
│   │   │   ├── signuphospital.jsx
│   │   │   ├── LoginPatient.jsx
│   │   │   ├── logindoctor.jsx
│   │   │   ├── loginhospital.jsx
│   │   │   ├── hospitalhomepage.jsx
│   │   │   ├── doctorhomepage.jsx
│   │   │   └── patientdetails.jsx
│   │   └── App.jsx            # Main React component
│   └── package.json
├── .env                      # Environment variables
└── README.md
```

## 🚀 Getting Started

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (local installation or MongoDB Atlas)
- npm or yarn package manager

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd SRM
   ```

2. **Set up environment variables**
   Create a `.env` file in the root directory:
   ```env
   PORT=8000
   MongoDB_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret_key
   ```

3. **Install Backend Dependencies**
   ```bash
   cd Backend
   npm install
   ```

4. **Install Frontend Dependencies**
   ```bash
   cd ../Frontend
   npm install
   ```

### Running the Application

1. **Start the Backend Server**
   ```bash
   cd Backend
   npm run dev
   # or
   npm start
   ```
   The backend server will run on `http://localhost:8000`

2. **Start the Frontend Development Server**
   ```bash
   cd Frontend
   npm run dev
   ```
   The frontend will run on `http://localhost:5173`

3. **Access the Application**
   Open your browser and navigate to `http://localhost:5173`

## 📚 API Endpoints

### Authentication Routes (`/api/auth`)
- `POST /userRegister` - Patient registration
- `POST /userLogin` - Patient login
- `POST /userLogout` - Patient logout
- `POST /doctorRegister` - Doctor registration
- `POST /doctorLogin` - Doctor login
- `POST /doctorLogout` - Doctor logout
- `POST /hospitalRegister` - Hospital registration
- `POST /hospitalLogin` - Hospital login
- `POST /hospitalLogout` - Hospital logout

### User Management (`/api/user`)
- Patient-specific operations and data management

### Doctor Management (`/api/doctor`)
- Doctor-specific operations and patient management

### Hospital Management (`/api/hospital`)
- Hospital operations, bed management, and staff coordination

### Profile Management (`/api/profile`)
- User profile operations and medical record management

## 🔐 Security Features

- **JWT Authentication**: Secure token-based authentication
- **Password Hashing**: bcrypt for secure password storage
- **Role-Based Access Control**: Different access levels for users, doctors, and hospitals
- **CORS Protection**: Configured cross-origin resource sharing
- **Input Validation**: Server-side validation for all inputs
- **Secure File Upload**: Controlled file upload with validation

## 🤖 AI Integration

The platform includes an AI-powered medical assistant using Google's Gemini 2.0 Flash model:
- Provides accurate healthcare information
- Maintains ethical and safe responses
- Offers medical guidance and symptom information
- Ensures professional and unbiased medical advice

## 🎨 User Interface

- **Modern Design**: Clean and professional healthcare-focused UI
- **Responsive Layout**: Works seamlessly on desktop and mobile devices
- **Material Design**: Consistent design language using Material-UI
- **Accessibility**: Built with accessibility best practices
- **Intuitive Navigation**: User-friendly interface for all user types

## 📱 Supported User Roles

1. **Patients**: Personal health management and appointment booking
2. **Doctors**: Practice management and patient care
3. **Hospitals**: Comprehensive healthcare facility management

## 🔧 Development

### Available Scripts

**Backend:**
- `npm start` - Start production server
- `npm run dev` - Start development server with nodemon

**Frontend:**
- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint

### Database Models

- **Users**: Patient information and authentication
- **Doctors**: Healthcare provider profiles and credentials
- **Hospitals**: Healthcare facility information and management
- **Patients**: Hospital admission and bed management
- **Medical History**: Patient medical records and history
- **OPD**: Outpatient department management

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the ISC License.

## 👥 Support

For support and questions, please contact the development team or create an issue in the repository.

## 🚀 Future Enhancements

- Telemedicine integration
- Mobile application development
- Advanced analytics and reporting
- Integration with medical devices
- Multi-language support
- Enhanced AI capabilities

---

<<<<<<< HEAD
**MAAHI HealthCare** - Transforming healthcare management through technology.
=======
**MAAHI HealthCare** - Transforming healthcare management through technology.
>>>>>>> d1188ae (Final project)
