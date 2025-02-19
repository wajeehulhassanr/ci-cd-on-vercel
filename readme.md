To deploy a Flask app using Vercel, you can follow these steps:

1. First, make sure you have installed the Vercel CLI tool. You can install it using npm by running the following command:
$ npm install -g vercel
2. Next, Navigate to directory for your Flask app using the command line. then Add the required dependencies to the `requirements.txt` file:

$ pip freeze > requirements.txt
3. Create a new file called `vercel.json` in the root directory of your app. This file will contain the configuration information for Vercel.

4. Add the following JSON code to the vercel.json file:

{
  "version": 2,
  "builds": [
    { "src": "app.py", "use": "@vercel/python" }
  ],
  "routes": [
    { "src": "/(.*)", "dest": "/app.py" }
  ]
}
5. In the above code, replace app.py with the name of your Flask app file.

6. Finally, deploy your app to Vercel by running the following command:

$ vercel deploy