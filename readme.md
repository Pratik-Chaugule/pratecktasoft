<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PratecktaSoft | Digital Engineering and Innovation</title>
    <!-- Load Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Load Animate On Scroll (AOS) Library -->
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    <!-- FIX: Added AOS JavaScript library to resolve ReferenceError -->
    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script> 
    
    <script>
        // Tailwind Configuration
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        'prateckta-blue': '#1a73e8',
                        'prateckta-dark': '#0f172a',
                        'prateckta-light': '#f1f5f9',
                        'prateckta-accent': '#e92e7d', // A new vibrant color for emphasis
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    }
                }
            }
        }
    </script>

    <!-- 
    ====================================================================
    CUSTOM CSS: Including animations for header and hover effects.
    ==================================================================== 
    -->
    <style>
        /* Base styles */
        html {
            scroll-behavior: smooth;
        }

        /* --- Custom Keyframe Animation for Header Entry --- */
        @keyframes slideDown {
            from { transform: translateY(-100%); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }
        .animate-header {
            animation: slideDown 0.5s ease-out forwards;
            opacity: 0; /* Start hidden */
        }

        /* Custom style for the Hero Section background image (Placeholder) */
        .hero-background {
            /* Using a placeholder image for demonstration */
            background-image: url('background.jpg'); 
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            position: relative;
        }

        /* Overlay for readability */
        .hero-background::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: rgba(15, 23, 42, 0.9); /* Dark overlay */
            z-index: 1;
        }

        /* Ensures content is above the overlay */
        .hero-content {
            position: relative;
            z-index: 2;
        }

        /* Button Hover Effects */
        .btn-primary {
            transition: all 0.3s ease;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 15px rgba(26, 115, 232, 0.4);
        }
        /* Card Hover Effects */
        .card-hover:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15); /* Slightly stronger shadow */
        }
        .card-hover {
            transition: all 0.3s ease;
        }
        /* Style for the map placeholder */
        .map-placeholder {
            background: #e0e7ff; 
            border: 2px solid #1a73e8; 
            display: flex;
            align-items: center;
            justify-content: center;
            color: #1a73e8; 
            font-weight: 600;
            text-align: center;
        }
    </style>
