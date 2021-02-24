# interview-task
## Welcome
If you have been asked to run through the tasks in this repo, welcome. This is just a relatively high level developer check to see how you get on following a list of setup instructions, using git for source control, and REST API/Vue.js frontend - it shouldn't be too scary!

In this repo we have a set of instructions for you to follow, some for setup, and then some general ones where you have free rein to show us what you can do.
You can clone the repo, follow the setup instructions, and then once you have run through the tasks below, commit your code in your own public github repo - that way we can check out what you've worked on. Pass the url of your public repo back to your contact at AVCRM.

In preparation to completing the tasks in this repo, you will need to get a local install of Laravel running, below are some instructions if you don’t already have something like this.

### You should have...
* A fresh Laravel application installed, and accessible in your browser
* If you've got this, run through the real Tasks below!

### if you don't have Laravel running on your machine yet, read this...
* For a really simple setup, we recommend using Laravel Sail
* See here for a quickstart guide https://laravel.com/docs/8.x/installation#your-first-laravel-project
  * This enables you to run a completely containerised install on your machine within Docker containers, it's super quick to set up, and you don't even need to have php installed on your machine!


## Tasks
1. Setup
    1. Paste the __welcome.blade.php__ file provided in this repo over the welcome.blade.php file in the fresh laravel install (located in /resources/views/)
    2. Create a new directory /public/js and paste in the vue.js file provided in this repo
    3. You should now be able to browse to http://localhost (or wherever you are hosting it, if you didn't use Laravel Sail above), and see a Hello World message.
2. Laravel
    1. Create a new migration (located in /database/migrations/) to generate a table called __tasks__, with the following columns:
        * name (string)
        * description (longText)
        * complete (boolean)
        * (In the migration, you should also populate a couple of example tasks in the table)
    2. Create a __Task.php__ model in /App/Models that uses the __tasks__ table
    3. Create REST api endpoints for the Task model in /routes/api.php (No need for authentication!)
    4. Create a __TaskController.php__ file in /app/Http/Controllers with the methods for CRUD operations that map from the API endpoints that you created
3. Vue
    1. From within the javascript file, in the vue app, on load, call the api to get a list of available tasks (You might want to use [axios](https://github.com/axios/axios), here is a [CDN](https://cdnjs.com/libraries/axios) you could use)
    2. Create a `<table></table>` which loops through the tasks and displays each in it's own row
    3. For any bonus points, add __name__ and __description__ inputs below the table, which when submitted, calls the API, and creates a new task


Thanks very much for the time you have spent on this.

If you have issues with these instructions, please let us know! Also, if you don't manage to complete all the tasks, please still send us a link to your repository so that we can check out how you have got on with the coding.
