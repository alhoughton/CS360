# CS360
Mobile Architecture &amp; Programming

## Briefly summarize the requirements and goals of the app you developed. What user needs was this app designed to address?
The requirements of the weight tracking app are to allow users to register a username and associated password so that they can log into the app, they then can set a goal weight and record their daily weights. Users should be able to update and delete specific entries and there should be a button that allows users to provide or deny permission for SMS Notifications. 

The need that is being addressed by this app is for users who wish to track their daily weights while trying to acheive a certain weight goal. This works for people who want to lose weight, gain weight, or who are trying to stay within a certain weight range.

## What screens and features were necessary to support user needs and produce a user-centered UI for the app? How did your UI designs keep users in mind? Why were your designs successful?
There was a total of two needed screens. The first screen allows the user to log in while the second allows them to record their weight. On the log in screen, the user as a place for a username and password, along a button to Log In and another to Register. Once successfully logged in (or registered) the app takes the user to a new screen that has a field that takes a current weight and date from the user, followed by a button that allows the user to add that weight to a defined database table.

The design of the Log In/Register screen was very successful, though I think I could have improved on the second screen. I feel like, in hindsight, there was too much going on there and I could have moved some stuff to a different screen.

## How did you approach the process of coding your app? What techniques or strategies did you use? How could those be applied in the future?
I first started out with designing the UI, working on putting all the UI objects where I thought they looked best. After that, I started coding each step starting with the Registration button, then the Log In button.

## How did you test to ensure your code was functional? Why is this process important and what did it reveal?
I would test the code by putting in sample data to see what would happen. I would, also, monitor Logcat as the code was running to see if any errors presented themselves. When I created the code to add the weight information to the dailyWeights table I created I couldn't get it to work. I was able to view the database and saw that only one table was created (and not the three I wrote code for). After investigating the issue, I realized that because I created the database with one table initially (to test to make sure it worked), it wouldn't add additional tables. I had to rename the database (in the code) for it to create a new one which then created all three tables and my code was working.

## Considering the full app design and development process, from initial planning to finalization, where did you have to innovate to overcome a challenge?
On the first page, I needed to have a log in and registration button. I felt that having a seperate registation page would be an unnecessary extra page, but I needed a place for the user to set their goal weight. I, also, figured a user might want to change their goal weight (perhaps they realized that the goal is too challenging or not challenging enough). So, I decided to put the goal weight on the same page as where all the weights are added and shown. 

To ensure that the users knew to put a weight in, I created a Toast message that reminded them if that field was blank. To keep the goalWeight table to only one row per user, I had to create an IF statement that checked if there was data for that user or not. If there wasn't then I called an INSERT method, otherwise I would call an UPDATE method. Doing so kept the goal weight to a single row and allowed a user to change it.

## In what specific component from your mobile app were you particularly successful in demonstrating your knowledge, skills, and experience?
I was quite pleased with the log in and registration functions. They showed the ability to access data from a database table using SQL, confirm that a username existed in the Users table and confirm that the password inputted matched the password associated to that username in the table. From there, it's not a larger leap to creating a log in page for a website or other application (other than adding security features like a hash function to the password).
