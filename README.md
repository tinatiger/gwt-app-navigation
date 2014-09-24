GWT_AppNavigation-Project

One of the main features of a GWT application is, that you can write all your code in Java and do not need to care about HTML, CSS and JavaScript. All content can be loaded into the same div-element in one HTML-Standardpage. Sounds perfectly alright, but how do you navigate between different views, if for example you need a loginpage and don´t want the user to have access to your application before entering the right logindata?

Of course there is the possibility to have more than one HTML-Page in GWT as well, but if you want to do it the pure GWT-way, you can use a method to exchange the content on the page from inside your javacode.

In this GWT-Example-Project i used a switch-case statement in a java method to change the content on the page depending on the userstatus. There are three different views for the application. A loginview, a view to choose a database and open it and the main view of the application.

Step-by-Step Instructions:

1. Unzip the project into your eclipse workspace.

2. Import the project as a GWT-Web-Application-Project into eclipse.

3. Run the project with Project -> Run As -> Web Application and open the URL in your favourite browser.

Customize the example application:

1. Customize the HTML-Page

First of all you need a simple HTML-page with three divs in it for a header, a footer and the main content. These three divs will be filled with content from the java method "SetContent()" that will be introduced below. The HTML-page is placed in the war-directory of the standard GWT "Web Application Project". You can use the example-page of the GWT_AppNavigation-Project as it is now, or change it to your needs.

2. Add views to put into the div-elements

These views include all gwt-elements that are needed to build the page. Therefore all java classes can be collected in different packages on the client side of the gwt-application, named for the corresponding views. In the example application they are named com.exampleapp.client.loginview, com.exampleapp.databaseview and com.exampleapp.mainview.

3. Define SetContent-Method to navigate between views

The SetContent()-method is defined in the entry point class of the GWT-application. First you need to create objects of all views and put them into attributes of the main class. Also containers for these views are needed, which will be put into the div elements. On start of the example application the loginview is shown. After the user entered the logindata and clicks the login button, the status changes and the setContent-method is called with the second status to show the second view. The same procedure is done, after the user chooses a database and clicks the open database button. The SetContent-method is called with the third status to show the main view of the application. In the main view there are two buttons for navigation back to the databaseview and the loginview. 


Link to the project page at SourceForge.net:
https://sourceforge.net/projects/gwtappnavigation

Email-Contact: talk@tigertech.de
