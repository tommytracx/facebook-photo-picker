Uses the Facebook Javascript Client and XFBML, designed to work in an iframe.

A Facebook application has been created which points at this Google Code repository. The widget can be viewed through Facebook by simply going to:
http://apps.facebook.com/photo-picker/photoPicker.html

It will ask you to authorise the application, the application needs to access your photos in order to work.

You can browse the source at:
http://facebook-photo-picker.googlecode.com/svn/trunk/

# Setting up your own development environment #

The photo picker is just static HTML and javascript. So, all you'll need to get it running on your PC so that you can start improving it is:
  * An HTTP server (I use Apache Tomcat, but that does more than you need)
  * A SVN client to grab the source code from this repository (I use Eclipse and the svn command line)
  * A connection to http://www.facebook.com via the Internet, many companies block it :o(
  * A web browser and your favourite text/javascript editor.

## Steps ##

  1. Checkout the facebook-photo-picker source from [this repository](http://code.google.com/p/facebook-photo-picker/source/checkout).
  1. Start your HTTP server and mount your SVN sandbox at a URL of your choice (e.g. http://localhost/facebook-photo-picker). Check that you can access http://localhost/facebook-photo-picker/photoPicker.html.
  1. Go to http://apps.facebook.com/developer and create a new Facebook application specifically for the purpose of hosting this application in your development environment. For example, you can call it "photo-picker-myname-dev"
    * Make a note of the API\_KEY that you get allocated, you'll need it later.
    * Go to "Edit Settings" and set the canvas URL and the connect URL to your SVN sandbox where you have your pages checked out. I make my PC's server available on the Internet but you may be able to get away without doing this and just setting the URL to http://localhost/facebook-photo-picker. If this doesn't work, get yourself a Dynamic DNS entry pointed to your PC and open up your firewall to accept incoming connections to the relevant host and port.
  1. Update the photoPickerConfig.js file with your own API\_KEY. This should be the only configuration that you need to change within your SVN sandbox.
  1. Visit http://apps.facebook.com/photo-picker-myname-dev/photoPicker.html and you should see the application working.