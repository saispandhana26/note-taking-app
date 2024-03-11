# note-taking-app
Bug-Fixes-in-Note-Taking-App
Scenario:

A team of enthusiastic data scientists embarked on a mission to develop a Note Taking Application using Python, Flask, and HTML. However, their lack of experience in backend development has led to challenges in making the application fully functional. Recognizing your proficiency in backend development, you have been tasked with fixing the broken code and ensuring the application works seamlessly.

Task:

Refactor the existing codebase and ensure the proper functioning of the Note Taking Application. Document all identified bugs during the debugging process. Remember, the task is not about recreating the app from scratch. Your goal is to fix the already existing codebase and make the application work as intended.

More Details:

The application's home route contains a text field and a button. Users can add a note, and all the notes should be displayed as an unordered list below the text field on the same page.

All work is done on visual studio and then first step is to open it And go to the note app folder and open it in studio and do follow steps to fix bugs in it and all this done terminal by using python and flask frame work.

Mandatory steps:

       create a virtual environment in note app folder by running this code.
           python –m venv .env_note .

       activate the virtual environment   by running this code
        .env_note\Scripts\activate  in terminal (cmd) on visual studio.       

       Run the app.py file to check how was web interface once and we run
           this after all bugs fixing also.
Bug 1: Form Submission Issue

Description: Users were unable to submit notes using the form on the home page.

Bug Identification: The form in the HTML template lacked a specified action attribute, causing it to default to an empty action.

Fix Applied: Modified the form tag in the HTML template to include action="/" method="post". Ensured the form properly submits data to the root URL using the POST method.

Result: Users can now successfully submit notes through the form on the home page.
Bug 2: Note Validation and Empty Submission Description: Users were able to submit empty notes, leading to unwanted entries in the notes list.

Bug Identification: The Flask route did not check whether the submitted note was empty before appending it to the notes list.

Fix Applied: Implemented a check in the Flask route using if note: before appending the note to the list. Ensured that only non-empty notes are added to the list.

Result: Empty notes are no longer added to the list, maintaining data integrity. ---------------------------------------------------------------------------------------- Additional Improvements:

Form Button Type Attribute:

Description: The form button lacked a specified type attribute.

Fix Applied: Added type="submit" to the form button in the HTML template.

Result: Ensured proper form submission behavior.
