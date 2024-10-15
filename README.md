# MoodWellnessApp

**MoodWellnessApp** is a personalized, mood-based wellness app designed to help users manage their emotional well-being. By selecting a mood, users receive tailored activity recommendations and reminders. The app is powered by a React Native frontend and an Appwrite backend for secure data storage and real-time functionality.

## Features
- **Mood-Based Activity Suggestions**: Activities are recommended based on the user’s selected mood, such as "Read" for burnout, "Meditate" for anxiety, and more.
- **Customizable Moods and Reminders**: Users can create their own moods and set reminder preferences for personalized notifications.
- **Regular Mood Check-Ins**: Every two hours, the app prompts users to log their current mood, helping to track changes and tailor activity recommendations.
- **Offline Functionality**: Select activities that can be completed offline, like journaling or listening to a pre-downloaded meditation.
- **Activity Tracking and History**: Logs of completed activities and mood check-ins are stored securely, allowing users to track their progress and review their wellness trends over time.
- **Real-Time Notifications**: Receive push notifications tailored to mood preferences with Appwrite and Firebase Cloud Messaging.

## Tech Stack
- **Frontend**: React Native
- **Backend**: Appwrite for user authentication, data storage, and real-time capabilities
- **Push Notifications**: Firebase Cloud Messaging (FCM)
- **Offline Capabilities**: Local storage and offline data sync

## Getting Started
### Prerequisites
1. Node.js and npm installed on your local machine.
2. An Appwrite server (self-hosted or cloud) with a project setup.
3. Firebase account for FCM (for push notifications).
4. React Native development environment.

### Installation
1. **Clone the repository**:
   ```bash
   git clone https://github.com/YourUsername/MoodWellnessApp.git
   cd MoodWellnessApp
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Configure Appwrite**:
   - Go to the [Appwrite console](https://appwrite.io/) and set up a new project.
   - Add a new database and create collections for `Users`, `Moods`, and `ActivityLogs`.
   - Enable authentication providers, such as email/password and OAuth.

4. **Set Up Firebase for Push Notifications**:
   - Follow the [Firebase setup guide](https://firebase.google.com/docs/android/setup) to register your app with FCM.
   - Copy your Firebase configuration file (`google-services.json` for Android or `GoogleService-Info.plist` for iOS) into your project.

5. **Configure Environment Variables**:
   - Create an `.env` file and include your Appwrite and Firebase credentials:
     ```plaintext
     APPWRITE_ENDPOINT=https://[YOUR_APPWRITE_ENDPOINT]
     APPWRITE_PROJECT_ID=[YOUR_PROJECT_ID]
     FIREBASE_API_KEY=[YOUR_FIREBASE_API_KEY]
     ```

6. **Run the App**:
   ```bash
   npx react-native run-android // or run-ios
   ```

## Usage
1. **Sign Up / Login**: Users can register or sign in using email/password or OAuth.
2. **Mood Selection**: Choose a predefined mood or create a new one with a custom activity.
3. **Set Reminder Preferences**: Define the frequency and timing for reminders based on the selected mood.
4. **Regular Mood Check-Ins**: The app will prompt you every two hours to log your current mood, supporting better tracking and personalized activity recommendations.
5. **Receive Notifications**: Notifications are sent as reminders for selected activities, even when offline.
6. **Track Activities and Mood History**: Review past activities and mood trends in the app’s history section.

## Offline Functionality
The app includes several offline activities. These are saved locally and synced with Appwrite when the app is back online. Offline activities include:
- **Journaling**: Users can write in a mood journal, which will sync to the server later.
- **Meditation**: The app provides audio-guided meditation tracks that can be pre-downloaded and accessed offline.
- **Breathing Exercises**: Guided breathing sessions that work without an internet connection.

## Contribution Guidelines
We welcome contributions from the community! Please follow these steps to contribute:
1. **Fork the Repository**: Click the “Fork” button at the top right of this page.
2. **Clone Your Forked Repository**:
   ```bash
   git clone https://github.com/YourUsername/MoodWellnessApp.git
   cd MoodWellnessApp
   ```
3. **Create a New Branch**:
   ```bash
   git checkout -b feature/YourFeatureName
   ```
4. **Make Your Changes**:
   - Add extra activities, improve offline capabilities, or suggest new features.
   - Ensure your code follows the existing style and structure of the project.
5. **Commit and Push**:
   ```bash
   git commit -m "Add feature: YourFeatureName"
   git push origin feature/YourFeatureName
   ```
6. **Submit a Pull Request**: Go to the original repository, and click “New Pull Request.”

### Development Guidelines
- **Code Style**: Please follow [Airbnb’s JavaScript style guide](https://github.com/airbnb/javascript).
- **Testing**: Include tests for any new features, and ensure all existing tests pass.
- **Documentation**: Update the README or any relevant documentation files for your changes.

## Roadmap
- **Integration with Health Apps**: Sync with other wellness apps or platforms.
- **Expanded Offline Activities**: Add more offline features like downloadable workout videos or mindfulness games.
- **Internationalization (i18n)**: Make the app available in multiple languages.

## License
This project is open-source and available under the [MIT License](LICENSE).

## Acknowledgments
Thanks to all contributors and the open-source community for making this project possible!