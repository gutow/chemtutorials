# Server Config info
1. This directory must have the option set to `IncludesNoExec`. With Apache2
   I was having trouble getting this recognized in the `.htaccess` file. It
   worked fine in the vhost config file in the list of options for this 
   directory in the `<Directory>..</Directory>` block.
2. Server or vhost must activate the `includes` mod.
3. Server or vhost must also include the following in its configuration:
``` 
        # Allow server-side includes
        AddType text/html .shtml
        AddOutputFilter INCLUDES .shtml
```
# Links to set or verify
1. Contents of "hosted-by" div in `VSEPR_Header.html`,`AO_Viewer_Header.html`,
 `Hybrid Orbitals Header.html` and `Lewis_Tutorial_Header.html`.
```
    <div id="hosted-by">
        Hosted by <a href="https://uwosh.edu/Chemistry">UW Oshkosh Chemistry</a>
    </div>
```
# Installing on webserver
1. Choose location in webserver directory tree and do a `git pull <URL of 
your modified fork>`.
2. This combination of tutorials should appear at 
   `https:\\your_server_address\path_on_server\Dr_Gs_Tutorials.html`.