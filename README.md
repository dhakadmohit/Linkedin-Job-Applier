# LinkedIn Job Application Automation Script

This script automates the process of applying for jobs on LinkedIn using Selenium WebDriver. It searches for jobs, logs in using provided credentials, and attempts to apply to each job listing found.

## Prerequisites

1. **Python**: Ensure Python is installed on your machine.
2. **Selenium**: Install Selenium using pip.
   ```sh
   pip install selenium
   ```
3. **WebDriver**: Download the appropriate WebDriver for your browser (e.g., ChromeDriver for Chrome) and add it to your system's PATH.

## Setup

1. **Email and Password**: Replace the placeholders for `ACCOUNT_EMAIL` and `ACCOUNT_PASSWORD` with your LinkedIn login credentials.
2. **Phone Number**: Replace the placeholder for `PHONE` with your contact number.

## Usage

1. Save the script to a Python file, for example, `linkedin_job_apply.py`.
2. Open a terminal or command prompt and navigate to the directory where the script is saved.
3. Run the script using Python:
   ```sh
   python linkedin_job_apply.py
   ```

## Script Overview

1. **Initialization**: The script starts by setting up Selenium WebDriver with options to keep the browser open in case of crashes.
2. **Navigation**: It navigates to the LinkedIn job search page.
3. **Login**: It handles the login process using the provided email and password.
4. **Job Listings**: It fetches all job listings on the page.
5. **Application Process**:
   - For each job listing, it tries to apply by clicking the apply button.
   - If additional steps are required (e.g., filling out complex forms), it skips that job.
   - Otherwise, it submits the application.

## Detailed Steps

1. **Reject Cookies**: Clicks the "Reject Cookies" button if present.
2. **Sign In**: Navigates to the sign-in page and logs in.
3. **Captcha Handling**: Waits for the user to manually solve the CAPTCHA.
4. **Job Listings**: Fetches all job listings available on the search page.
5. **Applying for Jobs**:
   - Opens each job listing.
   - Clicks the apply button.
   - Fills in the phone number if the field is empty.
   - Attempts to submit the application.
   - If the application is complex (requires additional forms), it skips to the next job listing.

## Notes

- **CAPTCHA**: The script pauses and waits for the user to manually solve any CAPTCHA challenges.
- **Error Handling**: If the script encounters elements it cannot find (e.g., apply button not present), it skips to the next job listing.
- **Browser Detachment**: The browser remains open if the script crashes, allowing the user to inspect the state.

Happy Job Hunting!
