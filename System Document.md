## **1. Introduction**

This document is prepared as part of deliverable 2 for the Consortia Management System project, aiming to provide a detailed overview of domain analysis and the initial interface designs based on the system's goals. The deliverable is structured into several key sections, including the domain description, initial description of the problem, interface prototypes, and a summary of the team roles and contributions, ensuring a comprehensive approach to the system's development.

### **Glossary / List of Acronyms**

- **CMS**: Consortia Management System
- **KFUPM**: King Fahd University of Petroleum and Minerals
- **IPMS**: Industry Partnership Management System
- **R&D**: Research and Development

### **References**

- [***Pure KFUPM***](http://pure.kfupm.edu.sa/)
- [Drawio](https://www.notion.so/2nd-Phase-590a46ffd0fd420484fb7844b3415919?pvs=21)
- [Consortia  (kfupm.edu.sa)](https://ri.kfupm.edu.sa/research-centers/consortia)
- Figma
- Material3 UI Kit


## 2. Domain description (UML Class Diagram)

![UML Diagrams](###)

## 3. Initial description of the problem

### 3.1. Stakeholders and Their Goals

**Stakeholders**

1. **KFUPM (King Fahd University of Petroleum & Minerals)**
2. **Industrial End Users (e.g., SABIC, Aramco, Maadn)**
3. **Governmental/Regulatory Entities (e.g., RDIA, Ministry of Energy, PIF)**
4. **Technology Developers/Providers (e.g., HoneyWell, SIRC, ExonMobil)**
5. **Academic/Research Institutions (e.g., KACST, KAUST)**

**Goals**

1. **KFUPM**
    - **G1:** Ensure compliance with IT security and privacy standards.
    - **G2:** Facilitate efficient communication and collaboration among consortia members.
    - **G3:** Provide a dashboard for tracking the status of agreements and project outcomes.
    - **G4:** Maintain version control for all agreement documents.
    - **G5:** Enable resource sharing among consortia members.
2. **Industrial End Users**
    - **G6:** Share financial burdens and risks associated with R&D projects.
    - **G7:** Gain access to specialized equipment and intellectual property.
3. **Governmental/Regulatory Entities**
    - **G8:** Ensure that consortia activities align with national research and development goals.
    - **G9:** Monitor compliance with regulatory standards and practices.
    - **G10:** Facilitate the formation of committees and define research themes.
4. **Technology Developers/Providers**
    - **G12:** Collaborate on innovative technology development projects.
    - **G13:** Share expertise and technical knowledge with consortia members.
5. **Academic/Research Institutions**
    - **G14:** Tracking the fund for research projects properly.
    - **G15:** Publish research findings and contribute to scientific knowledge.

### 3.2. System Scope

General Features Within the Scope:

1. **Communication Platform**
    - Timed and tracked communication between all parties.
    - Notifications for users to complete their tasks.
    - Automated email notifications and reminders.
2. **Agreement Management**
    - Creation and management of consortia agreements.
    - Version control for agreement documents.
    - Visible approval process with status indicators and notifications.
3. **Resource Sharing**
    - Enable resource sharing among consortia members.
    - Tools for defining and managing research themes.
    - Mechanism to facilitate the formation of committees.
4. **Dashboard and Reporting**
    - Dashboard showing the status of agreements and project outcomes.
    - Tools for tracking the time spent by each team/party on reviewing agreements.
    - Progress reports and project outcome reviews.
5. **User Management and Authentication**
    - User authentication and role-based access control.
    - Ability to create and manage user accounts.
    - Integration with KFUPM accounts for sign-in.
6. **Proposal Management**
    - Submission and evaluation of research proposals.
    - Scoring and assessment by reviewers.
    - Automated workflow for proposal review and approval phases.

What is Not Within the Scope

1. **Financial Management**
    - Detailed financial accounting and budgeting for consortia projects.
    - Payroll and expense management for consortia members.
2. **Human Resources Management**
    - Recruitment, hiring, and management of consortia staff.
    - Employee performance evaluations and HR-related tasks.
3. **Detailed Project Management**
    - Day-to-day project management tasks such as task assignments, scheduling, and resource allocation.
    - Detailed project tracking and Gantt charts.
4. **External Communication Tools**
    - Integration with external communication tools like Slack, Microsoft Teams, etc.
    - Social media management and external public relations.

Description of Dependencies and Expected Interactions with External Systems

1. **KFUPM IT Infrastructure**
    - The system must be compatible with the existing IT infrastructure at KFUPM.
    - Integration with KFUPM's authentication systems for user sign-in.
2. **Email and SMS Services**
    - The system will use external email and SMS services for notifications and reminders.
    - Dependencies on reliable email and SMS service providers.
3. **External Databases and Repositories**
    - Integration with external databases for resource sharing and data storage.
    - Access to external research repositories and intellectual property databases.
4. **Regulatory and Compliance Systems**
    - Interaction with governmental and regulatory systems for compliance monitoring.
    - Dependencies on external regulatory databases and reporting tools.
5. **Collaboration Tools**
    - Potential integration with collaboration tools for document sharing and real-time communication.
    - Dependencies on APIs and services provided by collaboration tool vendors.

### 3.3 User Stories

Yellow indicates semi-assumption

Red indicates full-assumption

**S1: Define Research Area**

**As KFUPM Administrator,** I want to define research areas for consortia to facilitate the proposal submission process. He can add new research areas with its descriptions. The system suggests existing research areas while offering the ability to define a new one.

**S2: Inviting Potential Partners**

**As KFUPM Administrator,** I want to invite potential partners to participate in a consortium by sending invitations through the system. He can search for organizations based on industry, expertise, or location. The system sends a message invitation with details about the consortium and a link for registration.

**S3: Registering as Consortium Member**

**As a Representative from an Invited Organization,** I want to register as a member of a consortium by creating an account within the system. He can create an account using his organizational email address using the invitation link. The system verifies the email address and grants access based on the consortium invitation.

**S4: Submit Research Proposal**

**As a Consortium Member,** I want to submit a research proposal for a specific consortium, attaching relevant documents and outlining the research plan. He can access the proposal submission form for a chosen consortium. The system shows a form includes sections for proposal title, abstract, research team members, budget, file uploads and other important fields.

**S5: Review Assigned Proposals**

**As a Reviewer,** I want to access and review assigned proposals within the system, providing scores and feedback. He receives notifications for assigned proposals with deadlines. The system provides access to the proposal details, evaluation criteria, and a scoring interface. He can leave written comments and suggestions for improvement.

**S6: Track Review Progress**

**As a KFUPM Administrator,** I want to track the progress of proposal reviews by reviewers and identify any delays. The system displays a dashboard showing assigned proposals, reviewer names, and deadlines, also it sends automated reminders to reviewers.

**S7: View Review Results**

**As a Consortium Member,** I want to view the evaluation results and feedback for my submitted proposal.

**S8: Submit Progress Reports**

**As a Project Team Member,** I want to submit progress reports for ongoing projects within the system, providing updates and milestones achieved. The user can access a progress report submission form for their assigned project.

**S9: Review Final Reports**

**As a Closure Committee Member,** I want to review final reports submitted by project teams and provide feedback or recommendations. The user can access final reports for completed projects within the system. The system allows for downloading reports, leaving comments, and marking the project as closed.

**S10: (Negative User Story) Technical Review**

**As a Reviewer,** I want to avoid unintentionally revealing my identity to the proposal authors while providing feedback. The system should offer the option for anonymous reviews, ensuring reviewer independence and unbiased evaluation.

### 3.4 Preliminary Requirements

[2nd Phase - Preliminary Requirements](###)

### 3.5 Risks

- **Risk 1: Data Security Breaches**
    - **Description**: There is a risk of unauthorized access to sensitive consortia data.
    - **Potential Consequences**:  This could lead to a loss of trust among consortium members, legal implications, and financial losses.
    
- **Risk 2: Integration Complexities with Existing Systems**
    - **Description**: Challenges may arise in integrating the new system with KFUPM's existing software infrastructure.
    - **Potential Consequences**: Potential delays in project deployment, increased operational costs, and reduced system effectiveness.
    
- **Risk 3: Scope Creep**
    - **Description**: There is a potential for the project scope to expand gradually beyond initial agreements without appropriate reviews.
    - **Potential Consequences**: This could lead to overstretched resources, delayed project timelines, and potential budget overruns.
    
- **Risk 4: Inadequate Stakeholder Involvement**
    - **Description**: Insufficient involvement of key stakeholders might occur during crucial phases of the project.
    - **Potential Consequences**: Misalignment of the system functionalities with actual user needs, resulting in underutilization and dissatisfaction.
    
- **Risk 5: Technical Debt**
    - **Description**: In an effort to meet deadlines, the project team might resort to quick fixes that could lead to technical debt.
    - **Potential Consequences**: Increased costs for future system maintenance, reduced scalability, and potential system failures.

 ## 4. Interface Prototypes

[4. Interface prototypes](###)

## 5. Description of group and roles

The group collaborated through three meetings to complete this phase. Although we divided the tasks, every task was discussed collectively to ensure correctness and accuracy.

- Riyadh worked on the Introduction (Section 1) and Risks (Section 3.5).
- Mohammed worked on Domain Requirements (Section 2).
- Nawaf worked on Stakeholders and Their Goals (Section 3.1) and System Scope (Section 3.2).
- Moutaz worked on User Stories (Section 3.3).
- Kenan worked on Interface Prototypes (Section 4).

For Preliminary Requirements (Section 3.4), we all worked together. However, we exceeded the required number of requirements for the second phase during phase one. We added 2 more requirements and modified one, which is few because the stakeholder was very busy and unable to conduct a meeting with our group. Consequently, we linked the existing requirements to the goals and user stories.
