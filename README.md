## Flask Application Design for AI Quest Registration Website

**HTML Files**

- `index.html`: This is the homepage of the website, serving as the starting point for visitors. It should include a header displaying the workshop name and organizers, a brief description of AI Quest, and a registration form for participants.
- `registration_confirmation.html`: This page will be displayed after a successful registration, providing a confirmation message with necessary details (e.g., registration ID, workshop date and time, any additional information). It should also include a link to download a virtual event pass (if applicable).

**Routes**

- `/`: This route handles requests for the homepage, serving the `index.html` file.
- `/register`: This route handles the registration process. When a user submits the registration form on the homepage, a POST request is sent to this route. This route should validate the submitted data, store the registration details in a database or a spreadsheet, and redirect the user to the `registration_confirmation.html` page.
- `/download_pass`: This route serves the virtual event pass (if applicable) for registered participants. It should require proper authentication (e.g., registration ID and a secret code) to ensure only registered individuals can access the pass.

**Additional Considerations**

- For the registration form, consider using Flask-WTF, a popular Flask extension that simplifies form validation and processing.
- Implement appropriate security measures to protect user data, such as encrypting sensitive information and preventing unauthorized access to registration records.
- Depending on your requirements, you may want to implement email functionality to send confirmation emails to registered participants or provide updates about the workshop.