</head>
<body class="bg-white text-prateckta-dark font-sans">

    <!-- Header & Navigation - Now Animated -->
    <header class="sticky top-0 z-50 bg-white shadow-lg animate-header">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center py-4 md:justify-start md:space-x-10">
                <div class="flex justify-start lg:w-0 lg:flex-1">
                    <a href="#" class="flex items-center space-x-3">
                        <!-- LOGO PLACEHOLDER - Using text fallback for robust display -->
                        <div class="h-20.5 w-24 hover:opacity-80 transition duration-150 hover:scale-105">
                            <img src="logo.png" alt="">
                        </div>
                    </a>
                </div>
                <nav class="hidden md:flex space-x-10">
                    <a href="#services" class="text-base font-medium text-gray-600 hover:text-prateckta-blue transition duration-150">Services</a>
                    <a href="#industries" class="text-base font-medium text-gray-600 hover:text-prateckta-blue transition duration-150">Industries</a>
                    <a href="#about" class="text-base font-medium text-gray-600 hover:text-prateckta-blue transition duration-150">About</a>
                    <a href="#contact" class="text-base font-medium text-gray-600 hover:text-prateckta-blue transition duration-150">Contact</a>
                </nav>
                <div class="hidden md:flex items-center justify-end md:flex-1 lg:w-0">
                    <a href="#contact" class="btn-primary ml-8 whitespace-nowrap inline-flex items-center justify-center px-6 py-3 border border-transparent rounded-full text-base font-semibold text-white bg-prateckta-blue hover:bg-blue-700">
                        Start a Project
                    </a>
                </div>
            </div>
        </div>
    </header>

    <main>
        <!-- Hero Section: With Background Image -->
        <section class="hero-background relative overflow-hidden pt-20 sm:pt-32 lg:pt-40 rounded-b-[4rem] mb-12">
            <div class="hero-content max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 pb-32 grid md:grid-cols-2 gap-12 items-center">
                
                <!-- Hero Text -->
                <div data-aos="fade-right" data-aos-duration="1200" data-aos-delay="200">
                    <h1 class="text-4xl tracking-tight font-extrabold text-white sm:text-5xl md:text-6xl lg:text-7xl">
                        Future-Proof <span class="block text-prateckta-accent xl:inline">Your Enterprise.</span>
                    </h1>
                    <p class="mt-4 text-xl text-gray-300 sm:text-2xl" data-aos="fade-right" data-aos-duration="1200" data-aos-delay="400">
                        We build high-performance, cloud-native software products and enable enterprise digital transformation with AI, Data, and relentless quality engineering.
                    </p>
                    <div class="mt-10 flex space-x-4">
                        <a href="#services" class="btn-primary flex items-center justify-center px-8 py-3 border border-transparent text-base font-medium rounded-full text-prateckta-dark bg-prateckta-accent hover:bg-prateckta-accent/80 md:py-4 md:text-lg md:px-10" data-aos="zoom-in" data-aos-delay="600">
                            View Technologies
                        </a>
                        <a href="#contact" class="btn-primary flex items-center justify-center px-8 py-3 border-2 border-white text-base font-medium rounded-full text-white hover:bg-prateckta-blue md:py-4 md:text-lg md:px-10" data-aos="zoom-in" data-aos-delay="700">
                            Book a Strategy Call
                        </a>
                    </div>
                </div>

                <!-- Secondary Hero Image/Illustration Placeholder -->
                <div data-aos="fade-left" data-aos-duration="1200" class="hidden md:block">
                    <img class="w-full h-auto rounded-xl shadow-2xl" 
                              src="background2.png" 
                              alt="Illustration of software development and team collaboration">
                </div>
            </div>
        </section>

        <!-- Services Section -->
        <section id="services" class="py-20 sm:py-32 bg-prateckta-light">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center" data-aos="fade-up">
                    <h2 class="text-base text-prateckta-blue font-semibold tracking-wide uppercase">What We Offer</h2>
                    <p class="mt-2 text-4xl font-extrabold tracking-tight text-prateckta-dark sm:text-5xl">
                        Full Spectrum Digital Engineering
                    </p>
                    <p class="mt-4 max-w-3xl text-xl text-gray-600 mx-auto">
                        Our integrated services cover the entire value chain, ensuring speed, security, and scalability from concept to production.
                    </p>
                </div>
                <div class="mt-16 grid grid-cols-1 gap-10 md:grid-cols-2 lg:grid-cols-3">
                    
                    <!-- Service Card 1: Cloud & DevOps -->
                    <div class="card-hover pt-6 bg-white rounded-xl p-8 shadow-xl border-t-4 border-prateckta-blue" data-aos="zoom-in-up" data-aos-delay="100">
                        <div class="inline-flex items-center justify-center p-3 rounded-xl shadow-lg bg-prateckta-blue text-white mb-4">
                            <!-- Cloud Icon -->
                            <svg class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 15a4 4 0 004 4h9a5 5 0 10-.1-9.975 4 4 0 10-7.75 1.45L5.5 12.5H7.5M10 17v-4m-2 0h4m-2 0h-4"/></svg>
                        </div>
                        <h3 class="mt-2 text-2xl font-bold text-prateckta-dark">Cloud & DevOps</h3>
                        <p class="mt-3 text-gray-500">
                            AWS, Azure, GCP architecture, Kubernetes orchestration, CI/CD automation, and Site Reliability Engineering (SRE).
                        </p>
                    </div>
                    
                    <!-- Service Card 2: Data Intelligence -->
                    <div class="card-hover pt-6 bg-white rounded-xl p-8 shadow-xl border-t-4 border-prateckta-accent" data-aos="zoom-in-up" data-aos-delay="200">
                        <div class="inline-flex items-center justify-center p-3 rounded-xl shadow-lg bg-prateckta-accent text-white mb-4">
                            <!-- Data Icon -->
                            <svg class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 7h16M4 17h16M14 4h6M4 4h6M4 20h6M14 20h6"/></svg>
                        </div>
                        <h3 class="mt-2 text-2xl font-bold text-prateckta-dark">Data Intelligence</h3>
                        <p class="mt-3 text-gray-500">
                            Modern data platforms, ETL/ELT pipelines, real-time analytics, predictive modeling, and business intelligence (BI).
                        </p>
                    </div>
                    
                    <!-- Service Card 3: AI & Generative AI -->
                    <div class="card-hover pt-6 bg-white rounded-xl p-8 shadow-xl border-t-4 border-prateckta-blue" data-aos="zoom-in-up" data-aos-delay="300">
                        <div class="inline-flex items-center justify-center p-3 rounded-xl shadow-lg bg-prateckta-blue text-white mb-4">
                            <!-- AI Icon -->
                            <svg class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 3v2m6-2v2M9 19v2m6-2v2M5 12h2m10 0h2M3 9h2m14 0h2M3 15h2m14 0h2M11 5h2M11 19h2M12 2a10 10 0 100 20 10 10 0 000-20z"/></svg>
                        </div>
                        <h3 class="mt-2 text-2xl font-bold text-prateckta-dark">AI & Generative AI</h3>
                        <p class="mt-3 text-gray-500">
                            Custom ML/DL model development, NLP, computer vision, and building LLM-powered applications (RAG architectures).
                        </p>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- Industries Section -->
        <section id="industries" class="py-20 sm:py-32 bg-white">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="lg:grid lg:grid-cols-2 lg:gap-12 items-center">
                    <div data-aos="fade-right" data-aos-duration="1000">
                        <h2 class="text-base text-prateckta-accent font-semibold tracking-wide uppercase">Industry Depth</h2>
                        <p class="mt-2 text-4xl font-extrabold tracking-tight text-prateckta-dark sm:text-5xl">
                            Specialized Expertise for Complex Sectors
                        </p>
                        <p class="mt-4 text-xl text-gray-600">
                            Our team combines technical mastery with specific domain knowledge to deliver solutions that comply with industry regulations and address unique challenges.
                        </p>
                        
                        <div class="mt-8 space-y-4">
                            <div class="flex items-start space-x-3" data-aos="fade-up" data-aos-delay="100">
                                <svg class="flex-shrink-0 h-6 w-6 text-prateckta-blue mt-1" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8c1.657 0 3 .895 3 2s-1.343 2-3 2-3-.895-3-2 1.343-2 3-2zM12 20s-7-5.5-7-10s3-7 7-7 7 2.5 7 7-7 10-7 10z"/></svg>
                                <p class="text-lg font-semibold text-prateckta-dark">FinTech & Banking: <span class="font-normal text-gray-600">Compliance, core system modernization, secure payment gateways.</span></p>
                            </div>
                            <div class="flex items-start space-x-3" data-aos="fade-up" data-aos-delay="200">
                                <svg class="flex-shrink-0 h-6 w-6 text-prateckta-blue mt-1" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 11H5m14 0a2 2 0 012 2v6a2 2 0 01-2 2H5a2 2 0 01-2-2v-6a2 2 0 012-2m14 0V9a2 2 0 00-2-2M5 11V9a2 2 0 012-2m0 0V5a2 2 0 012-2h6a2 2 0 012 2v2M7 7h10"/></svg>
                                <p class="text-lg font-semibold text-prateckta-dark">Healthcare: <span class="font-normal text-gray-600">HIPAA readiness, EMR integration, remote patient monitoring systems.</span></p>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Industry Image Placeholder -->
                    <div data-aos="fade-left" data-aos-duration="1000" class="mt-10 lg:mt-0">
                        <img class="w-full h-auto rounded-xl shadow-2xl" 
                              src="background22.png" 
                              alt="Professional image representing industry expertise">
                    </div>
                </div>
            </div>
        </section>

        <!-- About Us/Our Values Section -->
        <section id="about" class="py-20 sm:py-32 bg-prateckta-dark text-white">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center" data-aos="fade-up">
                    <h2 class="text-base text-prateckta-accent font-semibold tracking-wide uppercase">Our Philosophy</h2>
                    <p class="mt-2 text-4xl font-extrabold tracking-tight sm:text-5xl">
                        A Partnership Built on Trust and Execution
                    </p>
                </div>
                <div class="mt-16 grid grid-cols-1 md:grid-cols-3 gap-8">
                    
                    <!-- Value 1: Transparency -->
                    <div class="text-center p-6 bg-gray-800 rounded-xl card-hover" data-aos="fade-up" data-aos-delay="100">
                        <h3 class="text-2xl font-bold mb-3 text-prateckta-blue">Transparency</h3>
                        <p class="text-gray-400">
                            We maintain open communication channels and provide clear, continuous updates. No black boxes, just honest, collaborative development.
                        </p>
                    </div>
                    
                    <!-- Value 2: Excellence -->
                    <div class="text-center p-6 bg-gray-800 rounded-xl card-hover" data-aos="fade-up" data-aos-delay="200">
                        <h3 class="text-2xl font-bold mb-3 text-prateckta-blue">Excellence</h3>
                        <p class="text-gray-400">
                            Our engineers are constantly learning and applying the newest standards in security, performance, and maintainability.
                        </p>
                    </div>
                    
                    <!-- Value 3: Impact -->
                    <div class="text-center p-6 bg-gray-800 rounded-xl card-hover" data-aos="fade-up" data-aos-delay="300">
                        <h3 class="text-2xl font-bold mb-3 text-prateckta-blue">Impact</h3>
                        <p class="text-gray-400">
                            We measure success not just by product delivery, but by the tangible business value and ROI we create for our clients.
                        </p>
                    </div>
                </div>
            </div>
        </section>

        <!-- CTA Section -->
        <section class="py-20 sm:py-32 bg-prateckta-light">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="bg-white p-10 lg:p-16 rounded-3xl shadow-2xl border-l-8 border-prateckta-accent" data-aos="zoom-in" data-aos-duration="800">
                    <div class="lg:grid lg:grid-cols-12 lg:gap-8 items-center">
                        <div class="lg:col-span-8">
                            <h3 class="text-4xl font-extrabold text-prateckta-dark mb-4">Your Next Big Idea Starts Here.</h3>
                            <p class="text-xl text-gray-600">
                                Let's discuss how our digital engineering teams can integrate with your vision to create something extraordinary.
                            </p>
                        </div>

                        <div class="mt-10 lg:mt-0 lg:col-span-4 flex justify-center lg:justify-end">
                            <a href="#contact" class="btn-primary inline-flex items-center justify-center px-10 py-4 border border-transparent text-lg font-semibold rounded-full text-white bg-prateckta-accent hover:bg-prateckta-blue shadow-lg">
                                Get Started Today
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- 
        ====================================================================
        NEW CONTACT FORM & DETAILS SECTION
        ==================================================================== 
        -->
        <section id="contact" class="py-20 sm:py-32 bg-white">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center mb-16" data-aos="fade-up">
                    <h2 class="text-base text-prateckta-blue font-semibold tracking-wide uppercase">Let's Connect</h2>
                    <p class="mt-2 text-4xl font-extrabold tracking-tight text-prateckta-dark sm:text-5xl">
                        Talk to Our Engineering Team
                    </p>
                    <p class="mt-4 max-w-3xl text-xl text-gray-600 mx-auto">
                        Fill out the inquiry form below or use the direct details to speak with an expert about your digital needs.
                    </p>
                </div>

                <!-- Contact Grid: Form and Details/Map -->
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-12" >
                    
                    <!-- Contact Form (Left) -->
                    <div data-aos="fade-right" data-aos-duration="1000" class="bg-prateckta-light p-8 sm:p-10 rounded-xl shadow-2xl">
                        <h3 class="text-3xl font-bold text-prateckta-dark mb-6">Send Us a Direct Inquiry</h3>
                        
                        <form id="contactForm" onsubmit="handleContactFormSubmit(event)" class="space-y-6">
                            
                            <div>
                                <label for="form_name" class="block text-sm font-medium text-gray-700 mb-1">Full Name</label>
                                <input type="text" id="form_name" name="name" required
                                    class="w-full px-4 py-3 border border-gray-300 rounded-lg shadow-sm focus:ring-prateckta-blue focus:border-prateckta-blue transition duration-150 ease-in-out"
                                    placeholder="Your Name">
                            </div>

                            <div>
                                <label for="form_email" class="block text-sm font-medium text-gray-700 mb-1">Work Email</label>
                                <input type="email" id="form_email" name="email" required
                                    class="w-full px-4 py-3 border border-gray-300 rounded-lg shadow-sm focus:ring-prateckta-blue focus:border-prateckta-blue transition duration-150 ease-in-out"
                                    placeholder="work@company.com">
                            </div>

                            <div>
                                <label for="form_service" class="block text-sm font-medium text-gray-700 mb-1">Area of Interest</label>
                                <select id="form_service" name="service" required
                                    class="w-full px-4 py-3 border border-gray-300 rounded-lg shadow-sm focus:ring-prateckta-blue focus:border-prateckta-blue transition duration-150 ease-in-out">
                                    <option value="" disabled selected>Select a Service...</option>
                                    <option value="cloud">Cloud & DevOps</option>
                                    <option value="data">Data Intelligence</option>
                                    <option value="ai">AI & Generative AI</option>
                                    <option value="general">General Inquiry</option>
                                </select>
                            </div>

                            <div>
                                <label for="form_message" class="block text-sm font-medium text-gray-700 mb-1">Project Details / Message</label>
                                <textarea id="form_message" name="message" rows="4" required
                                    class="w-full px-4 py-3 border border-gray-300 rounded-lg shadow-sm focus:ring-prateckta-blue focus:border-prateckta-blue transition duration-150 ease-in-out"
                                    placeholder="Briefly describe your project or question..."></textarea>
                            </div>

                            <button type="submit"
                                class="btn-primary w-full px-6 py-3 bg-prateckta-accent text-white font-semibold rounded-full shadow-md hover:bg-prateckta-blue focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-prateckta-accent transition duration-150 ease-in-out">
                                Submit Inquiry
                            </button>
                        </form>
                        <!-- Status Message Box -->
                        <div id="contactStatusMessage" class="mt-4 p-3 rounded-lg hidden" role="alert"></div>
                    </div>

                    <!-- Details & Map (Right) -->
                    <div data-aos="fade-left" data-aos-duration="1000" class="space-y-8">
                        
                        <!-- Information Details Block -->
                        <div class="p-8 bg-white rounded-xl shadow-xl border-t-4 border-prateckta-blue">
                            <h3 class="text-2xl font-bold text-prateckta-dark mb-4">Owner & Global Office</h3>
                            <div class="space-y-4">
                                <!-- Address -->
                                <div class="flex items-start space-x-3">
                                    <svg class="w-6 h-6 text-prateckta-accent flex-shrink-0 mt-1" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.828 0l-4.243-4.243a8 8 0 1111.314 0z"></path><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"></path></svg>
                                    <div>
                                        <p class="font-semibold text-prateckta-dark">Global Headquarters</p>
                                        <p class="text-gray-600">4500 Digital Avenue, Suite 700</p>
                                        <p class="text-gray-600">Tech Park, Bengaluru, 560103, India</p>
                                    </div>
                                </div>

                                <!-- Phone -->
                                <div class="flex items-start space-x-3">
                                    <svg class="w-6 h-6 text-prateckta-accent flex-shrink-0 mt-1" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"></path></svg>
                                    <div>
                                        <p class="font-semibold text-prateckta-dark">Sales & Inquiries</p>
                                        <a href="tel:+15551234567" class="text-prateckta-blue hover:text-prateckta-accent transition duration-150 font-medium">+1 (555) 123-4567 (US/Global)</a>
                                    </div>
                                </div>

                                <!-- Email -->
                                <div class="flex items-start space-x-3">
                                    <svg class="w-6 h-6 text-prateckta-accent flex-shrink-0 mt-1" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path></svg>
                                    <div>
                                        <p class="font-semibold text-prateckta-dark">General Contact</p>
                                        <a href="mailto:contact@pratecktasoft.com" class="text-prateckta-blue hover:text-prateckta-accent transition duration-150 font-medium">contact@pratecktasoft.com</a>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <!-- Map Placeholder -->
                        <div data-aos="zoom-in" data-aos-delay="200" class="h-64 w-full map-placeholder rounded-xl shadow-xl overflow-hidden">
                            <div class="text-xl p-4 w-full h-full flex items-center justify-center font-bold">
                                <map name="https://maps.app.goo.gl/E5H6ZMK2bs2zj3mE9"></map>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <!-- END CONTACT FORM & DETAILS SECTION -->


        <!-- Footer Section (Original dark section, ID changed to avoid conflict) -->
        <footer id="site-footer" class="bg-gray-900 pt-16 pb-8">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="grid grid-cols-2 gap-8 md:grid-cols-5">
                    
                    <!-- Company Info (Retained from original footer) -->
                    <div class="col-span-2 md:col-span-1" data-aos="fade-up" data-aos-delay="50">
                        <h3 class="text-3xl font-extrabold text-white tracking-tight mb-4">
                            Prateckta<span class="text-prateckta-blue">Soft</span>
                        </h3>
                        <p class="text-gray-400 text-sm mb-4">Building the future of digital commerce and enterprise technology.</p>
                        <!-- Contact Details - Removed phone/email here as they are now in the main contact section. -->
                    </div>

                    <!-- Quick Links -->
                    <div data-aos="fade-up" data-aos-delay="150">
                        <h3 class="text-lg font-semibold text-white mb-4">Company</h3>
                        <ul class="space-y-3">
                            <li><a href="#about" class="text-gray-400 hover:text-prateckta-blue text-sm transition duration-150">Our Story</a></li>
                            <li><a href="#" class="text-gray-400 hover:text-prateckta-blue text-sm transition duration-150">Careers</a></li>
                            <li><a href="#" class="text-gray-400 hover:text-prateckta-blue text-sm transition duration-150">Blog</a></li>
                        </ul>
                    </div>
                    <!-- Services -->
                    <div data-aos="fade-up" data-aos-delay="250">
                        <h3 class="text-lg font-semibold text-white mb-4">Solutions</h3>
                        <ul class="space-y-3">
                            <li><a href="#services" class="text-gray-400 hover:text-prateckta-blue text-sm transition duration-150">Cloud Adoption</a></li>
                            <li><a href="#services" class="text-gray-400 hover:text-prateckta-blue text-sm transition duration-150">Digital Products</a></li>
                            <li><a href="#services" class="text-gray-400 hover:text-prateckta-blue text-sm transition duration-150">AI Integration</a></li>
                        </ul>
                    </div>
                    <!-- Legal -->
                    <div data-aos="fade-up" data-aos-delay="350">
                        <h3 class="text-lg font-semibold text-white mb-4">Legal</h3>
                        <ul class="space-y-3">
                            <li><a href="#" class="text-gray-400 hover:text-prateckta-blue text-sm transition duration-150">Privacy Policy</a></li>
                            <li><a href="#" class="text-gray-400 hover:text-prateckta-blue text-sm transition duration-150">Terms of Service</a></li>
                        </ul>
                    </div>
                    <!-- Newsletter -->
                    <div class="col-span-2 md:col-span-1" data-aos="fade-up" data-aos-delay="450">
                        <h3 class="text-lg font-semibold text-white mb-4">Stay Updated</h3>
                        <form class="space-y-3">
                            <input type="email" placeholder="Enter your work email" class="w-full p-3 rounded-lg bg-gray-700 text-white placeholder-gray-400 focus:ring-prateckta-blue focus:border-prateckta-blue border-none">
                            <button type="submit" class="btn-primary w-full px-4 py-3 bg-prateckta-accent text-white font-semibold rounded-full hover:bg-prateckta-blue transition duration-300">Subscribe Now</button>
                        </form>
                    </div>

                </div>

                <div class="mt-16 border-t border-gray-700 pt-8 text-center" data-aos="fade-up" data-aos-delay="550">
                    <p class="text-base text-gray-400">
                        Copyright &copy; 2025 PratecktaSoft. All Rights Reserved.
                    </p>
                </div>
            </div>
        </footer>

    </main>

    <!-- 
    ====================================================================
    JAVASCRIPT: AOS Initialization & New Contact Form Handler 
    ==================================================================== 
    -->
    <script>
        // AOS Initialization Script (For animations)
        document.addEventListener('DOMContentLoaded', () => {
            AOS.init({
                duration: 1000, 
                once: true,
                delay: 50,
                offset: 50, // Trigger slightly earlier
            });
        });

        /**
         * Simulates contact form submission. 
         * In a live environment, this function would send data to a backend endpoint.
         */
        function handleContactFormSubmit(event) {
            event.preventDefault();

            const form = document.getElementById('contactForm');
            const statusMessage = document.getElementById('contactStatusMessage');
            const submitButton = form.querySelector('button[type="submit"]');

            const formData = {
                name: document.getElementById('form_name').value,
                email: document.getElementById('form_email').value,
                service: document.getElementById('form_service').value,
                message: document.getElementById('form_message').value
            };

            // Simple client-side validation check
            if (!formData.name || !formData.email || !formData.service || !formData.message) {
                displayMessage('Please ensure all fields are filled out correctly.', 'error');
                return;
            }

            // Disable button and show loading state
            submitButton.disabled = true;
            submitButton.textContent = 'Sending Message...';
            submitButton.classList.remove('bg-prateckta-accent');
            submitButton.classList.add('bg-gray-500');

            // Simulate server request delay
            setTimeout(() => {
                // Success Simulation
                displayMessage('Success! Your inquiry has been received. Our team will contact you within 24 hours.', 'success');
                form.reset(); 

                // Reset button state
                submitButton.disabled = false;
                submitButton.textContent = 'Submit Inquiry';
                submitButton.classList.remove('bg-gray-500');
                submitButton.classList.add('bg-prateckta-accent');

            }, 2500); // 2.5 second delay
        }

        /**
         * Displays a formatted status message (success or error).
         */
        function displayMessage(message, type) {
            const statusMessage = document.getElementById('contactStatusMessage');
            statusMessage.textContent = message;
            
            // Clear previous classes
            statusMessage.className = 'mt-4 p-3 rounded-lg';
            
            if (type === 'success') {
                statusMessage.classList.add('bg-green-100', 'text-green-800', 'border', 'border-green-400');
            } else if (type === 'error') {
                statusMessage.classList.add('bg-red-100', 'text-red-800', 'border', 'border-red-400');
            }
            
            statusMessage.classList.remove('hidden');
        }

    </script>
</body>
</html>
