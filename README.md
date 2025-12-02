<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Leaving Cert Grinds - Computer Science &amp; Maths Tuition</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #2563eb;
            --primary-dark: #1d4ed8;
            --primary-light: #3b82f6;
            --secondary: #10b981;
            --accent: #f59e0b;
            --text: #1f2937;
            --text-light: #6b7280;
            --bg: #f9fafb;
            --bg-card: #ffffff;
            --border: #e5e7eb;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', sans-serif;
            line-height: 1.6;
            color: var(--text);
            background: var(--bg);
        }

        header {
            background: var(--bg-card);
            border-bottom: 1px solid var(--border);
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 1px 3px rgba(0,0,0,0.05);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 1rem 2rem;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary);
            text-decoration: none;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        nav a {
            text-decoration: none;
            color: var(--text);
            font-weight: 500;
            transition: color 0.3s;
            cursor: pointer;
        }

        nav a:hover, nav a.active {
            color: var(--primary);
        }

        .hero {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 6rem 2rem;
            text-align: center;
        }

        .hero-content {
            max-width: 900px;
            margin: 0 auto;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            font-weight: 800;
        }

        .hero p {
            font-size: 1.25rem;
            margin-bottom: 2rem;
            opacity: 0.95;
        }

        .btn-primary {
            background: var(--secondary);
            color: white;
            padding: 1rem 2rem;
            border: none;
            border-radius: 8px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            text-decoration: none;
            display: inline-block;
        }

        .btn-primary:hover {
            background: #059669;
            transform: translateY(-2px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        section {
            padding: 4rem 0;
        }

        .section-title {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            text-align: center;
            color: var(--text);
        }

        .section-subtitle {
            text-align: center;
            color: var(--text-light);
            font-size: 1.1rem;
            margin-bottom: 3rem;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        .subjects {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .subject-card {
            background: var(--bg-card);
            padding: 2rem;
            border-radius: 12px;
            border: 1px solid var(--border);
            text-align: center;
            transition: all 0.3s;
        }

        .subject-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            border-color: var(--primary);
        }

        .subject-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .subject-card h3 {
            color: var(--primary);
            margin-bottom: 0.5rem;
        }

        .subject-card p {
            color: var(--text-light);
            line-height: 1.8;
        }

        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .feature {
            display: flex;
            gap: 1rem;
        }

        .feature-icon {
            font-size: 1.5rem;
            color: var(--secondary);
            flex-shrink: 0;
        }

        .feature h4 {
            color: var(--text);
            margin-bottom: 0.5rem;
        }

        .feature p {
            color: var(--text-light);
        }

        .reviews-section {
            background: var(--bg);
        }

        .review-card {
            background: var(--bg-card);
            padding: 2rem;
            border-radius: 12px;
            border-left: 4px solid var(--primary);
            margin-bottom: 1.5rem;
        }

        .review-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1rem;
        }

        .reviewer-name {
            font-weight: 600;
            color: var(--text);
        }

        .stars {
            color: var(--accent);
            font-size: 1.1rem;
            letter-spacing: 2px;
        }

        .review-text {
            color: var(--text-light);
            line-height: 1.8;
            font-style: italic;
        }

        .about-section {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border-radius: 12px;
            padding: 3rem;
            margin: 2rem 0;
        }

        .about-section h3 {
            font-size: 2rem;
            margin-bottom: 1rem;
        }

        .about-section p {
            font-size: 1.1rem;
            line-height: 1.9;
            margin-bottom: 1rem;
        }

        .contact-section {
            background: var(--bg);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
            color: var(--text);
        }

        input, select, textarea {
            width: 100%;
            padding: 0.75rem;
            border: 1px solid var(--border);
            border-radius: 8px;
            font-family: inherit;
            font-size: 1rem;
            transition: border-color 0.3s;
        }

        input:focus, select:focus, textarea:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 3px rgba(37, 99, 235, 0.1);
        }

        textarea {
            resize: vertical;
            min-height: 120px;
        }

        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1rem;
        }

        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
        }

        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 2rem;
        }

        .contact-item {
            display: flex;
            gap: 1rem;
        }

        .contact-icon {
            font-size: 1.5rem;
            color: var(--primary);
            flex-shrink: 0;
        }

        .contact-item h4 {
            margin-bottom: 0.25rem;
        }

        .contact-item p {
            color: var(--text-light);
            margin: 0;
        }

        footer {
            background: var(--text);
            color: white;
            padding: 2rem;
            text-align: center;
            margin-top: 4rem;
        }

        .testimonials-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .success-message {
            display: none;
            background: #d1fae5;
            color: #065f46;
            padding: 1rem;
            border-radius: 8px;
            margin-bottom: 1rem;
            border: 1px solid #a7f3d0;
        }

        .success-message.show {
            display: block;
        }

        .page {
            display: none;
        }

        .page.active {
            display: block;
        }

        @media (max-width: 768px) {
            nav ul {
                gap: 1rem;
            }

            .hero h1 {
                font-size: 2rem;
            }

            .section-title {
                font-size: 1.8rem;
            }

            .form-row {
                grid-template-columns: 1fr;
            }

            .contact-content {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <nav>
            <a class="logo">📚 Leaving Cert Grinds</a>
            <ul>
                <li><a class="nav-link active" data-page="home">Home</a></li>
                <li><a class="nav-link" data-page="subjects">Subjects</a></li>
                <li><a class="nav-link" data-page="reviews">Reviews</a></li>
                <li><a class="nav-link" data-page="contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- HOME PAGE -->
    <div id="home" class="page active">
        <section class="hero">
            <div class="hero-content">
                <h1>Ace Your Leaving Cert</h1>
                <p>Expert grinds in Computer Science &amp; Maths for students across Ireland</p>
                <button class="btn-primary" onclick="navigateTo('contact')">Book a Class Now</button>
            </div>
        </section>

        <section class="container">
            <h2 class="section-title">Why Choose Us?</h2>
            <p class="section-subtitle">Professional tutoring designed to maximize your exam performance</p>
            <div class="features">
                <div class="feature">
                    <div class="feature-icon">🎯</div>
                    <div>
                        <h4>Exam-Focused</h4>
                        <p>Tailored lessons based on the latest Leaving Cert syllabus and exam papers</p>
                    </div>
                </div>
                <div class="feature">
                    <div class="feature-icon">👨‍🏫</div>
                    <div>
                        <h4>Expert Tutors</h4>
                        <p>Experienced tutors with proven track records of student success</p>
                    </div>
                </div>
                <div class="feature">
                    <div class="feature-icon">📈</div>
                    <div>
                        <h4>Results Guaranteed</h4>
                        <p>Average student improvement: +15 points in final exam scores</p>
                    </div>
                </div>
                <div class="feature">
                    <div class="feature-icon">⏰</div>
                    <div>
                        <h4>Flexible Scheduling</h4>
                        <p>Classes available before school, after school, and weekends</p>
                    </div>
                </div>
                <div class="feature">
                    <div class="feature-icon">💻</div>
                    <div>
                        <h4>Online &amp; In-Person</h4>
                        <p>Choose between online lessons via Zoom or face-to-face tuition</p>
                    </div>
                </div>
                <div class="feature">
                    <div class="feature-icon">📝</div>
                    <div>
                        <h4>Detailed Progress Reports</h4>
                        <p>Weekly progress tracking and personalized feedback on your improvement</p>
                    </div>
                </div>
            </div>
        </section>

        <section class="container about-section">
            <h3>About Our Tutoring Service</h3>
            <p>We&rsquo;ve been helping students excel in their Leaving Cert exams since 2019. Our team of dedicated tutors brings years of teaching experience and deep expertise in Computer Science and Higher Level Maths.</p>
            <p>Whether you&rsquo;re struggling with algorithms and data structures or mastering differential equations, we have the right tutor to guide you to success. Our personalized approach ensures every student reaches their full potential.</p>
        </section>
    </div>

    <!-- SUBJECTS PAGE -->
    <div id="subjects" class="page">
        <section class="container">
            <h2 class="section-title">Our Subjects</h2>
            <p class="section-subtitle">Comprehensive coverage of Leaving Cert Computer Science and Higher Level Maths</p>
            <div class="subjects">
                <div class="subject-card">
                    <div class="subject-icon">💻</div>
                    <h3>Computer Science</h3>
                    <p><strong>Topics covered:</strong> Data Representation, Networking, Cybersecurity, Software Development, Computational Thinking, Programming (Python/Java), Algorithms, Data Structures, Boolean Logic, and more</p>
                    <p style="margin-top: 1rem; color: var(--secondary); font-weight: 600;">Higher Level: €40/session | Ordinary Level: €30/session</p>
                </div>
                <div class="subject-card">
                    <div class="subject-icon">📐</div>
                    <h3>Higher Level Maths</h3>
                    <p><strong>Topics covered:</strong> Algebra, Functions, Calculus, Trigonometry, Complex Numbers, Sequences &amp; Series, Differential Equations, Linear Algebra, Probability, and Statistics</p>
                    <p style="margin-top: 1rem; color: var(--secondary); font-weight: 600;">Higher Level: €40/session | Ordinary Level: €30/session</p>
                </div>
                <div class="subject-card">
                    <div class="subject-icon">📦</div>
                    <h3>Combination Packages</h3>
                    <p><strong>Get better value:</strong> Take both Computer Science and Maths together and receive 15% discount on combined tuition hours</p>
                    <p style="margin-top: 1rem; color: var(--secondary); font-weight: 600;">Combined: €65/2-hour session</p>
                </div>
            </div>

            <h2 class="section-title" style="margin-top: 4rem;">Our Teaching Approach</h2>
            <div class="features" style="margin-top: 2rem;">
                <div class="feature">
                    <div class="feature-icon">🔍</div>
                    <div>
                        <h4>Diagnostic Assessment</h4>
                        <p>First session includes a full assessment to identify knowledge gaps and learning style</p>
                    </div>
                </div>
                <div class="feature">
                    <div class="feature-icon">🎓</div>
                    <div>
                        <h4>Personalized Curriculum</h4>
                        <p>Customized lesson plans tailored to your specific needs and exam goals</p>
                    </div>
                </div>
                <div class="feature">
                    <div class="feature-icon">✅</div>
                    <div>
                        <h4>Mock Exams</h4>
                        <p>Regular practice with past papers and mock exams under exam conditions</p>
                    </div>
                </div>
                <div class="feature">
                    <div class="feature-icon">💬</div>
                    <div>
                        <h4>Email Support</h4>
                        <p>Ongoing email and WhatsApp support between sessions for quick questions</p>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <!-- REVIEWS PAGE -->
    <div id="reviews" class="page">
        <section class="container reviews-section">
            <h2 class="section-title">Student Reviews</h2>
            <p class="section-subtitle">See what our students have to say about their experience</p>

            <div class="testimonials-grid">
                <div class="review-card">
                    <div class="review-header">
                        <span class="reviewer-name">Sarah O&rsquo;Brien, Dublin</span>
                        <span class="stars">★★★★★</span>
                    </div>
                    <p class="review-text">&ldquo;I was struggling with Computer Science algorithms, but after just 6 weeks of grinds, everything clicked. The tutor broke down complex concepts into simple explanations. I went from a D to an A in my mocks!&rdquo;</p>
                </div>

                <div class="review-card">
                    <div class="review-header">
                        <span class="reviewer-name">Aoife Murphy, Cork</span>
                        <span class="stars">★★★★★</span>
                    </div>
                    <p class="review-text">&ldquo;Differential equations were my nightmare until I started grinds here. The step-by-step approach and practice problems really helped me understand the concepts. Highly recommended!&rdquo;</p>
                </div>

                <div class="review-card">
                    <div class="review-header">
                        <span class="reviewer-name">James Keane, Galway</span>
                        <span class="stars">★★★★★</span>
                    </div>
                    <p class="review-text">&ldquo;Taking both Maths and CS grinds saved me so much money with the combination package. Both tutors are exceptional and really know their stuff. I&rsquo;ve improved so much in both subjects.&rdquo;</p>
                </div>

                <div class="review-card">
                    <div class="review-header">
                        <span class="reviewer-name">Emma Walsh, Limerick</span>
                        <span class="stars">★★★★★</span>
                    </div>
                    <p class="review-text">&ldquo;The mock exams under timed conditions really helped me prepare for the real thing. Went from band 3 to band 1 in the actual Leaving Cert. Worth every euro!&rdquo;</p>
                </div>

                <div class="review-card">
                    <div class="review-header">
                        <span class="reviewer-name">Sean Doyle, Belfast</span>
                        <span class="stars">★★★★★</span>
                    </div>
                    <p class="review-text">&ldquo;Started grinds in 5th year when I was seriously behind. The tutors caught me up and I ended up getting a respectable grade. The flexibility with online sessions was perfect with my schedule.&rdquo;</p>
                </div>

                <div class="review-card">
                    <div class="review-header">
                        <span class="reviewer-name">Rachel Lynch, Waterford</span>
                        <span class="stars">★★★★★</span>
                    </div>
                    <p class="review-text">&ldquo;Finally someone who can explain boolean logic in a way that makes sense! The tutor is patient, knowledgeable, and actually cares about student progress. Best investment for my education.&rdquo;</p>
                </div>
            </div>

            <div style="background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); color: white; padding: 2rem; border-radius: 12px; text-align: center; margin-top: 3rem;">
                <h3 style="margin-bottom: 0.5rem;">Average Student Results</h3>
                <p style="font-size: 1.2rem; margin: 0.5rem 0;"><strong>+15 points</strong> average improvement in exam scores</p>
                <p style="font-size: 1.2rem; margin: 0.5rem 0;"><strong>93%</strong> of students move up at least one grade band</p>
                <p style="font-size: 1.2rem; margin: 0.5rem 0;"><strong>4.9/5</strong> average rating from 240+ reviews</p>
            </div>
        </section>
    </div>

    <!-- CONTACT PAGE -->
    <div id="contact" class="page">
        <section class="container contact-section">
            <h2 class="section-title">Book Your Class</h2>
            <p class="section-subtitle">Get in touch to arrange your personalized grinds</p>

            <div class="contact-content">
                <div class="contact-info">
                    <div class="contact-item">
                        <div class="contact-icon">📍</div>
                        <div>
                            <h4>Location</h4>
                            <p>Letterkenny, Co. Donegal, Ireland</p>
                            <p style="font-size: 0.9rem; margin-top: 0.25rem;">Online and in-person sessions available</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">📞</div>
                        <div>
                            <h4>Phone</h4>
                            <p>+353 (0) 74 912 3456</p>
                            <p style="font-size: 0.9rem; margin-top: 0.25rem;">Available 9am-9pm, 7 days a week</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">✉️</div>
                        <div>
                            <h4>Email</h4>
                            <p>contact@leavingcertgrinds.ie</p>
                            <p style="font-size: 0.9rem; margin-top: 0.25rem;">Response within 2 hours</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">⏱️</div>
                        <div>
                            <h4>Response Time</h4>
                            <p>Fast turnaround on booking requests</p>
                            <p style="font-size: 0.9rem; margin-top: 0.25rem;">Most bookings confirmed within 24 hours</p>
                        </div>
                    </div>
                </div>

                <div>
                    <div class="success-message" id="successMessage">
                        ✅ Thank you! We&rsquo;ll be in touch shortly to confirm your booking.
                    </div>

                    <form id="contactForm" onsubmit="handleSubmit(event)">
                        <div class="form-row">
                            <div class="form-group">
                                <label for="name">Full Name *</label>
                                <input type="text" id="name" name="name" required>
                            </div>
                            <div class="form-group">
                                <label for="email">Email Address *</label>
                                <input type="email" id="email" name="email" required>
                            </div>
                        </div>

                        <div class="form-row">
                            <div class="form-group">
                                <label for="phone">Phone Number</label>
                                <input type="tel" id="phone" name="phone">
                            </div>
                            <div class="form-group">
                                <label for="school">School Name</label>
                                <input type="text" id="school" name="school">
                            </div>
                        </div>

                        <div class="form-group">
                            <label for="subject">Subject *</label>
                            <select id="subject" name="subject" required>
                                <option value="">Select a subject</option>
                                <option value="computer-science">Computer Science (Higher)</option>
                                <option value="computer-science-ordinary">Computer Science (Ordinary)</option>
                                <option value="maths">Maths (Higher)</option>
                                <option value="maths-ordinary">Maths (Ordinary)</option>
                                <option value="both">Both Subjects</option>
                            </select>
                        </div>

                        <div class="form-group">
                            <label for="level">Current Level in Subject *</label>
                            <select id="level" name="level" required>
                                <option value="">Select your current level</option>
                                <option value="struggling">Struggling (Below D)</option>
                                <option value="below-average">Below Average (D-C)</option>
                                <option value="average">Average (C-B)</option>
                                <option value="good">Good (B-A)</option>
                                <option value="excellent">Excellent (A+)</option>
                            </select>
                        </div>

                        <div class="form-group">
                            <label for="format">Preferred Format *</label>
                            <select id="format" name="format" required>
                                <option value="">Select format</option>
                                <option value="online">Online (Zoom)</option>
                                <option value="in-person">In-Person</option>
                                <option value="flexible">Flexible (Both)</option>
                            </select>
                        </div>

                        <div class="form-group">
                            <label for="availability">When can you attend? *</label>
                            <select id="availability" name="availability" required>
                                <option value="">Select availability</option>
                                <option value="weekday-morning">Weekday Morning (8-12)</option>
                                <option value="weekday-afternoon">Weekday Afternoon (12-17)</option>
                                <option value="weekday-evening">Weekday Evening (17-21)</option>
                                <option value="weekend">Weekends</option>
                                <option value="flexible">Flexible</option>
                            </select>
                        </div>

                        <div class="form-group">
                            <label for="message">Additional Information</label>
                            <textarea id="message" name="message" placeholder="Tell us about your specific needs, goals, or any questions you have..."></textarea>
                        </div>

                        <button type="submit" class="btn-primary" style="width: 100%; font-size: 1.1rem; padding: 1.2rem;">
                            Request a Booking
                        </button>
                    </form>
                </div>
            </div>
        </section>
    </div>

    <footer>
        <p>&copy; 2025 Leaving Cert Grinds. All rights reserved. | Trusted by 500+ students | Based in Letterkenny, Donegal</p>
    </footer>

    <script>
        function navigateTo(pageId) {
            // Hide all pages
            const pages = document.querySelectorAll('.page');
            pages.forEach(page => page.classList.remove('active'));

            // Show selected page
            document.getElementById(pageId).classList.add('active');

            // Update nav links
            const navLinks = document.querySelectorAll('.nav-link');
            navLinks.forEach(link => link.classList.remove('active'));
            document.querySelector(`[data-page="${pageId}"]`).classList.add('active');

            // Scroll to top
            window.scrollTo(0, 0);
        }

        function handleSubmit(event) {
            event.preventDefault();

            // Collect form data
            const formData = {
                name: document.getElementById('name').value,
                email: document.getElementById('email').value,
                phone: document.getElementById('phone').value,
                school: document.getElementById('school').value,
                subject: document.getElementById('subject').value,
                level: document.getElementById('level').value,
                format: document.getElementById('format').value,
                availability: document.getElementById('availability').value,
                message: document.getElementById('message').value
            };

            // Show success message
            document.getElementById('successMessage').classList.add('show');

            // Reset form
            document.getElementById('contactForm').reset();

            // Hide message after 5 seconds
            setTimeout(() => {
                document.getElementById('successMessage').classList.remove('show');
            }, 5000);

            console.log('Booking request:', formData);
        }

        // Navigation click handlers
        document.querySelectorAll('.nav-link').forEach(link => {
            link.addEventListener('click', function(e) {
                e.preventDefault();
                navigateTo(this.dataset.page);
            });
        });
    </script>
</body>
</html>
