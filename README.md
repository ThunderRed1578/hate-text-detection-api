HATE TEXT DETECTION PUBLIC API <br>

This project provides a model that detects toxic comments on social media platforms, specifically designed for the English language.

📌 Setup <br>
This model is based on the work of JensBender to detect hate speech and offensive comments in English. I have reimplemented this model as a server API, which can detect toxic comments posted in real-time on social media.<br>
This is his github repository model : [hate-speech-detection](https://github.com/JensBender/hate-speech-detection)

The server is hosted using Ngrok for a static domain and is accessible for testing.

🔧 Requirements
Before using this project, please ensure the following:

Python 3.8

Required Python libraries listed in requirements.txt

Ngrok for hosting the server

🛠️ Installation and Setup
Clone the Repository

```bash
git clone https://github.com/ThunderRed1578/hate-text-detection-api.git
cd hate-text-detection-api-main
```
Install Dependencies Install all required libraries using requirements.txt:

```bash
pip install -r requirements.txt
```
Install Ngrok

If you're using Windows, you can install Ngrok via Chocolatey with the following command:

```bash
choco install ngrok
```
For other operating systems, follow the instructions on the official Ngrok website.

Set Up Ngrok Authtoken

Run the following command to add your Ngrok authentication token:

```bash
ngrok authtoken <your-auth-token>
```
Run the Ngrok Server
Use Ngrok to host the server on port 80. Replace the URL with your own if you want a custom domain:

```bash
ngrok http 80
```
This will expose the server and make it accessible through a public URL like https://crab-enjoyed-buck.ngrok-free.app.

Run the Application

Open and run app.py:

```bash
python app.py
```
This will start the model and process comments in real-time.

🔍 API Usage
The API will return the following classifications:

'1': Neutral

'-1': Negative

⚡ Example of Using the API:<br>
You can send POST requests to the hosted server with a comment. The model will return one of the above labels indicating whether the comment is neutral, or negative.

💡 Notes: <br>
Ensure your Ngrok tunnel remains active to keep the server running.

This model specifically handles Vietnamese-language comments and is built for detecting hate speech and offensive content.