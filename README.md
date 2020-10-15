# RES-Project
1) Create a resource source file:

filename: resource.rc that contains the following:

/* standard resource # for HTML */
#define HTML 23
 
/* include all resource from external files */
XSS      HTML    "index.html"
HELP      HTML    "help.html"

2. Compile the source file:

CMD: rc.exe resource.rc

Output: resource.res

3. Create EXE file from .res file, the output from pervious step. resource.res
CMD: GoLink.exe resource.res

4. Render file on IE as follow: res://C:\path\to\resource.exe/XSS
or using iframe as follow: 
<iframe src="res://C:\path\to\resource.exe/XSS"  height="400" width="400"></iframe>
