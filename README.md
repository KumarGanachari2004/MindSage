# MindSage
MindSage is a real-time AI-powered mental health tracker that uses facial, voice, and text analysis to provide personalized emotional support while ensuring privacy, accessibility, and proactive care.
1. Chat Interface:
The heart of the platform is an intuitive, AI-driven chat interface that facilitates empathetic conversations. The AI responds to users' mental health-related inquiries in a compassionate, understanding manner, offering guidance, suggestions, and emotional support. Whether someone feels overwhelmed or needs someone to "talk" to, the chat interface is designed to feel like a personal companion. The chat can also recommend therapists on request. Another feature of the chat interface is its ability to recommend websites likes when asked and not only does it do that, but it presents it in a user-friendly interface design. Key Features:

Speech-to-Text and Text-to-Speech: Users can interact using voice input and receive audio responses, enhancing accessibility and providing a more natural conversation experience.

Multi-Source Web Search Integration: The AI utilizes Tavily, Bing, Google, and YouTube searches to recommend therapists, articles, videos, and other resources upon request, presented in a user-friendly interface.

Personalized Recommendations: It offers tailored suggestions for well-being routines, mindfulness practices, and stress-relief techniques based on user input and mood.

Location-Based Assistance: The AI can help users find nearby mental health professionals or wellness centers when asked.

Use Case Diagram:
Use Case Diagram

2. Well-being Routines:
Earlent encourages users to maintain daily or weekly routines focused on mental and emotional health. These routines might include mindfulness practices, meditation activities, or stress relief techniques, tailored to individual needs and preferences. This feature makes use of YouTube and Google API to pull resources and display them based on the users' inputted search data

3. Mood Logger:
Users can record and store their daily moods, functioning as a digital journal to help track emotional states over time. When a chat session is finalized, the AI analyzes the user's mood based on the conversation and provides immediate insights. This helps users reflect on their emotions and better understand their mental health. While the app currently offers mood analysis at the end of chats, future updates may include more extensive AI-driven analysis and trend identification based on users' logged data.

4. Schedule Check-in:

Earlent enables users to schedule periodic check-ins to reflect on their mental state and stay on track with managing their mental health. After scheduling a check-in, users will receive timely notifications to remind them of their upcoming sessions. Specifically, the app sends notifications:

1 month before the scheduled check-in
1 day before the scheduled check-in
1 hour before the scheduled check-in
These reminders ensure users are consistently engaged and receive supportive nudges to prioritize their mental well-being. The notifications are delivered using pywebpush, allowing for reliable and timely push notifications directly to the user's device.

5. Anonymous Login:

Earlent offers an anonymous login option for users who prefer not to create an account or disclose personal information. This feature allows users to access the chat interface and other functionalities without providing identifiable data, ensuring privacy and encouraging more individuals to seek support without hesitation. Anonymous users can benefit from the AI-driven chat interface and receive guidance while maintaining complete anonymity.

6. Forgot Password Feature:

Earlent provides a secure "Forgot Password" feature. Users who have forgotten their passwords can enter their registered email addresses to receive a tokenized link. This link allows them to create a new password securely, ensuring they regain access to their accounts without compromising security.

7. Data Management:

Users have control over their data with the ability to download or delete all or selected portions of their chat history with the AI. This can be done periodically or as needed, giving users the flexibility to manage their personal information according to their preferences.

8. Account Deletion:

For users who wish to discontinue using the service, Earlent offers an option to delete their accounts completely. This process ensures that all personal data, including chat histories and user profiles, are permanently removed from the system, respecting user privacy and data protection preferences.

In Summary:

Earlent - The Mental Health Companion is an innovative and AI-powered platform designed to provide personalized and empathetic mental health support. By offering features like a responsive chat interface, customizable well-being routines, mood logging with AI analysis, scheduled check-ins with reminders, anonymous login options, secure password recovery, comprehensive data management, and the option to delete accounts, Earlent empowers users to take control of their mental health in a convenient, supportive, and accessible way.

