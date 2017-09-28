# MongoScrape
lets users leave comments on the latest news using Mongoose and Cheerio



### Team Members:
* Jonathan Ansley


### Links:
 * [GitHub Repository](https://github.com/jonathanansley/MongoScrape)
 * [Heroku](https://murmuring-refuge-76293.herokuapp.com/)


### Overview

create a web app that lets users view and leave comments on the latest news.

But you're not going to actually write any articles; instead, you'll flex your Mongoose and Cheerio muscles to scrape news from another site.



### Before You Begin

10. In order to deploy your project to Heroku,
    you must set up an mLab provision.
    mLab is remote MongoDB database that Heroku supports natively.
    Follow these steps to get it running:

11. Create a Heroku app in your project directory.
https://murmuring-refuge-76293.herokuapp.com/
done

12. Run this command in your Terminal/Bash window:

    * heroku addons:create mongolab
done

    * This command will add the free mLab provision to your project.
done

13. You'll need to find the URI string that connects Mongoose to mLab. Run this command to grab that string:

    * heroku config | grep MONGODB_URI
MONGODB_URI: mongodb://heroku_3zcp9nm4:hm7iedo30v4ool1gl2gpfn4b72@ds149324.mlab.com:49324/heroku_3zcp9nm4
done

    * Notice the value that appears after `MONGODB_URI =>`. This is your URI string. Copy it to a document for safekeeping.
done

14. When you’re ready to connect Mongoose with your remote database, simply paste the URI string as the lone argument of your `mongoose.connect()` function. That’s it!

mongoose.connect('mongodb://heroku_3zcp9nm4:hm7iedo30v4ool1gl2gpfn4b72@ds149324.mlab.com:49324/heroku_3zcp9nm4');
done

15. deployed demo application
http://nyt-mongo-scraper.herokuapp.com/



## Instructions

* Create an app that accomplishes the following:

  1. Whenever a user visits your site, the app should scrape stories from a news outlet of your choice and display them for the user.
  Each scraped article should be saved to your application database.
  At a minimum, the app should scrape and display the following information for each article:

     * Headline - the title of the article

     * Summary - a short summary of the article

     * URL - the url to the original article

     * Feel free to add more content to your database (photos, bylines, and so on).

  2. Users should also be able to leave comments on the articles displayed and revisit them later. The comments should be saved to the database as well and associated with their articles. Users should also be able to delete comments left on articles. All stored comments should be visible to every user.

* Beyond these requirements, be creative and have fun with this!




### Tips

* Go back to Saturday's activities if you need a refresher on how to partner one model with another.

* Whenever you scrape a site for stories, make sure an article isn't already represented in your database before saving it; we don't want duplicates.

* Don't just clear out your database and populate it with scraped articles whenever a user accesses your site.

  * If your app deletes stories every time someone visits, your users won't be able to see any comments except the ones that they post.




### Helpful Links

* [MongoDB Documentation](https://docs.mongodb.com/manual/)
* [Mongoose Documentation](http://mongoosejs.com/docs/api.html)
* [Cheerio Documentation](https://github.com/cheeriojs/cheerio)
