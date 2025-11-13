<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>CV - Mohamed Miladi</title>
    <style>
      * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
      }

      body {
        font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
        line-height: 1.5;
        color: #333;
        background: #fff;
        font-size: 11px;
      }

      .container {
        max-width: 210mm;
        margin: 0 auto;
        padding: 15mm;
        background: white;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
      }

      .header {
        display: flex;
        align-items: center;
        gap: 18px;
        margin-bottom: 22px;
        padding-bottom: 18px;
        border-bottom: 2px solid #e6eefc;
      }

      .header .left {
        flex: 1 1 auto;
      }

      .header h1 {
        font-size: 30px;
        color: #0f172a;
        margin-bottom: 4px;
        font-weight: 800;
        letter-spacing: -0.5px;
      }

      .header h2 {
        font-size: 14px;
        color: #475569;
        margin-bottom: 6px;
        font-weight: 500;
      }

      .header h3 {
        font-size: 11px;
        color: #64748b;
        margin-bottom: 0;
        font-weight: 400;
      }

      .contact-info {
        display: flex;
        gap: 8px;
        flex-wrap: wrap;
        font-size: 11px;
        align-items: center;
      }

      .contact-info a {
        text-decoration: none;
        color: #0f172a;
        background: #eef2ff;
        padding: 6px 10px;
        border-radius: 20px;
        border: 1px solid rgba(15, 23, 42, 0.05);
      }

      .contact-info a:hover {
        background: #e0e7ff;
      }

      .contact-info a::after {
        content: " (" attr(href) ")";
        font-size: 9px;
        color: #64748b;
        font-weight: 400;
      }

      .contact-info a[href^="tel"]::after {
        content: "";
      }
      .contact-info a[href^="mailto"]::after {
        content: "";
      }

      .section {
        margin-bottom: 25px;
      }

      .section-title {
        font-size: 16px;
        color: #0f172a;
        margin-bottom: 12px;
        padding-bottom: 6px;
        border-bottom: 1px solid #eef2ff;
        font-weight: 700;
      }

      .profile-summary {
        background: #f8fafc;
        padding: 18px;
        border-radius: 8px;
        border-left: 4px solid #2563eb;
        margin-bottom: 20px;
        font-size: 11px;
        line-height: 1.6;
        text-align: justify;
      }

      .profile-summary strong {
        color: #1e40af;
      }

      .availability-box {
        background: #ecfdf5;
        padding: 10px 14px;
        border-radius: 6px;
        border-left: 3px solid #10b981;
        margin-top: 12px;
        font-size: 10px;
        display: flex;
        gap: 20px;
        flex-wrap: wrap;
      }

      .availability-box span {
        color: #065f46;
      }

      .availability-box strong {
        color: #047857;
      }

      /* Skill chips */
      .skill-chips {
        display: flex;
        flex-wrap: wrap;
        gap: 8px;
        margin-top: 10px;
      }

      .chip {
        background: #f1f5f9;
        border-radius: 999px;
        padding: 6px 10px;
        font-size: 10px;
        color: #0f172a;
        border: 1px solid rgba(15, 23, 42, 0.04);
      }

      .experience-item {
        margin-bottom: 20px;
        padding: 16px;
        background: linear-gradient(180deg, #ffffff, #fbfdff);
        border-radius: 8px;
        box-shadow: 0 1px 4px rgba(16, 24, 40, 0.04);
        border-left: 3px solid #10b981;
      }

      .experience-header {
        margin-bottom: 12px;
      }

      .company-role {
        font-size: 14px;
        font-weight: 600;
        color: #1e40af;
        margin-bottom: 4px;
      }

      .period-project {
        font-size: 10px;
        color: #6b7280;
        margin-bottom: 8px;
      }

      .achievement-category {
        margin-bottom: 15px;
      }

      .achievement-category h4 {
        font-size: 12px;
        color: #059669;
        margin-bottom: 8px;
        font-weight: 600;
      }

      .achievement-list {
        list-style: none;
        padding-left: 0;
      }

      .achievement-list li {
        margin-bottom: 6px;
        padding-left: 15px;
        position: relative;
        font-size: 10px;
        line-height: 1.4;
      }

      .achievement-list li::before {
        content: "▶";
        position: absolute;
        left: 0;
        color: #10b981;
        font-size: 8px;
      }

      .achievement-list li strong {
        color: #047857;
      }

      .skills-grid {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 20px;
        margin-bottom: 20px;
      }

      .skill-category {
        background: #fff;
        padding: 12px;
        border-radius: 6px;
        border-left: 3px solid #8b5cf6;
        box-shadow: 0 1px 2px rgba(16, 24, 40, 0.03);
      }

      .skill-category h4 {
        font-size: 12px;
        color: #7c3aed;
        margin-bottom: 8px;
        font-weight: 600;
      }

      .skill-category p {
        font-size: 10px;
        line-height: 1.4;
        color: #4b5563;
      }

      .leadership-skills {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        gap: 8px;
        margin-top: 10px;
      }

      .leadership-skill {
        background: #ecfdf5;
        padding: 8px 12px;
        border-radius: 4px;
        font-size: 10px;
        color: #065f46;
        border-left: 2px solid #10b981;
      }

      .education-languages {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 25px;
      }

      .education-item,
      .language-item {
        margin-bottom: 12px;
      }

      .education-item h4 {
        font-size: 12px;
        color: #1e40af;
        margin-bottom: 4px;
      }

      .education-item p {
        font-size: 10px;
        color: #6b7280;
      }

      .language-item {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 8px 12px;
        background: #f3f4f6;
        border-radius: 4px;
      }

      .language-item span:first-child {
        font-weight: 600;
        color: #374151;
      }

      .language-item span:last-child {
        color: #6b7280;
        font-size: 10px;
      }

      .projects-grid {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 12px;
      }

      .project-item {
        background: #eff6ff;
        padding: 15px;
        border-radius: 6px;
        border-left: 3px solid #3b82f6;
      }

      .project-item h4 {
        font-size: 12px;
        color: #1e40af;
        margin-bottom: 8px;
      }

      .project-item p {
        font-size: 10px;
        color: #4b5563;
        line-height: 1.4;
      }

      .footer {
        text-align: center;
        margin-top: 26px;
        padding-top: 18px;
        border-top: 1px solid #eef2ff;
        font-style: italic;
        color: #64748b;
        font-size: 10px;
      }

      .core-tech-grid {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 12px;
        margin-top: 12px;
      }

      .tech-category {
        background: #f8fafc;
        padding: 10px;
        border-radius: 4px;
        border-left: 3px solid #3b82f6;
      }

      .tech-category h4 {
        font-size: 11px;
        color: #1e40af;
        margin-bottom: 6px;
        font-weight: 600;
      }

      .tech-category p {
        font-size: 10px;
        color: #4b5563;
        line-height: 1.3;
      }

      .highlight-metric {
        color: #059669;
        font-weight: 600;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <!-- Header -->
      <div class="header">
        <div class="left">
          <h1>Mohamed Miladi</h1>
          <h2>
            Tech Lead Full Stack (React/Spring Boot) | 7+ years of experience
          </h2>
          <h3>Sfax, Tunisia | 100% Remote or Hybrid</h3>
        </div>
        <div class="contact-info">
          <a href="mailto:mohamed.miladi.dev@gmail.com"
            >mohamed.miladi.dev@gmail.com</a
          ><a href="tel:+21652713230">+216 52 713 230</a>
          <a
            href="https://linkedin.com/in/mohamed-miladi-dev"
            target="_blank"
            rel="noopener"
            >LinkedIn</a
          >
          <a
            href="https://github.com/MohamedMiladiDev"
            target="_blank"
            rel="noopener"
            >GitHub</a
          >
        </div>
      </div>

      <!-- Professional Summary -->
      <div class="section">
        <div class="section-title">Professional Summary</div>
        <div class="profile-summary">
          <strong>Senior Full Stack Developer</strong> with
          <strong>7+ years of production experience</strong> in React Native,
          Spring Boot, and scalable cloud architectures. Proven expertise in
          designing and developing mobile applications with MVP approaches,
          building high-performing APIs, and implementing cloud-native solutions
          across multiple regions. Strong background in
          <strong
            >Hexagonal Architecture, microservices, and software
            craftsmanship</strong
          >. Team leadership of <strong>5 developers</strong> delivering
          <strong>15+ applications</strong> serving
          <strong>50K+ active users</strong> handling
          <strong>10M+ requests/day</strong> with <strong>99.9% uptime</strong>.
          Passionate about clean code, testability, and building scalable
          systems with <strong>35% performance optimization</strong> and
          <strong>40% time-to-market reduction</strong>.

          <div class="availability-box">
            <span><strong>Availability:</strong> January 1, 2026</span>
            <span
              ><strong>Mobility:</strong> 3 days on-site in Paris + Remote</span
            >
            <span
              ><strong>Languages:</strong> Fluent French (C1) & English (C1 -
              Technical)</span
            >
          </div>
        </div>
      </div>

      <!-- Technical Skills -->
      <div class="section">
        <div class="section-title">Technical Skills</div>
        <div class="core-tech-grid">
          <div class="tech-category">
            <h4>Frontend & Mobile</h4>
            <p>
              <strong
                >React 18+, Next.js 13+, TypeScript 5.x, Redux Toolkit, React
                Query, React Native, Expo SDK, React Navigation, Zustand,
                Storybook, TailwindCSS, Vite, Webpack, Responsive Design</strong
              >
            </p>
          </div>
          <div class="tech-category">
            <h4>Backend & APIs</h4>
            <p>
              <strong
                >Spring Boot 3.x, Java 17, Spring Security, Spring Cloud, Spring
                Data JPA, Hibernate, RESTful APIs, GraphQL, Microservices
                Architecture, OAuth2, JWT, OpenAPI/Swagger, Clean Code, SOLID
                Principles</strong
              >
            </p>
          </div>
          <div class="tech-category">
            <h4>Databases & Cache</h4>
            <p>
              <strong
                >PostgreSQL, MySQL, Redis, Elasticsearch, Liquibase, Database
                Optimization, Query Tuning, Indexing Strategies, Schema
                Design</strong
              >
            </p>
          </div>
          <div class="tech-category">
            <h4>DevOps & Cloud</h4>
            <p>
              <strong
                >Docker, Kubernetes, Helm, Jenkins, GitHub Actions, GitLab CI,
                AWS (EC2, S3, Lambda, RDS), Terraform, Prometheus, Grafana, ELK
                Stack, Infrastructure as Code</strong
              >
            </p>
          </div>
          <div class="tech-category">
            <h4>Cloud & Scaling</h4>
            <p>
              <strong
                >Azure (App Service, SQL Database, Cosmos DB, Azure DevOps),
                Multi-region Deployment, Cloud-native Architecture, Scalable
                Applications, Infrastructure as Code, Container
                Orchestration</strong
              >
            </p>
          </div>
          <div class="tech-category">
            <h4>Messaging & Events</h4>
            <p>
              <strong
                >Apache Kafka, Apache Pulsar, RabbitMQ, Event-Driven
                Architecture, CQRS, Message Queues, Async Processing,
                Distributed Systems</strong
              >
            </p>
          </div>
          <div class="tech-category">
            <h4>Testing & Methodology</h4>
            <p>
              <strong
                >Jest, React Testing Library, Cypress, Playwright, JUnit,
                Mockito, SonarQube, TDD, E2E Testing, Agile/Scrum Methodology,
                Code Review, CI/CD Pipelines</strong
              >
            </p>
          </div>
        </div>
      </div>

      <!-- Professional Experience -->
      <div class="section">
        <div class="section-title">Professional Experience</div>

        <div class="experience-item">
          <div class="experience-header">
            <div class="company-role">
              <strong>Byrsa Tech</strong> (FinTech Startup, 25 employees) | Tech
              Lead React/React Native & Senior Spring Boot Developer
            </div>
            <div class="period-project">
              06/2020 – Present (5+ years) | Flagship Project: Defmarket
              (Decentralized Marketplace Platform)
            </div>
            <div
              class="period-project"
              style="color: #1e40af; font-weight: 600; margin-bottom: 12px"
            >
              Tech Stack: React Native, Expo SDK, Spring Boot 3.x, Java 17,
              GraphQL, PostgreSQL, Redis, Apache Kafka, AWS EKS, Docker,
              Kubernetes, GitHub Actions, TypeScript, Hexagonal Architecture,
              RESTful APIs, OAuth2/JWT
            </div>
          </div>

          <div class="achievement-category">
            <h4>Technical Leadership & Architecture</h4>
            <ul class="achievement-list">
              <li>
                <strong>Team Management:</strong> Direct management of 5
                developers (3 React/React Native, 2 Backend Spring Boot) with
                recruitment and onboarding of 3 juniors who became autonomous in
                6 months, achieving
                <span class="highlight-metric">60% team velocity increase</span>
              </li>
              <li>
                <strong>Technical Architecture:</strong> Definition of
                React/TypeScript standards and Spring Boot patterns with modular
                architecture reducing time-to-market by
                <span class="highlight-metric">40%</span> and enabling
                <span class="highlight-metric">85% code UI reusability</span>
              </li>
              <li>
                <strong>Agile/Scrum Methodology:</strong> Implementation of
                2-week sprints with monthly releases,
                <span class="highlight-metric">95% deadline compliance</span>
                and coordination with 5 product managers
              </li>
              <li>
                <strong>Code Review & Quality:</strong> 500+ reviews conducted
                maintaining
                <span class="highlight-metric">90%+ code coverage</span> with
                technical debt < 5% via SonarQube integration and quality gates
              </li>
              <li>
                <strong>Advanced Mentoring:</strong> 200+ hours of continuous
                training on React Native/Expo and Spring Boot with complete
                technical documentation
              </li>
            </ul>
          </div>

          <div class="achievement-category">
            <h4>Major Technical Achievements</h4>
            <ul class="achievement-list">
              <li>
                <strong>React Native Mobile Applications:</strong> Delivery of 5
                production React Native applications (iOS/Android with Expo SDK
                52+) totaling 100K+ downloads with 4.5★ average rating, constant
                60fps performance, MVP methodology, offline-first architecture,
                and modular component design ensuring
                <span class="highlight-metric">85% code reusability</span>
              </li>
              <li>
                <strong>Spring Boot APIs with GraphQL:</strong> Designed and
                implemented RESTful and GraphQL APIs handling 10M+ requests/day
                with hexagonal architecture, average response time < 200ms,
                JWT/OAuth2 authentication for multi-tenant systems, and database
                modeling optimization
              </li>
              <li>
                <strong>Cloud-Native Architecture:</strong> Architected scalable
                applications on AWS EKS with multi-region deployment
                capabilities, auto-scaling policies handling 5x traffic peaks,
                enabling seamless scaling across international sites
              </li>
              <li>
                <strong>TypeScript Migration & Code Quality:</strong> Complete
                JavaScript to TypeScript migration (50K+ lines) with strict mode
                achieving
                <span class="highlight-metric">90%+ code coverage</span>,
                reducing production bugs by
                <span class="highlight-metric">70%</span>, demonstrating
                software craftsmanship excellence
              </li>
              <li>
                <strong>Event-Driven Architecture:</strong> Apache Pulsar
                integration processing 500K+ events/day with CQRS patterns,
                reducing asynchronous transaction latency by
                <span class="highlight-metric">60%</span>
              </li>
              <li>
                <strong>CI/CD & DevOps:</strong> GitHub Actions pipelines
                enabling 50+ deployments/month in < 15min with zero downtime,
                Git-based workflow, automated testing on multiple environments
              </li>
              <li>
                <strong>Observability & Monitoring:</strong> Prometheus/Grafana
                stack with 30+ real-time dashboards reducing MTTR by
                <span class="highlight-metric">70%</span>, proactive incident
                detection, performance metrics tracking
              </li>
            </ul>
          </div>
        </div>

        <div class="experience-item">
          <div class="experience-header">
            <div class="company-role">
              <strong>PRIMATEC Engineering</strong> (Automotive SME, 150
              employees) | Backend Developer
            </div>
            <div class="period-project">
              01/2020 – 04/2020 (4 months - Contract) | Specialization: IoT
              Car-sharing Solutions
            </div>
            <div
              class="period-project"
              style="color: #1e40af; font-weight: 600; margin-bottom: 12px"
            >
              Tech Stack: Python, Java, Spring Boot, GitLab CI, Automated
              Testing Frameworks, Embedded Systems, IoT Protocols, CI/CD
              Pipelines
            </div>
          </div>

          <div class="achievement-category">
            <h4>Automation & Performance</h4>
            <ul class="achievement-list">
              <li>
                <strong>Automated Testing Framework:</strong> Design of a Python
                tool for embedded system testing reducing test times by 30%
                (from 4h to 2h45) with 85%+ scenario coverage
              </li>
              <li>
                <strong>CI/CD Pipeline:</strong> GitLab CI implementation with
                automated tests on 3 environments enabling 40+ automatic
                deployments and detecting 95% of regressions
              </li>
              <li>
                <strong>System Stability:</strong> Resolution of 50+ critical
                bugs in coordination with QA team improving stability by 40% and
                reducing production incidents by 60%
              </li>
            </ul>
          </div>
        </div>

        <div class="experience-item">
          <div class="experience-header">
            <div class="company-role">
              <strong>ABS Computer</strong> (ERP Editor, 80 employees) | Full
              Stack ERP Developer & Mobile Applications Specialist
            </div>
            <div class="period-project">
              07/2017 – 12/2019 (2.5 years) | ERP Integrant (Java/Spring) &
              business mobile applications (Android/iOS)
            </div>
            <div
              class="period-project"
              style="color: #1e40af; font-weight: 600; margin-bottom: 12px"
            >
              Tech Stack: Java, Android, iOS, Windev Mobile, Webdev, REST APIs,
              MySQL, PostgreSQL, RBAC Security, Authentication Systems, Mobile
              Development
            </div>
          </div>

          <div class="achievement-category">
            <h4>ERP Development & Mobile Applications</h4>
            <ul class="achievement-list">
              <li>
                <strong>RBAC Security Module:</strong> Complete design of
                authentication/authorization system for 500+ users with granular
                management of 50+ roles and 200+ permissions including complete
                audit trail
              </li>
              <li>
                <strong>Customer Management System (CRM):</strong>
                Development of license management module for 1000+ clients with
                renewal automation reducing administrative time by 50%
              </li>
              <li>
                <strong>Professional Mobile Applications:</strong>
                Delivery of Smart Restaurant (deployed in 30+ establishments,
                200+ orders/day) and Routier (used by 100+ sales reps, 500+
                orders/day) with real-time synchronization and offline mode
              </li>
              <li>
                <strong>Redis Optimization:</strong> Distributed cache
                architecture reducing response times by 35% (from 2.5s to 1.6s)
                and API calls by 70%, supporting 1000+ concurrent users
              </li>
              <li>
                <strong>Data Migration:</strong> Migration of 3 legacy databases
                (2M+ records) to modern architecture with zero data loss and <
                4h downtime
              </li>
            </ul>
          </div>
        </div>
      </div>

      <!-- Innovation Projects -->
      <div class="section">
        <div class="section-title">Innovation Projects</div>
        <div class="projects-grid">
          <div class="project-item">
            <h4>Logistics Management Platform</h4>
            <p style="margin-bottom: 6px">
              <strong>Tech Stack:</strong> React 18, Next.js 13, TypeScript,
              Spring Boot 3.x, PostgreSQL, Redis, Kubernetes
            </p>
            <p style="margin-bottom: 6px">
              Complete solution for delivery planning and real-time tracking
              with route optimization and advanced analytics dashboard
            </p>
            <p style="font-size: 9px; color: #059669">
              ✓ 3000+ deliveries/day ✓ 25% logistics cost reduction ✓ Real-time
              < 2s
            </p>
          </div>
          <div class="project-item">
            <h4>AI Chatbot Assistant</h4>
            <p style="margin-bottom: 6px">
              <strong>Tech Stack:</strong> React 18, Next.js 13, TypeScript,
              LangChain, OpenAI, Supabase
            </p>
            <p style="margin-bottom: 6px">
              Intelligent multi-channel chatbot capable of answering users and
              triggering automated actions on site with continuous learning
            </p>
            <p style="font-size: 9px; color: #059669">
              ✓ 85% queries resolved without support ✓ Response time < 3s ✓
              Satisfaction 4.7/5
            </p>
          </div>
        </div>
      </div>

      <!-- Leadership & Management -->
      <div class="section">
        <div class="section-title">Leadership & Management</div>
        <div class="leadership-skills">
          <div class="leadership-skill">
            <strong>Tech Leadership:</strong> Management of 5-person developer
            team with recruitment of 3 juniors and 60% velocity increase
          </div>
          <div class="leadership-skill">
            <strong>Architecture Decisions:</strong> Definition of technical
            standards and modular architecture reducing time-to-market by 40%
          </div>
          <div class="leadership-skill">
            <strong>Technical Mentoring:</strong> 200+ hours of training on
            React/TypeScript/Spring Boot with 3 developers becoming autonomous
            in 6 months
          </div>
          <div class="leadership-skill">
            <strong>Agile Project Management:</strong> 24 Scrum sprints with 95%
            deadline compliance and coordination with 5 product managers
          </div>
          <div class="leadership-skill">
            <strong>Code Review & Quality:</strong> 500+ reviews maintaining
            90%+ code coverage with technical debt < 5%
          </div>
          <div class="leadership-skill">
            <strong>Stakeholder Communication:</strong> Monthly presentations
            simplifying technical concepts for business decisions
          </div>
          <div class="leadership-skill">
            <strong>Continuous Improvement:</strong> Sprint cycle reduction from
            3 to 2 weeks with refactoring reducing debt by 40%
          </div>
          <div class="leadership-skill">
            <strong>Incident Management:</strong> On-call system reducing MTTR
            by 70% via proactive detection
          </div>
        </div>
      </div>

      <!-- Education & Languages -->
      <div class="section">
        <div class="section-title">Education & Languages</div>
        <div class="education-languages">
          <div>
            <h3 style="font-size: 14px; color: #1e40af; margin-bottom: 15px">
              Education
            </h3>
            <div class="education-item">
              <h4>
                Master's Degree | Computer Networks and Telecommunications
              </h4>
              <p>ENET'COM Sfax | 2015 – 2017</p>
            </div>
            <div class="education-item">
              <h4>Bachelor's Degree | Network Systems</h4>
              <p>ENET'COM Sfax | 2012 – 2015</p>
            </div>
            <div
              style="
                margin-top: 16px;
                padding: 10px;
                background: #fef3c7;
                border-radius: 4px;
                border-left: 3px solid #f59e0b;
              "
            >
              <p style="font-size: 10px; color: #78350f; margin-bottom: 4px">
                <strong>Continuous Learning Active</strong>
              </p>
              <p style="font-size: 9px; color: #92400e">
                Udemy and daily technology watch
              </p>
            </div>
          </div>

          <div>
            <h3 style="font-size: 14px; color: #1e40af; margin-bottom: 15px">
              Languages
            </h3>
            <div class="language-item">
              <span>Arabic</span>
              <span>Native</span>
            </div>
            <div class="language-item">
              <span>French</span>
              <span>Fluent (C1)</span>
            </div>
            <div class="language-item">
              <span>English</span>
              <span>Fluent (C1 - Technical)</span>
            </div>
          </div>
        </div>
      </div>

      <!-- Footer -->
      <div class="footer">
        Full Stack Tech Lead available for ambitious technical challenges and
        development team management
      </div>
    </div>
  </body>
</html>
