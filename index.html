<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CoolKidZ</title>
  <style>
    /* General Styles */
    body {
      font-family: Arial, sans-serif;
      background-image: url('https://images.unsplash.com/photo-1579783902614-a3fb3927b6a5?w=900&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8M3x8YXJ0fGVufDB8fDB8fHww');
      background-color: #f4f4f4;
      margin: 0;
      padding: 0;
    }
    .header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      width: 100%;
      padding: 10px 20px;
      background: rgba(255, 255, 255, 0.7);
    }
    .header h1 {
      font-size: 28px;
      color: green;
      cursor: pointer;
      text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.2);
    }
    .buttons button {
      background-color: green;
      color: white;
      border: none;
      padding: 10px 15px;
      margin: 0 5px;
      border-radius: 5px;
      font-size: 16px;
      cursor: pointer;
      transition: background-color 0.3s;
    }
    .buttons button:hover {
      background-color: darkgreen;
    }
    .form-box {
      background: white;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
      margin-top: 20px;
      width: 350px;
      text-align: center;
    }
    .form-box h2 {
      margin-bottom: 15px;
      color: green;
      font-size: 22px;
    }
    .form-box input {
      width: 100%;
      padding: 10px;
      margin-bottom: 15px;
      border: 1px solid #ccc;
      border-radius: 5px;
      font-size: 14px;
    }
    .form-box button {
      background-color: green;
      color: white;
      border: none;
      padding: 10px 15px;
      border-radius: 5px;
      font-size: 16px;
      cursor: pointer;
      transition: background-color 0.3s;
    }
    .form-box button:hover {
      background-color: darkgreen;
    }
    .media-container {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
      margin-top: 20px;
      width: 100%;
      max-width: 1200px;
    }
    .media-entry {
      display: flex;
      flex-direction: column;
      align-items: center;
      border: 1px solid #ccc;
      border-radius: 5px;
      overflow: hidden;
      background-color: white;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
      position: relative;
    }
    video, img {
      width: 100%;
      max-height: 200px;
      object-fit: cover;
    }
    .media-title {
      background-color: green;
      color: white;
      padding: 10px;
      text-align: center;
      font-size: 14px;
    }
    .media-uploader {
      color: green;
      background-color: black;
      padding: 5px;
      text-align: center;
      font-size: 12px;
    }
    .delete-button {
      position: absolute;
      top: 10px;
      right: 10px;
      background-color: red;
      color: white;
      border: none;
      border-radius: 50%;
      padding: 10px;
      cursor: pointer;
      font-size: 18px;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .delete-button:hover {
      background-color: darkred;
    }
    .hidden {
      display: none;
    }
  </style>
</head>
<body>
  <div class="header">
    <h1 id="coolkidZHeading" onclick="refreshPage()">CoolKidZ</h1>
    <div class="buttons">
      <button id="signUpButton" onclick="showSignUp()">Sign Up</button>
      <button id="signInButton" onclick="showSignIn()">Sign In</button>
      <button id="logOutButton" class="hidden" onclick="logOut()">Log Out</button>
      <button id="addMediaButton" class="hidden" onclick="addMedia()">Add Media</button>
    </div>
  </div>

  <div class="container">
    <div id="welcomeMessage" class="welcome-message hidden"></div>
    
    <div id="loginForm" class="form-box hidden">
      <h2>Log In</h2>
      <input type="text" id="usernameInput" placeholder="Enter username" />
      <input type="password" id="passwordInput" placeholder="Enter password" />
      <button onclick="logIn()">Log In</button>
    </div>

    <div id="signUpForm" class="form-box hidden">
      <h2>Sign Up</h2>
      <input type="text" id="newUsernameInput" placeholder="Choose a username" />
      <input type="password" id="newPasswordInput" placeholder="Choose a password" />
      <button onclick="signUp()">Sign Up</button>
    </div>

    <div id="mediaContainer" class="media-container"></div>
  </div>

  <script>
   // Function to save media (video/image) to localStorage
function saveMediaToStorage(mediaData) {
  const media = JSON.parse(localStorage.getItem('media')) || [];
  media.push(mediaData);
  localStorage.setItem('media', JSON.stringify(media));
}

// Function to load media (video/image) from localStorage
function loadMedia() {
  const media = JSON.parse(localStorage.getItem('media')) || [];
  const currentUser = localStorage.getItem('currentUser');

  media.forEach((mediaData) => {
    renderMedia(mediaData, currentUser);
  });
}

// Function to render media (video/image) and the delete button
function renderMedia(mediaData, currentUser) {
  // Check if the media contains the expected properties
  if (!mediaData || !mediaData.src || !mediaData.title || !mediaData.uploader) {
    console.error('Invalid media data:', mediaData);
    return;
  }

  const mediaContainer = document.createElement('div');
  mediaContainer.className = 'media-entry';

  const mediaElement = document.createElement(mediaData.type === 'video' ? 'video' : 'img');
  mediaElement.src = mediaData.src;
  if (mediaData.type === 'video') {
    mediaElement.controls = true;
  }

  const titleBox = document.createElement('div');
  titleBox.className = 'media-title';
  titleBox.innerText = mediaData.title;

  const uploaderBox = document.createElement('div');
  uploaderBox.className = 'media-uploader';
  uploaderBox.innerText = Uploaded by ${mediaData.uploader};

  // Add delete button only if the current user is the uploader
  const deleteButton = document.createElement('button');
  deleteButton.className = 'delete-button';
  deleteButton.innerHTML = '🗑️'; // Trash icon
  deleteButton.onclick = function () {
    if (currentUser && mediaData.uploader === currentUser) {
      deleteMedia(mediaData);
    } else {
      alert('You must be logged in to delete your media!');
    }
  };

  mediaContainer.appendChild(mediaElement);
  mediaContainer.appendChild(titleBox);
  mediaContainer.appendChild(uploaderBox);
  if (currentUser && mediaData.uploader === currentUser) {
    mediaContainer.appendChild(deleteButton); // Show delete button only for the uploader
  }

  document.getElementById('mediaContainer').appendChild(mediaContainer);
}

// Function to delete media
function deleteMedia(mediaData) {
  let media = JSON.parse(localStorage.getItem('media')) || [];
  media = media.filter((item) => item.src !== mediaData.src);
  localStorage.setItem('media', JSON.stringify(media));

  // Reload media on the page to reflect the changes
  document.getElementById('mediaContainer').innerHTML = '';
  loadMedia();

  alert('Media deleted successfully!');
}

// Function to handle adding a video or image
function addMedia() {
  const mediaFile = document.createElement('input');
  mediaFile.type = 'file';
  mediaFile.accept = 'image/*, video/*'; // Allow both images and videos

  mediaFile.onchange = function () {
    const file = mediaFile.files[0];
    if (!file) {
      alert('Please select a media file!');
      return;
    }

    const reader = new FileReader();
    reader.onload = function (e) {
      const mediaTitle = prompt('Enter the title for your media:');
      if (!mediaTitle) {
        alert('Media title cannot be empty!');
        return;
      }

      const currentUser = localStorage.getItem('currentUser') || 'Unknown User';

      const mediaData = {
        src: e.target.result,
        title: mediaTitle,
        uploader: currentUser,
        type: file.type.startsWith('video') ? 'video' : 'image',
      };

      saveMediaToStorage(mediaData);
      renderMedia(mediaData, currentUser);
    };
    reader.readAsDataURL(file);
  };

  mediaFile.click();
}

// Function to handle Sign Up
function signUp() {
  const username = document.getElementById('newUsernameInput').value.trim();
  const password = document.getElementById('newPasswordInput').value.trim();

  if (!username || !password) {
    alert('Please fill in both username and password!');
    return;
  }

  const users = JSON.parse(localStorage.getItem('users')) || {};
  if (users[username]) {
    alert('Username already exists. Please choose another one.');
    return;
  }

  users[username] = password;
  localStorage.setItem('users', JSON.stringify(users));

  alert('Sign Up successful! You can now log in.');
  document.getElementById('newUsernameInput').value = '';
  document.getElementById('newPasswordInput').value = '';
  showSignIn();
}

// Function to handle Log In
function logIn() {
  const username = document.getElementById('usernameInput').value.trim();
  const password = document.getElementById('passwordInput').value.trim();

  if (!username || !password) {
    alert('Please fill in both username and password!');
    return;
  }

  const users = JSON.parse(localStorage.getItem('users')) || {};

  if (users[username] && users[username] === password) {
    alert(Welcome back, ${username}!);
    document.getElementById('welcomeMessage').innerText = Hello, ${username}!;
    document.getElementById('welcomeMessage').classList.remove('hidden');
    document.getElementById('loginForm').classList.add('hidden');
    document.getElementById('signUpForm').classList.add('hidden');
    toggleLoggedInState(true);
    localStorage.setItem('currentUser', username);
  } else {
    alert('Invalid username or password.');
  }
}

// Function to handle Log Out
function logOut() {
  document.getElementById('welcomeMessage').classList.add('hidden');
  toggleLoggedInState(false);
  alert('You have been logged out.');
  localStorage.removeItem('currentUser');

  // Reload media to remove delete buttons
  document.getElementById('mediaContainer').innerHTML = '';
  loadMedia();
}

// Function to toggle between logged-in and logged-out states
function toggleLoggedInState(isLoggedIn) {
  document.getElementById('logOutButton').classList.toggle('hidden', !isLoggedIn);
  document.getElementById('addMediaButton').classList.toggle('hidden', !isLoggedIn);
  document.getElementById('signUpButton').classList.toggle('hidden', isLoggedIn);
  document.getElementById('signInButton').classList.toggle('hidden', isLoggedIn);
}

// Function to show Sign Up form
function showSignUp() {
  document.getElementById('signUpForm').classList.remove('hidden');
  document.getElementById('loginForm').classList.add('hidden');
}

// Function to show Sign In form
function showSignIn() {
  document.getElementById('loginForm').classList.remove('hidden');
  document.getElementById('signUpForm').classList.add('hidden');
}

// Load media on page load
window.onload = function () {
  loadMedia();

  const currentUser = localStorage.getItem('currentUser');
  if (currentUser) {
    document.getElementById('welcomeMessage').innerText = Hello, ${currentUser}!;
    toggleLoggedInState(true);
  }
};
  </script>
</body>
</html>
