<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NexusBank | Secure Banking Solutions</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #0056b3;
            --secondary: #003366;
            --accent: #00a896;
            --light: #f8f9fa;
            --dark: #212529;
            --success: #28a745;
            --warning: #ffc107;
            --danger: #dc3545;
            --shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            --transition: all 0.3s ease;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f0f4f8;
            color: var(--dark);
            line-height: 1.6;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        /* Header Styles */
        header {
            background: linear-gradient(135deg, var(--secondary), var(--primary));
            color: white;
            padding: 1rem 0;
            box-shadow: var(--shadow);
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .logo i {
            font-size: 2rem;
            color: var(--accent);
        }
        
        .logo h1 {
            font-size: 1.8rem;
            font-weight: 700;
        }
        
        nav ul {
            display: flex;
            list-style: none;
            gap: 1.5rem;
        }
        
        nav a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: var(--transition);
            padding: 0.5rem;
            border-radius: 4px;
        }
        
        nav a:hover, nav a.active {
            background-color: rgba(255, 255, 255, 0.1);
        }
        
        .auth-buttons {
            display: flex;
            gap: 0.5rem;
        }
        
        .btn {
            padding: 0.6rem 1.2rem;
            border: none;
            border-radius: 4px;
            font-weight: 500;
            cursor: pointer;
            transition: var(--transition);
            text-decoration: none;
            display: inline-block;
            text-align: center;
        }
        
        .btn-primary {
            background-color: var(--accent);
            color: white;
        }
        
        .btn-outline {
            background-color: transparent;
            border: 1px solid white;
            color: white;
        }
        
        .btn:hover {
            transform: translateY(-2px);
            box-shadow: var(--shadow);
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 51, 102, 0.9), rgba(0, 86, 179, 0.9)), url('https://images.unsplash.com/photo-1601597111158-2fceff292cdc?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1770&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 5rem 0;
            text-align: center;
        }
        
        .hero h2 {
            font-size: 3rem;
            margin-bottom: 1rem;
            font-weight: 700;
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 2rem;
        }
        
        .hero-buttons {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-top: 2rem;
        }
        
        /* Services Section */
        .services {
            padding: 5rem 0;
            background-color: white;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            color: var(--secondary);
            margin-bottom: 1rem;
        }
        
        .section-title p {
            color: #666;
            max-width: 700px;
            margin: 0 auto;
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .service-card {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
        }
        
        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        .service-icon {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            height: 150px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .service-icon i {
            font-size: 4rem;
            color: white;
        }
        
        .service-content {
            padding: 1.5rem;
        }
        
        .service-content h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--secondary);
        }
        
        /* Dashboard Section */
        .dashboard {
            padding: 5rem 0;
            background-color: #f0f4f8;
        }
        
        .dashboard-container {
            display: grid;
            grid-template-columns: 1fr 2fr;
            gap: 2rem;
        }
        
        .user-profile {
            background: white;
            border-radius: 8px;
            box-shadow: var(--shadow);
            padding: 2rem;
            text-align: center;
        }
        
        .user-avatar {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            background: var(--light);
            margin: 0 auto 1rem;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
            color: var(--primary);
            border: 3px solid var(--accent);
        }
        
        .user-details {
            margin: 1.5rem 0;
        }
        
        .user-details h3 {
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
        }
        
        .accounts-summary {
            background: white;
            border-radius: 8px;
            box-shadow: var(--shadow);
            padding: 2rem;
        }
        
        .accounts-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1.5rem;
        }
        
        .accounts-header h2 {
            color: var(--secondary);
        }
        
        .account-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
        }
        
        .account-card {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            border-radius: 8px;
            padding: 1.5rem;
            transition: var(--transition);
        }
        
        .account-card:hover {
            transform: translateY(-5px);
        }
        
        .account-type {
            font-size: 0.9rem;
            opacity: 0.8;
            margin-bottom: 0.5rem;
        }
        
        .account-balance {
            font-size: 2rem;
            font-weight: 700;
            margin-bottom: 1rem;
        }
        
        .account-number {
            font-size: 0.9rem;
            letter-spacing: 1px;
            margin-bottom: 1.5rem;
        }
        
        .quick-actions {
            display: flex;
            gap: 0.5rem;
        }
        
        .quick-btn {
            flex: 1;
            background: rgba(255, 255, 255, 0.2);
            border: none;
            color: white;
            padding: 0.5rem;
            border-radius: 4px;
            cursor: pointer;
            transition: var(--transition);
        }
        
        .quick-btn:hover {
            background: rgba(255, 255, 255, 0.3);
        }
        
        /* Transactions Section */
        .transactions {
            margin-top: 2rem;
        }
        
        .transactions-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1rem;
        }
        
        .transactions-list {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: var(--shadow);
        }
        
        .transaction-item {
            display: grid;
            grid-template-columns: 50px 1fr auto;
            gap: 1rem;
            padding: 1rem;
            border-bottom: 1px solid #eee;
            align-items: center;
        }
        
        .transaction-item:last-child {
            border-bottom: none;
        }
        
        .transaction-icon {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: var(--light);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary);
        }
        
        .transaction-details h4 {
            margin-bottom: 0.25rem;
        }
        
        .transaction-date {
            font-size: 0.8rem;
            color: #666;
        }
        
        .transaction-amount {
            font-weight: 700;
        }
        
        .transaction-amount.income {
            color: var(--success);
        }
        
        .transaction-amount.expense {
            color: var(--danger);
        }
        
        /* Support Section */
        .support {
            padding: 5rem 0;
            background: linear-gradient(135deg, var(--secondary), var(--primary));
            color: white;
        }
        
        .support-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
        }
        
        .support-info h2 {
            font-size: 2.5rem;
            margin-bottom: 1.5rem;
        }
        
        .contact-methods {
            margin-top: 2rem;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            gap: 1rem;
            margin-bottom: 1.5rem;
        }
        
        .contact-icon {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
        }
        
        .contact-form {
            background: rgba(255, 255, 255, 0.1);
            padding: 2rem;
            border-radius: 8px;
            backdrop-filter: blur(10px);
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
        }
        
        .form-control {
            width: 100%;
            padding: 0.8rem;
            border: none;
            border-radius: 4px;
            background: rgba(255, 255, 255, 0.9);
        }
        
        textarea.form-control {
            min-height: 120px;
            resize: vertical;
        }
        
        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 3rem 0 1rem;
        }
        
        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }
        
        .footer-column h3 {
            font-size: 1.2rem;
            margin-bottom: 1.5rem;
            position: relative;
            padding-bottom: 0.5rem;
        }
        
        .footer-column h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 2px;
            background-color: var(--accent);
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 0.8rem;
        }
        
        .footer-links a {
            color: #ccc;
            text-decoration: none;
            transition: var(--transition);
        }
        
        .footer-links a:hover {
            color: white;
            padding-left: 5px;
        }
        
        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 1rem;
        }
        
        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.1);
            color: white;
            transition: var(--transition);
        }
        
        .social-links a:hover {
            background: var(--accent);
            transform: translateY(-3px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #aaa;
            font-size: 0.9rem;
        }
        
        /* Responsive */
        @media (max-width: 992px) {
            .dashboard-container,
            .support-container {
                grid-template-columns: 1fr;
            }
            
            nav ul {
                gap: 0.8rem;
            }
        }
        
        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
                gap: 1rem;
            }
            
            nav ul {
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .hero h2 {
                font-size: 2.2rem;
            }
            
            .hero-buttons {
                flex-direction: column;
                align-items: center;
            }
        }
        
        /* Login Modal */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            z-index: 2000;
            align-items: center;
            justify-content: center;
        }
        
        .modal-content {
            background: white;
            border-radius: 8px;
            width: 100%;
            max-width: 400px;
            overflow: hidden;
            animation: modalOpen 0.4s ease;
        }
        
        @keyframes modalOpen {
            from { opacity: 0; transform: translateY(-50px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .modal-header {
            background: var(--primary);
            color: white;
            padding: 1.5rem;
            text-align: center;
        }
        
        .modal-header h3 {
            font-size: 1.5rem;
        }
        
        .modal-body {
            padding: 2rem;
        }
        
        .close-modal {
            position: absolute;
            top: 15px;
            right: 15px;
            font-size: 1.5rem;
            color: white;
            cursor: pointer;
        }
        
        /* Demo notification */
        .demo-notification {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: var(--dark);
            color: white;
            padding: 15px 20px;
            border-radius: 8px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
            z-index: 3000;
            display: flex;
            align-items: center;
            gap: 10px;
            animation: slideIn 0.5s ease;
        }
        
        @keyframes slideIn {
            from { transform: translateX(100%); opacity: 0; }
            to { transform: translateX(0); opacity: 1; }
        }
        
        .close-notification {
            cursor: pointer;
            font-size: 1.2rem;
        }
    </style>
</head>
<body>
    <!-- Demo Notification -->
    <div class="demo-notification">
        <span>Staging Environment: nexusbank-staging.capital</span>
        <span class="close-notification" onclick="this.parentElement.style.display='none'">&times;</span>
    </div>

    <!-- Header -->
    <header>
        <div class="container header-container">
            <div class="logo">
                <i class="fas fa-university"></i>
                <h1>NexusBank</h1>
            </div>
            
            <nav>
                <ul>
                    <li><a href="#" class="active">Home</a></li>
                    <li><a href="#">Accounts</a></li>
                    <li><a href="#">Transfer</a></li>
                    <li><a href="#">Payments</a></li>
                    <li><a href="#">Investments</a></li>
                    <li><a href="#">Loans</a></li>
                    <li><a href="#">Support</a></li>
                </ul>
            </nav>
            
            <div class="auth-buttons">
                <button class="btn btn-outline" onclick="openLogin()">Login</button>
                <button class="btn btn-primary" onclick="openRegister()">Register</button>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <h2>Banking Made Simple, Secure, and Smart</h2>
            <p>Experience the future of banking with NexusBank - where cutting-edge technology meets personalized financial solutions for all your banking needs.</p>
            <div class="hero-buttons">
                <button class="btn btn-primary">Open an Account</button>
                <button class="btn btn-outline">Learn More</button>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section class="services">
        <div class="container">
            <div class="section-title">
                <h2>Our Banking Services</h2>
                <p>Discover a wide range of financial services designed to help you achieve your financial goals</p>
            </div>
            
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-piggy-bank"></i>
                    </div>
                    <div class="service-content">
                        <h3>Savings Accounts</h3>
                        <p>Grow your savings with competitive interest rates and flexible options tailored to your needs.</p>
                    </div>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-credit-card"></i>
                    </div>
                    <div class="service-content">
                        <h3>Credit Cards</h3>
                        <p>Choose from our range of credit cards with rewards, cashback, and low interest rates.</p>
                    </div>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-home"></i>
                    </div>
                    <div class="service-content">
                        <h3>Home Loans</h3>
                        <p>Make your dream home a reality with our flexible home loan solutions and expert guidance.</p>
                    </div>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <div class="service-content">
                        <h3>Investment Solutions</h3>
                        <p>Grow your wealth with our diverse investment portfolios and expert financial advice.</p>
                    </div>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-shield-alt"></i>
                    </div>
                    <div class="service-content">
                        <h3>Insurance</h3>
                        <p>Protect what matters most with our comprehensive insurance plans for life, health, and property.</p>
                    </div>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-globe"></i>
                    </div>
                    <div class="service-content">
                        <h3>International Banking</h3>
                        <p>Seamless global banking with multi-currency accounts and international money transfers.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Dashboard Section -->
    <section class="dashboard">
        <div class="container">
            <div class="dashboard-container">
                <div class="user-profile">
                    <div class="user-avatar">
                        <i class="fas fa-user"></i>
                    </div>
                    <div class="user-details">
                        <h3>Alex Johnson</h3>
                        <p>Premium Banking Member</p>
                        <p>Member since: Jan 2020</p>
                    </div>
                    <button class="btn btn-primary" style="width: 100%;">View Profile</button>
                    <div class="quick-links" style="margin-top: 1.5rem;">
                        <h4 style="margin-bottom: 1rem; text-align: left;">Quick Links</h4>
                        <ul style="list-style: none; text-align: left;">
                            <li style="margin-bottom: 0.8rem;"><a href="#" style="color: var(--primary); text-decoration: none;"><i class="fas fa-file-invoice-dollar"></i> Statements</a></li>
                            <li style="margin-bottom: 0.8rem;"><a href="#" style="color: var(--primary); text-decoration: none;"><i class="fas fa-cog"></i> Settings</a></li>
                            <li style="margin-bottom: 0.8rem;"><a href="#" style="color: var(--primary); text-decoration: none;"><i class="fas fa-shield-alt"></i> Security</a></li>
                            <li><a href="#" style="color: var(--primary); text-decoration: none;"><i class="fas fa-question-circle"></i> Help Center</a></li>
                        </ul>
                    </div>
                </div>
                
                <div class="accounts-summary">
                    <div class="accounts-header">
                        <h2>My Accounts</h2>
                        <button class="btn btn-primary">+ Add Account</button>
                    </div>
                    
                    <div class="account-cards">
                        <div class="account-card">
                            <div class="account-type">Checking Account</div>
                            <div class="account-balance">$12,568.42</div>
                            <div class="account-number">**** **** **** 1234</div>
                            <div class="quick-actions">
                                <button class="quick-btn"><i class="fas fa-exchange-alt"></i></button>
                                <button class="quick-btn"><i class="fas fa-money-bill-wave"></i></button>
                                <button class="quick-btn"><i class="fas fa-history"></i></button>
                            </div>
                        </div>
                        
                        <div class="account-card">
                            <div class="account-type">Savings Account</div>
                            <div class="account-balance">$45,789.31</div>
                            <div class="account-number">**** **** **** 5678</div>
                            <div class="quick-actions">
                                <button class="quick-btn"><i class="fas fa-exchange-alt"></i></button>
                                <button class="quick-btn"><i class="fas fa-money-bill-wave"></i></button>
                                <button class="quick-btn"><i class="fas fa-history"></i></button>
                            </div>
                        </div>
                    </div>
                    
                    <div class="transactions">
                        <div class="transactions-header">
                            <h3>Recent Transactions</h3>
                            <a href="#" style="color: var(--primary); text-decoration: none;">View All</a>
                        </div>
                        
                        <div class="transactions-list">
                            <div class="transaction-item">
                                <div class="transaction-icon">
                                    <i class="fas fa-shopping-cart"></i>
                                </div>
                                <div class="transaction-details">
                                    <h4>Amazon Purchase</h4>
                                    <div class="transaction-date">Today, 10:30 AM</div>
                                </div>
                                <div class="transaction-amount expense">-$89.99</div>
                            </div>
                            
                            <div class="transaction-item">
                                <div class="transaction-icon">
                                    <i class="fas fa-arrow-down"></i>
                                </div>
                                <div class="transaction-details">
                                    <h4>Salary Deposit</h4>
                                    <div class="transaction-date">May 1, 2023</div>
                                </div>
                                <div class="transaction-amount income">+$5,200.00</div>
                            </div>
                            
                            <div class="transaction-item">
                                <div class="transaction-icon">
                                    <i class="fas fa-home"></i>
                                </div>
                                <div class="transaction-details">
                                    <h4>Mortgage Payment</h4>
                                    <div class="transaction-date">Apr 28, 2023</div>
                                </div>
                                <div class="transaction-amount expense">-$1,850.00</div>
                            </div>
                            
                            <div class="transaction-item">
                                <div class="transaction-icon">
                                    <i class="fas fa-utensils"></i>
                                </div>
                                <div class="transaction-details">
                                    <h4>Restaurant Payment</h4>
                                    <div class="transaction-date">Apr 26, 2023</div>
                                </div>
                                <div class="transaction-amount expense">-$64.30</div>
                            </div>
                            
                            <div class="transaction-item">
                                <div class="transaction-icon">
                                    <i class="fas fa-arrow-up"></i>
                                </div>
                                <div class="transaction-details">
                                    <h4>Transfer to Savings</h4>
                                    <div class="transaction-date">Apr 25, 2023</div>
                                </div>
                                <div class="transaction-amount expense">-$500.00</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Support Section -->
    <section class="support">
        <div class="container">
            <div class="support-container">
                <div class="support-info">
                    <h2>We're Here to Help</h2>
                    <p>Our dedicated customer support team is available 24/7 to assist you with any questions or concerns you may have about your accounts, transactions, or our services.</p>
                    
                    <div class="contact-methods">
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-phone"></i>
                            </div>
                            <div>
                                <h3>Phone Support</h3>
                                <p>1-800-NEXUS-BANK (1-800-639-8722)</p>
                            </div>
                        </div>
                        
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-envelope"></i>
                            </div>
                            <div>
                                <h3>Email Support</h3>
                                <p>support@nexusbank.capital</p>
                            </div>
                        </div>
                        
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-comments"></i>
                            </div>
                            <div>
                                <h3>Live Chat</h3>
                                <p>Available 24/7 through our website or mobile app</p>
                            </div>
                        </div>
                        
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-map-marker-alt"></i>
                            </div>
                            <div>
                                <h3>Branch Locator</h3>
                                <p>Find the nearest NexusBank branch or ATM</p>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="contact-form">
                    <h3>Send us a Message</h3>
                    <form>
                        <div class="form-group">
                            <label for="name">Full Name</label>
                            <input type="text" id="name" class="form-control" placeholder="Enter your name">
                        </div>
                        
                        <div class="form-group">
                            <label for="email">Email Address</label>
                            <input type="email" id="email" class="form-control" placeholder="Enter your email">
                        </div>
                        
                        <div class="form-group">
                            <label for="subject">Subject</label>
                            <input type="text" id="subject" class="form-control" placeholder="What is this regarding?">
                        </div>
                        
                        <div class="form-group">
                            <label for="message">Message</label>
                            <textarea id="message" class="form-control" placeholder="How can we help you?"></textarea>
                        </div>
                        
                        <button type="submit" class="btn btn-primary" style="width: 100%;">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-grid">
                <div class="footer-column">
                    <div class="logo" style="margin-bottom: 1.5rem;">
                        <i class="fas fa-university"></i>
                        <h1>NexusBank</h1>
                    </div>
                    <p style="color: #ccc; margin-bottom: 1.5rem;">Your trusted financial partner for all banking needs, offering innovative solutions and exceptional service.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
                
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul class="footer-links">
                        <li><a href="#">Personal Banking</a></li>
                        <li><a href="#">Business Banking</a></li>
                        <li><a href="#">Loans & Mortgages</a></li>
                        <li><a href="#">Investments</a></li>
                        <li><a href="#">Credit Cards</a></li>
                        <li><a href="#">Insurance</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3>Services</h3>
                    <ul class="footer-links">
                        <li><a href="#">Online Banking</a></li>
                        <li><a href="#">Mobile Banking</a></li>
                        <li><a href="#">Wealth Management</a></li>
                        <li><a href="#">International Services</a></li>
                        <li><a href="#">Account Services</a></li>
                        <li><a href="#">Security Center</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3>Legal</h3>
                    <ul class="footer-links">
                        <li><a href="#">Privacy Policy</a></li>
                        <li><a href="#">Terms of Service</a></li>
                        <li><a href="#">Disclosures</a></li>
                        <li><a href="#">Compliance</a></li>
                        <li><a href="#">Security</a></li>
                        <li><a href="#">Accessibility</a></li>
                    </ul>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2023 NexusBank Capital. All rights reserved. | FDIC insured | Equal Housing Lender</p>
                <p style="margin-top: 0.5rem;">Staging Environment: nexusbank-staging.capital | Production: nexusbank.capital</p>
            </div>
        </div>
    </footer>

    <!-- Login Modal -->
    <div class="modal" id="loginModal">
        <div class="modal-content">
            <div class="modal-header">
                <h3>Login to Your Account</h3>
                <span class="close-modal" onclick="closeModal()">&times;</span>
            </div>
            <div class="modal-body">
                <form>
                    <div class="form-group">
                        <label for="login-email">Email Address</label>
                        <input type="email" id="login-email" class="form-control" placeholder="Enter your email">
                    </div>
                    
                    <div class="form-group">
                        <label for="login-password">Password</label>
                        <input type="password" id="login-password" class="form-control" placeholder="Enter your password">
                    </div>
                    
                    <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 1.5rem;">
                        <div>
                            <input type="checkbox" id="remember">
                            <label for="remember">Remember me</label>
                        </div>
                        <a href="#" style="color: var(--primary); text-decoration: none;">Forgot Password?</a>
                    </div>
                    
                    <button type="submit" class="btn btn-primary" style="width: 100%;">Login</button>
                    
                    <p style="text-align: center; margin-top: 1.5rem;">
                        Don't have an account? <a href="#" style="color: var(--primary); text-decoration: none;" onclick="openRegister()">Register now</a>
                    </p>
                </form>
            </div>
        </div>
    </div>

    <script>
        // Modal functions
        function openLogin() {
            document.getElementById('loginModal').style.display = 'flex';
        }
        
        function openRegister() {
            alert('Registration page would open here. This is a frontend demo.');
        }
        
        function closeModal() {
            document.getElementById('loginModal').style.display = 'none';
        }
        
        // Close modal when clicking outside
        window.onclick = function(event) {
            const modal = document.getElementById('loginModal');
            if (event.target === modal) {
                closeModal();
            }
        }
        
        // Simulate backend functionality
        document.addEventListener('DOMContentLoaded', function() {
            // Add current year to footer
            document.getElementById('currentYear').textContent = new Date().getFullYear();
            
            // Simulate account balance update
            setInterval(() => {
                const balanceElement = document.querySelector('.account-balance');
                if (balanceElement) {
                    const currentBalance = parseFloat(balanceElement.textContent.replace('$', '').replace(',', ''));
                    const newBalance = currentBalance + Math.random() * 10;
                    balanceElement.textContent = '$' + newBalance.toFixed(2);
                }
            }, 10000);
        });
    </script>
</body>
</html>
