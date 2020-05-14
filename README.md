# CustomWebView
## Introduction
CustomWebView is an extended form of web viewer with more customization and flexibility (For MIT AI2 and its distros)

## Features
- More customization options than normal web viewer
- Long Click event
- New window request event
- Load local files and content using Html and Js
- Find words and phrases in webview
- Evaluate Js and get result
- Block network loads to save data and load faster
- Upload files to websites(requires Android 5.0)
- Error occurred event
- Get output from console
- FormResubmission event
- Get content height
- Get SSL Certificate of website
- Get cookies for particular url/website
- Event for permission(s) request
- Grant permission(s) manually
- Print web content

## Designer Properties

<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/4/7/47aaaa83879e73d42ecc93935bfa83819e7ef69a.png">

<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/9/a/9a46ff9628b1695817c56b1f8555c32106a423fd.png">

## Blocks
#### Events
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/c/3/c3dc649571f81de591acd6d91f1cde7e25cd95dc.png">

<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/e/b/ebd3525bba1f84800189545b9af733731d6bab09.png">

<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/d/a/daa7b33c9a784a9ef5da85f19c292b3562c302ea.png">

#### Methods
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/5/e/5eed2dfc182329af169cb3879b6f4b751d38eec3.png">

<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/3/1/31ea76a6dcb53bcb194302a24593d4e3f0a455d1.png">

<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/9/d/9d2ce4eebfe20ac57a27d31a2e37e393e87dd447.png">

#### Properties
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/d/c/dc25b49f065626e300f3b6c7f96817b8ae7ccd53.png">

<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/4/f/4f6dc91f4eca6e74b11dcf5fe4cc73c5a9ffb8dc.png">

<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/b/1/b1d5f11b6e4ef1bad1e2dcf93d01bbe25fb18538.png">

<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/a/0/a090a99c4daf7da535f97728b10924d6f8e349bf.png">

### Documentation
#### Events
>- **AfterJavaScriptEvaluated**
Event raised after evaluating Js with result
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/8/b/8bbd83e08a6fd64f29325ffcf19017dfdc928091.png">
result ~ text

>- **Cookies Removed**
Event raised after 'ClearCokies' method with result
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/a/d/ad2fac53aba7a32bb3b6996bf7b8c7f7d39af0c1.png">
successful ~ boolean

>- **Find Result Received**
Event raised after 'Find' method with int 'activeMatchOrdinal','numberOfMatches' and 'isDoneCounting'
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/e/e/ee11ce248b7c1da84ab1c3aba841a90163d3b640.png">
activeMatchOrdinal ~ int
numberOfMatches ~ int
isDoneCounting ~ boolean

>- **Got Ssl Certificate**
Event raised after getting SSL certificate of current displayed url/website with boolean 'isSecure' and Strings 'issuedBy','issuedTo' and 'validTill'.If 'isSecure' is false and other values are empty then assume that website is not secure
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/5/0/50e8a959b0a8475154314bdadb6b959cf8ab2a7f.png">
isSecure ~ boolean
issuedBy ~ text
issuedTo ~ text
validTill ~ text

>- **Got Print Result**
Event raised after getting previus print's result
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/8/5/857a11afada7f35b29d846db53c0dff86716a808.png">
id ~ text
isCompleted ~ boolean 
isFailed ~ boolean 
isBlocked ~ boolean 

>- **Long Clicked**
Event raised when something is long clicked in webview with item(image,string,empty,etc) and type(item type like 0,1,8,etc)
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/2/6/26238a95392665c5fcb3a0d418f8d846640374e8.png">
item ~ text
type - int

>- **On Console Message**
Event raised after getting console message
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/2/e/2e6cabc5498ec197fc427395a61aec6eaf7beeb9.png">
message ~ text
lineNumber ~ int
sourceID ~ int
level ~ text

>- **On Download Needed**
Event raised when downloading is needed
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/c/d/cdebb9b304e2222e57ee94a659ad04571d1f5a6e.png">
url ~ text
contentDisposition ~ text
mimeType ~ text
size ~ int (long)

>- **On Error Received**
Event raised when any error is received during loading url and returns message,error code and failing url
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/7/1/712b12d48e896960a4cd68ff87ac61953ed49243.png">
message ~ text
errorCode ~ int
url ~ text

>- **On Form Resubmission**
Event raised when resubmission of form is needed
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/4/9/499ddf3d6fc35bf525e8b024231671b7b7977726.png">

>- **On New Window Request**
Event raised when new window is requested by webview with target url ,boolean 'isDialog' and 'isPopup'
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/7/3/73db7f4d362abf3afac5bfd9c04090fe579384bb.png">
url ~ text
isDialog ~ boolean
isPopUp ~ boolean

>- **On Permission Request**
Event raised when a website asks for specific permission(s)
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/0/f/0fec1b4536fd6e6905ac27770cfc677899afb5be.png">
permissionsList ~ list < String >

>- **On Progress Changed**
Event raised when page loading progress has changed
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/5/1/514b37ee05051f5b0996171f7ee47ab21c5b0c89.png">
progress ~ int

>- **Page Loaded**
Event raised when page loading has finished
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/c/8/c833386b8a67f372897b013c5171db586599cbc7.png">

