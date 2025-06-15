# alprazolam-webpage
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Alprazolam Monograph - UMT School of Pharmacy</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script src="https://translate.google.com/translate_a/element.js?cb=googleTranslateElementInit"></script>
    <style>
        :root {
            --primary-black: #000;
            --primary-white: #fff;
            --light-gray: #f5f5f5;
            --medium-gray: #e0e0e0;
            --dark-gray: #333;
            --border-gray: #ccc;
            --accent-color: #2c3e50;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--primary-white);
            color: var(--primary-black);
            line-height: 1.6;
            overflow-x: hidden;
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header Styles */
        header {
            background: linear-gradient(135deg, var(--accent-color) 0%, #1a2530 100%);
            color: var(--primary-white);
            padding: 15px 0;
            position: relative;
            box-shadow: 0 4px 12px rgba(0,0,0,0.2);
            animation: headerSlide 0.8s ease-out;
        }
        
        @keyframes headerSlide {
            0% { transform: translateY(-100%); }
            100% { transform: translateY(0); }
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo-container {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .logo {
            width: 60px;
            height: 60px;
            background: linear-gradient(45deg, #3498db, #2c3e50);
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            font-weight: bold;
            color: var(--primary-white);
            font-size: 24px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
            animation: logoSpin 10s linear infinite;
        }
        
        @keyframes logoSpin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        
        .header-text {
            font-size: 22px;
            font-weight: 600;
            letter-spacing: 1px;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.3);
        }
        
        .header-right {
            display: flex;
            gap: 15px;
            align-items: center;
        }
        
        .options-btn {
            background: transparent;
            color: var(--primary-white);
            border: 2px solid var(--primary-white);
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            transition: all 0.3s ease;
            border-radius: 4px;
            display: flex;
            align-items: center;
            gap: 8px;
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(255,255,255,0.4); }
            70% { box-shadow: 0 0 0 10px rgba(255,255,255,0); }
            100% { box-shadow: 0 0 0 0 rgba(255,255,255,0); }
        }
        
        .options-btn:hover {
            background-color: var(--primary-white);
            color: var(--accent-color);
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
            animation: none;
        }
        
        .translate-container {
            background: rgba(255, 255, 255, 0.2);
            border-radius: 4px;
            padding: 5px;
            min-width: 150px;
        }
        
        /* Navigation Bar */
        .nav-bar {
            background-color: var(--primary-white);
            padding: 15px 0;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .nav-links {
            display: flex;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
        }
        
        .nav-btn {
            background: var(--light-gray);
            color: var(--dark-gray);
            border: none;
            padding: 10px 20px;
            border-radius: 30px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 500;
            display: flex;
            align-items: center;
            gap: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        
        .nav-btn:hover {
            background: var(--accent-color);
            color: var(--primary-white);
            transform: translateY(-3px);
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
        }
        
        /* Main Content Styles */
        .drug-header {
            text-align: center;
            padding: 40px 0 20px;
            margin-bottom: 30px;
            border-radius: 10px;
            margin-top: 20px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            background: linear-gradient(135deg, #ffffff 0%, #f1f3f5 100%);
            animation: fadeIn 1s ease-out;
        }
        
        @keyframes fadeIn {
            0% { opacity: 0; transform: translateY(20px); }
            100% { opacity: 1; transform: translateY(0); }
        }
        
        .drug-name {
            font-size: 42px;
            margin-bottom: 15px;
            letter-spacing: 1px;
            color: var(--accent-color);
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
            animation: colorShift 6s infinite alternate;
        }
        
        @keyframes colorShift {
            0% { color: var(--accent-color); }
            50% { color: #2980b9; }
            100% { color: var(--accent-color); }
        }
        
        .pronunciation {
            font-size: 18px;
            color: var(--dark-gray);
            font-style: italic;
            margin-bottom: 25px;
        }
        
        .chemical-formula {
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            padding: 25px;
            border-radius: 8px;
            margin: 30px 0;
            border: 1px solid var(--border-gray);
            box-shadow: 0 4px 12px rgba(0,0,0,0.08);
            animation: slideInLeft 0.8s ease-out;
        }
        
        @keyframes slideInLeft {
            0% { transform: translateX(-100px); opacity: 0; }
            100% { transform: translateX(0); opacity: 1; }
        }
        
        .formula-container {
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 20px;
        }
        
        .formula-text {
            flex: 1;
        }
        
        .formula-image {
            flex: 0 0 200px;
            height: 200px;
            background-color: var(--medium-gray);
            border-radius: 8px;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 14px;
            color: var(--dark-gray);
            overflow: hidden;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            background: linear-gradient(45deg, #2c3e50, #4a6491);
            position: relative;
        }
        
        .formula-image::before {
            content: "C₁₇H₁₄ClN₄";
            position: absolute;
            font-size: 24px;
            font-weight: bold;
            color: rgba(255,255,255,0.8);
            text-shadow: 0 0 10px rgba(0,0,0,0.3);
        }
        
        section {
            margin: 40px 0;
            padding: 20px;
            border-radius: 8px;
            background: var(--primary-white);
            box-shadow: 0 4px 15px rgba(0,0,0,0.08);
            transition: transform 0.3s ease;
            border-left: 4px solid var(--accent-color);
            opacity: 0;
            transform: translateY(30px);
            animation: sectionAppear 0.8s forwards;
        }
        
        @keyframes sectionAppear {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        section:nth-child(1) { animation-delay: 0.1s; }
        section:nth-child(2) { animation-delay: 0.2s; }
        section:nth-child(3) { animation-delay: 0.3s; }
        section:nth-child(4) { animation-delay: 0.4s; }
        section:nth-child(5) { animation-delay: 0.5s; }
        section:nth-child(6) { animation-delay: 0.6s; }
        section:nth-child(7) { animation-delay: 0.7s; }
        section:nth-child(8) { animation-delay: 0.8s; }
        section:nth-child(9) { animation-delay: 0.9s; }
        section:nth-child(10) { animation-delay: 1.0s; }
        section:nth-child(11) { animation-delay: 1.1s; }
        
        section:hover {
            transform: translateY(-5px);
            box-shadow: 0 6px 20px rgba(0,0,0,0.12);
        }
        
        h2 {
            font-size: 28px;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid var(--accent-color);
            display: inline-block;
            color: var(--accent-color);
        }
        
        h3 {
            font-size: 22px;
            margin: 25px 0 15px;
            color: var(--accent-color);
        }
        
        p {
            margin-bottom: 15px;
            font-size: 17px;
        }
        
        .highlight {
            background: linear-gradient(to right, #f8f9fa, #e9ecef);
            padding: 15px;
            border-left: 4px solid var(--accent-color);
            margin: 20px 0;
            font-size: 17px;
            border-radius: 4px;
            animation: highlightPulse 3s infinite;
        }
        
        @keyframes highlightPulse {
            0% { box-shadow: 0 0 0 0 rgba(44,62,80,0.2); }
            70% { box-shadow: 0 0 0 10px rgba(44,62,80,0); }
            100% { box-shadow: 0 0 0 0 rgba(44,62,80,0); }
        }
        
        ul {
            margin: 15px 0 15px 40px;
        }
        
        li {
            margin-bottom: 8px;
            font-size: 17px;
            position: relative;
            animation: listItemAppear 0.5s forwards;
            opacity: 0;
            transform: translateX(-20px);
        }
        
        @keyframes listItemAppear {
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }
        
        li:nth-child(1) { animation-delay: 0.1s; }
        li:nth-child(2) { animation-delay: 0.2s; }
        li:nth-child(3) { animation-delay: 0.3s; }
        li:nth-child(4) { animation-delay: 0.4s; }
        li:nth-child(5) { animation-delay: 0.5s; }
        li:nth-child(6) { animation-delay: 0.6s; }
        li:nth-child(7) { animation-delay: 0.7s; }
        li:nth-child(8) { animation-delay: 0.8s; }
        li:nth-child(9) { animation-delay: 0.9s; }
        li:nth-child(10) { animation-delay: 1.0s; }
        
        li:before {
            content: "•";
            color: var(--accent-color);
            font-weight: bold;
            position: absolute;
            left: -20px;
        }
        
        .dosing-section {
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            padding: 25px;
            border-radius: 8px;
            margin: 30px 0;
            border: 1px solid var(--border-gray);
            box-shadow: 0 4px 12px rgba(0,0,0,0.08);
            animation: slideInRight 0.8s ease-out;
        }
        
        @keyframes slideInRight {
            0% { transform: translateX(100px); opacity: 0; }
            100% { transform: translateX(0); opacity: 1; }
        }
        
        .dosing-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 25px;
        }
        
        .dosing-card {
            background-color: var(--primary-white);
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.08);
            transition: all 0.3s ease;
            border-top: 3px solid var(--accent-color);
            animation: cardAppear 0.6s ease-out;
        }
        
        @keyframes cardAppear {
            0% { transform: scale(0.9); opacity: 0; }
            100% { transform: scale(1); opacity: 1; }
        }
        
        .dosing-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 15px rgba(0,0,0,0.1);
        }
        
        .dosing-card h4 {
            font-size: 20px;
            margin-bottom: 15px;
            color: var(--accent-color);
            border-bottom: 1px solid var(--border-gray);
            padding-bottom: 8px;
        }
        
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
            background-color: var(--primary-white);
            box-shadow: 0 2px 10px rgba(0,0,0,0.08);
            border-radius: 8px;
            overflow: hidden;
            animation: fadeIn 0.8s ease-out;
        }
        
        th, td {
            border: 1px solid var(--border-gray);
            padding: 12px 15px;
            text-align: left;
        }
        
        th {
            background: var(--accent-color);
            color: var(--primary-white);
            font-weight: 600;
        }
        
        tr:nth-child(even) {
            background-color: #f9f9f9;
        }
        
        tr {
            animation: rowAppear 0.5s forwards;
            opacity: 0;
            transform: translateY(10px);
        }
        
        @keyframes rowAppear {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        tr:nth-child(1) { animation-delay: 0.1s; }
        tr:nth-child(2) { animation-delay: 0.2s; }
        tr:nth-child(3) { animation-delay: 0.3s; }
        tr:nth-child(4) { animation-delay: 0.4s; }
        tr:nth-child(5) { animation-delay: 0.5s; }
        tr:nth-child(6) { animation-delay: 0.6s; }
        
        .video-container {
            position: relative;
            width: 100%;
            padding-bottom: 56.25%; /* 16:9 Aspect Ratio */
            height: 0;
            margin: 20px 0;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 8px 20px rgba(0,0,0,0.2);
            animation: videoAppear 1s ease-out;
        }
        
        @keyframes videoAppear {
            0% { opacity: 0; transform: scale(0.9); }
            100% { opacity: 1; transform: scale(1); }
        }
        
        .video-container iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: none;
        }
        
        .references {
            margin-top: 40px;
            padding: 25px;
            border-radius: 8px;
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            box-shadow: 0 4px 12px rgba(0,0,0,0.08);
            animation: fadeIn 1s ease-out;
        }
        
        .references ol {
            margin-left: 25px;
        }
        
        .references li {
            margin-bottom: 10px;
        }
        
        .references a {
            color: var(--accent-color);
            text-decoration: none;
            border-bottom: 1px dotted var(--accent-color);
            transition: all 0.3s ease;
        }
        
        .references a:hover {
            border-bottom: 1px solid var(--accent-color);
            color: #1a5276;
        }
        
        footer {
            background: linear-gradient(135deg, var(--accent-color) 0%, #1a2530 100%);
            color: var(--primary-white);
            text-align: center;
            padding: 30px 0;
            margin-top: 50px;
            border-top: 4px solid #3498db;
            animation: footerAppear 0.8s ease-out;
        }
        
        @keyframes footerAppear {
            0% { opacity: 0; transform: translateY(50px); }
            100% { opacity: 1; transform: translateY(0); }
        }
        
        .footer-content {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }
        
        .language-notice {
            background: rgba(255, 255, 255, 0.1);
            padding: 15px;
            border-radius: 8px;
            margin: 20px 0;
            text-align: center;
            font-size: 14px;
            animation: pulse 3s infinite;
        }
        
        @media (max-width: 768px) {
            .dosing-grid {
                grid-template-columns: 1fr;
            }
            
            .formula-container {
                flex-direction: column;
            }
            
            .formula-image {
                width: 100%;
            }
            
            .nav-links {
                flex-direction: column;
                align-items: center;
            }
            
            .nav-btn {
                width: 90%;
                text-align: center;
            }
            
            .header-content {
                flex-direction: column;
                gap: 15px;
            }
            
            .header-right {
                width: 100%;
                justify-content: center;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container header-content">
            <div class="logo-container">
                <div class="logo">UMT</div>
                <div class="header-text">SCHOOL OF PHARMACY</div>
            </div>
            <div class="header-right">
                <div class="translate-container" id="google_translate_element"></div>
                <button class="options-btn">
                    <i class="fas fa-cog"></i> Options
                </button>
            </div>
        </div>
    </header>
    
    <div class="nav-bar">
        <div class="container">
            <div class="nav-links">
                <button class="nav-btn" onclick="scrollToSection('mechanism')">
                    <i class="fas fa-brain"></i> Mechanism
                </button>
                <button class="nav-btn" onclick="scrollToSection('dosing')">
                    <i class="fas fa-pills"></i> Dosing
                </button>
                <button class="nav-btn" onclick="scrollToSection('pharmacokinetics')">
                    <i class="fas fa-chart-line"></i> Pharmacokinetics
                </button>
                <button class="nav-btn" onclick="scrollToSection('interactions')">
                    <i class="fas fa-exchange-alt"></i> Interactions
                </button>
                <button class="nav-btn" onclick="scrollToSection('contraindications')">
                    <i class="fas fa-ban"></i> Contraindications
                </button>
                <button class="nav-btn" onclick="scrollToSection('brands')">
                    <i class="fas fa-tags"></i> Brands
                </button>
            </div>
        </div>
    </div>
    
    <main class="container">
        <div class="language-notice">
            <i class="fas fa-language"></i> This page can be translated to any language using the dropdown at the top right
        </div>
        
        <div class="drug-header">
            <h1 class="drug-name">ALPRAZOLAM</h1>
            <div class="pronunciation">(al·pray·zuh·lam)</div>
            <div><strong>Brand Names:</strong> Xanax, Alp, Pralzo, Alprazolam, Pranax, Zenith</div>
            <div><strong>Class:</strong> Benzodiazepines (Schedule IV)</div>
        </div>
        
        <div class="chemical-formula">
            <div class="formula-container">
                <div class="formula-text">
                    <p><strong>Chemical Name:</strong> 8-Chloro-1-methyl-6-phenyl-4H-s-triazolo [4,3-α] [1,4] benzodiazepine</p>
                    <p><strong>Molecular Formula:</strong> C<sub>17</sub>H<sub>14</sub>ClN<sub>4</sub></p>
                </div>
                <div class="formula-image"></div>
            </div>
        </div>
        
        <section id="introduction">
            <h2>Introduction</h2>
            <p>Alprazolam is a potent benzodiazepine with anticonvulsant, anxiolytic, muscle relaxant, and hypnotic properties.</p>
            <div class="highlight">
                <p>Alprazolam was invented by Jackson Hester Jr. at the Upjohn Company and patented in 1971. Approved for medical use in the United States in 1981, it is now classified as a Schedule IV controlled substance. Despite its potential for abuse, alprazolam remains a widely prescribed medication, ranking as the 41st most commonly prescribed drug in the US in 2022 with over 14 million prescriptions.</p>
            </div>
        </section>
        
        <section id="mechanism">
            <h2>Mechanism of Action</h2>
            <p>Alprazolam exerts its therapeutic effects by binding to specific sites on GABA<sub>A</sub> receptors, enhancing the affinity of GABA for its receptor. This binding increases the frequency of chloride channel opening, resulting in hyperpolarization of neurons and reduced neuronal excitability.</p>
            
            <div class="video-container">
                <iframe src="https://www.youtube.com/embed/lcjISUSwNyk?si=ofnhW1Pc5AjFO2YK" title="Alprazolam Mechanism of Action" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            </div>
            
            <p class="highlight">By potentiating GABAergic neurotransmission, alprazolam produces CNS depression that manifests as anxiolysis, sedation, muscle relaxation, and anticonvulsant effects.</p>
        </section>
        
        <section id="indications">
            <h2>Indications</h2>
            <ul>
                <li><strong>Generalized Anxiety Disorder (GAD):</strong> Management of persistent anxiety symptoms</li>
                <li><strong>Panic Disorder:</strong> Treatment with or without agoraphobia</li>
                <li><strong>Adjunctive Therapy:</strong> For anxiety associated with depression</li>
            </ul>
        </section>
        
        <section id="dosing">
            <h2>Dosing</h2>
            <div class="dosing-section">
                <h3>1. Anxiety Disorders</h3>
                <div class="dosing-grid">
                    <div class="dosing-card">
                        <h4>Adults</h4>
                        <p><strong>Form:</strong> IR tablets, ODT, oral solution</p>
                        <p><strong>Dose:</strong> 0.25-0.5 mg PO TID</p>
                        <p><strong>Titration:</strong> Increase every 3-4 days by ≤1 mg/day</p>
                        <p><strong>Maximum:</strong> 4 mg/day</p>
                    </div>
                    <div class="dosing-card">
                        <h4>Geriatric Patients</h4>
                        <p><strong>Dose:</strong> 0.25 mg PO BID or TID</p>
                        <p><strong>Considerations:</strong> Reduced clearance, increased sensitivity</p>
                    </div>
                </div>
                
                <h3>2. Panic Disorder</h3>
                <div class="dosing-grid">
                    <div class="dosing-card">
                        <h4>Adults</h4>
                        <p><strong>Immediate-Release / ODT / Solution:</strong></p>
                        <p><strong>Initial:</strong> 0.5 mg PO TID</p>
                        <p><strong>Maximum:</strong> 10 mg/day</p>
                        <p><strong>Extended-Release:</strong></p>
                        <p><strong>Initial:</strong> 0.5-1 mg PO once daily</p>
                        <p><strong>Maintenance:</strong> 3-6 mg/day</p>
                        <p><strong>Maximum:</strong> 10 mg/day</p>
                    </div>
                    <div class="dosing-card">
                        <h4>Geriatric Patients</h4>
                        <p><strong>Immediate-Release / ODT / Solution:</strong></p>
                        <p><strong>Dose:</strong> 0.25 mg PO BID or TID</p>
                        <p><strong>Extended-Release:</strong></p>
                        <p><strong>Dose:</strong> 0.5 mg PO once daily</p>
                    </div>
                </div>
                
                <h3>3. Dose Adjustments in Hepatic Impairment</h3>
                <div class="dosing-grid">
                    <div class="dosing-card">
                        <h4>Immediate-Release / ODT</h4>
                        <p><strong>Recommended dose:</strong> 0.25 mg PO BID or TID</p>
                    </div>
                    <div class="dosing-card">
                        <h4>Extended-Release</h4>
                        <p><strong>Recommended dose:</strong> 0.5 mg PO once daily</p>
                    </div>
                </div>
                <p class="highlight"><strong>Note:</strong> Titrate slowly and monitor closely for sedation or respiratory depression due to reduced drug clearance.</p>
            </div>
        </section>
        
        <section id="off-label">
            <h2>Off-Label Uses</h2>
            <ul>
                <li>Premenstrual syndrome (PMS)</li>
                <li>Adjunctive treatment of depression</li>
                <li>Short-term management of insomnia</li>
                <li>Alcohol withdrawal syndrome</li>
                <li>Chemotherapy-induced nausea</li>
            </ul>
        </section>
        
        <section id="pharmacokinetics">
            <h2>Pharmacokinetics</h2>
            <h3>Pharmacokinetic Parameters of Alprazolam</h3>
            <table>
                <tr>
                    <th>Parameter</th>
                    <th>Details</th>
                </tr>
                <tr>
                    <td><strong>Absorption</strong></td>
                    <td>
                        <p>Route: Oral</p>
                        <p>Bioavailability: 80-100%</p>
                        <p>T<sub>max</sub>: 1-2 hours</p>
                        <p>Onset: ~30 minutes</p>
                    </td>
                </tr>
                <tr>
                    <td><strong>Distribution</strong></td>
                    <td>
                        <p>Protein Binding: ~80% (albumin)</p>
                        <p>V<sub>d</sub>: 0.8-1.3L/kg</p>
                        <p>Crosses BBB and placenta</p>
                    </td>
                </tr>
                <tr>
                    <td><strong>Metabolism</strong></td>
                    <td>
                        <p>Primary Site: Liver</p>
                        <p>Enzyme: CYP3A4</p>
                        <p>Metabolites: α-OH-alprazolam, 4-OH-alprazolam</p>
                    </td>
                </tr>
                <tr>
                    <td><strong>Excretion</strong></td>
                    <td>
                        <p>Route: Renal (80%)</p>
                        <p>t<sub>½</sub>: Healthy: 11.2h; Hepatic: 16-20h</p>
                    </td>
                </tr>
                <tr>
                    <td><strong>Special Considerations</strong></td>
                    <td>
                        <p>Hepatic impairment: ↓ clearance</p>
                        <p>Elderly: ↑ sensitivity</p>
                        <p>Pregnancy Category: D</p>
                    </td>
                </tr>
            </table>
        </section>
        
        <section id="contraindications">
            <h2>Contraindications</h2>
            <ul>
                <li>Hypersensitivity to benzodiazepines</li>
                <li>Acute narrow-angle glaucoma</li>
                <li>Severe respiratory insufficiency (COPD, sleep apnea)</li>
                <li>Myasthenia gravis</li>
                <li>Severe hepatic impairment</li>
                <li>Pregnancy and breastfeeding</li>
                <li>Concurrent use with potent CYP3A4 inhibitors</li>
            </ul>
            <div class="highlight">
                <p>Alprazolam is absolutely contraindicated in patients with respiratory depression, acute alcohol intoxication, and those with a history of drug dependence due to its high abuse potential.</p>
            </div>
        </section>
        
        <section id="adverse-effects">
            <h2>Adverse Effects</h2>
            <div class="dosing-grid">
                <div>
                    <h3>Common Effects (≥1%)</h3>
                    <ul>
                        <li>Sedation and drowsiness</li>
                        <li>Dizziness and lightheadedness</li>
                        <li>Impaired coordination</li>
                        <li>Memory disturbances</li>
                        <li>Slurred speech</li>
                        <li>Fatigue and lethargy</li>
                        <li>Constipation</li>
                    </ul>
                </div>
                <div>
                    <h3>Serious Effects</h3>
                    <ul>
                        <li>Respiratory depression</li>
                        <li>Paradoxical reactions</li>
                        <li>Dependence and withdrawal</li>
                        <li>Depression and suicidal ideation</li>
                        <li>Hepatic impairment</li>
                        <li>Severe hypotension</li>
                    </ul>
                </div>
            </div>
        </section>
        
        <section id="pregnancy">
            <h2>Pregnancy & Lactation</h2>
            <div class="highlight">
                <p><strong>Pregnancy Category D</strong>—Contraindicated in pregnancy. Alprazolam crosses the placenta and may cause fetal harm including congenital malformations (1st trimester) and neonatal complications (sedation, respiratory depression, withdrawal) when used later in pregnancy.</p>
            </div>
            
            <h3>Lactation</h3>
            <p>Alprazolam is excreted in breast milk. Breastfeeding is not recommended due to risks of sedation, feeding difficulties, and weight loss in the infant.</p>
        </section>
        
        <section id="interactions">
            <h2>Drug Interactions</h2>
            <table>
                <tr>
                    <th>Interacting Drug</th>
                    <th>Mechanism</th>
                    <th>Clinical Effect</th>
                </tr>
                <tr>
                    <td><strong>Azole Antifungals</strong></td>
                    <td>CYP3A4 inhibition</td>
                    <td>↑ Alprazolam levels → toxicity</td>
                </tr>
                <tr>
                    <td><strong>Rifampin</strong></td>
                    <td>CYP3A4 induction</td>
                    <td>↓ Efficacy → treatment failure</td>
                </tr>
                <tr>
                    <td><strong>Opioids</strong></td>
                    <td>Additive CNS depression</td>
                    <td>↑ Risk of respiratory depression</td>
                </tr>
                <tr>
                    <td><strong>Alcohol</strong></td>
                    <td>Synergistic CNS depression</td>
                    <td>↑ Impairment, memory loss</td>
                </tr>
                <tr>
                    <td><strong>Grapefruit Juice</strong></td>
                    <td>Inhibits CYP3A4</td>
                    <td>↑ Bioavailability → toxicity</td>
                </tr>
            </table>
        </section>
        
        <section id="storage">
            <h2>Storage & Handling</h2>
            <ul>
                <li>Store at controlled room temperature (15-25°C)</li>
                <li>Protect from light and moisture</li>
                <li>Keep in original container</li>
                <li>Secure storage required (Schedule IV)</li>
                <li>Dispose of unused medication properly</li>
            </ul>
        </section>
        
        <section id="brands">
            <h2>Common Brands in Pakistan</h2>
            <table>
                <tr>
                    <th>Brand Name</th>
                    <th>Manufacturer</th>
                    <th>Available Strengths</th>
                </tr>
                <tr>
                    <td>Xanax</td>
                    <td>Pfizer</td>
                    <td>0.25mg, 0.5mg, 1mg, 2mg</td>
                </tr>
                <tr>
                    <td>Alprax</td>
                    <td>Sun Pharma</td>
                    <td>0.25mg, 0.5mg, 1mg</td>
                </tr>
                <tr>
                    <td>Alzam</td>
                    <td>Martin Dow</td>
                    <td>0.25mg, 0.5mg</td>
                </tr>
                <tr>
                    <td>Pralzo</td>
                    <td>Searle</td>
                    <td>0.5mg, 1mg</td>
                </tr>
                <tr>
                    <td>Alprol</td>
                    <td>High-Q Pharma</td>
                    <td>0.25mg, 0.5mg</td>
                </tr>
                <tr>
                    <td>Alpraz</td>
                    <td>Genix Pharma</td>
                    <td>0.25mg, 0.5mg</td>
                </tr>
            </table>
        </section>
        
        <div class="references">
            <h2>References</h2>
            <ol>
                <li>British National Formulary (BNF) 2024-25</li>
                <li>PharmaGuide, 31st edition (2024)</li>
                <li><a href="https://en.wikipedia.org/wiki/Alprazolam">Wikipedia - Alprazolam</a></li>
                <li>Medscape: Alprazolam Drug Monograph</li>
                <li>NIH: Alprazolam - LiverTox Database</li>
                <li>Alprazolam Prescribing Information, FDA</li>
            </ol>
        </div>
    </main>
    
    <footer>
        <div class="container footer-content">
            <p>© 2025 UMT School of Pharmacy | Alprazolam Monograph</p>
            <p>Documented by Adan Ali | Clinical Pharmacology Division</p>
            <p>This information is intended for healthcare professionals only.</p>
            <p><i class="fas fa-exclamation-triangle"></i> Alprazolam is a Schedule IV controlled substance with abuse potential</p>
        </div>
    </footer>

    <script>
        function scrollToSection(sectionId) {
            const section = document.getElementById(sectionId);
            if (section) {
                window.scrollTo({
                    top: section.offsetTop - 100,
                    behavior: 'smooth'
                });
            }
        }
        
        // Google Translate initialization
        function googleTranslateElementInit() {
            new google.translate.TranslateElement({
                pageLanguage: 'en',
                includedLanguages: 'en,ur,ar,es,fr,zh-CN',
                layout: google.translate.TranslateElement.InlineLayout.SIMPLE
            }, 'google_translate_element');
        }
        
        // Animation for elements when they come into view
        document.addEventListener('DOMContentLoaded', function() {
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.animationPlayState = 'running';
                    }
                });
            }, { threshold: 0.1 });
            
            document.querySelectorAll('section, .dosing-card, li, tr').forEach(el => {
                observer.observe(el);
            });
        });
    </script>
</body>
</html>
