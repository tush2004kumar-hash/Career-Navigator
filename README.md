# Career-Navigator
This application is a "Career Navigator" that analyzes your skills, compares them to your desired job, and then generates a personalized, prioritized learning roadmap to help you efficiently close your skill gaps and achieve your career goals.
<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Career Navigator | Your Career GPS</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #F8F7F4; 
            color: #2c3e50;
        }
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
            height: 40vh;
            max-height: 500px;
        }
        .nav-link {
            transition: color 0.3s;
        }
        .nav-link:hover {
            color: #3b82f6;
        }
        .step-card {
            border-left-width: 4px;
            transition: all 0.3s ease;
        }
        .step-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.05), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
        }
        .slider-thumb::-webkit-slider-thumb {
            -webkit-appearance: none;
            appearance: none;
            width: 20px;
            height: 20px;
            background: #3b82f6;
            cursor: pointer;
            border-radius: 50%;
        }
        .slider-thumb::-moz-range-thumb {
            width: 20px;
            height: 20px;
            background: #3b82f6;
            cursor: pointer;
            border-radius: 50%;
        }
    </style>
</head>
<body class="antialiased">

    <header class="bg-white/80 backdrop-blur-lg fixed top-0 left-0 right-0 z-50 shadow-sm">
        <div class="container mx-auto px-6 py-4 flex justify-between items-center">
            <h1 class="text-2xl font-bold text-gray-800">Career <span class="text-blue-600">Navigator</span></h1>
            <nav class="hidden md:flex space-x-8">
                <a href="#vision" class="nav-link text-gray-600">Vision</a>
                <a href="#process" class="nav-link text-gray-600">How It Works</a>
                <a href="#demo" class="nav-link text-gray-600">Interactive Demo</a>
                <a href="#features" class="nav-link text-gray-600">Features</a>
            </nav>
            <a href="#demo" class="bg-blue-600 text-white px-5 py-2 rounded-full hover:bg-blue-700 transition hidden md:block">Get Started</a>
        </div>
    </header>

    <main class="pt-20">
        <section id="vision" class="py-20 md:py-32">
            <div class="container mx-auto px-6 text-center">
                <h2 class="text-4xl md:text-6xl font-bold text-gray-800 mb-4">Feeling Lost in Your Career Path?</h2>
                <p class="text-lg md:text-xl text-gray-600 max-w-3xl mx-auto mb-8">
                    You've got the ambition, but the path isn't clear. Generic advice doesn't work. You need a personalized plan, a GPS for your career that understands your starting point and guides you to your dream job.
                </p>
                <a href="#demo" class="bg-blue-600 text-white px-8 py-4 rounded-full text-lg font-semibold hover:bg-blue-700 transition transform hover:scale-105">Discover Your Personalized Roadmap</a>
            </div>
        </section>

        <section id="process" class="py-20 bg-white">
            <div class="container mx-auto px-6">
                <div class="text-center mb-16">
                    <h2 class="text-3xl md:text-4xl font-bold text-gray-800">Your Journey, Simplified in 3 Steps</h2>
                    <p class="text-lg text-gray-600 mt-2">Transforming ambiguity into an actionable plan.</p>
                </div>
                <div class="grid md:grid-cols-3 gap-8 text-center">
                    <div class="p-8">
                        <div class="flex items-center justify-center h-20 w-20 mx-auto bg-blue-100 text-blue-600 rounded-full text-3xl font-bold mb-4">1</div>
                        <h3 class="text-2xl font-semibold mb-2">Assess Your Skills</h3>
                        <p class="text-gray-600">Start by telling us what you know. Our simple, intuitive assessment helps create your unique skill profile.</p>
                    </div>
                    <div class="p-8">
                        <div class="flex items-center justify-center h-20 w-20 mx-auto bg-blue-100 text-blue-600 rounded-full text-3xl font-bold mb-4">2</div>
                        <h3 class="text-2xl font-semibold mb-2">Analyze Skill Gaps</h3>
                        <p class="text-gray-600">Our intelligent engine compares your profile to the skills required for your dream job, instantly visualizing what to learn next.</p>
                    </div>
                    <div class="p-8">
                        <div class="flex items-center justify-center h-20 w-20 mx-auto bg-blue-100 text-blue-600 rounded-full text-3xl font-bold mb-4">3</div>
                        <h3 class="text-2xl font-semibold mb-2">Launch Your Roadmap</h3>
                        <p class="text-gray-600">Receive a step-by-step learning plan, filled with curated resources, designed to efficiently close your skill gaps.</p>
                    </div>
                </div>
            </div>
        </section>

        <section id="demo" class="py-20 md:py-24">
            <div class="container mx-auto px-6">
                <div class="text-center mb-16">
                    <h2 class="text-3xl md:text-4xl font-bold text-gray-800">Interactive Demo</h2>
                    <p class="text-lg text-gray-600 mt-2">Experience the Career Navigator in action. Adjust your skill levels to see your personalized roadmap update in real-time.</p>
                </div>

                <div class="bg-white p-8 rounded-2xl shadow-xl max-w-6xl mx-auto">
                    <div class="grid lg:grid-cols-5 gap-8">
                        <div class="lg:col-span-2">
                            <h3 class="text-2xl font-semibold mb-4">Step 1: Assess Your Skills</h3>
                            <div class="mb-6">
                                <label for="career-select" class="block mb-2 text-sm font-medium text-gray-700">Select Your Target Role:</label>
                                <select id="career-select" class="w-full p-2 border border-gray-300 rounded-md shadow-sm focus:ring-blue-500 focus:border-blue-500">
                                    <option value="data-analyst">Data Analyst</option>
                                    <option value="full-stack-developer">Full-Stack Web Developer</option>
                                    <option value="frontend-developer">Frontend Developer</option>
                                    <option value="backend-developer">Backend Developer</option>
                                    <option value="software-tester">Software Tester</option>
                                    <option value="ui-ux-designer">UI/UX Designer</option>
                                    <option value="software-engineer">Software Engineer (Language Focused)</option>
                                </select>
                            </div>
                            <div id="skills-assessment" class="space-y-6"></div>
                        </div>
                        <div class="lg:col-span-3">
                            <h3 class="text-2xl font-semibold mb-6">Step 2: Your Skill Gap Analysis</h3>
                            <div class="chart-container">
                                <canvas id="skillGapChart"></canvas>
                            </div>
                            <div class="mt-8">
                                <h3 class="text-2xl font-semibold mb-6">Step 3: Your Personalized Roadmap</h3>
                                <div id="roadmap" class="space-y-4">
                                    <p class="text-gray-500 text-center p-4 border-2 border-dashed rounded-lg">Your learning plan will appear here once you assess your skills.</p>
                                </div>
                                <div id="companies-section" class="mt-8">
                                    <h3 class="text-2xl font-semibold mb-6">Companies You Could Target</h3>
                                    <p class="text-gray-600 mb-4">Based on your high proficiency, here are some companies that use these languages:</p>
                                    <div id="company-list" class="space-y-3"></div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="features" class="py-20 bg-white">
            <div class="container mx-auto px-6">
                <div class="text-center mb-16">
                    <h2 class="text-3xl md:text-4xl font-bold text-gray-800">Platform Core Features</h2>
                    <p class="text-lg text-gray-600 mt-2">Everything you need to succeed, all in one place.</p>
                </div>
                <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
                    <div class="bg-gray-50 p-8 rounded-lg">
                        <div class="text-3xl mb-4 text-blue-600">➔</div>
                        <h3 class="text-xl font-semibold mb-2">Intelligent Roadmap Generation</h3>
                        <p class="text-gray-600">Our platform doesn't use static templates. It analyzes your unique skill gaps to create a logical, efficient learning path just for you.</p>
                    </div>
                    <div class="bg-gray-50 p-8 rounded-lg">
                        <div class="text-3xl mb-4 text-blue-600">📚</div>
                        <h3 class="text-xl font-semibold mb-2">Dynamic Resource Integration</h3>
                        <p class="text-gray-600">Get the best free and paid learning content from platforms like YouTube, Coursera, and edX, matched to each step of your journey.</p>
                    </div>
                    <div class="bg-gray-50 p-8 rounded-lg">
                        <div class="text-3xl mb-4 text-blue-600">📊</div>
                        <h3 class="text-xl font-semibold mb-2">Progress Tracking</h3>
                        <p class="text-gray-600">Stay motivated by tracking your progress through weekly milestones. Our "Next Step" engine suggests what to focus on next based on your achievements.</p>
                    </div>
                    <div class="bg-gray-50 p-8 rounded-lg">
                        <div class="text-3xl mb-4 text-blue-600">🌐</div>
                        <h3 class="text-xl font-semibold mb-2">Peer Comparison (Bonus)</h3>
                        <p class="text-gray-600">Anonymously compare your progress with peers on a similar journey, providing motivation and context for your growth.</p>
                    </div>
                    <div class="bg-gray-50 p-8 rounded-lg">
                        <div class="text-3xl mb-4 text-blue-600">🧑‍🏫</div>
                        <h3 class="text-xl font-semibold mb-2">Mentor Suggestions (Bonus)</h3>
                        <p class="text-gray-600">Connect with industry professionals. The platform can suggest potential mentors based on your career goals and location.</p>
                    </div>
                    <div class="bg-gray-50 p-8 rounded-lg">
                        <div class="text-3xl mb-4 text-blue-600">🏆</div>
                        <h3 class="text-xl font-semibold mb-2">Industry Certifications (Bonus)</h3>
                        <p class="text-gray-600">Your roadmap can include key industry certifications as major milestones, giving you tangible credentials to aim for.</p>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <footer class="bg-gray-800 text-white py-12">
        <div class="container mx-auto px-6 text-center">
            <p>&copy; 2025 Career Navigator. All rights reserved.</p>
            <p class="text-gray-400 mt-2">Your Personal GPS for a Fulfilling Career.</p>
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function () {
        
            const careerPaths = {
                'data-analyst': {
                    labels: ['SQL', 'Statistics', 'Python', 'Excel', 'Tableau', 'Communication'],
                    requiredProficiency: [8, 7, 6, 8, 7, 9],
                    userProficiency: [2, 3, 1, 4, 1, 5],
                    skillDetails: {
                        'SQL': {
                            description: "Master database querying to extract and manipulate data.",
                            resources: [
                                { name: "SQL for Data Science", platform: "Coursera" },
                                { name: "Intro to SQL", platform: "Khan Academy (Free)" }
                            ],
                            companies: ['Microsoft', 'Google', 'IBM']
                        },
                        'Statistics': {
                            description: "Understand foundational stats for data interpretation and modeling.",
                            resources: [
                                { name: "Statistics and Probability", platform: "Khan Academy (Free)" },
                                { name: "Intro to Descriptive Statistics", platform: "Udacity (Free)" }
                            ]
                        },
                        'Python': {
                            description: "Learn Python with Pandas & NumPy for data analysis.",
                            resources: [
                                { name: "Python for Everybody", platform: "Coursera (Free Audit)" },
                                { name: "Pandas Tutorial", platform: "YouTube (Free)" }
                            ],
                            companies: ['Google', 'Facebook', 'Spotify']
                        },
                        'Excel': {
                            description: "Advanced Excel skills for data cleaning and analysis.",
                            resources: [
                                { name: "Excel Skills for Business", platform: "Coursera" },
                                { name: "Excel Pivot Tables", platform: "YouTube (Free)" }
                            ],
                            companies: ['Deloitte', 'PwC', 'KPMG']
                        },
                        'Tableau': {
                            description: "Create compelling data visualizations and dashboards.",
                            resources: [
                                { name: "Tableau Public Training", platform: "Tableau (Free)" },
                                { name: "Data Visualization with Tableau", platform: "Coursera" }
                            ],
                            companies: ['Tableau', 'Netflix', 'Amazon']
                        },
                        'Communication': {
                            description: "Learn to present data insights clearly to stakeholders.",
                            resources: [
                                { name: "Storytelling with Data (Book)", platform: "Offline PDF/Book" },
                                { name: "Effective Communication", platform: "edX" }
                            ]
                        }
                    }
                },
                'full-stack-developer': {
                    labels: ['HTML/CSS', 'JavaScript', 'React', 'Node.js', 'Databases', 'API Design'],
                    requiredProficiency: [9, 8, 8, 7, 6, 7],
                    userProficiency: [3, 4, 2, 1, 1, 3],
                    skillDetails: {
                        'HTML/CSS': {
                            description: "Build a strong foundation in structuring and styling websites.",
                            resources: [
                                { name: "Build Websites from Scratch", platform: "Coursera" },
                                { name: "CSS Flexbox & Grid", platform: "YouTube (Free)" }
                            ]
                        },
                        'JavaScript': {
                            description: "Learn the core language for front-end and back-end development.",
                            resources: [
                                { name: "JavaScript 30", platform: "Wes Bos (Free)" },
                                { name: "The Complete JavaScript Course", platform: "Udemy" }
                            ],
                            companies: ['Google', 'PayPal', 'Netflix']
                        },
                        'React': {
                            description: "Master a popular library for building user interfaces.",
                            resources: [
                                { name: "React - The Complete Guide", platform: "Udemy" },
                                { name: "React Docs", platform: "Official Docs (Free)" }
                            ],
                            companies: ['Airbnb', 'Netflix', 'Uber']
                        },
                        'Node.js': {
                            description: "Use JavaScript on the server-side to build back-end services.",
                            resources: [
                                { name: "Node.js and Express.js", platform: "Coursera" },
                                { name: "Node.js Crash Course", platform: "YouTube (Free)" }
                            ],
                            companies: ['LinkedIn', 'Walmart', 'Netflix']
                        },
                        'Databases': {
                            description: "Learn to work with both SQL and NoSQL databases.",
                            resources: [
                                { name: "Databases for Developers", platform: "edX" },
                                { name: "SQL Tutorial", platform: "W3Schools (Free)" }
                            ],
                            companies: ['Oracle', 'Microsoft', 'Google']
                        },
                        'API Design': {
                            description: "Build and design RESTful APIs to connect your front-end and back-end.",
                            resources: [
                                { name: "APIs: A Practical Guide", platform: "Coursera" },
                                { name: "REST API Tutorial", platform: "YouTube (Free)" }
                            ]
                        }
                    }
                },
                'frontend-developer': {
                    labels: ['HTML/CSS', 'JavaScript', 'React', 'Responsive Design', 'API Integration', 'UI/UX Principles'],
                    requiredProficiency: [9, 9, 8, 8, 7, 6],
                    userProficiency: [3, 4, 2, 3, 2, 3],
                    skillDetails: {
                        'HTML/CSS': {
                            description: "The core building blocks for every web page.",
                            resources: [
                                { name: "The Odin Project", platform: "odinproject.com (Free)" },
                                { name: "Frontend Masters", platform: "frontendmasters.com" }
                            ]
                        },
                        'JavaScript': {
                            description: "Bring websites to life with dynamic and interactive elements.",
                            resources: [
                                { name: "Eloquent JavaScript (Book)", platform: "eloquentjavascript.net (Free)" },
                                { name: "JavaScript.info", platform: "javascript.info (Free)" }
                            ],
                            companies: ['Google', 'Meta', 'Spotify']
                        },
                        'React': {
                            description: "Master the most popular library for building modern user interfaces.",
                            resources: [
                                { name: "Official React Documentation", platform: "react.dev (Free)" },
                                { name: "React and Redux Course", platform: "Coursera" }
                            ],
                            companies: ['Airbnb', 'Netflix', 'Uber']
                        },
                        'Responsive Design': {
                            description: "Ensure your web pages look great on any device.",
                            resources: [
                                { name: "Responsive Web Design", platform: "freecodecamp.org (Free)" },
                                { name: "Tailwind CSS Documentation", platform: "tailwindcss.com (Free)" }
                            ]
                        },
                        'API Integration': {
                            description: "Connect to backend services to fetch and display data.",
                            resources: [
                                { name: "Build a Simple API", platform: "YouTube (Free)" },
                                { name: "Full-Stack Web Development Course", platform: "Coursera" }
                            ]
                        },
                        'UI/UX Principles': {
                            description: "Learn the fundamentals of designing intuitive user experiences.",
                            resources: [
                                { name: "UI Design Course", platform: "Udemy" },
                                { name: "Don't Make Me Think (Book)", platform: "Book/PDF" }
                            ]
                        }
                    }
                },
                'backend-developer': {
                    labels: ['Node.js', 'Databases', 'API Design', 'Authentication', 'Security', 'Deployment'],
                    requiredProficiency: [8, 8, 9, 7, 7, 6],
                    userProficiency: [1, 2, 1, 1, 1, 1],
                    skillDetails: {
                        'Node.js': {
                            description: "Build scalable and high-performance server-side applications.",
                            resources: [
                                { name: "Node.js API Development", platform: "Coursera" },
                                { name: "Node.js in a Nutshell", platform: "YouTube (Free)" }
                            ],
                            companies: ['Netflix', 'LinkedIn', 'Uber']
                        },
                        'Databases': {
                            description: "Store and retrieve data from a variety of database systems.",
                            resources: [
                                { name: "MongoDB University", platform: "mongodb.com (Free)" },
                                { name: "SQL Essentials", platform: "edX" }
                            ],
                            companies: ['Oracle', 'Microsoft', 'Google']
                        },
                        'API Design': {
                            description: "Design and build clean, maintainable, and efficient APIs.",
                            resources: [
                                { name: "RESTful API Design", platform: "Udemy" },
                                { name: "API Design Course", platform: "Coursera" }
                            ]
                        },
                        'Authentication': {
                            description: "Implement secure user login and session management.",
                            resources: [
                                { name: "Authentication in Node.js", platform: "YouTube (Free)" },
                                { name: "Passport.js Docs", platform: "passportjs.org (Free)" }
                            ]
                        },
                        'Security': {
                            description: "Protect your applications from common security vulnerabilities.",
                            resources: [
                                { name: "Web Security Fundamentals", platform: "freecodecamp.org (Free)" },
                                { name: "OWASP Top 10", platform: "owasp.org (Free)" }
                            ]
                        },
                        'Deployment': {
                            description: "Deploy your backend applications to the cloud.",
                            resources: [
                                { name: "Deploying a Node App", platform: "YouTube (Free)" },
                                { name: "Intro to Cloud Computing", platform: "Coursera" }
                            ]
                        }
                    }
                },
                'software-tester': {
                    labels: ['Manual Testing', 'Automation', 'Bug Reporting', 'Agile/Scrum', 'Test Planning', 'Regression Testing'],
                    requiredProficiency: [8, 7, 9, 8, 7, 8],
                    userProficiency: [4, 2, 5, 3, 2, 3],
                    skillDetails: {
                        'Manual Testing': {
                            description: "Execute test cases manually to identify defects and ensure quality.",
                            resources: [
                                { name: "Manual Software Testing", platform: "Udemy" },
                                { name: "ISTQB Foundation", platform: "ISTQB.org" }
                            ]
                        },
                        'Automation': {
                            description: "Write scripts and use tools to automate test cases.",
                            resources: [
                                { name: "Selenium WebDriver with Java", platform: "Udemy" },
                                { name: "Cypress Fundamentals", platform: "cypress.io (Free)" }
                            ],
                            companies: ['Microsoft', 'Apple', 'Adobe']
                        },
                        'Bug Reporting': {
                            description: "Learn to write clear, concise, and reproducible bug reports.",
                            resources: [
                                { name: "Jira for Beginners", platform: "YouTube (Free)" },
                                { name: "Effective Bug Reporting", platform: "Article" }
                            ]
                        },
                        'Agile/Scrum': {
                            description: "Understand the software development lifecycle and your role in it.",
                            resources: [
                                { name: "Scrum Master Certification", platform: "Scrum.org" },
                                { name: "Agile Development Course", platform: "Coursera" }
                            ],
                            companies: ['Amazon', 'Google', 'Cisco']
                        },
                        'Test Planning': {
                            description: "Design comprehensive test plans to cover all features.",
                            resources: [
                                { name: "Test Plan Documentation", platform: "YouTube (Free)" },
                                { name: "Test Management Tools", platform: "Article" }
                            ]
                        },
                        'Regression Testing': {
                            description: "Run tests to ensure new code doesn't break existing functionality.",
                            resources: [
                                { name: "What is Regression Testing?", platform: "Article" },
                                { name: "Automation Frameworks", platform: "Tutorial" }
                            ]
                        }
                    }
                },
                'ui-ux-designer': {
                    labels: ['User Research', 'Wireframing', 'Prototyping', 'Figma', 'User Testing', 'Design Principles'],
                    requiredProficiency: [8, 9, 8, 9, 7, 9],
                    userProficiency: [3, 2, 2, 1, 3, 4],
                    skillDetails: {
                        'User Research': {
                            description: "Understand user needs and behaviors through interviews and data.",
                            resources: [
                                { name: "User Research Fundamentals", platform: "Coursera" },
                                { name: "The User Experience Research Field Guide", platform: "Book/PDF" }
                            ]
                        },
                        'Wireframing': {
                            description: "Create low-fidelity outlines of a product's structure and layout.",
                            resources: [
                                { name: "Wireframing for Beginners", platform: "YouTube (Free)" },
                                { name: "Balsamiq Mockups Tutorial", platform: "Tutorial" }
                            ]
                        },
                        'Prototyping': {
                            description: "Build interactive prototypes to test user flows before development.",
                            resources: [
                                { name: "Figma Prototyping", platform: "YouTube (Free)" },
                                { name: "Figma Official Tutorials", platform: "help.figma.com (Free)" }
                            ]
                        },
                        'Figma': {
                            description: "Master the industry-standard tool for collaborative design.",
                            resources: [
                                { name: "Figma for Beginners", platform: "YouTube (Free)" },
                                { name: "Figma Official Tutorials", platform: "help.figma.com (Free)" }
                            ],
                            companies: ['Figma', 'Microsoft', 'Google']
                        },
                        'User Testing': {
                            description: "Gather feedback on prototypes and designs from real users.",
                            resources: [
                                { name: "Conducting User Interviews", platform: "Course" },
                                { name: "Usability Testing 101", platform: "Article" }
                            ]
                        },
                        'Design Principles': {
                            description: "Learn fundamental principles like hierarchy, color theory, and typography.",
                            resources: [
                                { name: "The Design of Everyday Things (Book)", platform: "Book/PDF" },
                                { name: "Intro to Graphic Design", platform: "Coursera" }
                            ],
                            companies: ['Apple', 'Adobe', 'IDEO']
                        }
                    }
                },
                'software-engineer': {
                    labels: ['Python', 'Java', 'C++', 'JavaScript', 'Go', 'Rust'],
                    requiredProficiency: [8, 7, 8, 8, 6, 6],
                    userProficiency: [2, 1, 1, 3, 1, 1],
                    skillDetails: {
                        'Python': {
                            description: "A versatile language used in web dev, data science, and automation.",
                            resources: [
                                { name: "Python for Everybody", platform: "Coursera (Free Audit)" },
                                { name: "Python.org Docs", platform: "Official Docs (Free)" }
                            ],
                            companies: ['Google', 'Facebook', 'Spotify', 'Instagram']
                        },
                        'Java': {
                            description: "An object-oriented language widely used for large-scale enterprise applications and Android development.",
                            resources: [
                                { name: "Java Programming: A Software Engineer's Guide", platform: "edX" },
                                { name: "Oracle Java Docs", platform: "Official Docs (Free)" }
                            ],
                            companies: ['Amazon', 'Netflix', 'Uber', 'LinkedIn']
                        },
                        'C++': {
                            description: "A powerful language for systems programming, game development, and high-performance computing.",
                            resources: [
                                { name: "C++ for Programmers", platform: "Coursera" },
                                { name: "LearnCpp.com", platform: "Website (Free)" }
                            ],
                            companies: ['Microsoft', 'Apple', 'Adobe', 'NVIDIA']
                        },
                        'JavaScript': {
                            description: "The core language of the web, used for both frontend and backend development.",
                            resources: [
                                { name: "JavaScript.info", platform: "Website (Free)" },
                                { name: "The Complete JavaScript Course", platform: "Udemy" }
                            ],
                            companies: ['Google', 'PayPal', 'Netflix', 'Airbnb']
                        },
                        'Go': {
                            description: "Developed by Google, Go is known for its simplicity and concurrency, ideal for building scalable network services.",
                            resources: [
                                { name: "Go by Example", platform: "Website (Free)" },
                                { name: "Go Tour", platform: "Official Docs (Free)" }
                            ],
                            companies: ['Google', 'Dropbox', 'Twitch', 'Uber']
                        },
                        'Rust': {
                            description: "A modern language focused on safety, performance, and concurrency.",
                            resources: [
                                { name: "The Rust Programming Language", platform: "Official Book (Free)" },
                                { name: "Rustlings", platform: "GitHub Repo (Free)" }
                            ],
                            companies: ['Mozilla', 'Microsoft', 'AWS', 'Cloudflare']
                        }
                    }
                }
            };
            
            let currentCareerPathKey = 'data-analyst';

            const careerSelect = document.getElementById('career-select');
            const assessmentContainer = document.getElementById('skills-assessment');
            const roadmapContainer = document.getElementById('roadmap');
            const companiesSection = document.getElementById('companies-section');
            const companyList = document.getElementById('company-list');

            let skillGapChart;

            function createSliders(skills) {
                assessmentContainer.innerHTML = '';
                skills.labels.forEach((skill, index) => {
                    const skillValue = skills.userProficiency[index];
                    const sliderHTML = `
                        <div>
                            <label for="${skill}-slider" class="block mb-2 text-sm font-medium text-gray-700">${skill}</label>
                            <div class="flex items-center space-x-4">
                                <input id="${skill}-slider" type="range" min="0" max="10" value="${skillValue}" data-index="${index}" class="w-full h-2 bg-gray-200 rounded-lg appearance-none cursor-pointer slider-thumb">
                                <span class="font-semibold text-blue-600 w-6 text-center" id="${skill}-value">${skillValue}</span>
                            </div>
                        </div>
                    `;
                    assessmentContainer.insertAdjacentHTML('beforeend', sliderHTML);
                });
            }

            function createChart() {
                const ctx = document.getElementById('skillGapChart').getContext('2d');
                const career = careerPaths[currentCareerPathKey];
                
                
                if (skillGapChart) {
                    skillGapChart.destroy();
                }

                skillGapChart = new Chart(ctx, {
                    type: 'radar',
                    data: {
                        labels: career.labels,
                        datasets: [{
                            label: 'Your Current Skills',
                            data: career.userProficiency,
                            backgroundColor: 'rgba(59, 130, 246, 0.2)',
                            borderColor: 'rgba(59, 130, 246, 1)',
                            borderWidth: 2,
                            pointBackgroundColor: 'rgba(59, 130, 246, 1)',
                        }, {
                            label: 'Required for Role',
                            data: career.requiredProficiency,
                            backgroundColor: 'rgba(107, 114, 128, 0.2)',
                            borderColor: 'rgba(107, 114, 128, 1)',
                            borderWidth: 2,
                            pointBackgroundColor: 'rgba(107, 114, 128, 1)',
                        }]
                    },
                    options: {
                        maintainAspectRatio: false,
                        responsive: true,
                        scales: {
                            r: {
                                angleLines: {
                                    color: 'rgba(0, 0, 0, 0.1)'
                                },
                                grid: {
                                    color: 'rgba(0, 0, 0, 0.1)'
                                },
                                pointLabels: {
                                    font: {
                                        size: 13,
                                        weight: '500'
                                    },
                                    color: '#4b5563'
                                },
                                ticks: {
                                    beginAtZero: true,
                                    max: 10,
                                    stepSize: 2,
                                    backdropColor: 'rgba(255, 255, 255, 0.75)'
                                }
                            }
                        },
                        plugins: {
                            legend: {
                                position: 'top',
                            }
                        }
                    }
                });
            }

            function updateChart() {
                const career = careerPaths[currentCareerPathKey];
                skillGapChart.data.datasets[0].data = career.userProficiency;
                skillGapChart.update();
            }

            function generateRoadmap() {
                roadmapContainer.innerHTML = '';
                const career = careerPaths[currentCareerPathKey];
                const gaps = [];
                career.labels.forEach((skill, index) => {
                    const diff = career.requiredProficiency[index] - career.userProficiency[index];
                    if (diff > 0) {
                        gaps.push({ skill, diff, index });
                    }
                });

                if (gaps.length === 0) {
                    roadmapContainer.innerHTML = `
                        <div class="p-4 text-center bg-green-100 text-green-800 rounded-lg">
                            <h4 class="font-bold">Congratulations!</h4>
                            <p>You've met all the skill requirements. Time to focus on building your portfolio!</p>
                        </div>
                    `;
                    return;
                }
                
                gaps.sort((a, b) => b.diff - a.diff);

                gaps.forEach(({ skill, index }, order) => {
                    const skillInfo = career.skillDetails[skill];
                    const resourcesHTML = skillInfo.resources.map(res => `<li><span class="font-semibold">${res.name}</span> (${res.platform})</li>`).join('');

                    const roadmapStepHTML = `
                        <div class="step-card border-l-blue-500 bg-gray-50 p-4 rounded-r-lg">
                            <h4 class="font-bold text-lg text-gray-800">
                                <span class="text-blue-600">Step ${order + 1}:</span> Focus on ${skill}
                            </h4>
                            <p class="text-gray-600 mt-1">${skillInfo.description}</p>
                            <div class="mt-3">
                                <h5 class="font-semibold text-gray-700">Suggested Resources:</h5>
                                <ul class="list-disc list-inside text-gray-600 mt-1 space-y-1">
                                    ${resourcesHTML}
                                </ul>
                            </div>
                        </div>
                    `;
                    roadmapContainer.insertAdjacentHTML('beforeend', roadmapStepHTML);
                });
            }

            function generateCompanies() {
                const career = careerPaths[currentCareerPathKey];
                companyList.innerHTML = '';
                let foundCompanies = new Set();
                let hasHighProficiency = false;

                career.labels.forEach((skill, index) => {
                    
                    if (career.skillDetails[skill].companies && career.userProficiency[index] >= 8) {
                        hasHighProficiency = true;
                        const companies = career.skillDetails[skill].companies || [];
                        companies.forEach(company => {
                            if (!foundCompanies.has(company)) {
                                companyList.insertAdjacentHTML('beforeend', `
                                    <div class="p-4 bg-gray-100 rounded-lg flex items-center justify-between">
                                        <span class="font-semibold text-gray-800">${company}</span>
                                        <span class="text-xs text-gray-500">Known for ${skill}</span>
                                    </div>
                                `);
                                foundCompanies.add(company);
                            }
                        });
                    }
                });

                if (foundCompanies.size > 0) {
                    companiesSection.classList.remove('hidden');
                } else {
                    companiesSection.classList.add('hidden');
                }
            }
            careerSelect.addEventListener('change', (e) => {
                currentCareerPathKey = e.target.value;
                const career = careerPaths[currentCareerPathKey];
                createSliders(career);
                createChart();
                generateRoadmap();
                generateCompanies();
            });

            
            assessmentContainer.addEventListener('input', function (e) {
                if (e.target.type === 'range') {
                    const index = e.target.dataset.index;
                    const value = parseInt(e.target.value, 10);
                    const career = careerPaths[currentCareerPathKey];
                    career.userProficiency[index] = value;
                    document.getElementById(`${career.labels[index]}-value`).textContent = value;
                    updateChart();
                    generateRoadmap();
                    generateCompanies();
                }
            });

            const navLinks = document.querySelectorAll('a[href^="#"]');
            navLinks.forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                    document.querySelector(this.getAttribute('href')).scrollIntoView({
                        behavior: 'smooth'
                    });
                });
            });
            
            // Initial setup
            createSliders(careerPaths[currentCareerPathKey]);
            createChart();
            generateRoadmap();
            generateCompanies();
        });
    </script>
</body>
</html>
