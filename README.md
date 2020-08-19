**Advanced Node and Express - Implementation of Social Authentication**

The basic path this kind of authentication will follow in the app is:

    User clicks a button or link sending them to our route to authenticate using a specific strategy (EG. GitHub)
    Your route calls passport.authenticate('github') which redirects them to GitHub.
    The page the user lands on, on GitHub, allows them to login if they aren't already. It then asks them to approve access to their profile from our app.
    The user is then returned to our app at a specific callback url with their profile if they are approved.
    They are now authenticated and your app should check if it is a returning profile, or save it in your database if it is not.
