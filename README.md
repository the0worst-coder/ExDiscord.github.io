<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>𝔰k҉𝔶 𝔤e҉𝔫 𝔬n҉𝔩i҉𝔫e҉</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Arial', sans-serif;
      background: url('https://tse2.mm.bing.net/th/id/OIP.HBSIF3oZHFrBXpntH9dr_wHaEn?cb=12&rs=1&pid=ImgDetMain&o=7&rm=3') center/cover fixed;
      overflow: hidden;
      color: white;
    }

    .particle {
      position: fixed;
      width: 8px;
      height: 8px;
      border-radius: 50%;
      pointer-events: none;
      z-index: 1;
      animation: float linear infinite;
    }

    @keyframes float {
      0% {
        transform: translateY(100vh) translateX(0);
        opacity: 0;
      }
      10% {
        opacity: 1;
      }
      90% {
        opacity: 1;
      }
      100% {
        transform: translateY(-100vh) translateX(var(--drift));
        opacity: 0;
      }
    }

    .glow-button {
      position: relative;
      background: rgba(30, 30, 40, 0.9);
      border: 2px solid rgba(139, 92, 246, 0.5);
      color: white;
      padding: 12px 24px;
      border-radius: 12px;
      cursor: pointer;
      transition: all 0.3s ease;
      box-shadow: 0 0 20px rgba(139, 92, 246, 0.3);
      font-weight: bold;
    }

    .glow-button:hover {
      transform: scale(1.1);
      box-shadow: 0 0 30px rgba(139, 92, 246, 0.6);
      border-color: rgba(139, 92, 246, 0.8);
    }

    .glow-button-small {
      padding: 8px 16px;
      font-size: 14px;
    }

    .glow-button-large {
      padding: 16px 32px;
      font-size: 18px;
    }

    .sidebar {
      width: 250px;
      background: rgba(20, 20, 30, 0.95);
      border-right: 2px solid rgba(139, 92, 246, 0.3);
      overflow-y: auto;
      z-index: 10;
    }

    .tab-button {
      width: 100%;
      padding: 12px 16px;
      background: rgba(30, 30, 40, 0.8);
      border: 1px solid rgba(139, 92, 246, 0.3);
      color: white;
      cursor: pointer;
      transition: all 0.3s ease;
      text-align: left;
      margin: 4px 0;
      border-radius: 8px;
    }

    .tab-button:hover {
      transform: scale(1.05);
      background: rgba(139, 92, 246, 0.3);
      box-shadow: 0 0 15px rgba(139, 92, 246, 0.4);
    }

    .tab-button.active {
      background: rgba(139, 92, 246, 0.5);
      border-color: rgba(139, 92, 246, 0.8);
      box-shadow: 0 0 20px rgba(139, 92, 246, 0.5);
    }

    .chat-container {
      flex: 1;
      display: flex;
      flex-direction: column;
      background: rgba(20, 20, 30, 0.9);
      border-radius: 12px;
      margin: 16px;
      overflow: hidden;
    }

    .messages {
      flex: 1;
      overflow-y: auto;
      padding: 16px;
      display: flex;
      flex-direction: column;
    }

    .message {
      background: rgba(30, 30, 40, 0.9);
      padding: 12px;
      border-radius: 8px;
      margin-bottom: 8px;
      border: 1px solid rgba(139, 92, 246, 0.3);
    }

    .message img, .message video {
      max-width: 300px;
      border-radius: 8px;
      margin-top: 8px;
    }

    .message a {
      color: #60a5fa;
      text-decoration: underline;
      word-break: break-all;
    }

    .input-area {
      padding: 16px;
      background: rgba(30, 30, 40, 0.95);
      border-top: 2px solid rgba(139, 92, 246, 0.3);
    }

    .modal {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.8);
      display: flex;
      align-items: center;
      justify-content: center;
      z-index: 1000;
    }

    .modal-content {
      background: rgba(20, 20, 30, 0.98);
      padding: 32px;
      border-radius: 16px;
      border: 2px solid rgba(139, 92, 246, 0.5);
      box-shadow: 0 0 40px rgba(139, 92, 246, 0.4);
      max-width: 500px;
      width: 90%;
    }

    input, textarea {
      width: 100%;
      padding: 12px;
      background: rgba(30, 30, 40, 0.9);
      border: 2px solid rgba(139, 92, 246, 0.3);
      border-radius: 8px;
      color: white;
      margin: 8px 0;
      font-size: 16px;
    }

    input::placeholder, textarea::placeholder {
      color: rgba(255, 255, 255, 0.5);
    }

    .profile-icon {
      width: 40px;
      height: 40px;
      border-radius: 50%;
      object-fit: cover;
      border: 2px solid rgba(139, 92, 246, 0.5);
    }

    .slide-panel {
      position: fixed;
      right: -400px;
      top: 0;
      width: 400px;
      height: 100%;
      background: rgba(20, 20, 30, 0.98);
      border-left: 2px solid rgba(139, 92, 246, 0.5);
      transition: right 0.3s ease;
      z-index: 999;
      overflow-y: auto;
      padding: 20px;
    }

    .slide-panel.open {
      right: 0;
    }

    ::-webkit-scrollbar {
      width: 10px;
    }

    ::-webkit-scrollbar-track {
      background: rgba(30, 30, 40, 0.5);
    }

    ::-webkit-scrollbar-thumb {
      background: rgba(139, 92, 246, 0.5);
      border-radius: 5px;
    }

    ::-webkit-scrollbar-thumb:hover {
      background: rgba(139, 92, 246, 0.7);
    }

    .voice-participant {
      background: rgba(30, 30, 40, 0.9);
      padding: 16px;
      border-radius: 8px;
      border: 2px solid rgba(139, 92, 246, 0.3);
      margin: 8px;
      text-align: center;
    }

    .voice-participant.speaking {
      border-color: rgba(34, 197, 94, 0.8);
      box-shadow: 0 0 20px rgba(34, 197, 94, 0.4);
    }

    .crop-container {
      position: relative;
      width: 300px;
      height: 300px;
      margin: 20px auto;
      border: 2px solid rgba(139, 92, 246, 0.5);
      overflow: hidden;
      border-radius: 8px;
    }

    .crop-image {
      max-width: 100%;
      max-height: 100%;
      cursor: move;
    }

    label {
      color: white;
      font-weight: bold;
      display: block;
      margin: 12px 0 4px 0;
    }
  </style>
