# AI-Powered Insurance for India’s Gig Economy
AI-Powered Insurance for India’s Gig Economy – Income Protection for Delivery Partners
About the Project
In today’s fast-growing gig economy, delivery partners (like Swiggy, Zomato, Zepto workers) play a very important role. But one major issue they face is loss of income due to external factors like heavy rain, pollution, or sudden curfews. Through this project, we are trying to build a simple AI-based insurance system that helps delivery workers get compensated when they are unable to work due to such conditions.

Target User (Persona)
We considered a typical delivery partner:

Name: Ravi
Works for: Swiggy
Location: Vijayawada
Problem: During heavy rain or high pollution days, he cannot deliver orders and loses his daily earnings Our solution is designed mainly for users like him.
Our Idea
We are building a parametric insurance platform, where:

The user pays a small weekly premium
If a predefined condition (like heavy rain) occurs,
The system automatically gives compensation (no need to manually apply for claims)
How the System Works
User signs up on the platform
Basic details like location and work type are collected
The system calculates a weekly premium based on risk
External data (like weather) is monitored
If a trigger condition is met (e.g., heavy rainfall),
Claim is automatically processed and payout is given
Weekly Premium Model
We are using a weekly pricing system because gig workers usually earn weekly. Premium depends on:

Area (high-risk or low-risk zone)
Weather conditions
Past disruption frequency
Example:

Low risk area → ₹20/week
Medium risk → ₹30–40/week
High risk → ₹50/week
Parametric Triggers (Automatic Conditions)
Some example triggers we are considering:

Rainfall exceeds a certain limit
AQI (pollution level) is very high
Flood alerts in the area
Government curfew When these happen, the system directly triggers payout.
Use of AI/ML
We are planning to use basic AI/ML for:

Calculating risk and premium dynamically
Predicting possible disruptions
Detecting fraud (like fake claims or location mismatch)
Platform Choice
We chose to develop a web application for Phase 1 because:

It is accessible on any device (mobile, laptop)
No installation is required
Faster to develop within limited time
Easy to maintain and update
In future phases, we plan to expand this into a mobile application for better user experience and real-time notifications.
Tech Stack (Planned)
Frontend: HTML, CSS, JavaScript
Backend: Python (Flask)
Database: SQLite / MongoDB
APIs: Weather API (or simulated data)
Development Plan (Phase 1)
Understanding problem and user needs
Designing workflow
Planning system architecture
Setting up GitHub repository
Future Scope
In the next phases, we plan to:

Build full working system
Add automated claims and payouts
Create dashboard for users and admin
Improve AI models
Frontend Overview
We have designed a simple and user-friendly web interface for delivery partners to interact with the system.

