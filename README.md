#{LESS} + .NET + Bootstrap

## Static CSS

    <head>
        <!-- Direct link the standard out-of-the-box bootstrap CSS -->
        <link href="//netdna.bootstrapcdn.com/twitter-bootstrap/2.3.2/css/bootstrap-combined.min.css" rel="stylesheet">
    </head>

## Compiling with LESS.JS

	<head>
    	 <!-- File reference to the bootstrap.less file - note the rel="stylesheet/less"! -->
        <link rel="stylesheet/less" type="text/css" href="styles/bootstrap/bootstrap.less" />

        <!-- The less javascript compiler - this needs to be AFTER your less file reference above! -->
        <script src="Scripts/less-1.3.3.min.js"></script>
	</head>

### Configuring ASP.NET/IIS to server .less file type

Including the follow in your `web.config`:
    
    <configuration>
        <system.webServer>
            <staticContent>
                <mimeMap fileExtension=".less" mimeType="text/css" /> 
            </staticContent>  
        </system.webServer>
    </configuration>

## Precompiling LESS

### Node.js

#### Precomile with `lessc`
- Install [node.js] (http://nodejs.org/)
- Run Powershell as Administrator
- Install the LESS compiler via npm
    - `npm install -g less`
- Compile your stylesheet(s)
    - `lessc bootstrap.less bootstrap.css`

#### Reference the compiled stylesheet in your web app

    <head>
        <!-- Direct link the standard out-of-the-box bootstrap CSS -->
        <link href="bootstrap.css" rel="stylesheet">
    </head>



### Visual Studio
- [Web Essentials 2012] (http://visualstudiogallery.msdn.microsoft.com/07d54d12-7133-4e15-becb-6f451ea3bea6)
- [Web Workbench] (http://www.mindscapehq.com/products/web-workbench)
- [DOTLESS] (http://www.dotlesscss.org/)
- [Chirpy] (http://chirpy.codeplex.com/)
- Build Events





