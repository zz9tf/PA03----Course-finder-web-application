## PA03 -- Course finder web application
due Friday 4/22 at 11am (during break)

### Team Assignment

#### Motivation

Much of today's software development involves working database-backed responsive interactive web applications. 
Having an experience modifying such a website using Express/Mongoose/EJS will make it easier to understand similar 
frameworks and to jump into a full-stack web development project.  Most web apps these days use a front end framework 
too (e.g. React, ReactNative, Angular), but even these are based on HTML and have a CSS Bootstrap-like styling feature.  
Working with this PA will help you on CPA02 where you need to build on this code base and build something 
interesting demonstrating your mastery of the core full-stack skills and your ability to learn new techniques on your own.


#### Learning Objectives --
  * add fields to a model and adjust the operations to create and find documents
  * be able to use the findOne and find features by reading the documentation
  * be able to add new pages with bootstrap styled CSS

#### Steps

1. Pick a Team Captain and have them set up the repository for you 

    a. Clone the cs103aExpressApp to your computer (if you haven't already)

    b. Pull down all of the branches (git fetch -a)

    c. Checkout the pa03 branch (git checkout pa03)

    d. Add all collaborators to the repository

2. Test out the app and see how it works

    a. Open in VScode, view app.js, and use the Run/startdebugging menu item

    b. sign in, view classes, add and delete them from your schedule

3. Currently, the app passes in a function times2str to convert the times JSON object ot a list of strings.  Modify the code so it doesn't have to do that:

    a. Modify the model to add strTimes field which will contain the list of strings strTimes: [String],

    b. Modify the  '/upsertDB' route so that it sets the course.strTimes field, just as it did for course.num and course.suffix which are the components of course.coursenum

    c. Modify the course.ejs and courselist.ejs, so they use the course.strTimes field

    d. Modify the '/courses' and '/course' routes so they don't pass times2str into res.locals

4. Add a new form on the index.ejs which asks the user for a keyword and searches for all courses that have that keyword in their course.name. Then create the app.post route which will take that keyword and find those courses and send them to courselist.ejs

5. Modify the schedule.ejs so that it uses flexboxes as we did in the api-final branch rather than an ol list, and put in more information into the flexboxes (similar to the course.ejs pages)

6. Create a README.md page where you describe how to download and install the app

7. Create a short movie showing you using the app and especially features 4 and 5 and post a link to the movie on your README.md page 

What to upload to mastery.cs.brandeis.edu

a link to your team github repository

a reflection:

    a. what I learned doing this project (if anything)
  
    b. what was confusing or challenging (if anything)
  
    c. what I did personally on the project (including group coding with others)

Rubric
  * This will be graded on the basis of a good faith effort.... if your code generally works, then you will get full credit, if not, then you will be asked to revise and resubmit.


