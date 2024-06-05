# vulnerable login remediation

This application had several vulnerabilities identified according to the OWASP Top Ten guidelines. Below are the vulnerabilities and the steps taken to remediate them.

## Vulnerabilities and Remediations

1. **Injection (A1:2017)**
   - **Issue:** User inputs were not sanitized.
   - **Solution:** Implemented input sanitization using a DOM method.

2. **Broken Authentication (A2:2017)**
   - **Issue:** Credentials stored in local storage.
   - **Solution:** Removed local storage usage for storing passwords; authentication logic should be server-side.

3. **Sensitive Data Exposure (A3:2017)**
   - **Issue:** Credentials exposed in local storage.
   - **Solution:** Addressed in the Broken Authentication remediation.

4. **Cross-Site Scripting (XSS) (A7:2017)**
   - **Issue:** Unsanitized user inputs injected into HTML.
   - **Solution:** Input sanitization as per Injection remediation.

5. **Insufficient Logging & Monitoring (A10:2017)**
   - **Issue:** No logging for login attempts.
   - **Solution:** Implemented basic logging for authentication attempts.

For other OWASP Top Ten vulnerabilities, the current application context did not apply, or they require server-side remediations which are not included in this frontend code.

## Git Workflow

- Created a `develop` branch from `main`.
- For each vulnerability, a feature branch was created, changes were made and merged back into `develop`.
- Finally, merged `develop` into `main`.

Refer to the commit history for detailed changes and branch merges.
