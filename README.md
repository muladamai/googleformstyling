# googleformstyling
Style Google Forms

based on http://morning.am/tutorials/how-to-style-google-forms/

STEP 1.
Sign up for a Google Docs account if you haven’t already done so.

STEP 2.
Log into your new Google Docs account.

STEP 3.
Click New and choose Form from the drop down menu.

STEP 4.
Create your form using Google’s straight forward tools.

STEP 5.
When you have finished compiling your form, click the link at the bottom of the page titled: ‘You can view the published form here’

Here’s an example of what it should look like:

http://spreadsheets.google.com/viewform?key=pqbhTz7PIHum_4qKEdbUWVg

STEP 6.
Right click anywhere on the page and click View Source to look at the code behind the form.

STEP 7.
Copy all the code between <form> and </form> tags and paste it into the new form page on your web site.
Click here for an example

STEP 8.
Now you’re ready to style your form!

Insert your own stylesheet  between the <head> tags. I’ve prepared a version which takes Morning Copy website as it’s starting point.

Click here for an example

STEP 9.

Now you have a beautifully styled form but it still sends users to an ugly Google confirmation page.

Add a bit of javascript* to redirect the completed page to a confirmation page** of your choosing:

REPLACE:

<form action="YOUR-EMBEDDED-GOOGLE-SPREADSHEET-LINK" method="POST">
WITH:

<script type="text/javascript">var submitted=false;</script>
<iframe name="hidden_iframe" id="hidden_iframe"
style="display:none;" onload="if(submitted)
{window.location='http://YOUR-THANK-YOU-PAGE-URL';}"></iframe>
<form action="YOUR-EMBEDDED-GOOGLE-SPREADSHEET-LINK" method="post"
target="hidden_iframe" onsubmit="submitted=true;">