</head>
<body>
  <!-- Particles -->
  <div id="particles"></div>

  <!-- Kicked Screen -->
  <div id="kickedScreen" style="display: none;" class="modal">
    <div class="modal-content">
      <h2 style="font-size: 24px; margin-bottom: 20px; text-align: center;">You've been kicked from the server</h2>
      <label>Enter Server Code:</label>
      <input type="text" id="serverCodeInput" placeholder="Enter server code...">
      <button class="glow-button" style="width: 100%; margin-top: 16px;" onclick="checkServerCode()">Join Server</button>
      <p id="codeError" style="color: #ef4444; margin-top: 8px; display: none;">Invalid server code</p>
    </div>
  </div>

  <!-- Sign In Modal -->
  <div id="signInModal" class="modal">
    <div class="modal-content">
      <h2 style="font-size: 28px; margin-bottom: 24px; text-align: center;">𝔰k҉𝔶 𝔤e҉𝔫 𝔬n҉𝔩i҉𝔫e҉</h2>
      
      <label>Username:</label>
      <input type="text" id="username" placeholder="Enter username...">
      
      <label>Password:</label>
      <input type="password" id="password" placeholder="Enter password...">
      
      <label>Profile Picture:</label>
      <input type="file" id="profileImage" accept="image/*" onchange="handleImageUpload(event)" style="padding: 8px;">
      
      <div id="cropContainer" style="display: none;">
        <div class="crop-container">
          <img id="cropImage" class="crop-image" draggable="false">
        </div>
        <div style="margin-top: 12px;">
          <label>Zoom:</label>
          <input type="range" id="zoomSlider" min="1" max="3" step="0.1" value="1" oninput="updateZoom()">
        </div>
      </div>
      
      <button class="glow-button" style="width: 100%; margin-top: 20px;" onclick="signIn()">Sign In</button>
    </div>
  </div>

  <!-- User List Panel -->
  <div id="userListPanel" class="slide-panel">
    <h3 style="font-size: 20px; margin-bottom: 16px; border-bottom: 2px solid rgba(139, 92, 246, 0.5); padding-bottom: 8px;">Server Members</h3>
    <div id="userList"></div>
  </div>

  <!-- Server Panel -->
  <div id="serverPanel" class="slide-panel">
    <h3 style="font-size: 20px; margin-bottom: 16px; border-bottom: 2px solid rgba(139, 92, 246, 0.5); padding-bottom: 8px;">Servers</h3>
    <div id="currentServer" style="margin-bottom: 24px;">
      <p style="color: rgba(255, 255, 255, 0.7); margin-bottom: 8px;">Current Server:</p>
      <div style="background: rgba(30, 30, 40, 0.9); padding: 16px; border-radius: 8px; border: 2px solid rgba(139, 92, 246, 0.5);">
        <p style="font-size: 18px; font-weight: bold;">SkyGenie Server</p>
        <p style="color: rgba(255, 255, 255, 0.6); font-size: 14px; margin-top: 4px;">Code: L00ECSkyGenie</p>
      </div>
    </div>
    <h4 style="font-size: 16px; margin-bottom: 12px;">Add Server</h4>
    <input type="text" id="newServerCode" placeholder="Enter server code...">
    <button class="glow-button" style="width: 100%; margin-top: 12px;" onclick="addServer()">Join Server</button>
    <div id="serverList" style="margin-top: 20px;"></div>
  </div>

  <!-- Main App -->
  <div id="mainApp" style="display: none; height: 100vh; display: flex; flex-direction: column;">
    <!-- Header -->
    <div style="background: rgba(20, 20, 30, 0.95); padding: 16px; border-bottom: 2px solid rgba(139, 92, 246, 0.5); display: flex; justify-content: space-between; align-items: center; z-index: 10;">
      <div style="display: flex; align-items: center; gap: 12px;">
        <img id="userProfileIcon" class="profile-icon" alt="Profile">
        <span id="userDisplayName" style="font-weight: bold; font-size: 16px;"></span>
        <button class="glow-button glow-button-small" onclick="toggleServerPanel()">
          <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <rect x="3" y="3" width="7" height="7" rx="1"></rect>
            <rect x="14" y="3" width="7" height="7" rx="1"></rect>
            <rect x="14" y="14" width="7" height="7" rx="1"></rect>
            <rect x="3" y="14" width="7" height="7" rx="1"></rect>
          </svg>
        </button>
      </div>
      <h1 style="font-size: 24px; font-weight: bold; text-shadow: 0 0 20px rgba(139, 92, 246, 0.6);">𝔰k҉𝔶 𝔤e҉𝔫 𝔬n҉𝔩i҉𝔫e҉</h1>
      <div style="display: flex; gap: 12px;">
        <button class="glow-button glow-button-small" onclick="toggleUserList()">
          <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"></path>
            <circle cx="9" cy="7" r="4"></circle>
            <path d="M23 21v-2a4 4 0 0 0-3-3.87"></path>
            <path d="M16 3.13a4 4 0 0 1 0 7.75"></path>
          </svg>
        </button>
        <button class="glow-button glow-button-small" onclick="signOut()">Sign Out</button>
      </div>
    </div>

    <!-- Content -->
    <div style="flex: 1; display: flex; overflow: hidden;">
      <!-- Sidebar -->
      <div class="sidebar">
        <div style="padding: 16px;">
          <button class="tab-button active" onclick="switchTab('chat')">💬 Chat</button>
          <button class="tab-button" onclick="switchTab('voice')">🎤 Voice Call</button>
          <div id="customTabs"></div>
          <button class="glow-button" style="width: 100%; margin-top: 16px;" onclick="showAddTabModal()">+ Add Tab</button>
        </div>
      </div>

      <!-- Main Content -->
      <div style="flex: 1; display: flex; flex-direction: column;">
        <!-- Chat View -->
        <div id="chatView" class="chat-container">
          <div class="messages" id="chatMessages"></div>
          <div class="input-area">
            <div style="display: flex; gap: 8px; margin-bottom: 12px;">
              <button class="glow-button glow-button-large" onclick="document.getElementById('imageInput').click()">📷 Image</button>
              <button class="glow-button glow-button-large" onclick="document.getElementById('videoInput').click()">🎥 Video</button>
              <button class="glow-button glow-button-large" onclick="focusTextInput()">💬 Text</button>
              <input type="file" id="imageInput" accept="image/*" style="display: none;" onchange="handleMediaUpload(event, 'image')">
              <input type="file" id="videoInput" accept="video/*" style="display: none;" onchange="handleMediaUpload(event, 'video')">
            </div>
            <textarea id="messageInput" placeholder="Type a message..." rows="3" onkeypress="handleKeyPress(event)"></textarea>
            <button class="glow-button" style="width: 100%; margin-top: 8px;" onclick="sendMessage()">Send</button>
          </div>
        </div>

        <!-- Voice Call View -->
        <div id="voiceView" class="chat-container" style="display: none;">
          <div style="padding: 24px; text-align: center;">
            <h2 style="font-size: 24px; margin-bottom: 24px;">Voice Call</h2>
            <div style="display: flex; gap: 16px; justify-content: center; margin-bottom: 32px;">
              <button class="glow-button glow-button-large" onclick="toggleVoiceCall()" id="voiceJoinBtn">Join Call</button>
              <button class="glow-button glow-button-large" onclick="toggleMute()" id="muteBtn" style="display: none;">Mute</button>
              <button class="glow-button glow-button-large" onclick="toggleSpeaker()" id="speakerBtn" style="display: none;">Speaker: ON</button>
            </div>
            <div id="voiceParticipants" style="display: grid; grid-template-columns: repeat(auto-fill, minmax(200px, 1fr)); gap: 16px;"></div>
          </div>
        </div>

        <!-- Custom Tab Views -->
        <div id="customTabViews"></div>
      </div>
    </div>
  </div>

  <!-- Add Tab Modal -->
  <div id="addTabModal" style="display: none;" class="modal">
    <div class="modal-content">
      <h3 style="font-size: 20px; margin-bottom: 16px;">Add New Tab</h3>
      <label>Tab Name:</label>
      <input type="text" id="newTabName" placeholder="Enter tab name...">
      <label>Tab Type:</label>
      <select id="newTabType" style="width: 100%; padding: 12px; background: rgba(30, 30, 40, 0.9); border: 2px solid rgba(139, 92, 246, 0.3); border-radius: 8px; color: white; margin: 8px 0;">
        <option value="chat">💬 Chat</option>
        <option value="voice">🎤 Voice Call</option>
      </select>
      <div style="display: flex; gap: 12px; margin-top: 20px;">
        <button class="glow-button" style="flex: 1;" onclick="addTab()">Add</button>
        <button class="glow-button" style="flex: 1;" onclick="closeAddTabModal()">Cancel</button>
      </div>
    </div>
  </div>

  <script>
    // Global state
    let currentUser = null;
    let currentTab = 'chat';
    let messages = {};
    let customTabs = [];
    let allUsers = [];
    let kickedUsers = [];
    let isInVoiceCall = false;
    let isMuted = false;
    let mediaStream = null;
    let voiceCallParticipants = {};
    let cropData = { x: 0, y: 0, scale: 1 };
    let isDragging = false;
    let dragStart = { x: 0, y: 0 };

    // Initialize particles
    function createParticles() {
      const colors = ['#ef4444', '#3b82f6', '#ffffff', '#a855f7'];
      const container = document.getElementById('particles');
      
      for (let i = 0; i < 50; i++) {
        const particle = document.createElement('div');
        particle.className = 'particle';
        particle.style.left = Math.random() * 100 + '%';
        particle.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
        particle.style.animationDuration = (Math.random() * 10 + 10) + 's';
        particle.style.animationDelay = Math.random() * 5 + 's';
        particle.style.setProperty('--drift', (Math.random() * 200 - 100) + 'px');
        container.appendChild(particle);
      }
    }

    // Load data from localStorage
    function loadData() {
      const savedUser = localStorage.getItem('skygenieUser');
      if (savedUser) {
        currentUser = JSON.parse(savedUser);
        const kicked = localStorage.getItem('skygenieKicked');
        if (kicked && JSON.parse(kicked).includes(currentUser.username)) {
          showKickedScreen();
        } else {
          showMainApp();
        }
      }

      messages = JSON.parse(localStorage.getItem('skygenieMessages') || '{"chat": [], "voice": []}');
      customTabs = JSON.parse(localStorage.getItem('skygenieTabs') || '[]');
      allUsers = JSON.parse(localStorage.getItem('skygenieAllUsers') || '[]');
      kickedUsers = JSON.parse(localStorage.getItem('skygenieKicked') || '[]');
      voiceCallParticipants = JSON.parse(localStorage.getItem('skygenieVoiceParticipants') || '{}');
    }

    // Save data to localStorage
    function saveData() {
      if (currentUser) {
        localStorage.setItem('skygenieUser', JSON.stringify(currentUser));
      }
      localStorage.setItem('skygenieMessages', JSON.stringify(messages));
      localStorage.setItem('skygenieTabs', JSON.stringify(customTabs));
      localStorage.setItem('skygenieAllUsers', JSON.stringify(allUsers));
      localStorage.setItem('skygenieKicked', JSON.stringify(kickedUsers));
      localStorage.setItem('skygenieVoiceParticipants', JSON.stringify(voiceCallParticipants));
    }

    // Image cropping
    function handleImageUpload(event) {
      const file = event.target.files[0];
      if (file) {
        const reader = new FileReader();
        reader.onload = function(e) {
          const img = document.getElementById('cropImage');
          img.src = e.target.result;
          document.getElementById('cropContainer').style.display = 'block';
          
          img.onload = function() {
            cropData = { x: 0, y: 0, scale: 1 };
            updateCropImage();
          };

          // Add drag functionality
          img.addEventListener('mousedown', startDrag);
          img.addEventListener('mousemove', drag);
          img.addEventListener('mouseup', endDrag);
          img.addEventListener('mouseleave', endDrag);
        };
        reader.readAsDataURL(file);
      }
    }

    function startDrag(e) {
      isDragging = true;
      dragStart = { x: e.clientX - cropData.x, y: e.clientY - cropData.y };
    }

    function drag(e) {
      if (isDragging) {
        cropData.x = e.clientX - dragStart.x;
        cropData.y = e.clientY - dragStart.y;
        updateCropImage();
      }
    }

    function endDrag() {
      isDragging = false;
    }

    function updateZoom() {
      cropData.scale = document.getElementById('zoomSlider').value;
      updateCropImage();
    }

    function updateCropImage() {
      const img = document.getElementById('cropImage');
      img.style.transform = `translate(${cropData.x}px, ${cropData.y}px) scale(${cropData.scale})`;
    }

    function getCroppedImage() {
      const img = document.getElementById('cropImage');
      const container = document.querySelector('.crop-container');
      
      const canvas = document.createElement('canvas');
      canvas.width = 200;
      canvas.height = 200;
      const ctx = canvas.getContext('2d');
      
      const scale = cropData.scale;
      const x = -cropData.x / scale;
      const y = -cropData.y / scale;
      
      ctx.drawImage(img, x, y, img.naturalWidth, img.naturalHeight, 0, 0, 200 * scale, 200 * scale);
      
      return canvas.toDataURL('image/png');
    }

    // Sign in
    function signIn() {
      const username = document.getElementById('username').value.trim();
      const password = document.getElementById('password').value.trim();
      
      if (!username || !password) {
        alert('Please enter username and password');
        return;
      }

      let profileIcon = '👤';
      const cropContainer = document.getElementById('cropContainer');
      if (cropContainer.style.display !== 'none') {
        profileIcon = getCroppedImage();
      }

      currentUser = { username, password, icon: profileIcon };
      
      // Add to all users if not exists
      if (!allUsers.find(u => u.username === username)) {
        allUsers.push(currentUser);
      }
      
      saveData();
      showMainApp();
    }

    // Sign out
    function signOut() {
      if (isInVoiceCall) {
        leaveVoiceCall();
      }
      currentUser = null;
      localStorage.removeItem('skygenieUser');
      location.reload();
    }

    // Show main app
    function showMainApp() {
      document.getElementById('signInModal').style.display = 'none';
      document.getElementById('mainApp').style.display = 'flex';
      document.getElementById('userDisplayName').textContent = currentUser.username;
      
      const profileIcon = document.getElementById('userProfileIcon');
      if (currentUser.icon.startsWith('data:') || currentUser.icon.startsWith('http')) {
        profileIcon.src = currentUser.icon;
      } else {
        profileIcon.src = 'data:image/svg+xml,' + encodeURIComponent(`<svg xmlns="http://www.w3.org/2000/svg" width="40" height="40"><text x="50%" y="50%" text-anchor="middle" dy=".3em" font-size="24">${currentUser.icon}</text></svg>`);
      }
      
      loadCustomTabs();
      renderMessages();
      setInterval(updateMessages, 1000);
      setInterval(updateVoiceParticipants, 1000);
    }

    // Kicked screen
    function showKickedScreen() {
      document.getElementById('signInModal').style.display = 'none';
      document.getElementById('mainApp').style.display = 'none';
      document.getElementById('kickedScreen').style.display = 'flex';
    }

    function checkServerCode() {
      const code = document.getElementById('serverCodeInput').value.trim();
      if (code === 'L00ECSkyGenie') {
        kickedUsers = kickedUsers.filter(u => u !== currentUser.username);
        saveData();
        document.getElementById('kickedScreen').style.display = 'none';
        showMainApp();
      } else {
        document.getElementById('codeError').style.display = 'block';
      }
    }

    // User list
    function toggleUserList() {
      const panel = document.getElementById('userListPanel');
      const serverPanel = document.getElementById('serverPanel');
      serverPanel.classList.remove('open');
      panel.classList.toggle('open');
      if (panel.classList.contains('open')) {
        renderUserList();
      }
    }

    function renderUserList() {
      const container = document.getElementById('userList');
      container.innerHTML = '';
      
      allUsers.forEach(user => {
        const isKicked = kickedUsers.includes(user.username);
        const userDiv = document.createElement('div');
        userDiv.style.cssText = 'background: rgba(30, 30, 40, 0.9); padding: 12px; border-radius: 8px; margin-bottom: 8px; display: flex; justify-content: space-between; align-items: center; border: 1px solid rgba(139, 92, 246, 0.3);';
        
        const userInfo = document.createElement('div');
        userInfo.style.cssText = 'display: flex; align-items: center; gap: 12px;';
        
        const icon = document.createElement('img');
        icon.className = 'profile-icon';
        icon.style.width = '32px';
        icon.style.height = '32px';
        if (user.icon.startsWith('data:') || user.icon.startsWith('http')) {
          icon.src = user.icon;
        } else {
          icon.src = 'data:image/svg+xml,' + encodeURIComponent(`<svg xmlns="http://www.w3.org/2000/svg" width="32" height="32"><text x="50%" y="50%" text-anchor="middle" dy=".3em" font-size="20">${user.icon}</text></svg>`);
        }
        
        const name = document.createElement('span');
        name.textContent = user.username;
        if (isKicked) {
          name.textContent += ' (Kicked)';
          name.style.color = '#ef4444';
        }
        
        userInfo.appendChild(icon);
        userInfo.appendChild(name);
        
        if (user.username !== currentUser.username) {
          const kickBtn = document.createElement('button');
          kickBtn.className = 'glow-button glow-button-small';
          kickBtn.textContent = isKicked ? 'Unkick' : 'Kick';
          kickBtn.style.background = isKicked ? 'rgba(34, 197, 94, 0.3)' : 'rgba(239, 68, 68, 0.3)';
          kickBtn.onclick = () => toggleKick(user.username);
          userDiv.appendChild(userInfo);
          userDiv.appendChild(kickBtn);
        } else {
          userDiv.appendChild(userInfo);
        }
        
        container.appendChild(userDiv);
      });
    }

    function toggleKick(username) {
      if (kickedUsers.includes(username)) {
        kickedUsers = kickedUsers.filter(u => u !== username);
      } else {
        kickedUsers.push(username);
      }
      saveData();
      renderUserList();
    }

    // Server panel
    function toggleServerPanel() {
      const panel = document.getElementById('serverPanel');
      const userPanel = document.getElementById('userListPanel');
      userPanel.classList.remove('open');
      panel.classList.toggle('open');
    }

    function addServer() {
      const code = document.getElementById('newServerCode').value.trim();
      if (code) {
        alert('Server feature coming soon! Code: ' + code);
        document.getElementById('newServerCode').value = '';
      }
    }

    // Tab management
    function switchTab(tabId) {
      currentTab = tabId;
      
      // Update button states
      document.querySelectorAll('.tab-button').forEach(btn => {
        btn.classList.remove('active');
      });
      event.target.classList.add('active');
      
      // Hide all views
      document.getElementById('chatView').style.display = 'none';
      document.getElementById('voiceView').style.display = 'none';
      document.querySelectorAll('[id^="customTab-"]').forEach(view => {
        view.style.display = 'none';
      });
      
      // Show selected view
      if (tabId === 'chat') {
        document.getElementById('chatView').style.display = 'flex';
        renderMessages();
      } else if (tabId === 'voice') {
        document.getElementById('voiceView').style.display = 'flex';
        updateVoiceParticipants();
      } else {
        const customView = document.getElementById('customTab-' + tabId);
        if (customView) {
          customView.style.display = 'flex';
          renderCustomTabMessages(tabId);
        }
      }
    }

    function showAddTabModal() {
      document.getElementById('addTabModal').style.display = 'flex';
    }

    function closeAddTabModal() {
      document.getElementById('addTabModal').style.display = 'none';
      document.getElementById('newTabName').value = '';
    }

    function addTab() {
      const name = document.getElementById('newTabName').value.trim();
      const type = document.getElementById('newTabType').value;
      
      if (!name) {
        alert('Please enter a tab name');
        return;
      }
      
      const tabId = 'tab-' + Date.now();
      customTabs.push({ id: tabId, name, type });
      messages[tabId] = [];
      saveData();
      loadCustomTabs();
      closeAddTabModal();
    }

    function loadCustomTabs() {
      const container = document.getElementById('customTabs');
      const viewsContainer = document.getElementById('customTabViews');
      container.innerHTML = '';
      viewsContainer.innerHTML = '';
      
      customTabs.forEach(tab => {
        // Add button
        const btn = document.createElement('button');
        btn.className = 'tab-button';
        btn.textContent = (tab.type === 'voice' ? '🎤 ' : '💬 ') + tab.name;
        btn.onclick = () => switchTab(tab.id);
        container.appendChild(btn);
        
        // Add view
        const view = document.createElement('div');
        view.id = 'customTab-' + tab.id;
        view.className = 'chat-container';
        view.style.display = 'none';
        
        if (tab.type === 'voice') {
          view.innerHTML = `
            <div style="padding: 24px; text-align: center;">
              <h2 style="font-size: 24px; margin-bottom: 24px;">${tab.name}</h2>
              <div style="display: flex; gap: 16px; justify-content: center; margin-bottom: 32px;">
                <button class="glow-button glow-button-large" onclick="toggleCustomVoiceCall('${tab.id}')" id="voiceJoinBtn-${tab.id}">Join Call</button>
                <button class="glow-button glow-button-large" onclick="toggleMute()" id="muteBtn-${tab.id}" style="display: none;">Mute</button>
                <button class="glow-button glow-button-large" onclick="toggleSpeaker()" id="speakerBtn-${tab.id}" style="display: none;">Speaker: ON</button>
              </div>
              <div id="voiceParticipants-${tab.id}" style="display: grid; grid-template-columns: repeat(auto-fill, minmax(200px, 1fr)); gap: 16px;"></div>
            </div>
          `;
        } else {
          view.innerHTML = `
            <div class="messages" id="messages-${tab.id}"></div>
            <div class="input-area">
              <div style="display: flex; gap: 8px; margin-bottom: 12px;">
                <button class="glow-button glow-button-large" onclick="document.getElementById('imageInput-${tab.id}').click()">📷 Image</button>
                <button class="glow-button glow-button-large" onclick="document.getElementById('videoInput-${tab.id}').click()">🎥 Video</button>
                <button class="glow-button glow-button-large" onclick="focusCustomInput('${tab.id}')">💬 Text</button>
                <input type="file" id="imageInput-${tab.id}" accept="image/*" style="display: none;" onchange="handleCustomMediaUpload(event, 'image', '${tab.id}')">
                <input type="file" id="videoInput-${tab.id}" accept="video/*" style="display: none;" onchange="handleCustomMediaUpload(event, 'video', '${tab.id}')">
              </div>
              <textarea id="messageInput-${tab.id}" placeholder="Type a message..." rows="3" onkeypress="handleCustomKeyPress(event, '${tab.id}')"></textarea>
              <button class="glow-button" style="width: 100%; margin-top: 8px;" onclick="sendCustomMessage('${tab.id}')">Send</button>
            </div>
          `;
        }
        
        viewsContainer.appendChild(view);
      });
    }

    // Messages
    function sendMessage() {
      const input = document.getElementById('messageInput');
      const text = input.value.trim();
      
      if (!text) return;
      
      if (!messages.chat) messages.chat = [];
      
      messages.chat.push({
        username: currentUser.username,
        userIcon: currentUser.icon,
        text: text,
        timestamp: Date.now()
      });
      
      input.value = '';
      saveData();
      renderMessages();
    }

    function sendCustomMessage(tabId) {
      const input = document.getElementById('messageInput-' + tabId);
      const text = input.value.trim();
      
      if (!text) return;
      
      if (!messages[tabId]) messages[tabId] = [];
      
      messages[tabId].push({
        username: currentUser.username,
        userIcon: currentUser.icon,
        text: text,
        timestamp: Date.now()
      });
      
      input.value = '';
      saveData();
      renderCustomTabMessages(tabId);
    }

    function handleMediaUpload(event, type) {
      const file = event.target.files[0];
      if (file) {
        const reader = new FileReader();
        reader.onload = function(e) {
          if (!messages.chat) messages.chat = [];
          
          messages.chat.push({
            username: currentUser.username,
            userIcon: currentUser.icon,
            type: type,
            url: e.target.result,
            timestamp: Date.now()
          });
          
          saveData();
          renderMessages();
        };
        reader.readAsDataURL(file);
      }
    }

    function handleCustomMediaUpload(event, type, tabId) {
      const file = event.target.files[0];
      if (file) {
        const reader = new FileReader();
        reader.onload = function(e) {
          if (!messages[tabId]) messages[tabId] = [];
          
          messages[tabId].push({
            username: currentUser.username,
            userIcon: currentUser.icon,
            type: type,
            url: e.target.result,
            timestamp: Date.now()
          });
          
          saveData();
          renderCustomTabMessages(tabId);
        };
        reader.readAsDataURL(file);
      }
    }

    function renderMessages() {
      const container = document.getElementById('chatMessages');
      container.innerHTML = '';
      
      if (!messages.chat) messages.chat = [];
      
      messages.chat.forEach(msg => {
        const msgDiv = document.createElement('div');
        msgDiv.className = 'message';
        
        let iconHtml = '';
        if (msg.userIcon && (msg.userIcon.startsWith('data:') || msg.userIcon.startsWith('http'))) {
          iconHtml = `<img src="${msg.userIcon}" class="profile-icon" style="width: 32px; height: 32px; margin-right: 8px;">`;
        } else {
          iconHtml = `<span style="font-size: 24px; margin-right: 8px;">${msg.userIcon || '👤'}</span>`;
        }
        
        if (msg.type === 'image') {
          msgDiv.innerHTML = `
            <div style="display: flex; align-items: start;">
              ${iconHtml}
              <div>
                <strong style="color: #a855f7;">${msg.username}</strong>
                <img src="${msg.url}" style="max-width: 300px; border-radius: 8px; margin-top: 8px; display: block;">
              </div>
            </div>
          `;
        } else if (msg.type === 'video') {
          msgDiv.innerHTML = `
            <div style="display: flex; align-items: start;">
              ${iconHtml}
              <div>
                <strong style="color: #a855f7;">${msg.username}</strong>
                <video controls style="max-width: 300px; border-radius: 8px; margin-top: 8px; display: block;">
                  <source src="${msg.url}">
                </video>
              </div>
            </div>
          `;
        } else {
          const textWithLinks = msg.text.replace(/(https?:\/\/[^\s]+)/g, '<a href="$1" target="_blank">$1</a>');
          msgDiv.innerHTML = `
            <div style="display: flex; align-items: start;">
              ${iconHtml}
              <div>
                <strong style="color: #a855f7;">${msg.username}</strong>
                <p style="margin-top: 4px; color: white;">${textWithLinks}</p>
              </div>
            </div>
          `;
        }
        
        container.appendChild(msgDiv);
      });
      
      container.scrollTop = container.scrollHeight;
    }

    function renderCustomTabMessages(tabId) {
      const container = document.getElementById('messages-' + tabId);
      if (!container) return;
      
      container.innerHTML = '';
      
      if (!messages[tabId]) messages[tabId] = [];
      
      messages[tabId].forEach(msg => {
        const msgDiv = document.createElement('div');
        msgDiv.className = 'message';
        
        let iconHtml = '';
        if (msg.userIcon && (msg.userIcon.startsWith('data:') || msg.userIcon.startsWith('http'))) {
          iconHtml = `<img src="${msg.userIcon}" class="profile-icon" style="width: 32px; height: 32px; margin-right: 8px;">`;
        } else {
          iconHtml = `<span style="font-size: 24px; margin-right: 8px;">${msg.userIcon || '👤'}</span>`;
        }
        
        if (msg.type === 'image') {
          msgDiv.innerHTML = `
            <div style="display: flex; align-items: start;">
              ${iconHtml}
              <div>
                <strong style="color: #a855f7;">${msg.username}</strong>
                <img src="${msg.url}" style="max-width: 300px; border-radius: 8px; margin-top: 8px; display: block;">
              </div>
            </div>
          `;
        } else if (msg.type === 'video') {
          msgDiv.innerHTML = `
            <div style="display: flex; align-items: start;">
              ${iconHtml}
              <div>
                <strong style="color: #a855f7;">${msg.username}</strong>
                <video controls style="max-width: 300px; border-radius: 8px; margin-top: 8px; display: block;">
                  <source src="${msg.url}">
                </video>
              </div>
            </div>
          `;
        } else {
          const textWithLinks = msg.text.replace(/(https?:\/\/[^\s]+)/g, '<a href="$1" target="_blank">$1</a>');
          msgDiv.innerHTML = `
            <div style="display: flex; align-items: start;">
              ${iconHtml}
              <div>
                <strong style="color: #a855f7;">${msg.username}</strong>
                <p style="margin-top: 4px; color: white;">${textWithLinks}</p>
              </div>
            </div>
          `;
        }
        
        container.appendChild(msgDiv);
      });
      
      container.scrollTop = container.scrollHeight;
    }

    function updateMessages() {
      const savedMessages = JSON.parse(localStorage.getItem('skygenieMessages') || '{"chat": [], "voice": []}');
      if (JSON.stringify(savedMessages) !== JSON.stringify(messages)) {
        messages = savedMessages;
        if (currentTab === 'chat') {
          renderMessages();
        } else if (currentTab.startsWith('tab-')) {
          renderCustomTabMessages(currentTab);
        }
      }
    }

    function handleKeyPress(event) {
      if (event.key === 'Enter' && !event.shiftKey) {
        event.preventDefault();
        sendMessage();
      }
    }

    function handleCustomKeyPress(event, tabId) {
      if (event.key === 'Enter' && !event.shiftKey) {
        event.preventDefault();
        sendCustomMessage(tabId);
      }
    }

    function focusTextInput() {
      document.getElementById('messageInput').focus();
    }

    function focusCustomInput(tabId) {
      document.getElementById('messageInput-' + tabId).focus();
    }

    // Voice call
    function toggleVoiceCall() {
      if (isInVoiceCall) {
        leaveVoiceCall();
      } else {
        joinVoiceCall();
      }
    }

    function joinVoiceCall() {
      navigator.mediaDevices.getUserMedia({ audio: true })
        .then(stream => {
          mediaStream = stream;
          isInVoiceCall = true;
          
          if (!voiceCallParticipants.voice) voiceCallParticipants.voice = {};
          voiceCallParticipants.voice[currentUser.username] = {
            username: currentUser.username,
            icon: currentUser.icon,
            muted: false,
            timestamp: Date.now()
          };
          
          saveData();
          
          document.getElementById('voiceJoinBtn').textContent = 'Leave Call';
          document.getElementById('muteBtn').style.display = 'inline-block';
          document.getElementById('speakerBtn').style.display = 'inline-block';
          
          updateVoiceParticipants();
        })
        .catch(err => {
          alert('Could not access microphone: ' + err.message);
        });
    }

    function leaveVoiceCall() {
      if (mediaStream) {
        mediaStream.getTracks().forEach(track => track.stop());
        mediaStream = null;
      }
      
      isInVoiceCall = false;
      isMuted = false;
      
      if (voiceCallParticipants.voice) {
        delete voiceCallParticipants.voice[currentUser.username];
      }
      
      saveData();
      
      document.getElementById('voiceJoinBtn').textContent = 'Join Call';
      document.getElementById('muteBtn').style.display = 'none';
      document.getElementById('speakerBtn').style.display = 'none';
      
      updateVoiceParticipants();
    }

    function toggleCustomVoiceCall(tabId) {
      const joinBtn = document.getElementById('voiceJoinBtn-' + tabId);
      const muteBtn = document.getElementById('muteBtn-' + tabId);
      const speakerBtn = document.getElementById('speakerBtn-' + tabId);
      
      if (joinBtn.textContent === 'Join Call') {
        navigator.mediaDevices.getUserMedia({ audio: true })
          .then(stream => {
            if (!voiceCallParticipants[tabId]) voiceCallParticipants[tabId] = {};
            voiceCallParticipants[tabId][currentUser.username] = {
              username: currentUser.username,
              icon: currentUser.icon,
              muted: false,
              timestamp: Date.now()
            };
            
            saveData();
            
            joinBtn.textContent = 'Leave Call';
            muteBtn.style.display = 'inline-block';
            speakerBtn.style.display = 'inline-block';
            
            updateCustomVoiceParticipants(tabId);
          })
          .catch(err => {
            alert('Could not access microphone: ' + err.message);
          });
      } else {
        if (voiceCallParticipants[tabId]) {
          delete voiceCallParticipants[tabId][currentUser.username];
        }
        
        saveData();
        
        joinBtn.textContent = 'Join Call';
        muteBtn.style.display = 'none';
        speakerBtn.style.display = 'none';
        
        updateCustomVoiceParticipants(tabId);
      }
    }

    function toggleMute() {
      isMuted = !isMuted;
      if (mediaStream) {
        mediaStream.getAudioTracks().forEach(track => {
          track.enabled = !isMuted;
        });
      }
      
      const btn = document.getElementById('muteBtn');
      if (btn) {
        btn.textContent = isMuted ? 'Unmute' : 'Mute';
      }
    }

    function toggleSpeaker() {
      alert('Speaker toggle feature');
    }

    function updateVoiceParticipants() {
      const container = document.getElementById('voiceParticipants');
      if (!container) return;
      
      container.innerHTML = '';
      
      const participants = voiceCallParticipants.voice || {};
      
      // Clean up old participants (older than 5 seconds)
      const now = Date.now();
      Object.keys(participants).forEach(username => {
        if (now - participants[username].timestamp > 5000) {
          delete participants[username];
        }
      });
      
      // Update current user's timestamp if in call
      if (isInVoiceCall && participants[currentUser.username]) {
        participants[currentUser.username].timestamp = now;
        voiceCallParticipants.voice = participants;
        saveData();
      }
      
      Object.values(participants).forEach(participant => {
        const div = document.createElement('div');
        div.className = 'voice-participant';
        
        let iconHtml = '';
        if (participant.icon && (participant.icon.startsWith('data:') || participant.icon.startsWith('http'))) {
          iconHtml = `<img src="${participant.icon}" class="profile-icon" style="width: 64px; height: 64px; margin: 0 auto 12px;">`;
        } else {
          iconHtml = `<div style="font-size: 48px; margin-bottom: 12px;">${participant.icon || '👤'}</div>`;
        }
        
        div.innerHTML = `
          ${iconHtml}
          <p style="font-weight: bold; font-size: 16px;">${participant.username}</p>
          <p style="color: rgba(255, 255, 255, 0.6); font-size: 14px; margin-top: 4px;">${participant.muted ? '🔇 Muted' : '🎤 Speaking'}</p>
        `;
        
        container.appendChild(div);
      });
    }

    function updateCustomVoiceParticipants(tabId) {
      const container = document.getElementById('voiceParticipants-' + tabId);
      if (!container) return;
      
      container.innerHTML = '';
      
      const participants = voiceCallParticipants[tabId] || {};
      
      // Clean up old participants
      const now = Date.now();
      Object.keys(participants).forEach(username => {
        if (now - participants[username].timestamp > 5000) {
          delete participants[username];
        }
      });
      
      // Update current user's timestamp if in call
      const joinBtn = document.getElementById('voiceJoinBtn-' + tabId);
      if (joinBtn && joinBtn.textContent === 'Leave Call' && participants[currentUser.username]) {
        participants[currentUser.username].timestamp = now;
        voiceCallParticipants[tabId] = participants;
        saveData();
      }
      
      Object.values(participants).forEach(participant => {
        const div = document.createElement('div');
        div.className = 'voice-participant';
        
        let iconHtml = '';
        if (participant.icon && (participant.icon.startsWith('data:') || participant.icon.startsWith('http'))) {
          iconHtml = `<img src="${participant.icon}" class="profile-icon" style="width: 64px; height: 64px; margin: 0 auto 12px;">`;
        } else {
          iconHtml = `<div style="font-size: 48px; margin-bottom: 12px;">${participant.icon || '👤'}</div>`;
        }
        
        div.innerHTML = `
          ${iconHtml}
          <p style="font-weight: bold; font-size: 16px;">${participant.username}</p>
          <p style="color: rgba(255, 255, 255, 0.6); font-size: 14px; margin-top: 4px;">${participant.muted ? '🔇 Muted' : '🎤 Speaking'}</p>
        `;
        
        container.appendChild(div);
      });
    }

    // Initialize
    createParticles();
    loadData();
  </script>
</body>
</html>
