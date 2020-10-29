# drupaldo

## Scenario

Tragedy strikes! The client made last minute revisions to the UI of the todo list and the project owner went to Paris (Ontario) on vacation. It's your job to take his work and make it as close to the new mockup as possible.

Your primary objective is to adapt the current functionality to appear as close to the new mockup as possible. The client knows that they are adding functionality with the mockup, and that everything might not be possible under such a short deadline. I know it's 3pm on a Friday and you have a hockey game to watch at 5pm, but please do your best in the time given; we're counting on you!

## Objective

![Objective](docs/todo_list.svg)

Try to make the current todo list look as close to this mockup as possible. Currently the functionality of "mark as complete" works a little how I'd imagine the delete icon in the mockup should work. This is primarily a front end task, testing a developer's ability to manipulate a Drupal backend task to look different from how a backend developer left it. Adapting the backend code to allow the crossed-out (checked) functionality would be a bonus feature that I'm sure the "client" would be impressed by, but should not be the main focus.

## Prerequisites
You will need the following before starting this project:

Git:
  https://git-scm.com/book/en/v2/Getting-Started-Installing-Git
  
Composer:
  https://getcomposer.org/doc/00-intro.md

## Setup

1. Clone this repository to your local computer:
    ```
    $ git clone git@github.com:advisorwebsites/drupaldo.git
    ```
2. Install dependencies with composer:
    ```
    $ cd drupaldo/
    $ composer install
    ```
3. Install the site from config with:

    ```
    $ ./vendor/bin/drush site:install --db-url=sqlite://web/sites/default/files/.ht.sqlite --existing-config
    ```
    
    Please note: non-Mac users will need to ensure [SQLite3](https://www.sqlite.org/index.html) is installed and running.

4. Create a test user, and login:

    ```
    $ ./vendor/bin/drush user:create demo
    $ ./vendor/bin/drush user:password demo "demo"
    ```

5. Host the site:

    ```
    $ cd web
    $ php -S localhost:8080
    ```

6. Login to your drupal website:

    ```
    localhost:8080/user with the demo:demo user
    ```


7. The todo list to work on:

    ```
    localhost:8080/todo
    ```
    
## Demo
![Watch the video](docs/drupaldo-demo.gif)

