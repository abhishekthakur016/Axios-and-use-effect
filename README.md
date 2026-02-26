JSONPlaceholder Users Fetch App
📌 Project Overview

This project demonstrates how to fetch and display user data from the JSONPlaceholder API using React Hooks and Axios.

The application fetches user data when the component mounts and dynamically renders user cards using a reusable User component.

🚀 Technologies Used

React (Functional Components)

useState Hook

useEffect Hook

Axios

JSONPlaceholder API

🔄 How It Works

When the App component mounts, useEffect runs.

Inside useEffect, the getData() function is triggered.

Axios sends a GET request to:

https://jsonplaceholder.typicode.com/users

The response data is stored in state using useState.

React re-renders automatically when the state updates.

The data is mapped and passed as props to the User component.

Each user is rendered dynamically inside a card layout.

📂 Code Structure
src/
 ├── App.js
 └── components/
      └── User.js
🧠 Key Concepts Demonstrated
useState

Used to store fetched API data.

const [allData, setAllData] = useState([])
useEffect

Used to perform side effects (API call on component mount).

useEffect(() => {
  getData()
}, [])
Axios

Used for making HTTP GET requests.

const response = await axios.get(
  'https://jsonplaceholder.typicode.com/users'
)
Dynamic Rendering with map()
{allData.map((elem, idx) => (
  <User key={idx} elem={elem} />
))}
🎯 Features

Fetches real-time API data

Uses modern React Hooks

Component-based architecture

Clean and reusable code structure

🛠 Installation
npm install
npm start
📈 Future Improvements

Add loading state

Add error handling

Add search/filter functionality

Improve UI styling

Replace index key with unique ID