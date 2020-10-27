# test-nikola

Public test repo for trying-out [Nikola](https://getnikola.com/).

## my notes on how to make github pages and nikola work together

To make github pages work, first set up a github repository and go to the Settings tab and choose whatever branch (e.g. `main`) for github pages.  Then clone the repository, e.g.:

    $ git clone git@github.com:bueler/test-nikola.git

On the laptop/desktop, install nikola.  Once it is installed, activate the venv:

    $ cd nikola/
    $ source bin/activate
    (nikola) $

Now change to the site directory and initialize the nikola site:

    (nikola) $ cd ../test-nikola
    (nikola) $ nikola init .

It goes through questions ...

You can also add a few posts or whatever.  Local view of the site is by

    (nikola) $ nikola serve --browser

When ready to deploy, edit `conf.py` following these ["Deploying to GitHub" directions](https://getnikola.com/handbook.html#deployment).  The key is for `GITHUB_DEPLOY_BRANCH` to match the branch you set gor github pages at the repo.

Finally you should be able to deploy:

    (nikola) $ nikola github_deploy

Go to the settings tab on the repo to see the web address of the deployed site.

