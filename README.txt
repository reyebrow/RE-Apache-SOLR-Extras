This is a pretty straightforward module.

However when testing you may want to delete a core that you created. It's relatively simple to do once you know the path to your solr cores.

1. Remove the actual core files: sudo rm -rf /usr/share/solr/cores/<corename>
2. Remove the core declaration line from /usr/share/solr/solr.xml:   <core name="colin" instanceDir="/usr/share/solr/cores/<corename>/"/>
3. Restart Tomcat service: sudo /etc/init.d/tomcat6 restart
4. Restart Apache (just to be sure): sudo apache2ctl -k graceful

And that should remove all traces of core from your SOLR instance.