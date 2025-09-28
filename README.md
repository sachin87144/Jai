
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Personal Web Space</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background: linear-gradient(135deg, cyan,pink , #fdbb2d);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        .container {
            width: 100%;
            max-width: 900px;
            background-color: rgba(255, 255, 255, 0.95);
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            overflow: hidden;
        }

        .form-container {
            padding: 40px;
            transition: all 0.5s ease;
        }
        h1{
            text-align: center;
            margin-bottom:25px;
            color :deepskyblue;
        }

        h2 {
            text-align: center;
            margin-bottom: 25px;
            color: hotpink;
        }
        h3{
            text-align: center;
            margin-bottom:30px;
            color:salmon;
            
        }

        .input-group {
            margin-bottom: 20px;
            position: relative;
        }

        input {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-size: 16px;
            transition: border 0.3s;
        }

        input:focus {
            outline: none;
            border-color: #1a2a6c;
            box-shadow: 0 0 5px rgba(26, 42, 108, 0.3);
        }

        button {
            width: 100%;
            padding: 12px;
            background: linear-gradient(to right, grey, orange);
            border: none;
            border-radius: 8px;
            color: white;
            font-size: 16px;
            cursor: pointer;
            transition: opacity 0.3s;
        }

        button:hover {
            opacity: 0.9;
        }

        .error {
            color: #e74c3c;
            font-size: 14px;
            margin-top: 5px;
            display: none;
        }

        .dashboard {
            padding: 30px;
            display: none;
        }

        .header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 30px;
            padding-bottom: 15px;
            border-bottom: 1px solid #eee;
        }

        .welcome {
            text-align: left;
        }

        .welcome h2 {
            margin-bottom: 5px;
            text-align: left;
        }

        .last-login {
            background-color: #f8f9fa;
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 20px;
            text-align: center;
        }

        .last-login p {
            margin: 5px 0;
            background color:pink;
        }

        .logout-btn {
            background: linear-gradient(to right, #Tan, #e67e22);
            width: auto;
            padding: 8px 15px;
        }

        .user-info {
            background-color: #f0f8ff;
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 20px;
        }

        .user-info p {
            margin: 8px 0;
            color: #444;
        }

        .content-area {
            margin-top: 30px;
        }

        .content-area h3 {
            margin-bottom: 15px;
            color: darkslategrey;
        }

        textarea {
            width: 100%;
            height: 200px;
            padding: 15px;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-size: 16px;
            resize: vertical;
            transition: border 0.3s;
        }

        textarea:focus {
            outline: none;
            border-color: #1a2a6c;
            box-shadow: 0 0 5px rgba(26, 42, 108, 0.3);
        }

        .save-btn {
            background: linear-gradient(to right, #1a2a6c, #b21f1f);
            width: auto;
            padding: 10px 20px;
            margin-top: 10px;
        }

        .saved-message {
            color: mistyrose;
            margin-top: 10px;
            display: none;
        }

        @media (max-width: 768px) {
            .container {
                max-width: 95%;
            }
            
            .form-container, .dashboard {
                padding: 20px;
            }
            
            .header {
                flex-direction: column;
                align-items: flex-start;
            }
            
            .logout-btn {
                margin-top: 10px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Login Form -->
        <div class="form-container" id="loginForm">
            <h2>Welcome to study web</h2>
            <div class="input-group">
                <input type="text" id="username" placeholder="Username" required>
                <div class="error" id="usernameError">Please enter a valid username (min 3 characters)</div>
            </div>
            <div class="input-group">
                <input type="password" id="password" placeholder="Password" required>
                <div class="error" id="passwordError">Password must be at least 6 characters</div>
            </div>
            <button id="loginBtn">Login</button>
            <div class="input-group" style="text-align: center; margin-top: 15px;">
                <p>Sabhi prakar ke notes yaha milenge<br> 💞radhe radhe💞</p>
            </div>
        </div>

        <!-- Dashboard -->
        <div class="dashboard" id="dashboard">
            <div class="header">
                <div class="welcome">
                    <h2>Welcome, <span id="userDisplayName">User</span>!</h2>
                    <p>Idhar ati rehna me idhar hi msg write </p>
                </div>
                <button class="logout-btn" id="logoutBtn">Logout</button>
            </div>
            
            <div class="last-login">
                <h3>Radhe Radhe</h3>
                <h3>Update time ="5:00"</h3>
               <p>Bhen vo mujhe yes ka reply nahi mila tha isley update nahi kara ab kara sachin ki health ab sahi hai thodi ab kis problem me ho jo yes nahi likh pa rahi ho batao bhen ap abhi bhi irritate ho to me help karunga apkar man kar raha hoga ki kisi se baat nahi karni par bhen karo na ap batao kya hua jis bhi problem me ho bs yes hi to likhna hai</p>
                
            </div>
            
            <div class="user-info">
                <h3>bhen dekhti raha karna har 2 hour baad jab bhi dekh liya jaro yes likh diya karna prutha ke wp par. pls bhen dekha karo</h3>
<p>Bhen ap ab badal rahi hougi mujhe pata hai isley ap unblock kar sakti ho isse ap mujhe reply bhi de sakti ho bhen agar me apko dikkat du to block kar dena ya fir sachin par esa nahi hoga bhen pls unblock kar do or apki jo bhi problem hai ki sachin jayda msg karta hai asa kuch nahi hoga ap unblock kar do apko kuch dikhana bhi hai or apke pass jab time ho me jabhi baat kara karunga mujhe pata hai ki tumhare paper bhi hai bhen isley tum nahi karogi agar tum unblock kar dogi to fir sachin ko sach me bhot khushi milegi pls bhen unblock kar do🙄🥺🥺</p>
            </div>
            
            <div class="content-area">
                <h3>Your Personal Notes</h3>
                <p>me samjh gaya hu ki ap block ki isley bolti ho prutha se taki bo pareshan na ho par bo nahi karti block sach me bhot achi hai or ap ase block kar deti ho pata hai block kab kara jata hai jab apka breakuptype kuch hoya ho ya fir bilkul gali bali de di ho ya apko kuch khe diya ho asa ap bui na bhen age se nahi karogi na asa to fir yes 2 ke sath yes 3 likhna bhen😊🙃 pls</p><hr>
                                
               <p>bhen sorry par unblock kar do apne prutha ko yes bhi nahi likha msg kyu nahi padh rahi ho sachin apse baat karna chata hai ap irritate mat ho ki ap sach me ye hi soch rahi hogi ki me kin chakkaro me padh rahi hu pls bhen unblock kar do or hi ap dalna kyuonki mujhe apka number nahi pata apko meri kasam hai bhen unblock kar do</p>
               
                <br>
                <br>
                <h3>Bhen apko meri kassan hai unblock kar do agar ap ab apne bheaviour ko sudhar pa rahi ho to unblock kar do apko meri kasam hai bhen sachin ki khatir bss. me ase nahi bolta nahi to</h3>
               
              
                <button class="save-btn" id="saveNotesBtn">Save Notes</button>
                <div class="saved-message" id="savedMessage">Notes saved successfully!</div>
            </div>
        </div>
    </div>

    <script>
        // DOM Elements
        const loginForm = document.getElementById('loginForm');
        const dashboard = document.getElementById('dashboard');
        const loginBtn = document.getElementById('loginBtn');
        const logoutBtn = document.getElementById('logoutBtn');
        const usernameInput = document.getElementById('username');
        const passwordInput = document.getElementById('password');
        const usernameError = document.getElementById('usernameError');
        const passwordError = document.getElementById('passwordError');
        const userDisplayName = document.getElementById('userDisplayName');
        const displayUsername = document.getElementById('displayUsername');
        const lastLoginDate = document.getElementById('lastLoginDate');
        const accountCreated = document.getElementById('accountCreated');
        const personalNotes = document.getElementById('personalNotes');
        const saveNotesBtn = document.getElementById('saveNotesBtn');
        const savedMessage = document.getElementById('savedMessage');

        // Default credentials
        const DEFAULT_USERNAME = "Tamanna";
        const DEFAULT_PASSWORD = "123321";

        // Check if user is already logged in
        document.addEventListener('DOMContentLoaded', function() {
            const savedUser = localStorage.getItem('currentUser');
            if (savedUser) {
                const user = JSON.parse(savedUser);
                showDashboard(user);
                
                // Load saved notes
                const savedNotes = localStorage.getItem(`notes_${user.username}`);
                if (savedNotes) {
                    personalNotes.value = savedNotes;
                }
            }
        });

        // Login functionality
        loginBtn.addEventListener('click', function() {
            const username = usernameInput.value.trim();
            const password = passwordInput.value.trim();
            
            // Reset errors
            usernameError.style.display = 'none';
            passwordError.style.display = 'none';
            
            // Validate inputs
            let isValid = true;
            
            if (username.length < 3) {
                usernameError.textContent = 'Username must be at least 3 characters';
                usernameError.style.display = 'block';
                isValid = false;
            }
            
            if (password.length < 6) {
                passwordError.textContent = 'Password must be at least 6 characters';
                passwordError.style.display = 'block';
                isValid = false;
            }
            
            if (!isValid) return;
            
            // Check credentials (in a real app, this would connect to a server)
            if (username === DEFAULT_USERNAME && password === DEFAULT_PASSWORD) {
                // Successful login with default credentials
                handleSuccessfulLogin(username);
            } else {
                // Check if user exists in localStorage
                let users = JSON.parse(localStorage.getItem('users')) || {};
                
                if (users[username] && users[username].password === password) {
                    // Successful login with stored user
                    handleSuccessfulLogin(username);
                } else {
                    // Invalid credentials
                    passwordError.textContent = 'Invalid username or password';
                    passwordError.style.display = 'block';
                }
            }
        });

        function handleSuccessfulLogin(username) {
            // Get or create user data in localStorage
            let users = JSON.parse(localStorage.getItem('users')) || {};
            
            if (!users[username]) {
                // New user
                users[username] = {
                    username: username,
                    displayName: username.charAt(0).toUpperCase() + username.slice(1),
                    accountCreated: new Date().toLocaleDateString(),
                    lastLogin: null,
                    password: passwordInput.value // In a real app, passwords should be hashed
                };
            } else {
                // Update last login for existing user
                users[username].lastLogin = new Date().toISOString();
            }
            
            // Save updated user data
            localStorage.setItem('users', JSON.stringify(users));
            
            // Set current user
            localStorage.setItem('currentUser', JSON.stringify(users[username]));
            
            // Show dashboard
            showDashboard(users[username]);
            
            // Load saved notes for this user
            const savedNotes = localStorage.getItem(`notes_${username}`);
            if (savedNotes) {
                personalNotes.value = savedNotes;
            }
        }

        // Logout functionality
        logoutBtn.addEventListener('click', function() {
            localStorage.removeItem('currentUser');
            showLoginForm();
        });

        // Save notes functionality
        saveNotesBtn.addEventListener('click', function() {
            const currentUser = JSON.parse(localStorage.getItem('currentUser'));
            if (currentUser) {
                localStorage.setItem(`notes_${currentUser.username}`, personalNotes.value);
                
                // Show saved message
                savedMessage.style.display = 'block';
                setTimeout(function() {
                    savedMessage.style.display = 'none';
                }, 2000);
            }
        });

        // Show dashboard
        function showDashboard(user) {
            loginForm.style.display = 'none';
            dashboard.style.display = 'block';
            
            // Update user info
            userDisplayName.textContent = user.displayName;
            displayUsername.textContent = user.username;
            accountCreated.textContent = user.accountCreated;
            
            // Format and display last login
            if (user.lastLogin) {
                const lastLogin = new Date(user.lastLogin);
                lastLoginDate.textContent = lastLogin.toLocaleString();
            } else {
                lastLoginDate.textContent = 'This is your first login!';
            }
        }

        // Show login form
        function showLoginForm() {
            dashboard.style.display = 'none';
            loginForm.style.display = 'block';
            
            // Clear form
            usernameInput.value = '';
            passwordInput.value = '';
            usernameError.style.display = 'none';
            passwordError.style.display = 'none';
        }

        // Allow login with Enter key
        passwordInput.addEventListener('keypress', function(e) {
            if (e.key === 'Enter') {
                loginBtn.click();
            }
        });
    </script>
</body>
</html>
