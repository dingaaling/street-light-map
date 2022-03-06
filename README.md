# Street Lighting Map

Based on Citi Map: Urban Data Collection & Mapping Tool - https://github.com/dingaaling/citi-map

## Requirements

- Node V16.0.0 or higher 
- Yarn V1.17.3 or higer 

## Basic Usage

1. Clone of fork the repo template. 
2. Switch to the branch that corresponds with the number of items you plan to log (`trash_map_1object` - 1 item, `sound_map` - 2 items, `main` - 3 items, `light_map` - 4 items)
3. Run `yarn install` to download the required packages
4. Upload your images to the `src/images/` folder. Name them in a format like `icon1.png`, `icon2.png`, etc. starting your numbering from 1 and up to 4. Note: for best results, use square sized images (e.g. 80 x 80)
5. Run `yarn start` to launch the app
6. Click each image to raise to log an instance of that category. This should increment the count below that object and display its location on the map.
7. Click the `Download CSV` button to download your session data.

## Hosting the App on Firebase

The app may be hosted on any platform of your choice. Here is an example of how to host the app and database using Firebase.

1. Run `yarn add firebase` to install firebase
2. Follow [these instructions](https://firebase.google.com/docs/cli#install-cli-mac-linux) to install firebase cli tools
3. Create the project on the Firebase console following Step 1 in this [documentation](https://firebase.google.com/docs/web/setup#create-firebase-project-and-app).
4. Go to the Project Settings page in your Firebase console and select the `</>` option to add a web app
<img width="250" alt="Screen Shot 2022-03-06 at 8 10 29 PM" src="https://user-images.githubusercontent.com/5104098/156940765-a4869b01-ab1e-4810-8760-1afbfdb6c5eb.png">
5. Follow the instructions to add Firebase to your web app
<img width="250" alt="Screen Shot 2022-03-06 at 8 10 04 PM" src="https://user-images.githubusercontent.com/5104098/156940778-824cbdde-f2e2-4a9b-b04f-f943539a1235.png">

- Note: make sure to use `yarn` instead of `npm` for installation

6. Run `yarn add firebase` on the command line
7. Set up firebase command line tools following this [documentation] (https://firebase.google.com/docs/cli#install-cli-mac-linux) to connect your app with Firebase.
8.  Select the `Database` and `Hosting options for Firebase CLI features

- Select `Use an existing project` and connect to the project you created in step 1.
- Add Real-time Database using us-central1
- Use `build` as your public directory
- Yes, configure as a single-page app

9. Copy the config information provided on the Project settings page (just what's inside the const firebaseConfig brackes) into `src/config.js`
10. Run `yarn build` to compile the project and prepare for deployment
11. Run `firebase deploy` to deploy the app
12. Go to the Realtime Database page and select Create Database to start logging data.
