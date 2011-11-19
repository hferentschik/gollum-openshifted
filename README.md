# Get your own gollom wiki onto OpenShift

This project is all about getting your own [gollum](https://github.com/github/gollum) wiki hosted on
Red Hat's [Openshift](https://openshift.redhat.com/app/). It's quite straight forward. Just sign up
for an OpenShift account and follow these instructions:

    $ git clone git@github.com:hferentschik/gollum-openshifted.git
    $ git remote rm origin
    $ rhc-create-domain -n <your-domain> -l <email> -p <password>
    $ rhc-create-app -a <app> -t rack-1.1 -l <email> -p <password> --nogit
      <git-url>
    $ git remote add openshift <git-url>  
    $ git push -f openshift master
    
* \<your-domain\> - The domain name you want to use for your apps
* \<email\>       - The email you signed up with for OpenShift  
* \<password\>    - Your OpenShift password
* \<git-url\>     - The OpenShift git URL which you receive when creating the app	

See also

* http://www.highlevelbits.com/2011/11/gollum-wiki-reloaded.html
* http://www.highlevelbits.com/2011/11/my-precious-wiki.html

Let me know if you have problems ...

Enjoy,

Hardy