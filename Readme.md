# ImAble: A Communication & Safety App for Children with Autism

**ImAble** ("I'm Able") is an Android app that helps **non-verbal or minimally verbal children with Autism Spectrum Disorder (ASD)** express their needs. It also gives their **parents** tools to follow their child's day, keep them safe, and find support in Bangladesh.

<!-- Add 3–4 screenshots here: home screen, parent mode, emergency map, organisations page -->
Check here: https://drive.google.com/file/d/1It6PnDvzTbUx0S7z8a81xDLG4rafyYsg/view?usp=sharing
---

## The problem

Many children with autism find it hard to say what they need or feel, which can lead to frustration and missed signs of distress. Parents also worry about their child's safety when they are not together, and often don't know where to find trusted information and local organisations.

## Features

### For the child: tap-to-talk communication board
- Large picture buttons for everyday needs and feelings: *Help me, Hungry, Want to eat, Drink water, Toilet, Sleep, Want to play, Wash hands, Where's mom?, Happy, Sad, Angry, Scared, Sick, Cold, Don't touch me, Okay, No, Sorry, Thank you* and more
- Each tap **plays a recorded voice**, so the child can "speak" by pressing a picture
- **Custom buttons** ("Interact in your own way"): parents can upload the child's own photos with captions to make personal communication cards
- **Emergency button**: sends the child's **live GPS location by SMS** to the parent's registered phone number and shows it on a map

### For parents: Parent Mode
- **Activity history**: every button the child presses is saved with date and time, so parents can see what their child needed and when
- **Automatic location updates**: a background service texts the child's location to the parent at a set interval, and parents can switch it on or off
- **Anonymous Positivity**: a space to upload and share happy stories and photos
- **Learn more about your child**: curated must-read articles for parents and links to online autism screening tests
- **Organizations working for ASD**: quick links to Bangladeshi support organisations (e.g., CNAC, SWAC, ACWFB, SUCHONA Foundation, NCSE, JPUF, Dhaka Shishu Hospital Neurology Department)

### Accounts
- Email and password sign-up with email verification (Firebase Authentication)
- Each family's data is stored separately in the cloud

## Tech stack

| Area | Technology |
|---|---|
| Platform | Android (Java), min SDK 16 |
| Auth | Firebase Authentication |
| Database | Cloud Firestore, Firebase Realtime Database |
| Media | Firebase Storage, Picasso |
| Location & maps | Google Maps SDK, Fused Location Provider, Geocoder |
| Messaging | Android SmsManager |
| UI | Material Components, RecyclerView, CardView, Navigation Drawer |

## Running the project

1. Open the project in **Android Studio**.
2. Create a Firebase project, enable Email/Password auth, Firestore and Storage, and replace `app/google-services.json` with your own.
3. Add your own Google Maps API key in `google_maps_api.xml`.
4. Run on a device (SMS and GPS features need a real phone).

## Design notes

- Big, colourful picture buttons with sound, because many autistic children respond better to visual and audio cues than to text
- The parent features sit behind a separate mode, so the child's screen stays simple