Key Features of Frontend:
User Registration Form (Name, Location, Platform)
Weekly Premium Display based on user details
Simulation of external triggers (Rain, Pollution)
Automatic claim status updates
Clean and simple UI for easy usage
Screens Included:
Registration Page – User enters details
Premium Display Section – Shows calculated weekly premium
Trigger Simulation – Buttons to simulate rain/pollution events
Status Section – Displays claim and payout information
Technologies Used:
HTML for structure
CSS for styling
JavaScript for dynamic behavior
How to Run Frontend:
Download the project files
Open index.html in any web browser
Interact with the form and buttons
### Frontend Code

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GigGuard | Income Protection</title>
    <style>
        :root {
            --primary: #2563eb;
            --success: #10b981;
            --warning: #f59e0b;
            --danger: #ef4444;
            --dark: #1f2937;
            --light: #f3f4f6;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--light);
            margin: 0;
            padding: 20px;
            display: flex;
            justify-content: center;
        }

        .app-container {
            max-width: 450px;
            width: 100%;
            background: white;
            border-radius: 1.5rem;
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
            overflow: hidden;
        }

        .header {
            background: var(--primary);
            color: white;
            padding: 2rem 1.5rem;
            text-align: center;
        }

        .content { padding: 1.5rem; }

        .card {
            border: 1px solid #e5e7eb;
            border-radius: 1rem;
            padding: 1.2rem;
            margin-bottom: 1.5rem;
        }

        .hidden { display: none; }

        /* Form Styling */
        input, select {
            width: 100%;
            padding: 0.8rem;
            margin: 0.5rem 0 1.2rem;
            border: 1px solid #d1d5db;
            border-radius: 0.5rem;
            box-sizing: border-box;
        }

        button {
            width: 100%;
            padding: 1rem;
            border: none;
            border-radius: 0.5rem;
            font-weight: bold;
            cursor: pointer;
            transition: opacity 0.2s;
        }

        .btn-primary { background: var(--primary); color: white; }
        .btn-trigger { background: var(--dark); color: white; margin-top: 10px; }

        /* Status Badge */
        .badge {
            display: inline-block;
            padding: 0.25rem 0.75rem;
            border-radius: 999px;
            font-size: 0.875rem;
            font-weight: 600;
        }

        .badge-active { background: #dcfce7; color: #166534; }
        .badge-alert { background: #fee2e2; color: #991b1b; }

        .payout-alert {
            background: #ecfdf5;
            border-left: 5px solid var(--success);
            padding: 1rem;
            margin-top: 1rem;
            animation: slideIn 0.5s ease-out;
        }

        @keyframes slideIn {
            from { transform: translateY(20px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }
    </style>
</head>
<body>

<div class="app-container">
    <div class="header">
        <h1 style="margin:0">GigGuard AI</h1>
        <p style="margin:5px 0 0; opacity: 0.9;">Rain or Shine, You Get Paid.</p>
    </div>

    <div class="content">
        <div id="registration-screen">
            <h3>Register for Protection</h3>
            <label>Full Name</label>
            <input type="text" id="userName" placeholder="e.g. Ravi Kumar">
            
            <label>Work Platform</label>
            <select id="platform">
                <option value="Swiggy">Swiggy</option>
                <option value="Zomato">Zomato</option>
                <option value="Zepto">Zepto</option>
            </select>

            <label>Location (Risk Zone)</label>
            <select id="location">
                <option value="20">Vijayawada Central (Low Risk)</option>
                <option value="35">One Town (Medium Risk)</option>
                <option value="50">Benz Circle (High Risk Zone)</option>
            </select>

            <button class="btn-primary" onclick="showDashboard()">Calculate Premium</button>
        </div>

        <div id="dashboard-screen" class="hidden">
            <div class="card">
                <p style="color: #6b7280; margin: 0;">Welcome back, <span id="dispName" style="color: var(--dark); font-weight:bold;"></span></p>
                <h2 id="premiumAmt" style="margin: 10px 0; color: var(--primary);">₹0 / week</h2>
                <span class="badge badge-active">● Active Policy</span>
            </div>

            <div class="card">
                <h3>Live Weather Monitor</h3>
                <p id="weather-status">☀️ Clear Skies in <span id="dispLoc"></span></p>
                <p style="font-size: 0.8rem; color: #6b7280;">AI is monitoring local rainfall and AQI sensors...</p>
            </div>

            <div style="margin-top: 2rem;">
                <p style="font-weight: bold; color: var(--danger);">Admin Simulation (Test Triggers):</p>
                <button class="btn-trigger" onclick="simulateTrigger('Heavy Rain', '₹150')">🌧️ Simulate Heavy Rain</button>
                <button class="btn-trigger" onclick="simulateTrigger('Toxic AQI', '₹100')">😷 Simulate High Pollution</button>
            </div>

            <div id="payout-box" class="payout-alert hidden">
                <strong id="payout-reason"></strong>
                <p style="margin: 5px 0;">A compensation of <b id="payout-amt"></b> has been sent to your wallet. No action needed!</p>
            </div>
        </div>
    </div>
</div>

<script>
    function showDashboard() {
        const name = document.getElementById('userName').value;
        const premium = document.getElementById('location').value;
        const locationText = document.getElementById('location').options[document.getElementById('location').selectedIndex].text;

        if(!name) { alert("Please enter your name"); return; }

        // Update UI
        document.getElementById('dispName').innerText = name;
        document.getElementById('dispLoc').innerText = locationText.split('(')[0];
        document.getElementById('premiumAmt').innerText = `₹${premium} / week`;

        // Switch Screens
        document.getElementById('registration-screen').classList.add('hidden');
        document.getElementById('dashboard-screen').classList.remove('hidden');
    }

    function simulateTrigger(reason, amount) {
        const weatherStatus = document.getElementById('weather-status');
        const payoutBox = document.getElementById('payout-box');

        // Update Status to Alert
        weatherStatus.innerHTML = `<span style="color: var(--danger)">⚠️ ${reason} Detected!</span>`;
        
        // Show Payout
        document.getElementById('payout-reason').innerText = `${reason} Compensation Triggered`;
        document.getElementById('payout-amt').innerText = amount;
        payoutBox.classList.remove('hidden');

        // Reset after 5 seconds
        setTimeout(() => {
            weatherStatus.innerHTML = `☀️ Clear Skies`;
            payoutBox.classList.add('hidden');
        }, 8000);
    }
</script>

</body>
</html>
