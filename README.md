# Portfolio
Web portfolio that i use on [jwliusri.dev](https://www.jwliusri.dev/) using vue.js
utilizing Firebase as the backend and CMS(Firebase Console) so i don't need to re-deploy, or create a CMS to make a quick update

## Firebase Structure
- Firebase Hosting (serve HTML Vue.js)
- Firestore (store projects data)
- Cloud Storage (store image)

## Data Structure in Firestore
- info (collection)
  - profile (document)
    - greetingTitle (string)
    - greetingText (string)
    - picture (string)
    - social (array)
      - href (string)
      - icon (string: fontAwesome css code)
      - color (string)
- projects (collection)
  - (documents: projectID)
    - title (string)
    - content (string)
    - tags (array of string)
    - type (string: main/gallery)
    - index (int: sort desc)
    - images(if type main) / image (if type gallery)
    
## How to Use
Deploy this source code into firebase hosting, the firebase SDK configuration is setup using [firebase reserved URLs](https://firebase.google.com/docs/hosting/reserved-urls#sdk_auto-configuration). Then create the data in firestore following the structure mentioned above.
