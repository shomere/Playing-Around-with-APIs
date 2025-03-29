# Playing-Around-with-APIs

# Mental Health Support Assistant

## Overview
This web application is designed to help individuals assess their mental health by diagnosing potential mental disorders. Users can interact with the chatbot by either typing their feelings or using the voice recorder to express their emotions. The recorded speech is converted into text, which is then analyzed to identify possible mental health conditions. Based on the analysis, the system provides:
- A diagnosis of the mental disorder.
- Personalized tips to manage the condition.
- Recommendations for the nearest professional therapists.

## Features
1. **Reliable Mental Health Diagnosis** – Uses AI-powered analysis to provide mental health insights.
2. **Responsive Design** – Works seamlessly on both mobile devices and computers.

## Running the Application
The web app can run in two ways:

### Running Locally
1. Clone the repository:
   ```sh
   git clone https://github.com/Playing-Around-with-APIs/mental-health-support.git
   ```
2. Navigate to the project directory:
   ```sh
   cd mental-health-support
   ```
3. Open `index.html` in your preferred web browser.

### Running on Web Servers
1. Deploy the application to a hosting service (e.g., GitHub Pages, Vercel, Netlify, Digital Ocean).
2. Ensure API keys are properly configured in an environment variable or backend proxy.

## Technologies Used
The frontend and backend logic are integrated into a single project using:
- **HTML** – Structure of the web pages.
- **CSS** – Styling and responsiveness.
- **JavaScript** – Interactivity and API calls.
- **APIs** – External services for mental health analysis.

## APIs Used
The application relies on two external APIs:

### 1. **Mental Health Diagnosis API**
- **Endpoint:** `https://i-m-all-ears.p.rapidapi.com/?id=`
- **Purpose:** Generates mental health assessments based on user input.
- **Key Details:**
  - Host: `i-m-all-ears.p.rapidapi.com`
  - Requires RapidAPI key authentication.
  - Currently using mock implementation (replace with actual API details in production).

### 2. **AI Life Coach API**
- **Endpoint:** `https://ai-life-coach-api-personal-development-online-coaching.p.rapidapi.com/getLifeAdvice?noqueue=1`
- **Purpose:** Provides personalized recommendations for mental well-being and personal development.
- **Key Details:**
  - Host: `ai-life-coach-api-personal-development-online-coaching.p.rapidapi.com`
  - Requires RapidAPI key authentication.
  - Accepts `POST` requests with JSON payload containing:
    - User profile (age, current situation).
    - Goals and challenges.
    - Timeframe and focus areas (mental health, personal development, health).

## Implementation Notes
- **Mock Responses:** Placeholder responses are used since the exact API details may not be available.
- **Authentication:** Requires a RapidAPI key (`x-rapidapi-key`), which should be stored securely.
- **Fallback Mechanism:** Includes backup data in case API calls fail, ensuring continuous operation.
- **Expected API Responses:**
  - Mental health concerns.
  - Mood assessment.
  - Recommended articles and exercises.
  - Therapist recommendations.
  - Action plans (daily, weekly, monthly guidance).

## Security & Best Practices
- **Never expose API keys in client-side code** – Use backend services to manage keys securely.
- **Ensure user privacy** – Do not store sensitive mental health data without proper encryption and security protocols.
- **Consider alternative APIs** – Some potential replacements include:
  - **Wysa** – AI-powered mental health chatbot.
  - **Woebot** – Digital mental health companion.
  - **BetterHelp API** – Online therapy services.

## Challenges & Solutions
### Challenge: API Rate Limits Causing Failed Requests
**Solution:** Implemented client-side caching with `localStorage`.

### Challenge: Mobile Responsiveness Issues
**Solution:** Used Bootstrap’s grid system for better flexible layouts.

### Challenge: CORS Errors When Fetching APIs
**Solution:** Configured backend CORS policies or used a proxy server.

## Credits & Acknowledgments
Special thanks to:
- **Kamarul Adha** – Developer of **I'm All Ears API**.
- **Bilgisam LTD** – Developer of **AI Life Coach API**.
- The **RapidAPI** team for providing free API tiers that enabled this project.

---
This README provides a structured guide for users and developers to understand, run, and contribute to the project effectively. 