How we built it
Database: Azure Cosmos DB (v-core) for its robust, scalable database services to manage dynamic data requirements efficiently.

LLM: The Azure OpenAI platform was integrated for generating empathetic, context-aware responses through advanced AI models like GPT 4o mini.

AI Services: Azure Speech Services enable users to interact with the platform using their voice, improving accessibility and user experience. Speech-to-text allowed users to input requests through speech, while text-to-speech provided responses audibly using window.speechSynthesis.

Frontend: React was chosen for its efficiency in building interactive user interfaces, with Vite used to optimize the development experience and MUI (Material-UI) to design a modern, user-friendly interface.

Backend: Flask was chosen to manage backend operations, including API routing and middleware functionalities, due to its lightweight and unopinionated structure.

Agentic Framework: LangChain was integrated to enhance the AI's functionality, enabling the AI to keep track of conversation history and use tools for web search, vector search and map services.

APIs and Services: We utilized several external APIs to enrich the AI's capabilities:

Google Web Search API: For retrieving relevant search results from Google.
Bing Search API: To fetch search results from Bing, providing diverse information sources.
YouTube Search API: For accessing video content relevant to the user's queries.
Google Places API: To help users find nearby mental health professionals or wellness centers.
Tavily API: To access specialized or niche information that may not be readily available through mainstream search engines.
AI Vector Search with FAISS: We integrated FAISS (Facebook AI Similarity Search) for efficient similarity search and clustering of dense vectors, enhancing the AI's ability to retrieve relevant information quickly.

Services & Libraries: pywebpush allowed for real-time communication with users through web push notifications, facilitated by user subscriptions managed through the Subscription model. Flask-Mail was used to manage email communications within the app.

CI/CD Docker was used to containerize the application, ensuring consistency across different computing environments. Github Actions was used to optimize the deployment process by wiring it directly to Render's web services.

Export the Application
Clone the repo
https://github.com/dhrumilp12/Mental-Health-Companion.git
Configure environment variables:
Copy the .env.example file to a new file named .env.
Update the .env file with your specific configurations.
cp .env.example .env
Setup the frontend environment with NPM
cd ./client
npm install
npm run dev
Run the backend:
cd ./server
pip install -r requirements.txt
python app.py
Build the frontend:
npm run build
Build the backend with Docker
cd ./server
docker build --pull --rm -t mental-health-app:latest .
Execute the frontend:
npm run preview
Install FFmpeg and Add FFmpeg to System PATH
Download and Extract FFmpeg Properly
Download FFmpeg Again:

Go to the FFmpeg download page.
Click on the link for Windows builds provided by Gyan or BtbN (these are popular and reliable sources). This will redirect you to their respective pages where you can download the build.
Choose a static build (which includes all necessary files in a single package) and download the zip file.
Extract the FFmpeg Zip File:

Once downloaded, right-click on the zip file and choose 'Extract All...' or use any preferred extraction tool like 7-Zip or WinRAR.
Choose a location where you want to extract the files. You can extract them directly to C:\FFmpeg to keep things organized.
Verify the Contents:

Navigate to the folder where you extracted the files.
You should see a bin folder inside this directory. Inside bin, there will be at least three files: ffmpeg.exe, ffplay.exe, and ffprobe.exe.
Add FFmpeg to System PATH
If you've successfully located the bin folder now:

Edit the PATH Environment Variable:

Press Windows key + R, type sysdm.cpl, and press Enter.
Go to the 'Advanced' tab and click on 'Environment Variables'.
Under 'System Variables', scroll down to find the 'Path' variable and click on 'Edit'.
Click 'New' and add the full path to the bin folder, e.g., C:\FFmpeg\bin.
Click 'OK' to save your changes and close all remaining windows by clicking 'OK'.
Verify FFmpeg Installation:

Open a new command prompt or PowerShell window (make sure to open it after updating the PATH).
Type ffmpeg -version and press Enter. This command should now return the version of FFmpeg, confirming it's installed correctly and recognized by the system.
