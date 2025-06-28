# Chrome-_extension
codtech it solutions
># COMPANY NAME : CODTECH IT SOLUTIONS PVT.LTD
># INTERN NAME  : KOTYADA JAHNAVI
># INTERN ID    : CT04DF2117
># DOMAIN       : FULL STACK WEB DEVELOPMENT
># DURATION     : 4 WEEKS
># MENTOR       : NEELA SANTHOSH


### OVERVIEW :



### 1. Project Structure


chrome-productivity-tracker/
│
├── extension/          # Chrome Extension
│   ├── manifest.json
│   ├── background.js
│   ├── popup.html, .js, .css
│
├── backend/            # Node.js backend
│   ├── server.js
│   ├── models/Log.js
│   └── routes/logRoutes.js
│
├── dashboard/          # Analytics Dashboard (HTML + Chart.js)
│   ├── index.html
│   └── dashboard.js


### 2. Setup Backend Server

####  Requirements:

* [Node.js](https://nodejs.org/)
* [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) account (or local MongoDB)

####  Install Dependencies

bash
cd backend
npm install


####  Configure MongoDB Connection

Replace the MongoDB URI in `server.js` with your own connection string:


mongoose.connect('your_mongo_uri', { useNewUrlParser: true, useUnifiedTopology: true });


####  Start the Server

```bash
node server.js
```

The backend will run at: `http://localhost:5000`

---

### 3. Load the Chrome Extension

1. Open Google Chrome and go to: `chrome://extensions/`
2. Enable **Developer Mode**
3. Click **Load unpacked**
4. Select the `extension/` folder

✅ The extension will start tracking your tab activity automatically.

---

###  4. Open Analytics Dashboard

Go to the `dashboard/` folder and open `index.html` in your browser.

> The dashboard fetches time logs from the backend and shows productivity graphs (e.g., pie charts, bar charts).

---

###  5. Customize Productive/Unproductive Sites

You can edit the classification logic (hardcoded for now) inside the extension’s `background.js` or in the backend's aggregation logic.

Example:

```js
const productiveSites = ["leetcode.com", "github.com", "w3schools.com"];




###  6. Deployment (Optional)

* Use [Render](https://render.com/) or [Railway](https://railway.app/) to deploy the backend.
* Use [MongoDB Atlas](https://www.mongodb.com/atlas/database) for cloud DB storage.
* Package the dashboard in a React app or host as a static HTML page.



### 7. Summary

| Component | Description                               |
| --------- | ----------------------------------------- |
| Extension | Tracks time spent on sites via Chrome API |
| Backend   | Stores log data, processes stats          |
| Dashboard | Visualizes reports & productivity         |
| Database  | MongoDB stores timestamped logs           |

# OUTPUT:
![Image](https://github.com/user-attachments/assets/c14b6662-76ac-4365-9131-4ab295703471)

![Image](https://github.com/user-attachments/assets/c6aee904-c5cd-4077-8072-4e0d44efce7f)

![Image](https://github.com/user-attachments/assets/44bbf71d-b347-4ad3-86d6-eb7f0f6979a2)