>- **Web View String Change**
Event indicating change in webview string
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/e/6/e684d3d556edc00c2863806a97204f286fc6e149.png">
value ~ text

#### Methods
>- **Can Go Back**
Gets whether this WebView has a back history item
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/5/d/5deb60f0f2c2b86804c96b5db0ba3236bc48e427.png">
**Returns : boolean**

>- **Can Go Back Or Forward**
Gets whether the page can go back or forward the given number of steps
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/7/b/7b0fe125a515d65df34c46d426be704dcaef4456.png">
steps ~ int
**Returns : boolean**

>- **Can Go Forward**
Gets whether this WebView has a forward history item
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/6/a/6a725b765d0449af4e120b6902938c55246647b5.png">
**Returns : boolean**

>- **Cancel Printing**
Cancels current print job. You can request cancellation of a queued, started, blocked, or failed print job
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/d/7/d7c5933df5fc1ec0ecda73e35789e6da40b33874.png">

>- **Clear Cache**
Clears the resource cache
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/6/4/645cea3d953f4e5cc75ece1b8171a65e19aac601.png">

>- **Clear Internal History**
Tells this WebView to clear its internal back/forward list
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/1/8/18bec90c94bbb65ba9703c4914a5a36bf6df3e8b.png">

>- **Clear Location**
Clears all location preferences
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/a/e/aefef37c461d8d38b27a1918c16b0c0b44d500bd.png">

>- **Clear Matches**
Clears the highlighting surrounding text matches
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/1/e/1eddb2b757f546cd774996b1ef2c75991d5b8cf4.png">

>- **Content Height**
Returns content height of HTML content
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/4/8/4818d1a479d81014c9e69bbe08c25b414ea7719f.png">
**Returns : int**

>- **Create WebView**
Arrangement to create webview. Horizontal and Vertical Arrangements are recommended.
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/6/c/6c18ad0c917ce7e36e94f9416525526271c04f16.png">
container ~ arrangement

>- **Evaluate JavaScript**
Asynchronously evaluates JavaScript in the context of the currently displayed page
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/f/8/f867f66a8ee328217145e304b0c8c3d417c82247.png">
script ~ text

>- **Find** 
Finds all instances of find on the page and highlights them, asynchronously. Successive calls to this will cancel any pending searches
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/3/b/3b1a1ddb0ce9db4046273b2e9697b3ac057a9ff6.png">
string ~ text

>- **Find Next**
Highlights and scrolls to the next match if 'forward' is true else scrolls to previous match
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/d/f/df33538bc419788635a1cad19f6a7d1ca7d770fb.png">
forward ~ boolean

>- **Get Cookies**
Get cookies for specific url
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/8/d/8d444e9ffdb8dab7b3df29959cdd15047d99a513.png">
url ~ text

>- **Get Ssl Certificate**
Gets the SSL certificate for the main top-level page and raises 'GotCertificate' event
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/5/f/5fef7cd0d475632278424ef566291b43492ba829.png">

>- **Go Back** 
Goes back in the history of this WebView
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/c/b/cb461dc20cc0b19a7cf9e1d257437df22611df96.png">

>- **Go Back Or Forward**
Goes to the history item that is the number of steps away from the current item. Steps is negative if backward and positive if forward
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/f/5/f5819f5f07fa0dc5bd686718d485ae1c5b72457e.png">
steps ~ int

>- **Go Forward**
Goes forward in the history of this WebView
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/c/1/c1c8d07918553fa79281c8eec0679182230946da.png">

>- **Go To Url**
Loads the given URL
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/b/d/bd5d2ba9fbf1720ee00fef60520888ddcc9019c6.png">
url ~ text

>- **Grant Permission**
Grants permissions to webview.It accepts a list of permissions
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/7/d/7ddad44a0f1facbf999ab54d28202866b3a6977f.png">
permissions ~ list < String >

>- **Load HTML**
Loads the given data into this WebView using a 'data' scheme URL
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/0/5/0557df57665eb92c8c6bd97e02c9d3cd7444e88b.png">
html ~ text

>- **Print Web Content**
Prints the content of webview with color mode(Use 2 for color scheme , 1 for monochrome scheme and 0 for default scheme
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/f/0/f05407805caa8417d111379525233cdc4c5cb18f.png">
colorMode ~ int

>- **Reload**
Reloads the current URL
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/1/b/1be6643cfd756efdfde28f329c665c3d6427b946.png">

>- **Restart Printing**
Restarts current/previous print job. You can request restart of a failed print job
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/b/c/bc039fd059fbe13551700b27b3a819e2fb071e38.png">

>- **Resubmit Form**
Whether to resubmit form or not
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/0/e/0ed070cd64e6aaee28761457a03fd2ea92ae12a6.png">

>- **Stop Loading**
Stops the current load
<img src="https://kodular-community.s3.dualstack.eu-west-1.amazonaws.com/original/3X/c/3/c382e0ff39e983e222d0badd69b134cffd490cc2.png">

### Credits
I would like to say thank you to following people for helping me in making CustomWebView:

<img src="https://community.kodular.io/user_avatar/community.kodular.io/ontstudios/45/55737_2.png">  Mateja Srejić aka OntStudios (<a href="https://community.kodular.io/u/ontstudios/summary">Contact him</a>)</img>
