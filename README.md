# Docksal powered Drupal 7 Installation

This is a sample vanilla Drupal 7 installation pre-configured for use with Docksal.  

Features:

- Vanilla Drupal 7
- `fin init` example

## Setup instructions

### Step 1: Install Docksal

**This is a one time setup - skip this if you already have a working Docksal environment.**  

Follow [Docksal installation instructions](https://docs.docksal.io/getting-started/setup/)
   
### Step 2: Project setup

1. Clone this repo into your Projects directory

    ```
    git clone https://github.com/docksal/boilerplate-drupal7.git drupal7 && cd drupal7
    ```

2. Initialize the site

    This will initialize local settings and install the site via drush

    ```
    fin init
    ```

3. Point your browser to

    ```
    http://drupal7.docksal.site
    ```


## More automation with 'fin init'

Site provisioning can be automated using `fin init`, which calls the shell script in [.docksal/commands/init](.docksal/commands/init).  
This script is meant to be modified per project.

Some common tasks that can be handled in the init script:

- initialize local settings files for Docker Compose, Drupal, Behat, etc.
- import DB or perform a site install
- compile Sass
- run DB updates, revert features, clear caches, etc.
- enable/disable modules, update variables values
- run Behat tests
