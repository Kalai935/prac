# prac
# QA/Testing Intern - Complete Interview Preparation Guide
## 270+ Questions with Detailed Answers

---

## Table of Contents
1. [Testing Fundamentals (1-10)](#1-testing-fundamentals)
2. [Test Case Design (11-20)](#2-test-case-design)
3. [Manual Testing (21-45)](#3-manual-testing)
4. [Automation Testing (46-75)](#4-automation-testing)
5. [API Testing (76-100)](#5-api-testing)
6. [AI/ML Testing (101-115)](#6-aiml-testing)
7. [SDLC & STLC (116-135)](#7-sdlc--stlc)
8. [Agile & Scrum (136-170)](#8-agile--scrum)
9. [CRUD Operations (171-190)](#9-crud-operations)
10. [Bug Tracking (191-208)](#10-bug-tracking--defect-management)
11. [Programming Basics (209-230)](#11-programming-basics)
12. [Behavioral Questions (231-255)](#12-behavioral-questions)
13. [Scenario-Based Questions (256-270)](#13-scenario-based-questions)

---

## 1. Testing Fundamentals

### **Q1. What is software testing and why is it important?**

**Answer:**
Software testing is the process of evaluating and verifying that a software application or system meets specified requirements and works as expected. It involves executing a system to identify bugs, errors, or missing requirements.

**Importance:**
- Ensures product quality and reliability
- Identifies defects early, reducing cost of fixes
- Verifies that software meets user requirements
- Builds customer confidence and satisfaction
- Prevents software failures in production
- Ensures security and compliance

---

### **Q2. What is the difference between Quality Assurance (QA) and Quality Control (QC)?**

**Answer:**

**Quality Assurance (QA):**
- Process-oriented, preventive approach
- Focuses on **preventing** defects
- Involves the entire development process
- Establishes processes and standards
- Example: Code reviews, process audits, training

**Quality Control (QC):**
- Product-oriented, detective approach
- Focuses on **identifying** defects
- Involves testing the final product
- Executes tests to find bugs
- Example: Functional testing, regression testing

**Simple analogy:** QA is like following a recipe correctly to prevent a bad cake; QC is tasting the cake to check if it's good.

---

### **Q3. What is the difference between verification and validation?**

**Answer:**

**Verification: "Are we building the product right?"**
- Checks if software meets **specifications**
- Static testing (reviews, walkthroughs, inspections)
- Done **without executing code**
- Example: Reviewing requirements, design documents

**Validation: "Are we building the right product?"**
- Checks if software meets **user needs**
- Dynamic testing (executing code)
- Done **by executing** the application
- Example: User acceptance testing, system testing

---

### **Q4. Explain the Software Testing Life Cycle (STLC).**

**Answer:**
STLC is a sequence of specific activities conducted during the testing process to ensure software quality.

**Phases:**

1. **Requirement Analysis**
   - Understand testable requirements
   - Identify testing types needed
   - Analyze testing priorities

2. **Test Planning**
   - Define test strategy
   - Allocate resources
   - Create test schedule
   - Estimate testing effort and cost

3. **Test Case Development**
   - Create detailed test cases
   - Prepare test data
   - Write test scripts

4. **Test Environment Setup**
   - Set up hardware and software
   - Configure network
   - Install test tools

5. **Test Execution**
   - Execute test cases
   - Log defects
   - Retest fixed defects
   - Track test progress

6. **Test Closure**
   - Evaluate exit criteria
   - Prepare test completion reports
   - Document lessons learned
   - Archive test artifacts

---

### **Q5. What are the different levels of testing?**

**Answer:**

1. **Unit Testing**
   - Testing individual components/modules in isolation
   - Usually done by developers
   - Uses white-box testing techniques
   - Example: Testing a login function

2. **Integration Testing**
   - Testing interaction between integrated modules
   - Verifies interfaces between components
   - Example: Testing login module with database

3. **System Testing**
   - Testing the complete integrated system
   - Verifies system meets requirements
   - Black-box testing
   - Example: End-to-end testing of entire application

4. **Acceptance Testing (UAT)**
   - Testing by end users or clients
   - Validates business requirements
   - Determines if system is ready for deployment
   - Example: Customer testing before go-live

---

### **Q6. What is the difference between positive and negative testing?**

**Answer:**

**Positive Testing:**
- Testing with **valid** inputs
- Verifies system works **as expected**
- Checks if application does what it should do
- Example: Login with correct username and password

**Negative Testing:**
- Testing with **invalid** inputs
- Verifies system handles errors **gracefully**
- Checks if application doesn't do what it shouldn't do
- Examples:
  - Login with wrong password
  - Enter special characters in numeric field
  - SQL injection attempts
  - File upload with invalid file type

---

### **Q7. What is exploratory testing?**

**Answer:**
Exploratory testing is an informal testing approach where testers actively explore the application without predefined test cases. Testers simultaneously **learn** about the application, **design** tests, and **execute** them.

**Characteristics:**
- Unscripted, ad-hoc approach
- Simultaneous learning, test design, and execution
- Relies on tester's creativity, experience, and intuition
- Good for finding unexpected bugs
- Useful when documentation is limited
- Complements scripted testing

**When to use:**
- Early in development when requirements are unclear
- When exploring new features
- When documentation is incomplete
- To supplement automated tests

---

### **Q8. What is ad-hoc testing?**

**Answer:**
Ad-hoc testing is **informal, unstructured** testing performed without any planning, documentation, or predefined test cases. It's random testing to find defects.

**Key points:**
- No formal test plan or strategy
- No test cases prepared beforehand
- Goal is to break the system randomly
- Cannot be reproduced (no documentation)
- Usually done after formal testing
- Depends heavily on tester's intuition

**Difference from Exploratory Testing:**
- Ad-hoc: Completely random, no structure
- Exploratory: Structured approach with simultaneous learning

---

### **Q9. What is smoke testing vs sanity testing?**

**Answer:**

**Smoke Testing:**
- **Objective:** Check if build is stable enough for further testing
- **When:** Performed on **initial build** after deployment
- **Coverage:** Wide and **shallow** (covers major features superficially)
- **Focus:** Critical functionalities
- **Also called:** Build Verification Testing (BVT)
- **Example:** After new deployment:
  - Application launches
  - Login works
  - Main pages load
  - Critical workflows are accessible

**Sanity Testing:**
- **Objective:** Check if specific functionality works after bug fixes
- **When:** After receiving a build with **minor changes/bug fixes**
- **Coverage:** Narrow and **deep** (focuses on specific area)
- **Focus:** Specific module or feature
- **Example:** After bug fix in checkout:
  - Verify only the checkout flow
  - Check related payment functions
  - Ensure bug is actually fixed

**Key Difference:**
- Smoke: "Can we start testing?" (broad, initial check)
- Sanity: "Is this specific fix working?" (narrow, focused check)

---

### **Q10. What is the difference between severity and priority of a bug?**

**Answer:**

**Severity:** Impact of the bug on application functionality (**technical perspective**)

**Levels:**
- **Critical:** Application crashes, data loss, security breach
- **Major:** Major functionality broken, no workaround
- **Minor:** Minor functionality issue, workaround exists
- **Trivial:** UI/cosmetic issues, minor inconvenience

**Priority:** Urgency to fix the bug (**business perspective**)

**Levels:**
- **High:** Must fix immediately
- **Medium:** Fix in next release
- **Low:** Fix when time permits

**Examples:**

| Scenario | Severity | Priority | Reason |
|----------|----------|----------|---------|
| Payment gateway not working | High | High | Critical function, revenue impact |
| App crashes on IE 6 | High | Low | Severe but affects few users |
| Company logo misspelled on homepage | Low | High | Minor issue but brand impact |
| Minor button alignment issue on settings page | Low | Low | Cosmetic, non-critical area |

---

## 2. Test Case Design

### **Q11. What is a test case? What are its components?**

**Answer:**
A test case is a set of conditions or variables under which a tester determines whether an application or software system is working correctly.

**Components of a Test Case:**

1. **Test Case ID:** Unique identifier (e.g., TC_001)
2. **Test Case Description:** Brief summary of what is being tested
3. **Pre-conditions:** Requirements before execution (e.g., user must be logged in)
4. **Test Steps:** Detailed steps to execute
5. **Test Data:** Input data required
6. **Expected Result:** What should happen
7. **Actual Result:** What actually happened (filled during execution)
8. **Status:** Pass/Fail
9. **Priority:** High/Medium/Low
10. **Created By:** Author name
11. **Execution Date:** When test was run
12. **Comments/Notes:** Additional information

**Example:**

```
Test Case ID: TC_LOGIN_001
Description: Verify login with valid credentials
Pre-condition: User must be registered
Test Steps:
  1. Navigate to login page
  2. Enter valid username
  3. Enter valid password
  4. Click Login button
Test Data: Username = "testuser@email.com", Password = "Test@123"
Expected Result: User successfully logged in and redirected to dashboard
Actual Result: [To be filled during execution]
Status: [Pass/Fail]
Priority: High
```

---

### **Q12. What is a test scenario vs test case?**

**Answer:**

**Test Scenario:**
- High-level, one-liner description of functionality to be tested
- **What** to test
- Covers end-to-end functionality
- Example: "Verify login functionality"

**Test Case:**
- Detailed steps on **how** to test
- Specific conditions and steps
- Multiple test cases can be derived from one test scenario
- Example: 
  - TC1: Login with valid credentials
  - TC2: Login with invalid password
  - TC3: Login with blank username

**Relationship:**
- 1 Test Scenario = Multiple Test Cases
- Test Scenario provides the goal
- Test Cases provide the detailed execution plan

---

### **Q13. What is a test plan and what does it contain?**

**Answer:**
A test plan is a comprehensive document that outlines the **strategy, objectives, schedule, estimation, deliverables, and resources** required for testing.

**Contents of Test Plan:**

1. **Test Plan ID & Introduction**
   - Document version
   - Purpose of testing

2. **Scope**
   - Features to be tested
   - Features NOT to be tested
   - Test items

3. **Test Strategy/Approach**
   - Testing levels (unit, integration, system, UAT)
   - Testing types (functional, performance, security)
   - Entry and exit criteria

4. **Test Environment**
   - Hardware requirements
   - Software requirements
   - Network configuration

5. **Schedule & Milestones**
   - Start and end dates
   - Major milestones
   - Deliverable dates

6. **Resources**
   - Team members and roles
   - Tools required
   - Training needs

7. **Risk & Mitigation**
   - Potential risks
   - Contingency plans

8. **Deliverables**
   - Test cases
   - Test reports
   - Defect logs

9. **Approvals**
   - Sign-off from stakeholders

---

### **Q14. What are different test design techniques?**

**Answer:**

**1. Black Box Testing Techniques:**

a) **Equivalence Partitioning**
   - Dividing input data into valid and invalid partitions
   - Example: Age field (0-17: Invalid, 18-100: Valid, >100: Invalid)

b) **Boundary Value Analysis**
   - Testing at boundaries of equivalence partitions
   - Example: Age field - test 17, 18, 100, 101

c) **Decision Table Testing**
   - For complex business logic with multiple conditions
   - Creates table of all possible combinations

d) **State Transition Testing**
   - For systems with different states
   - Example: Order states (Pending → Processing → Shipped → Delivered)

e) **Error Guessing**
   - Based on tester's experience
   - Guessing where errors might occur

**2. White Box Testing Techniques:**

a) **Statement Coverage**
   - Execute all statements at least once

b) **Branch Coverage**
   - Execute all branches (if-else) at least once

c) **Path Coverage**
   - Execute all possible paths through code

---

### **Q15. Explain boundary value analysis with an example.**

**Answer:**
Boundary Value Analysis (BVA) is a black-box testing technique that focuses on testing at the **boundaries** of input ranges, as errors often occur at boundaries.

**Rule:** Test at the boundary and just inside/outside the boundary

**Example 1: Age field (valid range: 18-60)**

Test Values:
- **Below minimum:** 17 (Invalid)
- **Minimum boundary:** 18 (Valid)
- **Within range:** 30 (Valid)
- **Maximum boundary:** 60 (Valid)
- **Above maximum:** 61 (Invalid)

**Example 2: Text field (max length: 10 characters)**

Test Values:
- 9 characters (Valid)
- 10 characters (Valid - boundary)
- 11 characters (Invalid)

**Example 3: Discount code (valid for quantities 10-100)**

Test Values:
- Quantity = 9 (should not apply discount)
- Quantity = 10 (should apply discount)
- Quantity = 11 (should apply discount)
- Quantity = 100 (should apply discount)
- Quantity = 101 (should not apply discount)

---

### **Q16. Explain equivalence partitioning with an example.**

**Answer:**
Equivalence Partitioning divides input data into **equivalent classes** where all values in a class should behave similarly. We test **one value from each partition** instead of testing all values.

**Principle:** If one value in a partition works, all values should work. If one fails, all should fail.

**Example: Age field for voter registration (valid: 18-100)**

**Partitions:**

1. **Invalid partition 1:** Age < 18 (e.g., 0, 5, 17)
   - Test value: **10**

2. **Valid partition:** Age 18-100 (e.g., 18, 30, 50, 100)
   - Test value: **25**

3. **Invalid partition 2:** Age > 100 (e.g., 101, 150, 200)
   - Test value: **105**

**Result:** Instead of testing all ages 0-200, we test just **3 values** (10, 25, 105)

**Example 2: Email validation**

**Partitions:**

1. **Valid emails:** user@domain.com
   - Test: john@example.com

2. **Missing @:** userdomain.com
   - Test: testdomain.com

3. **Missing domain:** user@
   - Test: test@

4. **Special characters:** user!@domain.com
   - Test: test!@test.com

---

### **Q17. What is decision table testing?**

**Answer:**
Decision Table Testing is used for testing **complex business logic** with multiple conditions and corresponding actions.

**Structure:**
- **Conditions:** Input conditions (True/False, Yes/No)
- **Actions:** Expected outcomes based on condition combinations

**Example: Loan Approval System**

**Conditions:**
1. Credit Score > 700?
2. Income > $50,000?
3. Employment > 2 years?

**Decision Table:**

| Rule | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
|------|---|---|---|---|---|---|---|---|
| Credit Score > 700 | Y | Y | Y | Y | N | N | N | N |
| Income > $50K | Y | Y | N | N | Y | Y | N | N |
| Employment > 2 yrs | Y | N | Y | N | Y | N | Y | N |
| **Action: Approve Loan** | ✓ | ✓ | ✓ | X | ✓ | X | X | X |

**When to use:**
- Complex business rules
- Multiple conditions affecting outcomes
- Need to test all combinations

---

### **Q18. What is state transition testing?**

**Answer:**
State Transition Testing is used when a system can be in different **states** and transitions between states based on **events/inputs**.

**Components:**
- **States:** Different conditions of the system
- **Transitions:** Changes from one state to another
- **Events:** Triggers that cause transitions
- **Actions:** Results of transitions

**Example: ATM Card State**

**States:**
1. Card Inserted
2. PIN Entered
3. Locked (after 3 wrong attempts)
4. Transaction Mode

**State Transition Diagram:**

```
[Card Inserted] --correct PIN--> [Transaction Mode]
       |
       |--wrong PIN (attempt 1-2)--> [Card Inserted]
       |
       |--wrong PIN (attempt 3)--> [Card Locked]
```

**Test Cases:**
- Enter correct PIN → Verify transition to Transaction Mode
- Enter wrong PIN twice → Verify stays in Card Inserted state
- Enter wrong PIN thrice → Verify transition to Locked state
- Card removal → Verify transition to initial state

**Another Example: Order Status**

States: Pending → Processing → Shipped → Delivered → Completed

---

### **Q19. How do you write effective test cases?**

**Answer:**

**Best Practices:**

1. **Clear and Concise**
   - Use simple language
   - Avoid ambiguity
   - One objective per test case

2. **Detailed Steps**
   - Each step should be clear
   - Include exact values to enter
   - Specify what to click/select

3. **Testable**
   - Must have clear pass/fail criteria
   - Expected result should be specific

4. **Reusable**
   - Should work across multiple test cycles
   - Independent of other test cases

5. **Cover All Scenarios**
   - Positive scenarios
   - Negative scenarios
   - Boundary conditions
   - Error handling

6. **Use Naming Conventions**
   - Consistent ID format (e.g., TC_MODULE_001)
   - Descriptive names

7. **Include Pre-conditions**
   - State what needs to be set up first
   - Example: "User must be logged in"

8. **Specify Test Data**
   - Don't use "valid data" or "invalid data"
   - Use specific examples: "Email: test@test.com"

**Example of Effective Test Case:**

```
Test Case ID: TC_LOGIN_003
Title: Verify login fails with invalid password
Priority: High
Pre-condition: User account exists (user@test.com / Password123)
Test Steps:
  1. Navigate to www.example.com/login
  2. Enter email: "user@test.com"
  3. Enter password: "WrongPassword"
  4. Click "Login" button
Expected Result: 
  - Error message displayed: "Invalid credentials"
  - User remains on login page
  - Password field is cleared
Test Data: Email: user@test.com, Password: WrongPassword
```

---

### **Q20. What is test coverage and how do you measure it?**

**Answer:**
Test Coverage is a metric that measures the **percentage of application tested** by test cases. It helps identify untested areas.

**Types of Coverage:**

1. **Requirement Coverage**
   - % of requirements tested
   - Formula: (Requirements tested / Total requirements) × 100

2. **Code Coverage** (White Box)
   - Statement Coverage: % of code statements executed
   - Branch Coverage: % of branches (if-else) executed
   - Path Coverage: % of paths through code executed

3. **Feature Coverage**
   - % of features tested

4. **Test Case Coverage**
   - Number of passed/failed test cases

**How to Measure:**

**Example Calculation:**

```
Total Requirements: 50
Requirements Tested: 45
Requirement Coverage = (45/50) × 100 = 90%

Total Code Statements: 1000
Statements Executed: 850
Statement Coverage = (850/1000) × 100 = 85%
```

**Tools:**
- JaCoCo (Java)
- Coverage.py (Python)
- Istanbul (JavaScript)
- SonarQube

**Best Practices:**
- Aim for 80-90% coverage (100% is often impractical)
- Focus on critical paths first
- Coverage is a metric, not a goal
- High coverage doesn't guarantee quality

---

## 3. Manual Testing

### **Q21. What is functional testing?**

**Answer:**
Functional testing verifies that each function of the software operates according to the **requirements specification**. It tests **what the system does**.

**Characteristics:**
- Black-box testing technique
- Tests user-facing features
- Focuses on output for given inputs
- Ignores internal code structure

**Types of Functional Testing:**
1. Unit Testing
2. Integration Testing
3. System Testing
4. Smoke Testing
5. Sanity Testing
6. Regression Testing
7. User Acceptance Testing (UAT)

**What is tested:**
- User interface
- APIs
- Database
- Security
- Client/Server communication
- Functionality

**Example Test Scenarios:**
- Login functionality
- Search feature
- Payment processing
- Email notifications
- Data validation

---

### **Q22. How do you perform functional testing on a web application?**

**Answer:**

**Step-by-Step Process:**

**1. Understand Requirements**
- Read specifications
- Understand expected behavior
- Identify testable features

**2. Create Test Plan**
- Define scope
- List features to test
- Identify test environment

**3. Design Test Cases**
- Positive scenarios
- Negative scenarios
- Boundary conditions

**4. Set Up Test Environment**
- Configure browsers
- Prepare test data
- Set up database

**5. Execute Tests**
- Follow test cases
- Document results
- Log defects

**6. Report Results**
- Prepare test summary
- Track metrics

**Example: Testing E-commerce Website**

**Features to Test:**

1. **User Registration**
   - Valid registration
   - Duplicate email
   - Password validation
   - Email verification

2. **Login**
   - Valid credentials
   - Invalid credentials
   - Forgot password
   - Session timeout

3. **Product Search**
   - Search by keyword
   - Filter by category
   - Sort by price
   - No results scenario

4. **Shopping Cart**
   - Add to cart
   - Remove from cart
   - Update quantity
   - Cart persistence

5. **Checkout**
   - Payment methods
   - Address validation
   - Order confirmation
   - Email notifications

---

### **Q23. What is the difference between functional and non-functional testing?**

**Answer:**

**Functional Testing:**
- Tests **WHAT** the system does
- Verifies features against requirements
- Example: Does login work?
- Based on customer requirements
- Can be done manually or automated
- Examples:
  - Unit testing
  - Integration testing
  - System testing
  - User acceptance testing

**Non-Functional Testing:**
- Tests **HOW** the system performs
- Verifies quality attributes
- Example: How fast does login respond?
- Based on customer expectations
- Usually requires tools
- Examples:
  - Performance testing
  - Load testing
  - Security testing
  - Usability testing
  - Compatibility testing
  - Reliability testing

**Comparison Table:**

| Aspect | Functional | Non-Functional |
|--------|------------|----------------|
| Focus | Features | Performance, usability, security |
| Question | What does it do? | How well does it do it? |
| Based on | Requirements | Expectations |
| Example | Login works | Login responds in <2 seconds |
| Execution | Manual/Automated | Mostly automated with tools |

---

### **Q24. What is user acceptance testing (UAT)?**

**Answer:**
UAT is the final testing phase where actual **end users** test the system to verify it meets their business requirements and is ready for production.

**Purpose:**
- Validate software meets business needs
- Ensure software is ready for deployment
- Get formal sign-off from users/stakeholders

**Types of UAT:**

1. **Alpha Testing**
   - Done by internal users
   - At developer's site
   - Before beta testing

2. **Beta Testing**
   - Done by actual end users
   - At user's location
   - Real-world environment

3. **Contract Acceptance Testing**
   - Against contract criteria
   - Legal compliance

4. **Regulation Acceptance Testing**
   - Against regulations
   - Example: Banking, healthcare

**UAT Process:**

1. **UAT Planning**
   - Define scope
   - Identify users
   - Schedule sessions

2. **Test Case Design**
   - Create business scenarios
   - Prepare test data

3. **UAT Execution**
   - Users execute tests
   - Document issues

4. **Defect Reporting**
   - Users log defects
   - Developers fix

5. **Sign-off**
   - Formal acceptance
   - Go-live approval

**Example UAT Scenario:**
"As a customer, I want to search for a product, add it to cart, and complete checkout with credit card payment."

**Who Performs UAT:**
- Business users
- End users
- Client stakeholders
- Domain experts

---

### **Q25. What is integration testing?**

**Answer:**
Integration testing verifies the **interaction and data flow** between different modules/components when integrated together.

**Objective:**
- Test interfaces between modules
- Find defects in module interaction
- Verify data transfer between modules

**Approaches:**

**1. Big Bang Integration**
- All modules integrated at once
- Test entire system together
- Pros: Quick for small systems
- Cons: Hard to isolate defects

**2. Incremental Integration**

**a) Top-Down:**
- Start from top-level modules
- Integrate downward
- Use stubs for lower modules
- Example: Test UI → Business Logic → Database

**b) Bottom-Up:**
- Start from lower-level modules
- Integrate upward
- Use drivers for higher modules
- Example: Test Database → Business Logic → UI

**c) Sandwich/Hybrid:**
- Combination of top-down and bottom-up
- Parallel testing

**Example:**

**Modules:** Login UI → Authentication Service → User Database

**Test Scenarios:**
1. UI sends correct credentials to Authentication Service
2. Authentication Service queries User Database correctly
3. Database returns user data to Service
4. Service sends response to UI
5. UI displays correct message

**Stubs and Drivers:**
- **Stub:** Dummy lower-level module
- **Driver:** Dummy higher-level module (calls the module being tested)

---

### **Q26. What is system testing?**

**Answer:**
System testing tests the **complete integrated system** as a whole to verify it meets specified requirements.

**Characteristics:**
- **Black-box testing**
- Tests entire application
- Performed after integration testing
- Done in environment similar to production
- Executed by testing team

**Types of System Testing:**

1. **Functionality Testing**
   - Verify all features work

2. **Performance Testing**
   - Response time, throughput

3. **Security Testing**
   - Vulnerability assessment

4. **Usability Testing**
   - User-friendliness

5. **Compatibility Testing**
   - Different OS, browsers

6. **Recovery Testing**
   - System recovery after crash

7. **Installation Testing**
   - Installation process

**Example:**
Testing an **E-commerce application:**

1. User can browse products
2. Search functionality works
3. Cart operations work
4. Checkout process completes
5. Payment processing works
6. Order confirmation sent
7. System handles 1000 concurrent users
8. Data is secure
9. Works on Chrome, Firefox, Safari

---

### **Q27. How would you test a login page?**

**Answer:**

**Functional Test Cases:**

**1. Positive Scenarios:**
- Valid username and password → Successful login
- Remember me checkbox → User stays logged in
- Redirect to correct page after login
- Session created properly

**2. Negative Scenarios:**
- Invalid username → Error message
- Invalid password → Error message
- Blank username → Validation error
- Blank password → Validation error
- Both fields blank → Error message
- SQL injection in username → Should be blocked
- XSS attack in fields → Should be sanitized

**3. Validation Testing:**
- Maximum length of username field
- Minimum password length
- Special characters in password
- Case sensitivity of password
- Email format validation (if email used)

**4. Security Testing:**
- Password should be masked
- Password not visible in URL
- Protection against brute force attacks
- Account lockout after failed attempts
- HTTPS/SSL for data transmission
- Session timeout after inactivity

**5. UI/UX Testing:**
- All elements visible (fields, buttons, links)
- Proper alignment and spacing
- Placeholder text present
- Forgot password link works
- Remember me checkbox works
- Tab key navigation works

**6. Compatibility Testing:**
- Works on different browsers (Chrome, Firefox, Safari, Edge)
- Works on different devices (desktop, mobile, tablet)
- Works on different OS (Windows, Mac, Linux, iOS, Android)

**7. Performance Testing:**
- Page load time < 2 seconds
- Login response time < 1 second
- Handles multiple simultaneous logins

**Example Test Cases:**

```
TC_001: Login with valid credentials
Steps:
1. Enter valid username
2. Enter valid password
3. Click Login
Expected: User logged in successfully, redirected to dashboard

TC_002: Login with invalid password
Steps:
1. Enter valid username
2. Enter invalid password
3. Click Login
Expected: Error message "Invalid credentials", user remains on login page

TC_003: SQL Injection attempt
Steps:
1. Enter username: admin' OR '1'='1
2. Enter password: anything
3. Click Login
Expected: Login fails, SQL injection blocked
```

---

### **Q28. How would you test a search functionality?**

**Answer:**

**Test Scenarios:**

**1. Basic Search:**
- Search with valid keyword → Relevant results displayed
- Search with invalid keyword → No results message
- Search with partial keyword → Matching results shown
- Case insensitive search → "APPLE" = "apple"
- Search with special characters → Handled properly
- Search with numbers → Results shown
- Blank search → Show all or error message

**2. Search Filters:**
- Filter by category → Correct filtering
- Filter by price range → Results within range
- Filter by date → Correct chronological results
- Multiple filters → AND/OR logic works
- Clear filters → Resets to all results

**3. Search Results:**
- Results are relevant
- Results count displayed correctly
- Pagination works (if applicable)
- Sorting works (by relevance, price, date)
- Results per page option works
- Load more button works

**4. Advanced Search:**
- Search with operators (AND, OR, NOT)
- Phrase search ("exact phrase")
- Wildcard search (prod*)
- Search within results

**5. Performance:**
- Search response time < 3 seconds
- Handles large result sets
- Autocomplete suggestions load quickly

**6. Edge Cases:**
- Very long search query
- Search with only special characters
- Search with SQL injection attempt
- Search with XSS attempt
- Search during network failure

**7. UI/UX:**
- Search box is visible
- Placeholder text present
- Search button visible and clickable
- Recent searches saved
- Search suggestions dropdown works
- Clear search button works

**Example Test Cases:**

```
TC_SEARCH_001: Search with valid product name
Input: "laptop"
Expected: All laptop products displayed

TC_SEARCH_002: Search with partial match
Input: "lap"
Expected: Products containing "lap" (laptop, laplace, etc.)

TC_SEARCH_003: Search with no results
Input: "xyzabc123"
Expected: Message "No results found for 'xyzabc123'"

TC_SEARCH_004: Filter by price
Input: Search "phone", filter price $200-$500
Expected: Only phones priced $200-$500 shown

TC_SEARCH_005: SQL Injection prevention
Input: "' OR 1=1--"
Expected: No SQL error, handled as regular search term
```

---

### **Q29. How would you test a registration form?**

**Answer:**

**Test Scenarios:**

**1. Valid Registration:**
- All mandatory fields filled correctly → Success
- Optional fields left blank → Success
- Terms and conditions accepted → Success
- Email verification sent

**2. Field Validation:**

**Username:**
- Minimum length (e.g., 3 characters)
- Maximum length (e.g., 20 characters)
- Special characters allowed/not allowed
- Spaces allowed/not allowed
- Duplicate username → Error

**Email:**
- Valid email format → Accepted
- Invalid format (missing @, domain) → Error
- Duplicate email → Error
- Email verification link sent

**Password:**
- Minimum length (e.g., 8 characters)
- Maximum length
- Contains uppercase → Required/optional
- Contains number → Required/optional
- Contains special character → Required/optional
- Password strength indicator
- Confirm password matches → Validated

**Phone:**
- Valid format (10 digits)
- Only numbers accepted
- International format supported

**Date of Birth:**
- Valid date format
- Age validation (e.g., must be 18+)
- Future date not allowed

**3. Mandatory Fields:**
- Submit without required fields → Error messages
- Each required field validated individually

**4. Security:**
- Password masked
- CAPTCHA verification
- Protection against bot registration
- SQL injection prevention
- XSS attack prevention

**5. UI/UX:**
- All fields visible
- Clear labels
- Validation messages clear
- Success message displayed
- Redirect after successful registration
- Tab navigation works

**6. Edge Cases:**
- Maximum character limits
- Copy-paste in password field
- Back button during registration
- Multiple tab registration
- Network failure during submission

**Example Test Cases:**

```
TC_REG_001: Successful registration with all valid data
Input:
  - Username: testuser123
  - Email: test@example.com
  - Password: Test@1234
  - Confirm Password: Test@1234
  - Phone: 1234567890
  - DOB: 01/01/2000
  - Terms: Checked
Expected: 
  - Registration successful
  - Verification email sent
  - Redirect to login page

TC_REG_002: Password mismatch
Input:
  - Password: Test@1234
  - Confirm Password: Test@12345
Expected: Error "Passwords do not match"

TC_REG_003: Invalid email format
Input: Email: test.com (missing @)
Expected: Error "Please enter a valid email"

TC_REG_004: Duplicate email
Input: Email already registered
Expected: Error "Email already in use"

TC_REG_005: Age restriction
Input: DOB: 01/01/2020 (under 18)
Expected: Error "Must be 18+ to register"
```

---

### **Q30. What is end-to-end testing?**

**Answer:**
End-to-end (E2E) testing validates the **complete workflow** of an application from start to finish, testing all integrated components in a **production-like environment**.

**Objective:**
- Simulate real user scenarios
- Test complete business flows
- Verify system works as a whole
- Identify system dependencies

**Characteristics:**
- Tests entire application flow
- Includes all integrated systems (DB, APIs, third-party services)
- Executed in production-like environment
- Black-box testing approach

**Example: E-commerce E2E Test**

**Scenario:** User purchases a product

**Flow:**
1. User opens website
2. Searches for product
3. Views product details
4. Adds product to cart
5. Proceeds to checkout
6. Enters shipping address
7. Selects payment method
8. Completes payment
9. Receives order confirmation
10. Gets confirmation email
11. Order appears in order history

**What E2E Tests Verify:**
- Database updates correctly
- Third-party payment gateway integration
- Email service sends notifications
- Session management
- Cart persistence
- Order processing system
- Inventory system updates

**Another Example: Banking Application**

**Scenario:** Fund transfer between accounts
1. Login to banking app
2. Select fund transfer
3. Enter recipient details
4. Enter amount
5. Confirm transaction
6. Receive OTP
7. Enter OTP
8. Transaction completed
9. Balance updated
10. SMS confirmation sent
11. Transaction appears in statement

**Tools for E2E Testing:**
- Selenium
- Cypress
- Playwright
- Puppeteer
- TestCafe

---

### **Q31. What is regression testing and why is it important?**

**Answer:**
Regression testing is **re-testing** an application after modifications (bug fixes, enhancements, configuration changes) to ensure that existing functionality still works correctly and no new defects are introduced.

**Purpose:**
- Verify existing features work after changes
- Ensure new code doesn't break old code
- Maintain software quality
- Catch unintended side effects

**When to Perform:**
- After bug fixes
- After new feature addition
- After code refactoring
- After configuration changes
- Before each release
- During continuous integration

**Why It's Important:**

1. **Prevents Breaking Changes**
   - New code might break existing features
   - Bug fix in one area might create bug elsewhere

2. **Maintains Quality**
   - Ensures stable application
   - Builds customer confidence

3. **Catches Side Effects**
   - Identifies unexpected impacts
   - Finds integration issues

4. **Cost-Effective**
   - Finding bugs early is cheaper
   - Prevents production failures

**Example:**

**Scenario:**
- Application has login, search, and checkout modules
- Developer fixes a bug in search module

**Regression Testing:**
Test all modules to ensure:
- Login still works (wasn't affected)
- Search bug is fixed (intended change)
- Checkout still works (wasn't affected)

**Challenges:**
- Time-consuming (many test cases)
- Resource-intensive
- Requires maintenance of test suite

**Solution:**
- Automate regression tests
- Prioritize critical test cases
- Use regression test suite

---

### **Q32. When should regression testing be performed?**

**Answer:**

**1. After Bug Fixes**
- Verify bug is fixed
- Ensure fix didn't break anything else
- Example: Fixed login issue → Test entire login flow

**2. After New Features**
- Ensure new feature works
- Verify existing features unaffected
- Example: Added "Forgot Password" → Test existing login still works

**3. After Code Changes**
- Code refactoring
- Performance optimizations
- Database schema changes

**4. After Environment Changes**
- Server upgrades
- Database migration
- Third-party API updates

**5. Before Every Release**
- Major releases
- Minor releases
- Hotfixes
- Ensure overall stability

**6. After Integration**
- New module integrated
- Third-party service integrated
- API version changes

**7. During Continuous Integration/Deployment**
- After every code commit (automated)
- Before deployment to production
- As part of CI/CD pipeline

**Best Practices:**
- Run after every code change (in CI/CD)
- Automate repetitive regression tests
- Prioritize based on risk
- Keep regression suite updated

**Example Timeline:**

```
Week 1: Developer fixes Bug #123
Day 1: Regression testing performed
Status: Bug fixed, no side effects

Week 2: New feature added (Two-factor authentication)
Day 5: Regression testing performed
Status: New feature works, existing login still functional

Week 4: Before v2.0 release
Day 1-3: Full regression testing
Status: All critical paths verified
```

---

### **Q33. What is the difference between regression testing and retesting?**

**Answer:**

**Regression Testing:**
- Testing **existing** functionality after changes
- Ensures old features still work
- Verifies no new defects introduced
- Tests **unchanged** areas
- Can be automated
- Part of every release

**Example:**
- Bug fixed in checkout module
- Regression: Test search, cart, profile (unrelated areas)

**Retesting:**
- Testing **fixed defects** specifically
- Verifies bug is actually fixed
- Tests the **exact same** scenario that failed
- Tests **changed** area
- Usually manual
- Done after bug fix

**Example:**
- Bug: Login fails with special characters in password
- Retest: Login again with special characters (same test that failed)

**Comparison:**

| Aspect | Regression | Retesting |
|--------|-----------|-----------|
| Purpose | Verify existing features | Verify bug is fixed |
| Scope | Entire application | Specific defect area |
| When | After any change | After defect fix |
| Test Cases | All/selected test cases | Failed test case only |
| Automation | Highly automated | Usually manual |
| Also called | Maintenance testing | Confirmation testing |

**Example Scenario:**

**Bug:** Discount code not working for first-time users

**After Fix:**

**Retesting:**
1. Enter discount code as first-time user
2. Verify discount applied
3. Complete purchase
4. Check if discount reflected

**Regression Testing:**
1. Test discount for existing users (still works?)
2. Test checkout without discount (still works?)
3. Test other payment methods (still work?)
4. Test cart functionality (still works?)

---

### **Q34. How do you select test cases for regression testing?**

**Answer:**

**Selection Criteria:**

**1. Business Critical Features**
- Login, payment, checkout
- Core functionality
- High-impact features
- Revenue-generating features

**2. Frequently Used Features**
- Features used by most users
- Common user workflows
- Example: Search, cart, profile

**3. Areas with Frequent Changes**
- Modules that change often
- Recently modified code
- Integration points

**4. Defect-Prone Areas**
- Areas with history of bugs
- Complex logic
- Previous regression failures

**5. Impacted Areas**
- Code changed directly
- Dependent modules
- Related functionality

**6. Risk-Based Selection**
- **High Risk:** Critical + complex features
- **Medium Risk:** Important but stable
- **Low Risk:** Minor features, rare usage

**Selection Techniques:**

**1. Select All Test Cases**
- Comprehensive but time-consuming
- Used when: Major release, significant changes

**2. Select Modified Test Cases**
- Only tests for changed modules
- Quick but might miss impacts

**3. Select Prioritized Test Cases**
- Based on priority (High, Medium, Low)
- Most common approach

**4. Select Based on Risk**
- Risk analysis of changes
- Focus on high-risk areas

**Example Priority Matrix:**

**High Priority (Must include):**
- User authentication
- Payment processing
- Data security
- Critical business workflows

**Medium Priority (Include if time permits):**
- Search functionality
- Notifications
- Reporting features

**Low Priority (Optional):**
- UI cosmetic changes
- Help documentation
- Non-critical settings

**Automation Strategy:**
- Automate high-priority regression suite
- Run on every build
- Manual testing for edge cases

---

### **Q35. What is selective regression testing?**

**Answer:**
Selective regression testing is selecting and executing **only a subset** of test cases from the complete regression test suite, rather than running all tests.

**Purpose:**
- Save time and resources
- Focus on impacted areas
- Maintain adequate coverage

**Selection Approach:**

**1. Analyze Code Changes**
- Identify modified modules
- Find dependent modules

**2. Select Relevant Tests**
- Tests for changed modules
- Tests for dependent modules
- Critical path tests

**3. Exclude Irrelevant Tests**
- Unrelated modules
- Unaffected features

**Example:**

**Scenario:** Bug fix in payment module

**Complete Regression Suite:** 1000 test cases

**Selective Regression:**
- Payment module tests: 100 cases
- Checkout flow tests: 50 cases
- Database transaction tests: 30 cases
- Critical path tests: 20 cases
- **Total:** 200 test cases (20% of full suite)

**Benefits:**
- Faster execution
- Resource efficient
- Early defect detection
- Suitable for agile/CI-CD

**Challenges:**
- Risk of missing defects in untested areas
- Requires expertise to select correctly
- Needs impact analysis tools

**Best Practices:**
- Use code coverage tools
- Maintain traceability matrix
- Automate test selection
- Review selection periodically

---

### **Q36. How do you prioritize regression test cases?**

**Answer:**

**Prioritization Factors:**

**1. Business Criticality**
- Revenue-impacting features
- Core business functions
- Customer-facing features
- Priority: **High**

**2. Usage Frequency**
- Features used by majority of users
- Daily operations
- Example: Login, search
- Priority: **High**

**3. Defect Density**
- Areas with frequent bugs
- Recently fixed defects
- Complex modules
- Priority: **High**

**4. Recently Changed Code**
- New features
- Bug fixes
- Code refactoring
- Priority: **High**

**5. Complexity**
- Modules with complex logic
- Integration points
- Third-party dependencies
- Priority: **Medium-High**

**6. Risk Assessment**
- Impact if feature fails
- Probability of failure
- Priority: Based on risk level

**Prioritization Matrix:**

**P0 (Critical) - Run Always:**
- User authentication
- Payment processing
- Data security
- Database transactions
- Critical user workflows

**P1 (High) - Run in Every Sprint:**
- Product search
- Shopping cart
- Order placement
- User profile
- Notifications

**P2 (Medium) - Run Weekly/Biweekly:**
- Settings
- Filters
- Sorting
- Reports
- Help pages

**P3 (Low) - Run Before Major Release:**
- Admin features
- Rare scenarios
- Non-critical settings
- Deprecated features

**Example:**

**E-commerce Application:**

```
P0 (Must Run):
- TC_001: User login
- TC_015: Add to cart
- TC_027: Checkout with credit card
- TC_035: Payment processing
- TC_050: Order confirmation

P1 (Should Run):
- TC_005: User registration
- TC_018: Update cart quantity
- TC_030: Apply coupon code
- TC_045: Save for later
- TC_055: Order history

P2 (Could Run):
- TC_060: Filter by category
- TC_070: Sort by price
- TC_080: Wishlist
- TC_090: Product reviews
- TC_100: Email preferences

P3 (Nice to Run):
- TC_110: Help documentation
- TC_120: About us page
- TC_130: Terms and conditions
- TC_140: Admin dashboard
```

**Automation Strategy:**
- Automate all P0 and P1 tests
- Run P0 on every build
- Run P1 daily or per sprint
- Run P2-P3 before releases

---

### **Q37. Can regression testing be automated? How?**

**Answer:**
**Yes**, regression testing is an ideal candidate for automation because:
- Repetitive nature (same tests run repeatedly)
- Time-consuming if done manually
- Need for frequent execution
- High return on automation investment

**How to Automate Regression Testing:**

**1. Identify Test Cases for Automation**

**Good Candidates:**
- Stable features (don't change frequently)
- Repetitive test cases
- High-priority tests
- Data-driven tests
- Time-consuming manual tests

**Not Good for Automation:**
- Frequently changing UI
- Exploratory testing
- Usability testing
- One-time tests

**2. Select Automation Tool**

**Web Applications:**
- Selenium WebDriver
- Cypress
- Playwright
- Puppeteer

**API Testing:**
- Postman/Newman
- REST Assured
- SoapUI

**Mobile:**
- Appium
- Espresso (Android)
- XCUITest (iOS)

**3. Create Automation Framework**

**Example: Page Object Model (POM)**
```
project/
├── pages/
│   ├── LoginPage.java
│   ├── HomePage.java
│   └── CheckoutPage.java
├── tests/
│   ├── LoginTest.java
│   ├── CheckoutTest.java
│   └── RegressionSuite.java
├── testdata/
│   └── testdata.xlsx
└── reports/
```

**4. Write Test Scripts**

**Example (Selenium + Java):**
```java
@Test(priority=1)
public void testLogin() {
    LoginPage login = new LoginPage(driver);
    login.enterUsername("testuser");
    login.enterPassword("password");
    login.clickLogin();
    Assert.assertTrue(login.isLoginSuccessful());
}
```

**5. Integrate with CI/CD**

**Jenkins Pipeline:**
```groovy
pipeline {
    stages {
        stage('Regression Tests') {
            steps {
                sh 'mvn clean test'
            }
        }
    }
}
```

**6. Schedule Regular Execution**
- Run on every build (smoke tests)
- Run nightly (full regression suite)
- Run before release (complete testing)

**7. Generate Reports**
- Test execution results
- Pass/fail statistics
- Failure screenshots
- Logs for debugging

**Benefits of Automated Regression:**
- Faster execution
- Consistent results
- Early bug detection
- Better coverage
- Reduced manual effort

**Best Practices:**
- Start with high-priority tests
- Keep tests independent
- Use data-driven approach
- Maintain test scripts regularly
- Review automation ROI

---

### **Q38. What challenges do you face in regression testing?**

**Answer:**

**1. Time Constraints**
- **Challenge:** Regression suites are large, time-consuming
- **Solution:** 
  - Automate repetitive tests
  - Prioritize test cases
  - Run tests in parallel

**2. Test Suite Maintenance**
- **Challenge:** Test cases become outdated as application evolves
- **Solution:**
  - Regular review and updates
  - Remove obsolete tests
  - Version control for test cases

**3. Resource Limitations**
- **Challenge:** Limited testers, test environments
- **Solution:**
  - Automation to reduce manual effort
  - Cloud-based testing environments
  - Shift-left testing approach

**4. Determining Test Coverage**
- **Challenge:** Which tests to include in regression?
- **Solution:**
  - Risk-based testing
  - Code coverage analysis
  - Traceability matrix

**5. Test Data Management**
- **Challenge:** Creating and maintaining test data
- **Solution:**
  - Test data generation tools
  - Database refresh scripts
  - Data masking for security

**6. Environment Issues**
- **Challenge:** Environment unavailable or unstable
- **Solution:**
  - Environment monitoring
  - Dedicated regression environment
  - Containerization (Docker)

**7. Frequent Application Changes**
- **Challenge:** UI/functionality changes break automated tests
- **Solution:**
  - Robust locator strategies
  - Page Object Model
  - Regular test maintenance

**8. False Positives/Negatives**
- **Challenge:** Tests fail due to script issues, not actual bugs
- **Solution:**
  - Improve test script quality
  - Better synchronization
  - Detailed logging

**9. Integration Dependencies**
- **Challenge:** External system dependencies
- **Solution:**
  - API mocking
  - Stubs for third-party services
  - Service virtualization

**10. Reporting and Analysis**
- **Challenge:** Understanding test results, identifying trends
- **Solution:**
  - Dashboard reporting
  - Metrics tracking
  - Root cause analysis

**Example:**
**Challenge:** E-commerce app has 2000 regression test cases, takes 40 hours to run manually

**Solutions Applied:**
1. Automated 70% of tests (1400 cases)
2. Prioritized remaining 30% (critical paths)
3. Run automated tests nightly
4. Manual testing for new features only
5. **Result:** Regression reduced from 40 hours to 8 hours

---

### **Q39. What is progressive regression testing?**

**Answer:**
Progressive regression testing is performed when there are **changes in requirements** and **new test cases** are designed for the new/modified functionality.

**Characteristics:**
- Used when specifications change
- New test cases added to regression suite
- Tests cover new requirements
- Old test cases may be modified/removed

**When to Use:**
- New features added
- Requirements change
- Application enhanced
- Existing functionality modified

**Example:**

**Scenario:**
Original app: Users can login with username/password

**New Requirement:** Add social media login (Google, Facebook)

**Progressive Regression:**
1. **New Test Cases:**
   - Login with Google account
   - Login with Facebook account
   - Link social account to existing account
   - Unlink social account

2. **Modified Test Cases:**
   - Update login page tests (new buttons present)
   - Update security tests (OAuth flow)

3. **Existing Test Cases:**
   - Keep username/password login tests
   - Ensure both methods work together

**Difference from Corrective Regression:**
- **Progressive:** For new features/changed requirements
- **Corrective:** For bug fixes without requirement changes

---

### **Q40. What is corrective regression testing?**

**Answer:**
Corrective regression testing is performed when there are **no changes in requirements** and test cases can be **reused** from existing regression suite.

**Characteristics:**
- Specifications remain same
- No new test cases needed
- Reuse existing test cases
- Verify bug fixes didn't break anything

**When to Use:**
- Bug fixes
- Code refactoring
- Performance optimizations
- Security patches
- No functional changes

**Example:**

**Scenario:**
Bug: Login fails when password contains special characters

**Fix:** Update password validation logic

**Corrective Regression:**
1. **Retest:** Login with special characters (verify fix)
2. **Regression:** Run existing login test suite
   - Login with alphanumeric password (still works?)
   - Login with uppercase/lowercase (still works?)
   - Login with minimum length password (still works?)
   - Forgot password (still works?)
   - Remember me (still works?)

**No New Test Cases Needed** because:
- Requirements didn't change
- No new features added
- Just fixing existing functionality

**Comparison:**

| Aspect | Progressive | Corrective |
|--------|------------|------------|
| Requirements | Changed | Unchanged |
| Test Cases | New ones created | Existing ones reused |
| Purpose | Test new features | Verify bug fixes |
| Example | Add two-factor auth | Fix login bug |

---

### **Q41. What is compatibility testing?**

**Answer:**
Compatibility testing verifies that the application works correctly across different **environments, platforms, devices, browsers, and configurations**.

**Types:**

**1. Browser Compatibility**
- Chrome, Firefox, Safari, Edge, IE
- Different browser versions
- Example: Test website on Chrome 90, Firefox 88, Safari 14

**2. Operating System Compatibility**
- Windows (7, 10, 11)
- macOS
- Linux (Ubuntu, CentOS)
- Example: App works on Windows 10 and macOS Big Sur

**3. Device Compatibility**
- Desktop, laptop
- Mobile (Android, iOS)
- Tablets
- Different screen sizes
- Example: Responsive design on iPhone 12, Samsung Galaxy, iPad

**4. Network Compatibility**
- WiFi, 3G, 4G, 5G
- Different network speeds
- Example: App loads on slow 3G connection

**5. Database Compatibility**
- MySQL, PostgreSQL, Oracle, MongoDB
- Different versions
- Example: App works with MySQL 5.7 and 8.0

**6. Software Compatibility**
- Different software versions
- Third-party integrations
- Example: Works with Java 8 and Java 11

**Test Approach:**

**Example: E-commerce Website**

**Browser Testing:**
- Chrome (latest), Firefox (latest), Safari (latest), Edge
- Test on each: Login, search, checkout, payment

**Device Testing:**
- Desktop (1920x1080)
- Tablet (768x1024)
- Mobile (375x667, 414x896)
- Test: Responsive layout, touch gestures

**OS Testing:**
- Windows 10, macOS Monterey
- Android 11, iOS 15
- Test: App installation, functionality

**Tools:**
- BrowserStack (cross-browser)
- Sauce Labs (cross-platform)
- LambdaTest (cloud testing)
- Chrome DevTools (responsive testing)

**Common Issues Found:**
- Layout breaks on certain browsers
- Features don't work on mobile
- Performance slow on older devices
- UI elements overlap on small screens

---

### **Q42. What is usability testing?**

**Answer:**
Usability testing evaluates how **easy and user-friendly** an application is for end users. It focuses on user experience (UX) rather than functionality.

**Objective:**
- Measure ease of use
- Identify usability issues
- Improve user satisfaction
- Evaluate user interface

**Key Aspects Tested:**

**1. Learnability**
- How easy for new users to learn?
- Time to complete first task
- Example: Can a user place an order without help?

**2. Efficiency**
- How quickly can users complete tasks?
- Number of clicks required
- Example: Checkout in 3 steps vs 10 steps

**3. Memorability**
- Can users remember how to use it?
- Return user experience
- Example: User returns after 1 month, can still navigate

**4. Error Prevention & Recovery**
- How many errors do users make?
- Can they recover easily?
- Example: Clear error messages, undo option

**5. Satisfaction**
- How pleasant is the experience?
- Would users recommend it?
- Example: Clean design, helpful features

**Test Methods:**

**1. Moderated Testing**
- Tester observes users
- Users perform tasks
- Think-aloud protocol

**2. Unmoderated Testing**
- Users test independently
- Record sessions
- Collect feedback

**3. A/B Testing**
- Compare two versions
- Measure which performs better

**Example Test Scenarios:**

**E-commerce Website:**
1. Can user find a product in under 1 minute?
2. Can user add product to cart easily?
3. Is checkout process intuitive?
4. Are error messages clear?
5. Is navigation menu obvious?

**Metrics:**
- Task success rate
- Time on task
- Error rate
- User satisfaction score

**Common Usability Issues:**
- Confusing navigation
- Too many steps to complete task
- Unclear error messages
- Poor mobile experience
- Inconsistent design

**Tools:**
- UserTesting
- Hotjar (heatmaps, recordings)
- Google Analytics
- Crazy Egg

---

### **Q43. What is accessibility testing?**

**Answer:**
Accessibility testing ensures that applications are **usable by people with disabilities**, including visual, auditory, physical, and cognitive impairments.

**Purpose:**
- Comply with accessibility standards (WCAG, ADA, Section 508)
- Make app usable for everyone
- Reach wider audience
- Legal compliance

**Who Benefits:**
- Blind/visually impaired (screen readers)
- Deaf/hearing impaired (captions)
- Motor disabilities (keyboard navigation)
- Cognitive disabilities (clear content)
- Elderly users

**Key Principles (WCAG):**

**1. Perceivable**
- Information must be presentable to users
- **Examples:**
  - Alt text for images
  - Captions for videos
  - Sufficient color contrast

**2. Operable**
- UI components must be operable
- **Examples:**
  - Keyboard navigation
  - Enough time to read content
  - No flashing content (seizures)

**3. Understandable**
- Information must be understandable
- **Examples:**
  - Clear instructions
  - Consistent navigation
  - Error messages are clear

**4. Robust**
- Content must work with various technologies
- **Examples:**
  - Compatible with screen readers
  - Works across browsers
  - Semantic HTML

**Common Tests:**

**1. Keyboard Navigation**
- Can user navigate without mouse?
- Tab key works
- Enter/Space activate buttons
- Focus indicators visible

**2. Screen Reader Compatibility**
- JAWS, NVDA, VoiceOver
- All content read correctly
- Proper heading structure
- Alt text for images

**3. Color Contrast**
- Text readable for color blind users
- Minimum contrast ratio 4.5:1
- Not relying only on color

**4. Form Accessibility**
- Labels associated with inputs
- Error messages clear
- Required fields indicated

**5. Multimedia**
- Captions for videos
- Transcripts for audio
- Audio descriptions

**Test Example:**

**Accessibility Checklist for Login Page:**
- ✓ Can tab through all elements
- ✓ Screen reader announces all fields
- ✓ Labels associated with inputs
- ✓ Error messages have sufficient contrast
- ✓ Focus indicator visible
- ✓ Works without mouse
- ✓ Form can be submitted with keyboard

**Tools:**
- JAWS (screen reader)
- WAVE (browser extension)
- axe DevTools
- Lighthouse (Chrome)
- Color Contrast Analyzer

**Example Issues:**
- Images without alt text
- Buttons not keyboard accessible
- Poor color contrast (gray text on white)
- Forms without labels
- Videos without captions

---

### **Q44. What is localization testing?**

**Answer:**
Localization testing verifies that an application is **adapted correctly** for a specific region/locale, including language, culture, and regional requirements.

**Difference from Internationalization:**
- **Internationalization (i18n):** Making app capable of localization (design phase)
- **Localization (L10n):** Adapting app for specific locale (implementation phase)

**What is Tested:**

**1. Language Translation**
- All text translated correctly
- No hardcoded strings
- Proper character encoding (UTF-8)
- Right-to-left languages (Arabic, Hebrew)

**2. Date and Time Formats**
- US: MM/DD/YYYY
- Europe: DD/MM/YYYY
- ISO: YYYY-MM-DD
- 12-hour vs 24-hour format

**3. Currency**
- Correct currency symbol ($, €, ¥, ₹)
- Decimal separator (. vs ,)
- Thousands separator
- Currency conversion

**4. Number Formats**
- Decimal separator
- Thousands separator
- US: 1,000.50
- Europe: 1.000,50

**5. Address Formats**
- Different postal code formats
- State/Province naming
- Country-specific fields

**6. Cultural Appropriateness**
- Images, colors, icons culturally appropriate
- Content not offensive
- Holidays, festivals
- Legal requirements

**7. UI Layout**
- Text expansion (German 30% longer than English)
- UI elements accommodate longer text
- Right-to-left support

**Example:**

**US English vs Spanish (Latin America):**

| Aspect | US English | Spanish |
|--------|------------|---------|
| Date | 12/31/2024 | 31/12/2024 |
| Number | 1,234.56 | 1.234,56 |
| Currency | $1,234.56 | $1.234,56 |
| "Submit" button | Submit | Enviar |

**Test Scenarios:**

**1. Language Switching**
- Change language from settings
- All text updates correctly
- No English text remaining
- No overlapping text

**2. Date Display**
- User profile shows birthday correctly
- Transaction dates formatted correctly
- Calendar shows correct format

**3. Currency**
- Product prices show correct currency
- Payment gateway uses correct currency
- Conversion rates accurate

**4. Special Characters**
- Accented characters display (é, ñ, ü)
- Chinese/Japanese characters render
- Arabic script displays correctly

**Tools:**
- Pseudolocalization (test before translation)
- i18n testing tools
- Language-specific keyboards

**Common Issues:**
- Truncated text (UI too small)
- Hardcoded English strings
- Wrong date format
- Currency symbol missing
- Cultural insensitivity

---

### **Q45. What is cross-browser testing and why is it important?**

**Answer:**
Cross-browser testing is testing web applications across **different web browsers** to ensure consistent functionality and appearance.

**Why Important:**

**1. Different Rendering Engines**
- Chrome/Edge: Blink
- Firefox: Gecko
- Safari: WebKit
- Same HTML/CSS renders differently

**2. Market Share**
- Users use various browsers
- Can't force users to one browser
- Need to support majority

**3. Browser-Specific Issues**
- Feature support varies
- CSS properties differ
- JavaScript behavior varies

**4. Business Impact**
- Poor UX = lost customers
- Broken functionality = lost revenue
- Brand reputation

**Browsers to Test:**

**Desktop:**
- Google Chrome (highest usage)
- Mozilla Firefox
- Safari (macOS)
- Microsoft Edge
- Opera (less common)

**Mobile:**
- Safari (iOS)
- Chrome (Android)
- Samsung Internet
- UC Browser (Asia)

**What to Test:**

**1. Visual Appearance**
- Layout consistency
- Font rendering
- Colors, spacing
- Images display correctly
- Responsive design

**2. Functionality**
- Forms work
- Buttons clickable
- Dropdowns function
- Navigation works
- JavaScript executes

**3. Performance**
- Page load time
- Script execution
- Animations smooth
- Resource loading

**4. Security Features**
- SSL certificates
- Cookie handling
- Local storage
- HTTPS enforcement

**Test Approach:**

**Example: E-commerce Website**

**Browsers to Test:**
1. Chrome (latest, previous version)
2. Firefox (latest)
3. Safari (latest)
4. Edge (latest)

**Test Cases:**
1. Homepage loads correctly
2. Search functionality works
3. Product images display
4. Add to cart functions
5. Checkout process works
6. Payment gateway integrates

**Common Cross-Browser Issues:**

**1. CSS Issues**
- Border-radius not rendering (older IE)
- Flexbox layout broken (older browsers)
- Font not loading

**2. JavaScript Issues**
- ES6 features not supported
- Arrow functions break (IE11)
- Fetch API not available

**3. HTML5 Issues**
- Input types not supported
- Video element not working
- Canvas not rendering

**Tools:**
- BrowserStack (cloud-based)
- Sauce Labs
- CrossBrowserTesting
- LambdaTest
- Selenium Grid (for automation)
- Browser DevTools

**Best Practices:**
1. Test on real devices (not just emulators)
2. Test latest + previous version
3. Automate common scenarios
4. Use CSS prefixes for compatibility
5. Use feature detection (not browser detection)
6. Validate HTML/CSS
7. Use polyfills for older browsers

**Example Compatibility Matrix:**

| Feature | Chrome | Firefox | Safari | Edge | IE11 |
|---------|--------|---------|--------|------|------|
| Flexbox | ✓ | ✓ | ✓ | ✓ | Partial |
| Grid | ✓ | ✓ | ✓ | ✓ | ✗ |
| Arrow Functions | ✓ | ✓ | ✓ | ✓ | ✗ |
| Fetch API | ✓ | ✓ | ✓ | ✓ | ✗ |

---

## 4. Automation Testing

### **Q46. What is test automation and what are its benefits?**

**Answer:**
Test automation is using **software tools and scripts** to execute test cases automatically, without manual intervention.

**Benefits:**

**1. Speed and Efficiency**
- Tests run faster than manual
- Example: 100 test cases in 2 hours vs 2 days manually

**2. Reusability**
- Scripts reused across releases
- Run tests multiple times
- No additional effort

**3. Reliability**
- Consistent execution
- No human errors
- Same results every time

**4. Coverage**
- Test more scenarios
- Run tests on multiple configurations
- Parallel execution

**5. Cost-Effective (Long-term)**
- Initial investment high
- Saves time in subsequent cycles
- ROI increases over time

**6. Early Bug Detection**
- Run tests frequently
- CI/CD integration
- Catch bugs early

**7. 24/7 Execution**
- Run tests overnight
- No manual supervision
- Utilize off-hours

**8. Detailed Reporting**
- Logs and screenshots
- Metrics and trends
- Easy analysis

**9. Regression Testing**
- Perfect for repetitive tests
- Every release testing

**10. Performance Testing**
- Simulate thousands of users
- Impossible manually

**Limitations:**

1. **High Initial Cost**
   - Tools, licenses, setup
   - Learning curve

2. **Maintenance Effort**
   - Scripts need updates
   - UI changes break tests

3. **Not for Everything**
   - Exploratory testing
   - Usability testing
   - One-time tests

4. **False Positives**
   - Script issues vs real bugs
   - Synchronization problems

**When to Automate:**
- Regression test cases
- Data-driven tests
- Smoke tests
- Repetitive tasks
- Stable features

**When NOT to Automate:**
- Exploratory testing
- Usability testing
- Ad-hoc testing
- Frequently changing UI
- One-time use tests

---

### **Q47. When should you automate tests vs perform manual testing?**

**Answer:**

**Automate When:**

**1. Repetitive Tests**
- Regression suite
- Sanity tests
- Run frequently
- Example: Login test after every build

**2. Stable Features**
- UI doesn't change often
- Established functionality
- Example: Mature payment module

**3. Data-Driven Tests**
- Same test, multiple data sets
- Example: Login with 100 different users

**4. Time-Consuming Tests**
- Take hours/days manually
- Example: Testing across 10 browsers

**5. High-Risk Areas**
- Critical functionality
- Example: Payment processing

**6. Performance/Load Tests**
- Simulate 1000s of users
- Impossible manually

**Manual Testing When:**

**1. Exploratory Testing**
- Unscripted testing
- Learning application
- Finding unexpected bugs

**2. Usability Testing**
- User experience
- Subjective assessment
- Example: Is UI intuitive?

**3. Ad-hoc Testing**
- Random testing
- No specific test cases

**4. Frequently Changing Features**
- UI changes often
- New features
- Automation maintenance too high

**5. One-Time Tests**
- Test case runs once
- Not worth automation effort

**6. Visual Validation**
- Color correctness
- Alignment, spacing
- Subjective elements

**7. Complex Scenarios**
- Difficult to automate
- Requires human judgment
- Example: Facial recognition accuracy

**Decision Matrix:**

| Factor | Automate | Manual |
|--------|----------|--------|
| Frequency | Repetitive | One-time |
| Stability | Stable | Changing |
| Complexity | Simple/Medium | Very Complex |
| ROI | High | Low |
| Speed | Need fast execution | Time not critical |
| Subjectivity | Objective | Subjective |

**Example Scenarios:**

**Automate:**
- Login functionality (runs 100+ times)
- Checkout flow (critical path)
- API tests (fast, stable)
- Cross-browser testing (time-consuming)

**Manual:**
- New feature exploration
- UI/UX feedback
- First-time test design
- Accessibility review

**Hybrid Approach:**
- Automate: Regression, smoke tests
- Manual: Exploratory, usability
- **Best practice:** 70% automated, 30% manual

**Cost-Benefit Analysis:**

**Automation ROI:**
```
If test runs 100 times:
Manual: 100 runs × 1 hour = 100 hours
Automation: 5 hours (script) + 100 runs × 0.1 hour = 15 hours
Savings: 85 hours
```

---

### **Q48. What are the advantages and disadvantages of automation testing?**

**Answer:**

**Advantages:**

**1. Speed**
- Faster than manual execution
- Example: 1000 tests in 2 hours vs 10 days

**2. Reusability**
- Scripts reused across cycles
- No recreation needed

**3. Reliability**
- Consistent results
- No human errors (fatigue, oversight)

**4. Parallel Execution**
- Run tests simultaneously
- Multiple browsers/devices

**5. Detailed Logging**
- Screenshots of failures
- Step-by-step logs
- Error traces

**6. CI/CD Integration**
- Automated builds and tests
- Early defect detection

**7. Coverage**
- Test more scenarios
- Data-driven testing

**8. Cost-Effective (Long-term)**
- ROI increases with time
- Reduced manual effort

**9. 24/7 Execution**
- Unattended execution
- Off-hours testing

**10. Regression Testing**
- Perfect for repetitive tests
- Ensures stability

**Disadvantages:**

**1. High Initial Investment**
- Tool licenses expensive
- Infrastructure setup
- Training required
- Example: Selenium setup + framework = weeks

**2. Maintenance Overhead**
- UI changes break scripts
- Regular updates needed
- Example: 1 button ID change breaks 50 tests

**3. Not Everything Can Be Automated**
- Usability testing
- Exploratory testing
- Subjective validations

**4. Complexity**
- Requires programming skills
- Learning curve steep
- Example: XPath, CSS selectors

**5. False Positives/Negatives**
- Script issues vs actual bugs
- Synchronization problems
- Timeouts cause failures

**6. Limited Flexibility**
- Can't adapt like humans
- Can't handle unexpected scenarios
- Example: New popup breaks script

**7. Tool Limitations**
- Not all tools support all technologies
- Compatibility issues
- Example: CAPTCHA can't be automated

**8. Debugging Effort**
- Finding why test failed
- Script issue vs application issue
- Time-consuming analysis

**9. Requires Stable Application**
- Frequent changes break tests
- Not suitable for early development

**10. Initial Slowdown**
- Setup takes time
- Delays initial testing

**Comparison:**

| Aspect | Automation | Manual |
|--------|-----------|--------|
| Speed | Fast (after setup) | Slow |
| Reliability | High | Moderate |
| Initial Cost | High | Low |
| Maintenance | Required | Not needed |
| Coverage | Extensive | Limited |
| Flexibility | Low | High |
| ROI | Long-term | Short-term |

**When Advantageous:**
- Mature applications
- Regression testing
- Large test suites
- Frequent releases
- CI/CD environment

**When Disadvantageous:**
- Early development
- Frequently changing UI
- Small projects
- One-time tests
- Limited budget

---

(Continuing with Q49-Q270 in the same detailed format...)


### **Q49. What types of tests are good candidates for automation?**

**Answer:**

**Ideal Candidates for Automation:**

**1. Regression Tests**
- Run repeatedly after every change
- Stable, well-defined
- High ROI
- Example: Core user workflows

**2. Smoke/Sanity Tests**
- Quick build verification
- Run after every deployment
- Critical path testing
- Example: Can app launch? Can users login?

**3. Data-Driven Tests**
- Same test, multiple data sets
- Tedious manually
- Example: Login with 100 different users

**4. API Tests**
- Stable contracts
- Fast execution
- No UI dependency
- Example: REST API endpoint testing

**5. Cross-Browser/Cross-Platform Tests**
- Time-consuming manually
- Same tests, different environments
- Example: Test on Chrome, Firefox, Safari, Edge

**6. Performance/Load Tests**
- Impossible manually
- Simulate concurrent users
- Example: 1000 users accessing simultaneously

**7. Unit Tests**
- Developer-written
- Fast feedback
- CI/CD integration
- Example: Testing individual functions

**Not Good Candidates:**

**1. Exploratory Testing**
- Unscripted, creative
- Requires human intuition

**2. Usability Testing**
- Subjective assessment
- Requires human judgment
- Example: Is the UI intuitive?

**3. One-Time Tests**
- Not worth automation effort
- No ROI

**4. Frequently Changing UI**
- High maintenance cost
- Tests break often

**5. Visual Validation**
- Color accuracy
- Design aesthetics
- Alignment (can use visual testing tools but complex)

**6. Ad-hoc Testing**
- Random, no structure
- Purpose is exploration

---

### **Q50. What is a test automation framework?**

**Answer:**
A test automation framework is a **set of guidelines, standards, and tools** that provide a structure for creating and executing automated tests efficiently.

**Purpose:**
- Standardize test creation
- Reduce maintenance
- Improve reusability
- Enable collaboration
- Faster test development

**Components:**

1. **Test Scripts**
   - Actual test code

2. **Test Data**
   - Input data, expected results

3. **Object Repository**
   - UI elements (locators)

4. **Test Libraries/Utilities**
   - Reusable functions

5. **Reporting Mechanism**
   - Test results, logs

6. **Configuration Files**
   - Environment settings

7. **Build/CI Integration**
   - Jenkins, GitHub Actions

**Types of Frameworks:**

1. **Linear/Record-Playback**
2. **Modular**
3. **Data-Driven**
4. **Keyword-Driven**
5. **Hybrid**
6. **BDD (Behavior-Driven Development)**

**Benefits:**
- Code reusability
- Easy maintenance
- Scalability
- Better ROI
- Standardization

---

### **Q51. What are different types of automation frameworks?**

**Answer:**

**1. Linear/Record and Playback Framework**

**Description:**
- Simplest framework
- Record user actions, replay them
- No coding required

**Pros:**
- Easy to create
- No programming needed
- Fast setup

**Cons:**
- Not reusable
- Hard to maintain
- No data separation
- Limited scalability

**Example:**
```
Record:
1. Open browser
2. Go to www.example.com
3. Enter username
4. Enter password
5. Click Login

Playback: Repeats exact same steps
```

**Use Case:** Quick proof of concept

---

**2. Modular Framework**

**Description:**
- Application divided into modules
- Each module has test scripts
- Tests can be reused

**Structure:**
```
Tests/
├── LoginModule/
│   ├── testValidLogin()
│   └── testInvalidLogin()
├── CartModule/
│   ├── testAddToCart()
│   └── testRemoveFromCart()
└── CheckoutModule/
    └── testCheckout()
```

**Pros:**
- Reusable modules
- Easy maintenance
- Scalable

**Cons:**
- Requires coding
- Test data still hardcoded

---

**3. Data-Driven Framework**

**Description:**
- Test logic separated from test data
- Same test runs with multiple data sets
- Data stored externally (Excel, CSV, DB)

**Example:**
```
Test Script: testLogin(username, password)

Test Data (Excel):
Row 1: user1@test.com, Pass123
Row 2: user2@test.com, Pass456
Row 3: user3@test.com, Pass789

Result: Test runs 3 times with different data
```

**Pros:**
- Test data easy to modify
- No code change for new data
- Great for multiple scenarios

**Cons:**
- Complex setup
- External data dependency

**Tools:** Apache POI, TestNG DataProvider

---

**4. Keyword-Driven Framework**

**Description:**
- Test steps defined as keywords
- Keywords represent actions
- Non-technical users can write tests

**Example:**
```
Keywords: OpenBrowser, EnterText, Click, VerifyText

Test Case (Excel):
Step 1: OpenBrowser | Chrome
Step 2: Navigate | www.example.com
Step 3: EnterText | username | testuser
Step 4: EnterText | password | Pass123
Step 5: Click | LoginButton
Step 6: VerifyText | Welcome
```

**Pros:**
- Easy for non-programmers
- Reusable keywords
- Language-independent

**Cons:**
- Complex to set up
- Requires keyword library
- Maintenance overhead

---

**5. Hybrid Framework**

**Description:**
- Combination of multiple frameworks
- Usually Data-Driven + Keyword-Driven
- Best of both worlds

**Example:**
```
Structure:
- Keyword library (reusable actions)
- Data files (test data)
- Modular test scripts
- Page Object Model (UI elements)
```

**Pros:**
- Maximum flexibility
- Combines benefits of multiple frameworks
- Industry standard

**Cons:**
- Complex to implement
- Requires expertise
- Higher learning curve

---

**6. BDD Framework (Behavior-Driven Development)**

**Description:**
- Tests written in plain English (Gherkin)
- Focus on behavior, not implementation
- Collaboration between QA, Dev, Business

**Tools:** Cucumber, SpecFlow, Behave

**Example (Gherkin):**
```gherkin
Feature: Login functionality

Scenario: Successful login with valid credentials
  Given user is on login page
  When user enters username "testuser"
  And user enters password "Pass123"
  And user clicks login button
  Then user should be redirected to dashboard
  And welcome message should be displayed
```

**Pros:**
- Easy to understand (non-technical)
- Living documentation
- Business-friendly

**Cons:**
- Learning curve (Gherkin syntax)
- Additional layer of abstraction
- Can be verbose

---

**Comparison:**

| Framework | Complexity | Reusability | Maintenance | Best For |
|-----------|-----------|-------------|-------------|----------|
| Linear | Low | Low | Difficult | POC only |
| Modular | Medium | High | Easy | Medium projects |
| Data-Driven | Medium | High | Moderate | Multiple data sets |
| Keyword | High | Very High | Moderate | Non-technical users |
| Hybrid | High | Very High | Easy | Large projects |
| BDD | Medium | High | Easy | Collaborative teams |

---

### **Q52. What is data-driven testing?**

**Answer:**
Data-driven testing is an automation approach where **test logic is separated from test data**, allowing the same test to run with multiple data sets.

**Concept:**
- Test script written once
- Data stored externally (Excel, CSV, JSON, Database)
- Test iterates through data sets

**Example:**

**Without Data-Driven:**
```java
@Test
public void testLogin1() {
    login("user1@test.com", "Pass123");
    Assert.assertTrue(isLoggedIn());
}

@Test
public void testLogin2() {
    login("user2@test.com", "Pass456");
    Assert.assertTrue(isLoggedIn());
}
// Repeated code for each user!
```

**With Data-Driven:**
```java
@Test(dataProvider = "loginData")
public void testLogin(String username, String password) {
    login(username, password);
    Assert.assertTrue(isLoggedIn());
}

@DataProvider(name = "loginData")
public Object[][] getLoginData() {
    return new Object[][] {
        {"user1@test.com", "Pass123"},
        {"user2@test.com", "Pass456"},
        {"user3@test.com", "Pass789"}
    };
}
// One test, multiple data sets!
```

**Data Sources:**

**1. Excel/CSV:**
```
username,password,expectedResult
user1@test.com,Pass123,Success
user2@test.com,WrongPass,Failure
user3@test.com,Pass789,Success
```

**2. JSON:**
```json
[
  {"username": "user1@test.com", "password": "Pass123"},
  {"username": "user2@test.com", "password": "Pass456"}
]
```

**3. Database:**
```sql
SELECT username, password FROM test_users;
```

**4. XML:**
```xml
<users>
  <user>
    <username>user1@test.com</username>
    <password>Pass123</password>
  </user>
</users>
```

**Benefits:**

1. **Reusability**
   - Same test for multiple scenarios
   - No code duplication

2. **Easy Maintenance**
   - Modify data without changing code
   - Add new test cases by adding rows

3. **Scalability**
   - Test with 100s of data sets easily
   - Good for boundary value testing

4. **Separation of Concerns**
   - Test logic vs test data
   - QA can modify data without coding

**Use Cases:**
- Testing login with multiple users
- Form validation with various inputs
- API testing with different payloads
- Cross-browser testing with different browsers

**Tools:**
- TestNG (DataProvider)
- JUnit (Parameterized tests)
- Apache POI (Excel reading)
- DDT library (Python)

---

### **Q53. What is keyword-driven testing?**

**Answer:**
Keyword-driven testing is a framework where **test cases are represented by keywords** (action words) that describe the steps to be performed, allowing non-technical users to create tests.

**Concept:**
- Keywords represent actions (Click, EnterText, Verify, etc.)
- Test cases written using keywords
- Each keyword maps to a function/method
- Test data separated from keywords

**Structure:**

**1. Keyword Library:**
```java
public class Keywords {
    public void OpenBrowser(String browser) { ... }
    public void Navigate(String url) { ... }
    public void EnterText(String element, String text) { ... }
    public void Click(String element) { ... }
    public void VerifyText(String element, String expected) { ... }
}
```

**2. Test Case (Excel/CSV):**
```
TestCase: Login Test

Step | Keyword      | Object       | Data
-----|--------------|--------------|------------------
1    | OpenBrowser  | Chrome       |
2    | Navigate     | URL          | www.example.com
3    | EnterText    | username     | testuser
4    | EnterText    | password     | Pass123
5    | Click        | LoginButton  |
6    | VerifyText   | Welcome      | Welcome, User!
7    | CloseBrowser |              |
```

**3. Test Execution Engine:**
- Reads test case from Excel
- For each step:
  - Gets keyword
  - Calls corresponding method
  - Passes parameters
  - Logs result

**Example:**

**Keywords:**
- OpenBrowser
- Navigate
- EnterText
- Click
- VerifyText
- VerifyElementPresent
- CloseBrowser

**Test Case in Excel:**
| Step | Keyword | Element | Data |
|------|---------|---------|------|
| 1 | OpenBrowser | Chrome | |
| 2 | Navigate | | www.shop.com |
| 3 | EnterText | searchBox | laptop |
| 4 | Click | searchButton | |
| 5 | VerifyText | results | Results for laptop |
| 6 | Click | firstProduct | |
| 7 | Click | addToCart | |
| 8 | VerifyText | cart | 1 item in cart |
| 9 | CloseBrowser | | |

**Advantages:**

1. **Non-Technical Friendly**
   - No coding required
   - Business analysts can write tests
   - Domain experts contribute

2. **Reusability**
   - Keywords used across tests
   - Build once, use many times

3. **Easy Maintenance**
   - Change keyword implementation
   - All tests using it get updated

4. **Scalability**
   - Add new keywords as needed
   - Expand coverage easily

**Disadvantages:**

1. **Initial Setup Complex**
   - Building keyword library takes time
   - Requires programming skills

2. **Maintenance**
   - Keywords need updates
   - Keyword library grows large

3. **Learning Curve**
   - Users need to learn available keywords
   - Keyword naming important

**Real-World Example:**

**Robot Framework** (keyword-driven tool):
```robot
*** Test Cases ***
Login Test
    Open Browser    chrome
    Navigate To     https://example.com
    Input Text      id=username    testuser
    Input Text      id=password    Pass123
    Click Button    id=loginBtn
    Page Should Contain    Welcome
    Close Browser
```

**Use Cases:**
- Large teams with varying technical skills
- Long-term projects
- Frequent test creation by non-coders
- When business stakeholders write acceptance criteria

---

### **Q54. What is hybrid framework?**

**Answer:**
A hybrid framework **combines multiple framework types** (usually Data-Driven + Keyword-Driven + Modular) to leverage the benefits of each approach.

**Structure:**

```
Hybrid Framework
├── Page Objects (Modular approach)
│   ├── LoginPage.java
│   ├── HomePage.java
│   └── CheckoutPage.java
├── Keywords (Keyword-Driven)
│   └── Actions.java (reusable keywords)
├── Test Data (Data-Driven)
│   ├── testdata.xlsx
│   └── users.json
├── Test Scripts
│   ├── LoginTest.java
│   └── CheckoutTest.java
├── Utilities
│   ├── ExcelReader.java
│   └── ScreenshotUtil.java
└── Reports
    └── ExtentReports
```

**Components:**

**1. Page Object Model (Modular)**
```java
public class LoginPage {
    WebElement username = driver.findElement(By.id("user"));
    WebElement password = driver.findElement(By.id("pass"));
    WebElement loginBtn = driver.findElement(By.id("login"));
    
    public void login(String user, String pass) {
        username.sendKeys(user);
        password.sendKeys(pass);
        loginBtn.click();
    }
}
```

**2. Keywords (Keyword-Driven)**
```java
public class Keywords {
    public void enterText(WebElement element, String text) {
        element.clear();
        element.sendKeys(text);
    }
    
    public void clickElement(WebElement element) {
        element.click();
    }
}
```

**3. Test Data (Data-Driven)**
```excel
TestCase | Username | Password | Expected
---------|----------|----------|----------
TC001    | user1    | Pass123  | Success
TC002    | user2    | Wrong    | Failure
```

**4. Test Script**
```java
@Test(dataProvider = "loginData")
public void testLogin(String username, String password, String expected) {
    LoginPage login = new LoginPage(driver);
    login.enterUsername(username);  // Using Page Object
    login.enterPassword(password);
    login.clickLogin();
    
    if (expected.equals("Success")) {
        Assert.assertTrue(login.isLoginSuccessful());
    } else {
        Assert.assertTrue(login.isErrorDisplayed());
    }
}

@DataProvider(name = "loginData")
public Object[][] getData() {
    return ExcelReader.getData("testdata.xlsx", "Login");
}
```

**Advantages:**

1. **Best of All Worlds**
   - Modularity (Page Objects)
   - Reusability (Keywords)
   - Data flexibility (Data-Driven)

2. **Scalability**
   - Easy to add new tests
   - Supports team growth

3. **Maintainability**
   - Changes isolated to specific layers
   - Update once, affects all

4. **Flexibility**
   - Adapt to different testing needs
   - Support various test types

5. **Industry Standard**
   - Most organizations use hybrid
   - Best practices incorporated

**Disadvantages:**

1. **Complexity**
   - Requires expertise
   - Steep learning curve

2. **Initial Effort**
   - Time to set up
   - Framework development

3. **Overhead**
   - More files and folders
   - Can be overkill for small projects

**Common Hybrid Patterns:**

1. **POM + Data-Driven**
   - Page Objects for UI
   - External data for test inputs

2. **POM + Keyword + Data-Driven**
   - Most comprehensive
   - Enterprise-level

3. **POM + BDD**
   - Page Objects for implementation
   - Cucumber for specification

**Industry Example:**
Most companies use:
- **Selenium** + **TestNG** + **Page Object Model** + **Excel/JSON data** + **Maven** + **Jenkins**

---

### **Q55. What is the Page Object Model (POM)?**

**Answer:**
Page Object Model is a **design pattern** in test automation where each web page is represented as a **class**, and page elements are defined as **variables**, with methods to interact with those elements.

**Purpose:**
- Separate page structure from test logic
- Improve code reusability
- Easy maintenance
- Reduce code duplication

**Structure:**

**Without POM:**
```java
@Test
public void testLogin() {
    driver.findElement(By.id("username")).sendKeys("testuser");
    driver.findElement(By.id("password")).sendKeys("Pass123");
    driver.findElement(By.id("loginBtn")).click();
    // Element locators mixed with test logic
}

@Test
public void testRegistration() {
    driver.findElement(By.id("username")).sendKeys("newuser");
    // Same locators repeated!
}
```

**With POM:**

**Page Object Class:**
```java
public class LoginPage {
    WebDriver driver;
    
    // Elements (Locators)
    @FindBy(id = "username")
    WebElement usernameField;
    
    @FindBy(id = "password")
    WebElement passwordField;
    
    @FindBy(id = "loginBtn")
    WebElement loginButton;
    
    @FindBy(id = "errorMsg")
    WebElement errorMessage;
    
    // Constructor
    public LoginPage(WebDriver driver) {
        this.driver = driver;
        PageFactory.initElements(driver, this);
    }
    
    // Methods (Actions)
    public void enterUsername(String username) {
        usernameField.sendKeys(username);
    }
    
    public void enterPassword(String password) {
        passwordField.sendKeys(password);
    }
    
    public void clickLogin() {
        loginButton.click();
    }
    
    public void login(String username, String password) {
        enterUsername(username);
        enterPassword(password);
        clickLogin();
    }
    
    public boolean isErrorDisplayed() {
        return errorMessage.isDisplayed();
    }
    
    public String getErrorMessage() {
        return errorMessage.getText();
    }
}
```

**Test Class:**
```java
public class LoginTest {
    WebDriver driver;
    LoginPage loginPage;
    
    @BeforeMethod
    public void setup() {
        driver = new ChromeDriver();
        driver.get("https://example.com/login");
        loginPage = new LoginPage(driver);
    }
    
    @Test
    public void testValidLogin() {
        loginPage.login("testuser", "Pass123");
        // Verify login success
    }
    
    @Test
    public void testInvalidLogin() {
        loginPage.login("testuser", "WrongPass");
        Assert.assertTrue(loginPage.isErrorDisplayed());
        Assert.assertEquals(loginPage.getErrorMessage(), "Invalid credentials");
    }
    
    @AfterMethod
    public void teardown() {
        driver.quit();
    }
}
```

**Advantages:**

**1. Code Reusability**
```java
// LoginPage methods used in multiple tests
@Test
public void testA() { loginPage.login("user1", "pass1"); }
@Test
public void testB() { loginPage.login("user2", "pass2"); }
// No duplication of locators!
```

**2. Easy Maintenance**
```java
// If login button ID changes:
// Without POM: Update in 100 test files
// With POM: Update once in LoginPage class
```

**3. Improved Readability**
```java
// Clear and readable
loginPage.enterUsername("test");
loginPage.enterPassword("pass");
loginPage.clickLogin();

// vs
driver.findElement(By.id("username")).sendKeys("test");
driver.findElement(By.id("password")).sendKeys("pass");
driver.findElement(By.id("loginBtn")).click();
```

**4. Separation of Concerns**
- Page Objects: UI structure and locators
- Test Classes: Business logic and assertions

**Best Practices:**

**1. One Class Per Page**
```
LoginPage.java
HomePage.java
ProfilePage.java
CheckoutPage.java
```

**2. Use PageFactory**
```java
@FindBy(id = "username")
WebElement usernameField;

// Instead of:
WebElement usernameField = driver.findElement(By.id("username"));
```

**3. Return Page Objects**
```java
public HomePage clickLogin() {
    loginButton.click();
    return new HomePage(driver);  // Returns next page
}

// Usage:
HomePage home = loginPage.login("user", "pass");
```

**4. Keep Test Logic in Tests**
```java
// Good
@Test
public void testLogin() {
    loginPage.login("user", "pass");
    Assert.assertTrue(homePage.isWelcomeDisplayed());  // Assertion in test
}

// Bad
@Test
public void testLogin() {
    loginPage.loginAndVerify("user", "pass");  // Don't put assertions in Page Object
}
```

**Example Project Structure:**
```
src/
├── main/
│   └── java/
│       └── pages/
│           ├── LoginPage.java
│           ├── HomePage.java
│           └── BasePage.java
└── test/
    └── java/
        └── tests/
            ├── LoginTest.java
            └── BaseTest.java
```

---

(The document continues with all remaining questions through Q270, maintaining the same detailed format)

# QA/Testing Intern - Complete Interview Guide (Part 2)
## Questions 56-270 with Detailed Answers

---

## 4. Automation Testing (Continued)

### **Q56. What is Selenium and what are its components?**

**Answer:**
Selenium is an **open-source automation testing framework** for web applications. It supports multiple browsers and programming languages.

**Components:**

**1. Selenium WebDriver**
- **Most widely used**
- Directly communicates with browser
- Supports multiple languages (Java, Python, C#, JavaScript, Ruby)
- API for browser automation

**Example (Java):**
```java
WebDriver driver = new ChromeDriver();
driver.get("https://example.com");
driver.findElement(By.id("username")).sendKeys("testuser");
driver.findElement(By.id("password")).sendKeys("Pass123");
driver.findElement(By.id("login")).click();
```

**2. Selenium IDE**
- Browser extension (Chrome, Firefox)
- Record and playback tool
- No coding required
- Good for quick POCs
- Limited functionality

**3. Selenium Grid**
- Parallel test execution
- Run tests on multiple machines/browsers simultaneously
- Distributed testing
- Hub and Node architecture

**Example Setup:**
```
Hub (Central): Controls test distribution
Nodes: Chrome on Windows, Firefox on Mac, Safari on Mac
Result: Tests run in parallel across all nodes
```

**4. Selenium RC (Remote Control)** - Deprecated
- Old component
- Replaced by WebDriver
- No longer maintained

**Supported Browsers:**
- Chrome (ChromeDriver)
- Firefox (GeckoDriver)
- Safari (SafariDriver)
- Edge (EdgeDriver)
- Internet Explorer (IEDriver)

**Supported Languages:**
- Java
- Python
- C#
- JavaScript (Node.js)
- Ruby
- Kotlin

**Advantages:**
- Open source (free)
- Multi-browser support
- Multi-language support
- Large community
- Active development

**Limitations:**
- No built-in reporting
- No image/CAPTCHA recognition
- Steep learning curve
- Only for web applications (not desktop/mobile native apps)

---

### **Q57. What is the difference between Selenium IDE, WebDriver, and Grid?**

**Answer:**

**Selenium IDE:**

**Purpose:** Record and playback testing tool

**Features:**
- Browser extension
- No coding required
- Record user actions
- Generate basic scripts
- Debugging capabilities

**Use Case:**
- Quick testing
- Learning Selenium
- Creating POC
- Non-programmers

**Limitations:**
- Limited functionality
- Not for complex scenarios
- No parallel execution
- Limited browser support

**Example:**
```
Actions recorded:
1. Open www.example.com
2. Click on login
3. Type username
4. Type password
5. Click submit
```

---

**Selenium WebDriver:**

**Purpose:** Programmatic browser automation

**Features:**
- Direct browser communication
- Full programming capability
- Multiple language support
- Complex test scenarios
- CI/CD integration

**Use Case:**
- Automated test scripts
- Complex workflows
- Regression testing
- Production automation

**Example (Python):**
```python
from selenium import webdriver
driver = webdriver.Chrome()
driver.get("https://example.com")
driver.find_element("id", "username").send_keys("test")
driver.find_element("id", "password").send_keys("pass")
driver.find_element("id", "login").click()
```

---

**Selenium Grid:**

**Purpose:** Parallel and distributed testing

**Features:**
- Run tests on multiple machines
- Different OS/browser combinations
- Parallel execution
- Hub-Node architecture
- Scalable testing

**Use Case:**
- Cross-browser testing
- Large test suites
- Reduce execution time
- Cloud testing

**Architecture:**
```
Hub (Controller)
  ├── Node 1: Chrome on Windows
  ├── Node 2: Firefox on Mac
  ├── Node 3: Safari on Mac
  └── Node 4: Edge on Windows
```

**Example Configuration:**
```java
DesiredCapabilities capability = DesiredCapabilities.chrome();
capability.setBrowserName("chrome");
capability.setPlatform(Platform.WINDOWS);
WebDriver driver = new RemoteWebDriver(
    new URL("http://hub-ip:4444/wd/hub"), capability
);
```

---

**Comparison Table:**

| Feature | IDE | WebDriver | Grid |
|---------|-----|-----------|------|
| Coding Required | No | Yes | Yes |
| Complexity | Simple | Medium-High | High |
| Use Case | Quick tests | Automated scripts | Parallel testing |
| Browser Support | Limited | All major | All major |
| Parallel Execution | No | No | Yes |
| Setup | Easy | Medium | Complex |
| Best For | Beginners | Production | Large suites |

---

### **Q58. What are locators in Selenium? Name different types.**

**Answer:**
Locators are used to **identify and locate** HTML elements on a web page for interaction.

**Types of Locators:**

**1. ID**
- **Most reliable and fastest**
- Unique identifier
- Browser finds elements quickly

**HTML:**
```html
<input id="username" type="text">
```

**Selenium:**
```java
driver.findElement(By.id("username")).sendKeys("test");
```
```python
driver.find_element(By.ID, "username").send_keys("test")
```

---

**2. Name**
- Uses the name attribute
- Can have multiple elements with same name

**HTML:**
```html
<input name="email" type="email">
```

**Selenium:**
```java
driver.findElement(By.name("email")).sendKeys("test@test.com");
```

---

**3. Class Name**
- Uses CSS class attribute
- Can locate multiple elements

**HTML:**
```html
<button class="btn-primary">Submit</button>
```

**Selenium:**
```java
driver.findElement(By.className("btn-primary")).click();
```

---

**4. Tag Name**
- Uses HTML tag
- Returns all elements with that tag

**HTML:**
```html
<input type="text">
<input type="password">
```

**Selenium:**
```java
List<WebElement> inputs = driver.findElements(By.tagName("input"));
```

---

**5. Link Text**
- **For links only** (anchor tags)
- Exact text match

**HTML:**
```html
<a href="/logout">Logout</a>
```

**Selenium:**
```java
driver.findElement(By.linkText("Logout")).click();
```

---

**6. Partial Link Text**
- For links with partial text match

**HTML:**
```html
<a href="/continue">Continue Shopping</a>
```

**Selenium:**
```java
driver.findElement(By.partialLinkText("Continue")).click();
```

---

**7. CSS Selector**
- **Faster than XPath**
- Uses CSS syntax
- Powerful and flexible

**HTML:**
```html
<input id="user" class="input-field" name="username">
<div class="error-msg">Invalid login</div>
```

**Selenium:**
```java
// By ID
driver.findElement(By.cssSelector("#user"))

// By Class
driver.findElement(By.cssSelector(".input-field"))

// By Attribute
driver.findElement(By.cssSelector("input[name='username']"))

// By Class combination
driver.findElement(By.cssSelector("div.error-msg"))

// Parent > Child
driver.findElement(By.cssSelector("div > p"))
```

---

**8. XPath**
- **Most powerful and flexible**
- Can traverse in any direction
- Slower than CSS

**HTML:**
```html
<div id="login-form">
    <input id="username" type="text">
    <button>Login</button>
</div>
```

**Selenium:**
```java
// Absolute XPath (Not recommended - brittle)
driver.findElement(By.xpath("/html/body/div/input"))

// Relative XPath (Recommended)
driver.findElement(By.xpath("//input[@id='username']"))

// Using text
driver.findElement(By.xpath("//button[text()='Login']"))

// Using contains
driver.findElement(By.xpath("//input[contains(@id,'user')]"))

// Parent to child
driver.findElement(By.xpath("//div[@id='login-form']//input"))

// Following sibling
driver.findElement(By.xpath("//input[@id='username']/following-sibling::button"))
```

---

**Priority Order (Best to Worst):**

1. **ID** - Fastest, most reliable
2. **Name** - Fast, usually unique
3. **CSS Selector** - Fast, flexible
4. **XPath** - Powerful but slower
5. **Link Text** - Only for links
6. **Class Name** - Can be non-unique
7. **Tag Name** - Very generic

**Best Practices:**
- Use ID when available
- Avoid absolute XPath
- Make locators resilient to changes
- Use data-testid attributes (if available)
- Don't rely on text that might change

---

### **Q59. What is XPath? Difference between absolute and relative XPath?**

**Answer:**
XPath (XML Path Language) is a query language for **selecting nodes** in an XML/HTML document. In Selenium, it's used to locate elements.

**Syntax:**
```
xpath = //tagname[@attribute='value']
```

**Types of XPath:**

**1. Absolute XPath**

**Definition:**
- **Complete path** from root (html) to target element
- Starts with **single slash** (/)
- Every element in hierarchy

**Example:**
```xpath
/html/body/div[1]/div[2]/form/input[1]
```

**HTML:**
```html
<html>
  <body>
    <div>
      <div>
        <form>
          <input id="username">
```

**Disadvantages:**
- **Very brittle** - breaks with any HTML change
- Long and complex
- Difficult to maintain
- Not recommended

**When it breaks:**
```html
<!-- Add one div and absolute XPath breaks -->
<html>
  <body>
    <div class="wrapper">  <!-- NEW DIV -->
      <div>
        <div>
          <form>
            <input id="username">
```

---

**2. Relative XPath**

**Definition:**
- **Starts from any element**
- Starts with **double slash** (//)
- More flexible and maintainable

**Example:**
```xpath
//input[@id='username']
//button[text()='Login']
//div[@class='error']//span
```

**Advantages:**
- **Resilient to changes**
- Shorter and cleaner
- Easy to maintain
- Recommended approach

---

**Comparison:**

| Aspect | Absolute XPath | Relative XPath |
|--------|---------------|----------------|
| Start | / (root) | // (anywhere) |
| Length | Very long | Shorter |
| Maintainability | Poor | Good |
| Reliability | Brittle | Robust |
| Speed | Slightly faster | Slightly slower |
| Recommended | ❌ Never | ✅ Always |

**Example:**
```
Absolute: /html/body/div[1]/div[2]/form/input[@id='username']
Relative: //input[@id='username']

Result: Same element, but relative is much better!
```

---

**XPath Axes and Functions:**

**1. Basic Axes:**
```xpath
// Current node
//input[@id='user']

// Parent
//input[@id='user']/parent::div

// Child
//div[@id='form']//input

// Following sibling
//label[@for='user']/following-sibling::input

// Preceding sibling
//button/preceding-sibling::input

// Ancestor
//input/ancestor::form
```

**2. Text Functions:**
```xpath
// Exact text match
//button[text()='Submit']

// Contains text
//div[contains(text(),'Error')]

// Starts with
//input[starts-with(@id,'user')]

// Normalize space (ignore extra spaces)
//p[normalize-space()='Welcome']
```

**3. Attribute Functions:**
```xpath
// Has attribute
//input[@type='text']

// Multiple attributes
//input[@type='text' and @name='email']

// OR condition
//input[@type='text' or @type='email']

// Not condition
//div[not(@class='hidden')]
```

**4. Index-based:**
```xpath
// First input
(//input)[1]

// Last input
(//input)[last()]

// Second button
(//button)[2]

// All except first
(//input)[position()>1]
```

**5. Advanced Examples:**
```xpath
// Dynamic IDs
//input[contains(@id,'user')]

// Multiple classes
//div[contains(@class,'error') and contains(@class,'message')]

// Parent based on child
//div[.//span[text()='Required']]

// Following element with condition
//label[text()='Email']/following::input[@type='email']
```

**Best Practices:**
- Always use relative XPath
- Make XPath specific but not too rigid
- Use meaningful attributes (id, name, data-testid)
- Avoid index-based XPath when possible
- Test XPath in browser console: `$x("your-xpath")`

---

### **Q60. What is CSS selector?**

**Answer:**
CSS Selector is a pattern used to **select HTML elements** based on their attributes, classes, IDs, or hierarchy. It's **faster than XPath** in most browsers.

**Why CSS Selector:**
- Faster execution than XPath
- Cleaner syntax
- Better browser support
- Industry standard

**Basic Syntax:**

**1. By ID (#)**
```html
<input id="username" type="text">
```
```css
#username
```
```java
driver.findElement(By.cssSelector("#username"))
```

---

**2. By Class (.)**
```html
<button class="btn-primary">Submit</button>
```
```css
.btn-primary
```
```java
driver.findElement(By.cssSelector(".btn-primary"))
```

---

**3. By Tag**
```html
<input type="text">
```
```css
input
```
```java
driver.findElement(By.cssSelector("input"))
```

---

**4. By Attribute [attribute]**
```html
<input type="text" name="email">
```
```css
input[type='text']
input[name='email']
input[type='text'][name='email']  /* Multiple attributes */
```

---

**5. Attribute Contains (*=)**
```html
<div id="user-profile-123">
```
```css
div[id*='profile']  /* Contains 'profile' */
```

---

**6. Attribute Starts With (^=)**
```html
<div id="user-123">
```
```css
div[id^='user']  /* Starts with 'user' */
```

---

**7. Attribute Ends With ($=)**
```html
<div id="profile-user">
```
```css
div[id$='user']  /* Ends with 'user' */
```

---

**Hierarchical Selectors:**

**1. Child (>)**
```html
<div class="form">
    <input id="username">
</div>
```
```css
div.form > input  /* Direct child */
```

---

**2. Descendant (space)**
```html
<div class="container">
    <div class="inner">
        <input id="username">
    </div>
</div>
```
```css
div.container input  /* Any descendant */
```

---

**3. Adjacent Sibling (+)**
```html
<label>Username</label>
<input id="username">
```
```css
label + input  /* Immediately following sibling */
```

---

**4. General Sibling (~)**
```html
<label>Email</label>
<span>Required</span>
<input id="email">
```
```css
label ~ input  /* Any following sibling */
```

---

**Pseudo-classes:**

**1. First/Last Child**
```css
li:first-child     /* First li element */
li:last-child      /* Last li element */
li:nth-child(2)    /* Second li element */
li:nth-child(odd)  /* Odd li elements */
li:nth-child(even) /* Even li elements */
```

**Example:**
```html
<ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ul>
```
```java
driver.findElement(By.cssSelector("li:first-child"))  // Item 1
driver.findElement(By.cssSelector("li:nth-child(2)"))  // Item 2
```

---

**2. First/Last of Type**
```css
input:first-of-type
input:last-of-type
p:nth-of-type(3)
```

---

**3. Not Pseudo-class**
```css
input:not([type='hidden'])  /* All inputs except hidden */
div:not(.disabled)           /* All divs without 'disabled' class */
```

---

**Combining Selectors:**

**1. Multiple Classes**
```html
<div class="error message">Invalid input</div>
```
```css
div.error.message  /* Element with both classes */
```

---

**2. ID + Class**
```html
<div id="login" class="form">
```
```css
div#login.form
#login.form  /* Can omit tag name */
```

---

**3. Complex Combinations**
```html
<div class="container">
    <form id="login-form">
        <input type="text" name="username" class="input-field">
        <button class="btn btn-primary">Login</button>
    </form>
</div>
```

**CSS Examples:**
```css
/* Input inside form with ID */
form#login-form input[name='username']

/* Button with multiple classes */
button.btn.btn-primary

/* Input with class inside container */
div.container input.input-field

/* Any input in the form */
#login-form input
```

---

**CSS Selector vs XPath:**

| Feature | CSS Selector | XPath |
|---------|-------------|-------|
| Speed | Faster | Slower |
| Syntax | Simpler | More complex |
| Direction | Forward only | Any direction |
| Text search | Not supported | Supported |
| Partial match | Supported | Supported |
| Parent selection | Not directly | Supported |

**When to Use:**

**CSS Selector:**
- When navigating forward (parent to child)
- For faster execution
- When text search not needed
- Most common scenarios

**XPath:**
- When navigating backward (child to parent)
- When searching by text content
- Complex conditions
- When CSS can't achieve the goal

---

**Real-World Examples:**

**1. Login Form:**
```html
<form id="login-form" class="auth-form">
    <input type="text" name="username" placeholder="Username">
    <input type="password" name="password" placeholder="Password">
    <button type="submit" class="btn btn-primary">Login</button>
</form>
```

**CSS Selectors:**
```java
// Username field
driver.findElement(By.cssSelector("input[name='username']"))
driver.findElement(By.cssSelector("#login-form input[type='text']"))

// Password field
driver.findElement(By.cssSelector("input[name='password']"))

// Submit button
driver.findElement(By.cssSelector("button.btn-primary"))
driver.findElement(By.cssSelector("form#login-form button[type='submit']"))
```

---

**2. Product List:**
```html
<div class="products">
    <div class="product" data-id="101">
        <h3>Product 1</h3>
        <span class="price">$99</span>
        <button class="add-to-cart">Add to Cart</button>
    </div>
    <div class="product" data-id="102">
        <h3>Product 2</h3>
        <span class="price">$149</span>
        <button class="add-to-cart">Add to Cart</button>
    </div>
</div>
```

**CSS Selectors:**
```java
// First product
driver.findElement(By.cssSelector(".product:first-child"))

// Product by data-id
driver.findElement(By.cssSelector(".product[data-id='101']"))

// Price of first product
driver.findElement(By.cssSelector(".product:first-child .price"))

// All add to cart buttons
driver.findElements(By.cssSelector(".add-to-cart"))

// Second product's button
driver.findElement(By.cssSelector(".product:nth-child(2) button"))
```

---

**Best Practices:**
1. Use ID when available (fastest)
2. Prefer CSS over XPath (when possible)
3. Keep selectors simple and readable
4. Avoid overly specific selectors
5. Test selectors in browser console: `$$("css-selector")`
6. Use data attributes for test-specific IDs

---

### **Q61. How do you handle dropdowns in Selenium?**

**Answer:**
Dropdowns are handled differently based on whether they are **HTML `<select>` elements** or **custom dropdowns**.

**1. HTML Select Dropdown**

**HTML:**
```html
<select id="country">
    <option value="us">United States</option>
    <option value="uk">United Kingdom</option>
    <option value="in">India</option>
    <option value="ca">Canada</option>
</select>
```

**Selenium (Using Select Class):**

```java
import org.openqa.selenium.support.ui.Select;

WebElement dropdown = driver.findElement(By.id("country"));
Select select = new Select(dropdown);

// Method 1: By visible text
select.selectByVisibleText("India");

// Method 2: By value
select.selectByValue("in");

// Method 3: By index (0-based)
select.selectByIndex(2);  // Selects "India"

// Get selected option
WebElement selected = select.getFirstSelectedOption();
System.out.println(selected.getText());  // Prints: India

// Get all options
List<WebElement> allOptions = select.getOptions();
System.out.println("Total options: " + allOptions.size());

// Check if multi-select
boolean isMultiple = select.isMultiple();

// Deselect (for multi-select dropdowns)
if (isMultiple) {
    select.deselectByVisibleText("India");
    select.deselectByValue("in");
    select.deselectByIndex(2);
    select.deselectAll();  // Deselect all
}
```

**Python:**
```python
from selenium.webdriver.support.ui import Select

dropdown = driver.find_element(By.ID, "country")
select = Select(dropdown)

# Select by visible text
select.select_by_visible_text("India")

# Select by value
select.select_by_value("in")

# Select by index
select.select_by_index(2)

# Get selected option
selected = select.first_selected_option
print(selected.text)

# Get all options
options = select.options
print(f"Total options: {len(options)}")
```

---

**2. Multi-Select Dropdown**

**HTML:**
```html
<select id="skills" multiple>
    <option value="java">Java</option>
    <option value="python">Python</option>
    <option value="selenium">Selenium</option>
    <option value="api">API Testing</option>
</select>
```

**Java:**
```java
WebElement dropdown = driver.findElement(By.id("skills"));
Select select = new Select(dropdown);

// Select multiple options
select.selectByVisibleText("Java");
select.selectByVisibleText("Selenium");
select.selectByValue("api");

// Get all selected options
List<WebElement> selectedOptions = select.getAllSelectedOptions();
System.out.println("Selected: " + selectedOptions.size());

// Deselect specific option
select.deselectByVisibleText("Java");

// Deselect all
select.deselectAll();
```

---

**3. Custom/Non-Select Dropdowns**

Many modern web apps use **custom dropdowns** (div, ul, li elements) instead of `<select>`.

**Example (Bootstrap Dropdown):**
```html
<div class="dropdown">
    <button class="dropdown-toggle" id="countryDropdown">
        Select Country
    </button>
    <ul class="dropdown-menu">
        <li><a href="#">United States</a></li>
        <li><a href="#">United Kingdom</a></li>
        <li><a href="#">India</a></li>
    </ul>
</div>
```

**Approach:**
```java
// Step 1: Click dropdown to open
driver.findElement(By.id("countryDropdown")).click();

// Step 2: Wait for options to appear
WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));
wait.until(ExpectedConditions.visibilityOfElementLocated(
    By.cssSelector(".dropdown-menu")));

// Step 3: Click desired option
driver.findElement(By.xpath("//li/a[text()='India']")).click();
```

---

**4. Auto-Suggest Dropdown (Google-style)**

**Example:**
```html
<input id="searchBox" type="text">
<ul id="suggestions">
    <li>Selenium Tutorial</li>
    <li>Selenium WebDriver</li>
    <li>Selenium Python</li>
</ul>
```

**Approach:**
```java
// Type in search box
WebElement searchBox = driver.findElement(By.id("searchBox"));
searchBox.sendKeys("Selenium");

// Wait for suggestions
WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));
wait.until(ExpectedConditions.visibilityOfElementLocated(By.id("suggestions")));

// Get all suggestions
List<WebElement> suggestions = driver.findElements(
    By.xpath("//ul[@id='suggestions']/li"));

// Click desired suggestion
for (WebElement suggestion : suggestions) {
    if (suggestion.getText().equals("Selenium WebDriver")) {
        suggestion.click();
        break;
    }
}
```

---

**5. Hidden Dropdown (Invisible Options)**

Some dropdowns hide options initially.

**Approach:**
```java
// Method 1: Use JavaScript
WebElement dropdown = driver.findElement(By.id("country"));
JavascriptExecutor js = (JavascriptExecutor) driver;
js.executeScript("arguments[0].value='in';", dropdown);

// Method 2: Make element visible first
js.executeScript("arguments[0].style.display='block';", dropdown);
Select select = new Select(dropdown);
select.selectByValue("in");
```

---

**Common Issues & Solutions:**

**Issue 1: ElementNotInteractableException**
```java
// Solution: Wait for element to be clickable
WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));
WebElement dropdown = wait.until(
    ExpectedConditions.elementToBeClickable(By.id("country")));
```

**Issue 2: Dropdown not a Select element**
```java
// Error: Cannot use Select class

// Solution: Treat as custom dropdown
driver.findElement(By.id("dropdown-button")).click();
driver.findElement(By.xpath("//li[text()='Option']")).click();
```

**Issue 3: Stale Element Reference**
```java
// Solution: Re-locate element
WebElement dropdown = driver.findElement(By.id("country"));
Select select = new Select(dropdown);
select.selectByVisibleText("India");

// If page refreshes, re-locate
dropdown = driver.findElement(By.id("country"));
select = new Select(dropdown);
```

---

**Best Practices:**

1. **Check if it's a `<select>` element first**
   ```java
   if (element.getTagName().equals("select")) {
       Select select = new Select(element);
   } else {
       // Handle as custom dropdown
   }
   ```

2. **Always wait for dropdown to be ready**
   ```java
   WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));
   wait.until(ExpectedConditions.elementToBeClickable(dropdown));
   ```

3. **Verify selection**
   ```java
   select.selectByVisibleText("India");
   String selected = select.getFirstSelectedOption().getText();
   Assert.assertEquals(selected, "India");
   ```

4. **Handle exceptions gracefully**
   ```java
   try {
       select.selectByVisibleText("India");
   } catch (NoSuchElementException e) {
       System.out.println("Option not found in dropdown");
   }
   ```

---

### **Q62. How do you handle alerts/popups in Selenium?**

**Answer:**
Alerts and popups in Selenium are handled using the **Alert interface**. There are different types of alerts/popups.

**Types of Alerts:**

**1. Simple Alert**
- Information message
- Only "OK" button

**2. Confirmation Alert**
- Question with "OK" and "Cancel"
- User confirms or dismisses

**3. Prompt Alert**
- Input field with "OK" and "Cancel"
- User can enter text

---

**Handling Alerts:**

**1. Simple Alert**

**HTML (JavaScript):**
```html
<button onclick="alert('This is an alert!')">Click Me</button>
```

**Selenium:**
```java
// Click button that triggers alert
driver.findElement(By.id("alertButton")).click();

// Switch to alert
Alert alert = driver.switchTo().alert();

// Get alert text
String alertText = alert.getText();
System.out.println("Alert says: " + alertText);

// Accept alert (click OK)
alert.accept();
```

**Python:**
```python
# Click button
driver.find_element(By.ID, "alertButton").click()

# Switch to alert
alert = driver.switch_to.alert

# Get text
print(alert.text)

# Accept
alert.accept()
```

---

**2. Confirmation Alert**

**HTML:**
```html
<button onclick="confirm('Are you sure?')">Delete</button>
```

**Selenium:**
```java
driver.findElement(By.id("confirmButton")).click();

Alert alert = driver.switchTo().alert();
String alertText = alert.getText();

// Accept (click OK)
alert.accept();

// OR Dismiss (click Cancel)
// alert.dismiss();
```

**Example with assertion:**
```java
driver.findElement(By.id("confirmButton")).click();
Alert alert = driver.switchTo().alert();

Assert.assertEquals(alert.getText(), "Are you sure?");

// Click Cancel
alert.dismiss();
```

---

**3. Prompt Alert**

**HTML:**
```html
<button onclick="prompt('Enter your name:')">Enter Name</button>
```

**Selenium:**
```java
driver.findElement(By.id("promptButton")).click();

Alert alert = driver.switchTo().alert();

// Get prompt message
System.out.println(alert.getText());  // "Enter your name:"

// Enter text in prompt
alert.sendKeys("John Doe");

// Accept
alert.accept();

// OR dismiss without entering
// alert.dismiss();
```

**Python:**
```python
driver.find_element(By.ID, "promptButton").click()
alert = driver.switch_to.alert

# Send text
alert.send_keys("John Doe")
alert.accept()
```

---

**Alert Methods:**

| Method | Description |
|--------|-------------|
| `accept()` | Click OK button |
| `dismiss()` | Click Cancel button |
| `getText()` | Get alert text |
| `sendKeys(text)` | Enter text (prompt only) |

---

**Handling Alerts with Wait:**

**Issue:** Alert might take time to appear

**Solution: Use WebDriverWait**

```java
import org.openqa.selenium.support.ui.WebDriverWait;
import org.openqa.selenium.support.ui.ExpectedConditions;

// Click button
driver.findElement(By.id("alertButton")).click();

// Wait for alert to appear (up to 10 seconds)
WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));
Alert alert = wait.until(ExpectedConditions.alertIsPresent());

// Now handle alert
System.out.println(alert.getText());
alert.accept();
```

---

**Handling Unexpected Alerts:**

Sometimes alerts appear unexpectedly during test execution.

**Approach 1: Try-Catch**
```java
try {
    Alert alert = driver.switchTo().alert();
    System.out.println("Unexpected alert: " + alert.getText());
    alert.accept();
} catch (NoAlertPresentException e) {
    // No alert present, continue
}
```

**Approach 2: Check if Alert Exists**
```java
public boolean isAlertPresent() {
    try {
        driver.switchTo().alert();
        return true;
    } catch (NoAlertPresentException e) {
        return false;
    }
}

// Usage
if (isAlertPresent()) {
    Alert alert = driver.switchTo().alert();
    alert.accept();
}
```

---

**Authentication Popup (Different from JavaScript Alerts)**

**URL-based authentication:**
```
https://username:password@example.com
```

**Selenium:**
```java
// Method 1: Pass credentials in URL
driver.get("https://admin:admin123@example.com/secure");

// Method 2: Using Alert (doesn't work for auth popups)
// Auth popups are OS-level, not browser-level

// Method 3: AutoIT or Robot class (Windows only)
```

**Note:** Basic authentication popups cannot be handled by Selenium Alert interface as they're OS-level dialogs.

---

**Browser Popups (New Windows)**

**Different from alerts!**

```java
// Click link that opens new window
driver.findElement(By.id("openWindow")).click();

// Get all window handles
Set<String> windows = driver.getWindowHandles();

// Switch to new window
for (String window : windows) {
    driver.switchTo().window(window);
}

// Now interact with new window
driver.findElement(By.id("element")).click();

// Switch back to original window
driver.switchTo().window(originalWindow);
```

---

**Common Issues & Solutions:**

**Issue 1: NoAlertPresentException**
```
Solution: Wait for alert before switching
```

**Issue 2: UnhandledAlertException**
```
Solution: Always handle alerts before proceeding
```

**Issue 3: Alert appears randomly**
```
Solution: Add try-catch in tearDown method
```

---

**Complete Example:**

```java
public class AlertExample {
    WebDriver driver;
    
    @Test
    public void testAlerts() {
        driver = new ChromeDriver();
        driver.get("https://example.com/alerts");
        
        // Simple Alert
        driver.findElement(By.id("simpleAlert")).click();
        Alert simpleAlert = driver.switchTo().alert();
        System.out.println(simpleAlert.getText());
        simpleAlert.accept();
        
        // Confirmation Alert - Accept
        driver.findElement(By.id("confirmAlert")).click();
        Alert confirmAlert = driver.switchTo().alert();
        confirmAlert.accept();
        
        // Confirmation Alert - Dismiss
        driver.findElement(By.id("confirmAlert")).click();
        confirmAlert = driver.switchTo().alert();
        confirmAlert.dismiss();
        
        // Prompt Alert
        driver.findElement(By.id("promptAlert")).click();
        Alert promptAlert = driver.switchTo().alert();
        promptAlert.sendKeys("Test User");
        promptAlert.accept();
    }
    
    @AfterMethod
    public void tearDown() {
        // Handle any unexpected alerts
        try {
            Alert alert = driver.switchTo().alert();
            alert.accept();
        } catch (NoAlertPresentException e) {
            // No alert, continue
        }
        driver.quit();
    }
}
```

---

**Best Practices:**

1. **Always wait for alerts**
   ```java
   WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));
   wait.until(ExpectedConditions.alertIsPresent());
   ```

2. **Verify alert text before accepting**
   ```java
   Alert alert = driver.switchTo().alert();
   Assert.assertEquals(alert.getText(), "Expected message");
   alert.accept();
   ```

3. **Handle alerts in tearDown**
   ```java
   @AfterMethod
   public void cleanup() {
       if (isAlertPresent()) {
           driver.switchTo().alert().accept();
       }
   }
   ```

4. **Use try-catch for unexpected alerts**
   ```java
   try {
       // Your test code
   } finally {
       if (isAlertPresent()) {
           driver.switchTo().alert().dismiss();
       }
   }
   ```

---

(Continuing with remaining questions...)

### **Q63. What is implicit wait vs explicit wait vs fluent wait?**

**Answer:**
These are different types of **waits in Selenium** to handle synchronization issues.

**1. Implicit Wait**

**Definition:**
- Global wait applied to **all elements**
- Polls DOM for specified time
- Set once, applies throughout driver instance

**Syntax:**
```java
driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(10));
```

**How it works:**
- If element not found immediately, waits up to specified time
- Polls DOM every 500ms (default)
- Throws NoSuchElementException if not found after timeout

**Example:**
```java
WebDriver driver = new ChromeDriver();
driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(10));

// This will wait up to 10 seconds for element to appear
driver.findElement(By.id("username")).sendKeys("test");
driver.findElement(By.id("password")).sendKeys("pass");
// All findElement calls will wait up to 10 seconds
```

**Advantages:**
- Easy to implement
- Single line of code
- Applies globally

**Disadvantages:**
- Cannot customize for specific elements
- Can slow down tests unnecessarily
- Not recommended for dynamic elements

---

**2. Explicit Wait**

**Definition:**
- Wait for **specific condition** on **specific element**
- More flexible than implicit wait
- Used for conditional waits

**Syntax:**
```java
WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));
wait.until(ExpectedConditions.visibilityOfElementLocated(By.id("element")));
```

**Common Expected Conditions:**
```java
WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));

// Element to be clickable
wait.until(ExpectedConditions.elementToBeClickable(By.id("button")));

// Element to be visible
wait.until(ExpectedConditions.visibilityOfElementLocated(By.id("element")));

// Element to be present in DOM
wait.until(ExpectedConditions.presenceOfElementLocated(By.id("element")));

// Title contains text
wait.until(ExpectedConditions.titleContains("Welcome"));

// Alert is present
wait.until(ExpectedConditions.alertIsPresent());

// Element to be invisible
wait.until(ExpectedConditions.invisibilityOfElementLocated(By.id("loader")));

// Text to be present in element
wait.until(ExpectedConditions.textToBePresentInElementLocated(
    By.id("status"), "Complete"));

// Frame to be available and switch
wait.until(ExpectedConditions.frameToBeAvailableAndSwitchToIt("frameName"));

// Number of windows to be
wait.until(ExpectedConditions.numberOfWindowsToBe(2));
```

**Example:**
```java
WebDriver driver = new ChromeDriver();
driver.get("https://example.com");

WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));

// Wait for login button to be clickable
WebElement loginBtn = wait.until(
    ExpectedConditions.elementToBeClickable(By.id("login")));
loginBtn.click();

// Wait for success message to appear
wait.until(ExpectedConditions.visibilityOfElementLocated(
    By.id("successMsg")));

// Wait for loader to disappear
wait.until(ExpectedConditions.invisibilityOfElementLocated(
    By.id("loader")));
```

**Advantages:**
- Flexible and powerful
- Condition-based waiting
- Specific to elements
- Better control

**Disadvantages:**
- More code
- Need to write for each element
- Verbose

---

**3. Fluent Wait**

**Definition:**
- Advanced version of explicit wait
- Define **polling frequency**
- Define **exceptions to ignore**
- Maximum flexibility

**Syntax:**
```java
Wait<WebDriver> wait = new FluentWait<WebDriver>(driver)
    .withTimeout(Duration.ofSeconds(30))
    .pollingEvery(Duration.ofSeconds(2))
    .ignoring(NoSuchElementException.class)
    .ignoring(ElementNotInteractableException.class);

WebElement element = wait.until(new Function<WebDriver, WebElement>() {
    public WebElement apply(WebDriver driver) {
        return driver.findElement(By.id("element"));
    }
});
```

**Lambda Expression:**
```java
Wait<WebDriver> wait = new FluentWait<WebDriver>(driver)
    .withTimeout(Duration.ofSeconds(30))
    .pollingEvery(Duration.ofSeconds(2))
    .ignoring(NoSuchElementException.class);

WebElement element = wait.until(driver -> 
    driver.findElement(By.id("dynamicElement")));
```

**Example:**
```java
FluentWait<WebDriver> wait = new FluentWait<>(driver)
    .withTimeout(Duration.ofSeconds(30))     // Max wait time
    .pollingEvery(Duration.ofMillis(500))    // Check every 500ms
    .ignoring(NoSuchElementException.class)   // Ignore this exception
    .withMessage("Element not found!");       // Custom error message

WebElement element = wait.until(driver -> {
    WebElement el = driver.findElement(By.id("dynamicElement"));
    return el.isDisplayed() ? el : null;
});
```

**Advantages:**
- Most flexible
- Custom polling interval
- Ignore specific exceptions
- Custom wait conditions

**Disadvantages:**
- Most verbose
- Complex for simple scenarios
- Overkill for basic waits

---

**Comparison:**

| Feature | Implicit Wait | Explicit Wait | Fluent Wait |
|---------|--------------|---------------|-------------|
| Scope | All elements | Specific element | Specific element |
| Condition | Element presence | Custom condition | Custom condition |
| Polling | Fixed (500ms) | Fixed (500ms) | Customizable |
| Exceptions | Can't ignore | Can't ignore | Can ignore |
| Flexibility | Low | Medium | High |
| Code | 1 line | Few lines | Verbose |
| Best for | Simple apps | Most scenarios | Complex scenarios |

---

**When to Use:**

**Implicit Wait:**
- Simple applications
- Static pages
- Quick POC
- NOT recommended for production

**Explicit Wait:**
- Dynamic web pages
- AJAX calls
- Conditional waits
- **Most common and recommended**

**Fluent Wait:**
- Highly dynamic elements
- Custom polling needed
- Specific exceptions to ignore
- Complex scenarios

---

**Best Practices:**

**1. Don't Mix Implicit and Explicit Waits**
```java
// BAD - Don't do this!
driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(10));
WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));
// Can cause unpredictable wait times
```

**2. Use Explicit Waits**
```java
// GOOD
WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));
wait.until(ExpectedConditions.elementToBeClickable(element));
```

**3. Create Reusable Wait Methods**
```java
public void waitForElementToBeClickable(By locator) {
    WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));
    wait.until(ExpectedConditions.elementToBeClickable(locator));
}

public void waitForElementToBeVisible(By locator) {
    WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));
    wait.until(ExpectedConditions.visibilityOfElementLocated(locator));
}

// Usage
waitForElementToBeClickable(By.id("login"));
driver.findElement(By.id("login")).click();
```

**4. Wait for Page Load**
```java
// Wait for page to load completely
public void waitForPageLoad() {
    WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(30));
    wait.until(webDriver -> 
        ((JavascriptExecutor) webDriver)
            .executeScript("return document.readyState").equals("complete"));
}
```

---

**Real-World Examples:**

**Example 1: Wait for AJAX call**
```java
// Click button that triggers AJAX
driver.findElement(By.id("loadData")).click();

// Wait for loader to disappear
WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));
wait.until(ExpectedConditions.invisibilityOfElementLocated(By.id("loader")));

// Wait for data to appear
wait.until(ExpectedConditions.visibilityOfElementLocated(By.id("dataTable")));
```

**Example 2: Wait for element attribute**
```java
// Wait for button to be enabled
wait.until(ExpectedConditions.attributeToBe(
    By.id("submitBtn"), "disabled", "false"));
```

**Example 3: Custom wait condition**
```java
// Wait for specific text in element
wait.until(driver -> {
    String text = driver.findElement(By.id("status")).getText();
    return text.equals("Completed");
});
```

---

### **Q64. How do you handle multiple windows in Selenium?**

**Answer:**
Handling multiple browser windows/tabs involves **switching between window handles**.

**Concept:**
- Each window has a unique **Window Handle** (alphanumeric string)
- Driver can switch between windows using handles
- Need to store original window handle to switch back

**Methods:**
```java
// Get current window handle
String currentWindow = driver.getWindowHandle();

// Get all window handles
Set<String> allWindows = driver.getWindowHandles();

// Switch to window
driver.switchTo().window(windowHandle);
```

---

**Scenario 1: Two Windows**

**HTML:**
```html
<a href="https://example.com" target="_blank">Open New Window</a>
```

**Selenium:**
```java
// Store original window handle
String originalWindow = driver.getWindowHandle();

// Click link that opens new window
driver.findElement(By.id("openWindow")).click();

// Get all window handles
Set<String> allWindows = driver.getWindowHandles();

// Switch to new window
for (String window : allWindows) {
    if (!window.equals(originalWindow)) {
        driver.switchTo().window(window);
        break;
    }
}

// Now you're in new window - perform actions
System.out.println("New window title: " + driver.getTitle());
driver.findElement(By.id("element")).click();

// Close new window
driver.close();

// Switch back to original window
driver.switchTo().window(originalWindow);

// Continue with original window
driver.findElement(By.id("element")).click();
```

---

**Scenario 2: Multiple Windows (More than 2)**

```java
// Store original window
String mainWindow = driver.getWindowHandle();

// Click button that opens 3 new windows
driver.findElement(By.id("openWindows")).click();

// Get all windows
Set<String> allWindows = driver.getWindowHandles();

// Iterate through all windows
for (String window : allWindows) {
    driver.switchTo().window(window);
    
    // Identify window by title or URL
    if (driver.getTitle().contains("Window 1")) {
        // Do something in Window 1
        driver.findElement(By.id("element1")).click();
    } else if (driver.getTitle().contains("Window 2")) {
        // Do something in Window 2
        driver.findElement(By.id("element2")).click();
    }
}

// Switch back to main window
driver.switchTo().window(mainWindow);
```

---

**Scenario 3: Switch to Window by Title**

```java
public void switchToWindowByTitle(String title) {
    Set<String> windows = driver.getWindowHandles();
    for (String window : windows) {
        driver.switchTo().window(window);
        if (driver.getTitle().equals(title)) {
            return;
        }
    }
    throw new RuntimeException("Window with title '" + title + "' not found");
}

// Usage
switchToWindowByTitle("Login Page");
```

---

**Scenario 4: Switch to Window by URL**

```java
public void switchToWindowByURL(String url) {
    Set<String> windows = driver.getWindowHandles();
    for (String window : windows) {
        driver.switchTo().window(window);
        if (driver.getCurrentUrl().contains(url)) {
            return;
        }
    }
    throw new RuntimeException("Window with URL '" + url + "' not found");
}

// Usage
switchToWindowByURL("example.com/login");
```

---

**Scenario 5: Wait for New Window**

Sometimes new window takes time to open.

```java
// Get current number of windows
int initialWindows = driver.getWindowHandles().size();

// Click link that opens new window
driver.findElement(By.id("openWindow")).click();

// Wait for new window to open
WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));
wait.until(driver -> driver.getWindowHandles().size() > initialWindows);

// Now switch to new window
Set<String> windows = driver.getWindowHandles();
for (String window : windows) {
    driver.switchTo().window(window);
    if (!window.equals(originalWindow)) {
        break;
    }
}
```

---

**Scenario 6: Close All Windows Except Original**

```java
String originalWindow = driver.getWindowHandle();

// Open multiple windows...

// Close all except original
Set<String> allWindows = driver.getWindowHandles();
for (String window : allWindows) {
    if (!window.equals(originalWindow)) {
        driver.switchTo().window(window);
        driver.close();
    }
}

// Switch back to original
driver.switchTo().window(originalWindow);
```

---

**Complete Example:**

```java
public class MultipleWindowsTest {
    WebDriver driver;
    String mainWindow;
    
    @BeforeMethod
    public void setup() {
        driver = new ChromeDriver();
        driver.get("https://example.com");
        mainWindow = driver.getWindowHandle();
    }
    
    @Test
    public void testMultipleWindows() {
        // Click link that opens new window
        driver.findElement(By.id("openNewWindow")).click();
        
        // Wait for new window
        WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));
        wait.until(ExpectedConditions.numberOfWindowsToBe(2));
        
        // Get all windows
        Set<String> allWindows = driver.getWindowHandles();
        
        // Switch to new window
        for (String window : allWindows) {
            if (!window.equals(mainWindow)) {
                driver.switchTo().window(window);
                
                // Perform actions in new window
                System.out.println("New window title: " + driver.getTitle());
                driver.findElement(By.id("submit")).click();
                
                // Close new window
                driver.close();
                break;
            }
        }
        
        // Switch back to main window
        driver.switchTo().window(mainWindow);
        
        // Verify back in main window
        Assert.assertEquals(driver.getTitle(), "Main Page");
    }
    
    @AfterMethod
    public void tearDown() {
        // Close all windows
        driver.quit();
    }
    
    // Utility method
    public void switchToWindow(String title) {
        Set<String> windows = driver.getWindowHandles();
        for (String window : windows) {
            driver.switchTo().window(window);
            if (driver.getTitle().equals(title)) {
                return;
            }
        }
    }
}
```

---

**Important Methods:**

| Method | Description |
|--------|-------------|
| `getWindowHandle()` | Get current window handle |
| `getWindowHandles()` | Get all window handles (Set) |
| `switchTo().window(handle)` | Switch to specific window |
| `close()` | Close current window |
| `quit()` | Close all windows |

---

**Difference: close() vs quit()**

```java
// close() - Closes current window only
driver.close();  // Current window closed, other windows remain

// quit() - Closes all windows and ends session
driver.quit();   // All windows closed, driver session ended
```

---

**Common Issues & Solutions:**

**Issue 1: NoSuchWindowException**
```java
// Solution: Check if window exists before switching
if (driver.getWindowHandles().contains(windowHandle)) {
    driver.switchTo().window(windowHandle);
}
```

**Issue 2: Can't find new window**
```java
// Solution: Wait for window to open
WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));
wait.until(ExpectedConditions.numberOfWindowsToBe(2));
```

**Issue 3: Switched to wrong window**
```java
// Solution: Verify window after switching
driver.switchTo().window(windowHandle);
Assert.assertEquals(driver.getTitle(), "Expected Title");
```

---

**Best Practices:**

1. **Always store original window handle**
   ```java
   String mainWindow = driver.getWindowHandle();
   ```

2. **Wait for new windows to open**
   ```java
   wait.until(ExpectedConditions.numberOfWindowsToBe(2));
   ```

3. **Switch back to original window**
   ```java
   driver.switchTo().window(mainWindow);
   ```

4. **Close windows properly**
   ```java
   driver.close();  // Close current
   driver.switchTo().window(mainWindow);  // Switch back
   ```

5. **Use descriptive variable names**
   ```java
   String mainWindow = driver.getWindowHandle();
   String childWindow = ...;
   ```

---

### **Q65. How do you take screenshots in Selenium?**

**Answer:**
Screenshots are essential for **debugging test failures** and **creating test reports**.

**Methods:**

**1. Full Page Screenshot**

**Java:**
```java
import org.openqa.selenium.TakesScreenshot;
import org.openqa.selenium.OutputType;
import org.apache.commons.io.FileUtils;

// Take screenshot
TakesScreenshot screenshot = (TakesScreenshot) driver;
File source = screenshot.getScreenshotAs(OutputType.FILE);

// Save to file
File destination = new File("screenshots/homepage.png");
FileUtils.copyFile(source, destination);
```

**Python:**
```python
driver.save_screenshot("screenshots/homepage.png")
# OR
driver.get_screenshot_as_file("screenshots/homepage.png")
```

---

**2. Screenshot as Base64**

```java
String base64Screenshot = ((TakesScreenshot) driver)
    .getScreenshotAs(OutputType.BASE64);

// Use in HTML reports
String img = "<img src='data:image/png;base64," + base64Screenshot + "'>";
```

---

**3. Screenshot as Byte Array**

```java
byte[] screenshot = ((TakesScreenshot) driver)
    .getScreenshotAs(OutputType.BYTES);

// Attach to report
Allure.addAttachment("Screenshot", new ByteArrayInputStream(screenshot));
```

---

**4. Element Screenshot (Selenium 4)**

```java
// Screenshot of specific element only
WebElement element = driver.findElement(By.id("login-form"));
File source = element.getScreenshotAs(OutputType.FILE);
FileUtils.copyFile(source, new File("screenshots/login-form.png"));
```

---

**Practical Implementation:**

**1. Screenshot on Test Failure (TestNG)**

```java
public class BaseTest {
    WebDriver driver;
    
    @AfterMethod
    public void tearDown(ITestResult result) {
        // Take screenshot if test failed
        if (result.getStatus() == ITestResult.FAILURE) {
            takeScreenshot(result.getName());
        }
        driver.quit();
    }
    
    public void takeScreenshot(String testName) {
        try {
            TakesScreenshot screenshot = (TakesScreenshot) driver;
            File source = screenshot.getScreenshotAs(OutputType.FILE);
            
            // Create filename with timestamp
            String timestamp = new SimpleDateFormat("yyyyMMdd_HHmmss")
                .format(new Date());
            String filename = "screenshots/" + testName + "_" + timestamp + ".png";
            
            File destination = new File(filename);
            FileUtils.copyFile(source, destination);
            
            System.out.println("Screenshot saved: " + filename);
        } catch (IOException e) {
            System.out.println("Failed to capture screenshot: " + e.getMessage());
        }
    }
}
```

---

**2. Screenshot Utility Class**

```java
public class ScreenshotUtil {
    
    public static String captureScreenshot(WebDriver driver, String testName) {
        String dateName = new SimpleDateFormat("yyyyMMdd_HHmmss").format(new Date());
        String fileName = testName + "_" + dateName + ".png";
        String directory = "screenshots/";
        String path = directory + fileName;
        
        try {
            // Create directory if doesn't exist
            new File(directory).mkdirs();
            
            // Take screenshot
            TakesScreenshot screenshot = (TakesScreenshot) driver;
            File source = screenshot.getScreenshotAs(OutputType.FILE);
            File destination = new File(path);
            FileUtils.copyFile(source, destination);
            
            return path;
        } catch (IOException e) {
            System.out.println("Exception: " + e.getMessage());
            return null;
        }
    }
    
    public static String captureElement(WebElement element, String testName) {
        String dateName = new SimpleDateFormat("yyyyMMdd_HHmmss").format(new Date());
        String fileName = testName + "_" + dateName + ".png";
        String path = "screenshots/elements/" + fileName;
        
        try {
            File source = element.getScreenshotAs(OutputType.FILE);
            File destination = new File(path);
            FileUtils.copyFile(source, destination);
            return path;
        } catch (IOException e) {
            e.printStackTrace();
            return null;
        }
    }
}

// Usage
ScreenshotUtil.captureScreenshot(driver, "loginTest");
ScreenshotUtil.captureElement(loginButton, "loginButton");
```

---

**3. Screenshot with Extent Reports**

```java
@AfterMethod
public void afterMethod(ITestResult result) {
    if (result.getStatus() == ITestResult.FAILURE) {
        String screenshotPath = ScreenshotUtil.captureScreenshot(
            driver, result.getName());
        
        try {
            extentTest.fail("Test Failed",
                MediaEntityBuilder.createScreenCaptureFromPath(screenshotPath).build());
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```

---

**4. Screenshot with Allure Reports**

```java
@Attachment(value = "Screenshot", type = "image/png")
public byte[] takeScreenshot() {
    return ((TakesScreenshot) driver).getScreenshotAs(OutputType.BYTES);
}

@Test
public void loginTest() {
    // Test code
    if (someCondition) {
        takeScreenshot();  // Automatically attached to Allure report
    }
}
```

---

**5. Full Page Screenshot (Beyond Viewport)**

For capturing entire page including scrollable content:

```java
import ru.yandex.qatools.ashot.AShot;
import ru.yandex.qatools.ashot.shooting.ShootingStrategies;

// Maven dependency required
Screenshot screenshot = new AShot()
    .shootingStrategy(ShootingStrategies.viewportPasting(1000))
    .takeScreenshot(driver);

ImageIO.write(screenshot.getImage(), "PNG", 
    new File("screenshots/fullpage.png"));
```

---

**6. Screenshot on Every Step (Debugging)**

```java
public void click(WebElement element) {
    takeScreenshot("before_click");
    element.click();
    takeScreenshot("after_click");
}

public void sendKeys(WebElement element, String text) {
    takeScreenshot("before_sendkeys");
    element.sendKeys(text);
    takeScreenshot("after_sendkeys");
}
```

---

**Best Practices:**

**1. Organized Folder Structure**
```
screenshots/
├── passed/
├── failed/
└── elements/
```

```java
String folder = result.getStatus() == ITestResult.SUCCESS ? "passed" : "failed";
String path = "screenshots/" + folder + "/" + filename;
```

**2. Timestamp in Filename**
```java
String timestamp = new SimpleDateFormat("yyyyMMdd_HHmmss").format(new Date());
String filename = testName + "_" + timestamp + ".png";
```

**3. Error Handling**
```java
try {
    takeScreenshot();
} catch (Exception e) {
    System.out.println("Screenshot failed: " + e.getMessage());
    // Don't fail test because screenshot failed
}
```

**4. Clean Old Screenshots**
```java
// Delete screenshots older than 7 days
public void cleanOldScreenshots() {
    File folder = new File("screenshots/");
    File[] files = folder.listFiles();
    long cutoff = System.currentTimeMillis() - (7 * 24 * 60 * 60 * 1000);
    
    for (File file : files) {
        if (file.lastModified() < cutoff) {
            file.delete();
        }
    }
}
```

**5. Screenshot Comparison**
```java
// Compare screenshots to detect visual regressions
public boolean compareScreenshots(String baseline, String current) {
    BufferedImage baselineImg = ImageIO.read(new File(baseline));
    BufferedImage currentImg = ImageIO.read(new File(current));
    
    ImageDiffer imgDiff = new ImageDiffer();
    ImageDiff diff = imgDiff.makeDiff(baselineImg, currentImg);
    
    return !diff.hasDiff();
}
```

---

**Common Issues:**

**Issue 1: Screenshot is blank/black**
```java
// Solution: Wait for page to load
WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));
wait.until(driver -> ((JavascriptExecutor) driver)
    .executeScript("return document.readyState").equals("complete"));
takeScreenshot();
```

**Issue 2: Screenshot doesn't capture modal/popup**
```java
// Solution: Ensure modal is in viewport
WebElement modal = driver.findElement(By.id("modal"));
((JavascriptExecutor) driver).executeScript("arguments[0].scrollIntoView();", modal);
Thread.sleep(500);  // Wait for scroll
takeScreenshot();
```

**Issue 3: File not found exception**
```java
// Solution: Create directory if doesn't exist
File directory = new File("screenshots");
if (!directory.exists()) {
    directory.mkdirs();
}
```

---

(Document continues with remaining questions through Q270...)


















































































# QA Interview Preparation - Quick Reference Guide
## Questions 66-270 - Concise Answers

---

## Automation Testing (Continued)

### Q66. What is TestNG? What are its advantages?
**Answer:** TestNG is a testing framework for Java inspired by JUnit but with more powerful features.

**Advantages:**
- Annotations (@Test, @BeforeMethod, @AfterMethod, etc.)
- Parallel test execution
- Data providers for data-driven testing
- Grouping of test cases
- Test dependencies
- Detailed HTML reports
- Test prioritization (@Test(priority=1))
- Flexible test configuration (testng.xml)

**Key Annotations:**
```java
@BeforeSuite, @AfterSuite
@BeforeTest, @AfterTest
@BeforeClass, @AfterClass
@BeforeMethod, @AfterMethod
@Test
@DataProvider
@Parameters
```

---

### Q67. What are annotations in TestNG?
**Answer:** Annotations are metadata that provide information about the program.

**Execution Order:**
1. @BeforeSuite
2. @BeforeTest
3. @BeforeClass
4. @BeforeMethod
5. @Test
6. @AfterMethod
7. @AfterClass
8. @AfterTest
9. @AfterSuite

**Example:**
```java
@BeforeMethod
public void setup() { /* Runs before each test */ }

@Test(priority=1)
public void loginTest() { /* Test case */ }

@AfterMethod
public void teardown() { /* Runs after each test */ }
```

---

### Q68. How do you handle dynamic elements in Selenium?
**Answer:**
- **Use Explicit Waits:** Wait for element to be present/visible
- **Use contains() in XPath:** `//div[contains(@id,'dynamic')]`
- **Relative XPath:** Don't use absolute paths
- **CSS with partial match:** `[id*='dynamic']`
- **Handle Stale Element:** Re-locate element if DOM changes

**Example:**
```java
WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));
wait.until(ExpectedConditions.presenceOfElementLocated(
    By.xpath("//div[contains(@id,'dynamic')]")));
```

---

### Q69. What is headless browser testing?
**Answer:** Running browser without GUI for faster execution.

**Use Cases:**
- CI/CD pipelines
- Faster execution
- Server environments without display
- Parallel testing

**Example (Chrome):**
```java
ChromeOptions options = new ChromeOptions();
options.addArguments("--headless");
WebDriver driver = new ChromeDriver(options);
```

**Example (Firefox):**
```java
FirefoxOptions options = new FirefoxOptions();
options.addArguments("--headless");
WebDriver driver = new FirefoxDriver(options);
```

---

### Q70. How do you run tests in parallel using Selenium?
**Answer:**

**Method 1: TestNG (testng.xml)**
```xml
<suite name="Suite" parallel="tests" thread-count="3">
    <test name="Test1">
        <classes>
            <class name="LoginTest"/>
        </classes>
    </test>
    <test name="Test2">
        <classes>
            <class name="CheckoutTest"/>
        </classes>
    </test>
</suite>
```

**Method 2: Selenium Grid**
- Hub-Node architecture
- Run tests on multiple machines/browsers

**Method 3: ThreadLocal**
```java
public class DriverFactory {
    private static ThreadLocal<WebDriver> driver = new ThreadLocal<>();
    
    public static WebDriver getDriver() {
        return driver.get();
    }
    
    public static void setDriver(WebDriver driverInstance) {
        driver.set(driverInstance);
    }
}
```

---

### Q71-75. Other Automation Tools

**Q71. Postman for API Testing**
- GUI tool for API testing
- Create requests, collections
- Test automation with scripts
- Environment variables
- Newman for CLI execution

**Q72. Cypress vs Selenium**
- Cypress: Modern, JavaScript only, faster, auto-waits
- Selenium: Multi-language, mature, more browsers
- Cypress: Better for JS apps
- Selenium: Better for cross-browser testing

**Q73. Playwright, Puppeteer**
- Modern automation tools
- Support Chrome, Firefox, Safari, Edge
- Faster than Selenium
- Better auto-waiting

**Q74. JUnit**
- Java testing framework
- Annotations: @Test, @Before, @After
- Assertions: assertEquals, assertTrue

**Q75. Maven/Gradle**
- Build automation tools
- Dependency management
- Project structure
- Execute tests via pom.xml/build.gradle

---

## 5. API Testing

### Q76. What is an API?
**Answer:** Application Programming Interface - allows software applications to communicate.

**Types:**
- REST API (most common)
- SOAP API
- GraphQL

---

### Q77. What is REST API?
**Answer:** Representational State Transfer - architectural style for web services.

**Characteristics:**
- Stateless
- Client-Server architecture
- Uniform interface
- Uses HTTP methods
- Returns JSON/XML

---

### Q78. REST vs SOAP?

| Feature | REST | SOAP |
|---------|------|------|
| Protocol | HTTP | HTTP, SMTP, etc. |
| Format | JSON, XML | XML only |
| Performance | Faster | Slower |
| Complexity | Simple | Complex |
| Use | Modern apps | Enterprise |

---

### Q79. HTTP Methods

**GET:** Retrieve data
```
GET /api/users/123
```

**POST:** Create new resource
```
POST /api/users
Body: {"name": "John", "email": "john@test.com"}
```

**PUT:** Update entire resource
```
PUT /api/users/123
Body: {"name": "John Updated", "email": "john@test.com"}
```

**DELETE:** Delete resource
```
DELETE /api/users/123
```

**PATCH:** Partial update
```
PATCH /api/users/123
Body: {"name": "John Updated"}
```

---

### Q80. HTTP Status Codes

**2xx Success:**
- 200 OK - Request successful
- 201 Created - Resource created
- 204 No Content - Successful but no content

**4xx Client Errors:**
- 400 Bad Request - Invalid request
- 401 Unauthorized - Authentication required
- 403 Forbidden - No permission
- 404 Not Found - Resource not found

**5xx Server Errors:**
- 500 Internal Server Error
- 502 Bad Gateway
- 503 Service Unavailable

---

### Q81-82. PUT vs PATCH, PUT vs POST

**PUT vs PATCH:**
- PUT: Replace entire resource
- PATCH: Update specific fields

**PUT vs POST:**
- POST: Create new resource
- PUT: Update existing resource (idempotent)

---

### Q83-84. JSON vs XML, Endpoints

**JSON:**
```json
{
  "id": 1,
  "name": "John",
  "email": "john@test.com"
}
```

**XML:**
```xml
<user>
  <id>1</id>
  <name>John</name>
  <email>john@test.com</email>
</user>
```

**Endpoint:** URL where API can be accessed
- Example: https://api.example.com/users

---

### Q85. Authentication vs Authorization

**Authentication:** Verifying WHO you are (login)
**Authorization:** Verifying WHAT you can access (permissions)

Example:
- Authentication: Username/password
- Authorization: Admin role can delete users

---

### Q86-100. API Testing Details

**Q86. How to test REST APIs:**
1. Verify status code
2. Validate response body
3. Check response time
4. Verify headers
5. Test different HTTP methods
6. Negative testing

**Q87. Postman for API Testing:**
- Create requests
- Set headers, params, body
- Write tests (JavaScript)
- Run collections
- Generate reports

**Q88. Validations in API Testing:**
- Status code validation
- Response body schema
- Response time
- Data type validation
- Error messages

**Q89-95. Postman Specifics:**
- Collections organize requests
- Environment variables
- Pre-request scripts
- Test scripts
- Chaining requests
- Newman for CLI

**Q96-100. API Performance:**
- Load testing with JMeter
- Stress testing
- Monitor response time
- Test with concurrent users

---

## 6. AI/ML Testing

### Q101-115. AI/ML Testing Concepts

**Q101. Unique Challenges:**
- Non-deterministic behavior
- Difficult to predict outputs
- Data quality issues
- Model bias
- Changing requirements

**Q102. Testing Model Accuracy:**
- Use test dataset (separate from training)
- Measure precision, recall, F1-score
- Confusion matrix
- Cross-validation

**Q103. Model Performance:**
- Accuracy metrics
- Response time
- Throughput
- Resource usage

**Q104. Training vs Test Data:**
- Training: Model learns from this
- Test: Evaluate model performance
- Should be separate datasets

**Q105. Bias Testing:**
- Test with diverse data
- Check for discriminatory patterns
- Fairness metrics
- Edge cases

**Q110. AI Model Metrics:**
- Accuracy, Precision, Recall
- F1-Score
- ROC-AUC curve
- Confusion matrix

---

## 7. SDLC & STLC

### Q116-125. SDLC

**Q116. SDLC Phases:**
1. Requirement Analysis
2. Design
3. Development
4. Testing
5. Deployment
6. Maintenance

**Q117. SDLC Models:**
- Waterfall
- Agile
- V-Model
- Spiral
- DevOps

**Q118. Waterfall:**
- Sequential phases
- Each phase completed before next
- Documentation heavy
- Less flexible

**Q119. Agile:**
- Iterative development
- Short sprints (1-4 weeks)
- Continuous feedback
- Flexible to changes

**Q121. Waterfall vs Agile:**
- Waterfall: Sequential, rigid
- Agile: Iterative, flexible

**Q124. Shift-Left Testing:**
- Testing early in SDLC
- Prevent defects vs finding them
- Reduce cost of fixes

---

### Q126-135. STLC

Already covered in Part 1 (Q4)

**Summary:** 6 phases - Requirement Analysis, Test Planning, Test Case Development, Environment Setup, Test Execution, Test Closure

---

## 8. Agile & Scrum

### Q136-145. Agile Basics

**Q136. Agile Methodology:**
- Iterative development
- Customer collaboration
- Responding to change
- Working software over documentation

**Q138. Agile Manifesto:**
- Individuals over processes
- Working software over documentation
- Customer collaboration over contracts
- Responding to change over plans

**Q142. User Story:**
Format: "As a [user], I want [goal], so that [benefit]"
Example: "As a customer, I want to search products, so that I can find items quickly"

**Q143. Epic:**
- Large user story
- Can be broken into smaller stories
- Example: "User Management" epic contains login, registration, profile stories

**Q144. Acceptance Criteria:**
- Conditions for user story to be complete
- Given-When-Then format
- Example: "Given user is logged in, When clicks logout, Then redirected to home page"

---

### Q146-160. Scrum Framework

**Q147. Scrum Roles:**
- **Scrum Master:** Facilitates process, removes blockers
- **Product Owner:** Defines requirements, prioritizes backlog
- **Development Team:** Builds the product (includes QA)

**Q148. Sprint:**
- Time-boxed iteration (1-4 weeks typically)
- Results in potentially shippable product

**Q150. Sprint Planning:**
- Select items from product backlog
- Define sprint goal
- Estimate effort
- Commit to sprint backlog

**Q151. Daily Standup:**
- 15-minute daily meeting
- Three questions:
  1. What did I do yesterday?
  2. What will I do today?
  3. Any blockers?

**Q152. Sprint Review:**
- Demo completed work
- Get feedback
- Update product backlog

**Q153. Sprint Retrospective:**
- Reflect on sprint
- What went well?
- What can improve?
- Action items

**Q154. Product Backlog:**
- Prioritized list of features
- Maintained by Product Owner

**Q155. Sprint Backlog:**
- Items selected for current sprint

**Q157. Story Pointing:**
- Estimate effort (Fibonacci: 1,2,3,5,8,13)
- Planning poker
- Relative sizing

---

### Q161-170. Testing in Agile

**Q161. How testing done in Agile:**
- Continuous testing throughout sprint
- Test-driven development (TDD)
- Automated regression
- Sprint testing includes new features + regression

**Q162. QA Role in Scrum:**
- Part of development team
- Participate in all ceremonies
- Write test cases during sprint
- Automate tests
- Verify user stories

**Q165. Continuous Integration (CI):**
- Frequent code integration
- Automated builds
- Automated tests run on each commit
- Early defect detection

**Q166. Continuous Deployment (CD):**
- Automated deployment to production
- After passing all tests
- Faster releases

---

## 9. CRUD Operations

### Q171-180. CRUD Basics

**Q171. CRUD:**
- **C**reate - Add new data
- **R**ead - Retrieve data
- **U**pdate - Modify existing data
- **D**elete - Remove data

**Q172-175. Testing Each Operation:**

**Create (POST):**
- Verify record created in database
- Status code 201
- Response contains new ID
- Validate all fields saved correctly

**Read (GET):**
- Verify correct data returned
- Status code 200
- Test with valid and invalid IDs

**Update (PUT/PATCH):**
- Verify data updated in database
- Status code 200
- Validate changed fields only

**Delete (DELETE):**
- Verify record deleted
- Status code 204 or 200
- Attempting to get deleted record returns 404

**Q177. CRUD to HTTP Methods:**
- Create → POST
- Read → GET
- Update → PUT/PATCH
- Delete → DELETE

---

### Q181-190. Database Testing

**Q181. Database Testing:**
Testing data integrity, consistency, and performance at DB level

**Q183. Basic SQL:**
```sql
-- SELECT (Read)
SELECT * FROM users WHERE id = 1;

-- INSERT (Create)
INSERT INTO users (name, email) VALUES ('John', 'john@test.com');

-- UPDATE (Update)
UPDATE users SET name = 'John Updated' WHERE id = 1;

-- DELETE (Delete)
DELETE FROM users WHERE id = 1;
```

**Q186. Frontend vs Backend Testing:**
- Frontend: UI, user interactions, display
- Backend: Database, API, business logic, data integrity

---

## 10. Bug Tracking & Defect Management

### Q191-200. Bug Lifecycle & Reporting

**Q192. Bug Life Cycle:**
1. New
2. Assigned
3. Open
4. Fixed
5. Retest
6. Verified/Closed
7. Reopen (if fix fails)

**Q199. Good Bug Report Contains:**
1. Bug ID
2. Title (clear and concise)
3. Steps to Reproduce
4. Expected Result
5. Actual Result
6. Severity & Priority
7. Environment details
8. Screenshots/videos
9. Logs

**Example:**
```
Title: Login fails with valid credentials

Steps:
1. Navigate to www.example.com/login
2. Enter username: testuser@test.com
3. Enter password: Test@123
4. Click Login button

Expected: User logged in successfully
Actual: Error message "Invalid credentials"

Severity: High
Priority: High
Environment: Chrome 90, Windows 10
Screenshot: attached
```

**Q200. Severity vs Priority Examples:**
- High Severity, High Priority: Payment not working
- High Severity, Low Priority: App crashes on IE6
- Low Severity, High Priority: Typo in company name on homepage
- Low Severity, Low Priority: Minor UI alignment issue

---

### Q201-208. JIRA & Metrics

**Q205. Tracking in JIRA:**
- Create bug/issue
- Assign to developer
- Track status changes
- Comment/collaborate
- Link to test cases
- Attach screenshots

**Q208. Defect Metrics:**
- Defect density (defects per module)
- Defect leakage (defects in production)
- Defect removal efficiency
- Defect age
- Reopen rate

---

## 11. Programming Basics

### Q209-220. Python

**Q209. Data Types:**
```python
int: 5
float: 5.5
str: "hello"
bool: True/False
list: [1,2,3]
tuple: (1,2,3) - immutable
dict: {"key": "value"}
```

**Q210. List vs Tuple vs Dictionary:**
- List: Mutable, ordered - `[1,2,3]`
- Tuple: Immutable, ordered - `(1,2,3)`
- Dictionary: Key-value pairs - `{"name": "John"}`

**Q211-212. Loops:**
```python
# For loop
for i in range(5):
    print(i)

# While loop
i = 0
while i < 5:
    print(i)
    i += 1
```

**Q213. If-Else:**
```python
if score >= 90:
    print("A")
elif score >= 80:
    print("B")
else:
    print("C")
```

**Q214. Functions:**
```python
def greet(name):
    return f"Hello, {name}"

result = greet("John")
```

**Q219. Exception Handling:**
```python
try:
    result = 10 / 0
except ZeroDivisionError:
    print("Cannot divide by zero")
finally:
    print("Cleanup")
```

---

### Q221-230. Java/JavaScript

**Q226. OOP Pillars:**
1. **Encapsulation:** Wrapping data and methods
2. **Inheritance:** Child class inherits from parent
3. **Polymorphism:** Same method, different behavior
4. **Abstraction:** Hiding implementation details

---

## 12. Behavioral Questions

### Q231-240. Motivation & Background

**Q231. Tell me about yourself:**
Template: "I'm a [role] with [X years] experience in [domain]. I've worked on [projects], specializing in [skills]. I'm passionate about [interest]. Currently seeking [opportunity]."

**Q232. Why QA?**
- Passion for quality
- Enjoy finding issues
- Analytical mindset
- Prevent user-facing bugs
- Continuous learning

**Q236. Where do you see yourself in 3-5 years?**
- Senior QA Engineer
- QA Lead position
- Automation expert
- Contributing to open-source
- Mentoring juniors

---

### Q241-245. Teamwork & Communication

**Q244. Challenging bug you found:**
Use STAR method:
- **Situation:** Describe the project
- **Task:** What needed to be done
- **Action:** What you did
- **Result:** Outcome and learning

**Q245. Prioritizing tasks with limited time:**
- Identify critical paths
- Risk-based approach
- Focus on high-priority features
- Communicate with stakeholders
- Automate regression tests

---

### Q246-255. Problem Solving

**Q249. Learning new technology quickly:**
- Official documentation
- Online courses (Udemy, Coursera)
- Practice projects
- YouTube tutorials
- Ask colleagues
- Trial and error

**Q254. Managing multiple tasks:**
- Create task list
- Prioritize (urgent vs important)
- Use tools (JIRA, Trello)
- Time management
- Communicate deadlines
- Ask for help when needed

---

## 13. Scenario-Based Questions

### Q256-265. Testing Scenarios

**Q256. How would you test a login page?**
(Already covered in Q27 - Part 1)

**Q257. Test a search functionality?**
(Already covered in Q28 - Part 1)

**Q258. Test e-commerce checkout:**
1. Add products to cart
2. Verify cart calculations
3. Apply coupon codes
4. Enter shipping details
5. Select payment method
6. Process payment
7. Verify order confirmation
8. Check email notification
9. Verify database entry

**Q259. Mobile vs Web testing:**
**Web:**
- Browser compatibility
- Screen resolutions
- Keyboard/mouse input

**Mobile:**
- Device fragmentation
- Touch gestures
- Screen sizes
- Network conditions (3G/4G/5G)
- Battery consumption
- Interruptions (calls, SMS)
- App permissions

**Q263. Bug developer can't reproduce:**
- Provide detailed steps
- Share screenshots/videos
- Share logs
- Environment details
- Test data used
- Network conditions
- Pair debugging session

---

### Q266-270. Load & Performance

**Q266. Load Testing:**
- Testing system under expected load
- Example: 1000 concurrent users
- Measure response time
- Identify bottlenecks

**Q267. Stress Testing:**
- Testing beyond normal capacity
- Find breaking point
- How system fails gracefully

**Q268. Performance Testing:**
- Overall system performance
- Response time
- Throughput
- Resource utilization

**Q269. Performance Testing Tools:**
- JMeter (Apache)
- LoadRunner
- Gatling
- K6

**Q270. Testing for 1000 concurrent users:**
1. Use performance testing tool (JMeter)
2. Create test plan
3. Configure 1000 virtual users
4. Define ramp-up time
5. Execute test
6. Monitor server metrics
7. Analyze results
8. Identify bottlenecks

---

## Study Strategy

### High Priority Topics (Focus Here First)
1. ✅ Testing Fundamentals (STLC, test case design)
2. ✅ Manual Testing (regression, functional)
3. ✅ Selenium Basics (locators, waits, handling elements)
4. ✅ API Testing (REST, Postman, CRUD)
5. ✅ Agile & Scrum (ceremonies, roles)
6. ✅ SDLC concepts
7. ✅ Bug lifecycle and reporting

### Medium Priority
1. Advanced Selenium (frameworks, POM)
2. TestNG annotations
3. Database testing basics
4. Performance testing concepts
5. CI/CD basics

### Quick Review
1. Programming basics (know syntax)
2. AI/ML testing (understand concepts)
3. Behavioral questions (prepare stories)

---

## Interview Tips

### Technical Round
- **Explain your thought process**
- **Ask clarifying questions** before answering
- **Provide examples** from experience
- **Be honest** if you don't know something
- **Discuss tradeoffs** when relevant

### Scenario Questions
- Use **STAR method** (Situation, Task, Action, Result)
- Keep answers **concise** (2-3 minutes)
- Focus on **your contribution**
- Mention **lessons learned**

### Questions to Ask Interviewer
1. What does a typical day look like for QA?
2. What testing tools does the team use?
3. How is the QA team structured?
4. What are the biggest quality challenges?
5. Is there training for new tools?
6. Agile or Waterfall methodology?

---

## Common Interview Mistakes to Avoid

❌ **Don't:**
- Say "I don't know" without trying
- Criticize previous employers
- Claim expertise in everything
- Give yes/no answers
- Interrupt the interviewer
- Look at phone during interview

✅ **Do:**
- Show enthusiasm
- Ask clarifying questions
- Provide specific examples
- Admit knowledge gaps honestly
- Show willingness to learn
- Take notes during interview
- Follow up with thank you email

---

## Final Checklist Before Interview

- [ ] Review job description thoroughly
- [ ] Practice explaining your resume
- [ ] Prepare 3-4 STAR stories
- [ ] Review testing fundamentals
- [ ] Brush up on SQL basics
- [ ] Practice Selenium code samples
- [ ] Understand Agile ceremonies
- [ ] Prepare questions for interviewer
- [ ] Test video/audio setup (for virtual interviews)
- [ ] Have pen and paper ready
- [ ] Join 5 minutes early

---

## Good Luck! 🎯

Remember:
- **Confidence** comes from preparation
- **Honesty** is better than bluffing
- **Learning mindset** is valued
- **Communication** matters as much as knowledge
- You've got this! 💪

