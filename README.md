# Summary 
Full-stack Android nutrition app built in Kotlin with Jetpack Compose UI, MVVM architecture, Room database for local persistence, Retrofit REST integration (FruityVice API), and Google Gemini AI for personalised coaching. Features multi-user auth, HEIFA food quality scoring, and a clinician analytics dashboard.

<img width="610" height="650" alt="image" src="https://github.com/user-attachments/assets/14e6c657-d9be-4123-a5a3-fd47d04b045b" />

## Features 

- Authentication & account claiming — pre-registered users claim their account on first visit by verifying their user ID and phone number, then set a password. Credentials are stored in the app's Room database, with session persistence so users stay logged in.
  
- Food intake questionnaire — food category selection, dietary persona, and daily meal timings.
Food quality scoring (Insights) — HEIFA-based score breakdown across categories (vegetables, fruits, grains, whole grains, meat & alternatives, dairy, water, fats, sodium, sugar, alcohol, discretionary foods) with a total score out of 100, seeded from CSV data into Room. An "Improve my diet!" button routes straight to NutriCoach.

- NutriCoach — Fruit details retrieval: fetches live nutritional data (family, calories, fat, sugar, carbs, protein) from the FruityVice API
  
- AI motivational messages: generates encouraging diet tips via Google Gemini; every generated tip is persisted to a dedicated database table and viewable in a "Show All Tips" dialog
  
- Clinician dashboard — access-key-protected section (via Settings) showing average HEIFA scores by sex, plus AI-powered data analysis that sends the dataset to Gemini and returns three key data patterns as structured insights.
  
- Settings — account details (name, phone, ID), logout, and clinician login entry point.

## Tech stack 
<img width="258" height="164" alt="image" src="https://github.com/user-attachments/assets/ef09cfca-e451-45ca-99d5-9ecda9d4f49c" />

## Getting started

- Clone the repo and open it in Android Studio.
  
- Create/edit local.properties in the project root and add your Gemini API key (get one at Google AI Studio):
properties apiKey=YOUR_GEMINI_API_KEY

- The build reads apiKey from local.properties into BuildConfig, so the key is never committed to source control.

- Sync Gradle and run on an emulator or device (min SDK 35).

## Project structure
<img width="503" height="209" alt="image" src="https://github.com/user-attachments/assets/0ac8a4a9-37e8-45d6-927d-355f66467fd6" />

