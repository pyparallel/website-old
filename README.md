
    pydata.org:8080 - /www/pyparallel/website

    
## Local  Website Setup

Pull a copy of the website from github pyparallel/website.git
```
# Clone to local machine 
$ git clone git@github.com:pyparallel/website.git

```
We use the Hyde engine which uses django template structure for creating pages. 
```
$ conda install hyde
```

Update your local repo
```
$ git pull
```
Start the Hyde Server to view your changes locally.

From the root of the website repo execute from the command line:
```
$ hyde gen
$ hyde serve
```
You can view the changes locally by opening your browser and going to **http://localhost:8080** The files are stored in the deploy directory.

After making changes you will need to update the generated content using: **```hyde gen --regen```** or **```?refresh```** in your browser on the page you are viewing.

There are some examples of advanced scripting in hyde:

https://dayone.zendesk.com/hc/en-us/articles/200265094-Markdown-Guide
http://test.continuum.io/drafts/advanced-hyde

Aee what your document looks like as you are writting it:

http://dillinger.io

Once you have reviewed your changes locally, add and commit via standard git commands.

## Updating PyParallel Live Site

The PyParallel site is currently hosted on the pydata.org box.  You will need ssh access to this machine to push changes live.

After ssh-ing into the pydata box:

```
cd /www/pyparallel/website
git pull
hyde gen
```
This will pull your changes into the production environment and regenerate the site.  There is presently no staging environment, so make sure you've reviewed your work locally!
