Do you want to use Django-cms on dotcloud but don't know where to start? All you need to do is follow these 12 easy steps.


1. create a place to store your project

    mkdir -p ~/projects

2. go into the projects directory

    cd ~/projects

3. clone git repo from github, requires git client.

    git clone git://github.com/kencochrane/django-cms-dotcloud.git
    
4. Go into the new project directory
    
    cd django-cms-dotcloud

5. creating the virtualenv (using virtualenvwrapper, virtualenv, and pip

    mkvirtualenv --no-site-packages --distribute django-cms-dotcloud

6. installing the dotcloud client  http://docs.dotcloud.com/firststeps/install/ (here is the steps for Linux and Mac OSX)

    sudo pip install -U dotcloud

7. sign up for a dotcloud account https://www.dotcloud.com/accounts/register/ if you haven't already.

8. the first time you use the dotcloud account you will need to add your api key. So type dotcloud and follow the steps. You can find your API key at http://www.dotcloud.com/account/settings

    $ dotcloud

9. create your dotcloud application

    $ dotcloud create mycmsapp

10. push your code into dotcloud

    $ dotcloud push mycmsapp .

11. find out your application url.

    $ dotcloud url kencochrane mycmsapp

12. Open url in your browser and start using djangoCMS on dotcloud.

13. Optional: If you don't like the URL they gave you, you can use your custom domain. assuming your application was ramen.www and your domain was www.example.com you would do the following.

    $ dotcloud alias add ramen.www www.example.com

For more info about dotcloud and django-cms and what you can do with with it. check out their docs
 - http://docs.dotcloud.com/firststeps/platform-overview/
 - https://www.django-cms.org/en/documentation/
