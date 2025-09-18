# Mapty - 🏃‍♀️ Workout Tracker App

An interactive **map-based fitness tracker** built using **vanilla JavaScript** and the **Leaflet.js** mapping library. This app allows users to log their running and cycling workouts by clicking on a map and entering details like distance, duration, and cadence/elevation.

> 🚨 Educational project only. No backend or real-time database.

---

## 📑 Table of Contents

- [Features](#features)
- [Usage](#usage)
- [Technologies Used](#technologies-used)
- [Data Model](#data-model)
- [Local Storage](#local-storage)
- [File Structure](#file-structure)
- [Credits](#credits)
- [License](#license)

---

## 🚀 Features

- 📍 Geolocation-based map rendering (uses browser's GPS)
- 📌 Click on map to log workouts
- 🏃 Running and 🚴 Cycling types supported
- 📊 Calculate pace (min/km) and speed (km/h)
- 💾 Save workouts to `localStorage`
- 🔁 Restore data on page reload
- 📌 Map view pans to selected workout
- 🧹 Reset all workouts via `app.reset()` in console

---

## 🛠 Usage

1. Clone the repository.
2. Open `index.html` in a browser (requires internet for Leaflet tiles).
3. Allow location access in your browser.
4. Click on the map to add a workout.
5. View and interact with workouts in the sidebar.

---

## 🧰 Technologies Used

- **HTML**, **CSS**, **JavaScript**
- **[Leaflet.js](https://leafletjs.com/)** — for interactive maps
- **Geolocation API** — to get user's location
- **localStorage API** — for persistence

---

## 📦 Data Model

```js
{
  id: "unique_id",
  date: "2025-09-18T12:00:00.000Z",
  type: "running" | "cycling",
  coords: [lat, lng],
  distance: Number,   // in km
  duration: Number,   // in minutes
  cadence: Number,    // for running only
  elevationGain: Number, // for cycling only
  pace: Number,       // min/km
  speed: Number,      // km/h
}
```

---

## 💾 Local Storage

Workouts are stored in `localStorage` as JSON:

```js
localStorage.setItem('workouts', JSON.stringify(workoutsArray));
```

To reset all stored workouts:

```js
app.reset();
```

---

## 📁 File Structure

```
/project/
├── index.html
├── style.css
└── script.js  // This file contains all logic and OOP structure
```

---

## 🙌 Credits

This project is inspired by the mapty app built in  
**Jonas Schmedtmann’s [The Complete JavaScript Course](https://www.udemy.com/course/the-complete-javascript-course/)** on Udemy.

> Special thanks to Jonas for teaching advanced JS in such an approachable way.

