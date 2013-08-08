yo-angular-seed
===============

## First steps with yeoman generator-angular


### Steps

Below is the plan of what this seed/showcase was created for,
every step will be published as a tag
Its not a secret that npm often not works properly on Windows,
so modules will be placed on independent brach too. Mentioned modules are taken from Windows 7 x64 machine. You can use it on yor own responsibility.

@TODO: more verbose desription

#### Step-0
  Initial - directory is empty (except Readme.md)

#### Step-1
  Angular aplication innitalizing
```bash
  $ yo angular yoAngularSeed
  [?] Would you like to include Twitter Bootstrap? (Y/n) Y
  [2K?] Would you like to include Twitter Bootstrap? Yes
  [?] Would you like to use Twitter Bootstrap for Compass (as opposed to vanilla CSS)? (Y/n) Y
  ?] Would you like to use Twitter Bootstrap for Compass (as opposed to vanilla CSS)? Yes
  [?] Would you like to include angular-resource.js? (Y/n) Y
  ?] Would you like to include angular-resource.js? Yes
  [?] Would you like to include angular-cookies.js? (Y/n) N
  [2K[1A?] Would you like to include angular-cookies.js? No
  [?] Would you like to include angular-sanitize.js? (Y/n) N
  [2K   create app/styles/main.scss
  [1A[2K   create[?] Would you like to include angular-sanitize.js? No
   app\index.html
     createI'm all done....
 ```
 then after answering questions about base most-popular dependencies

By default dower_component folder is ignored,

#### Step-2
  Run dev server with grunt. Making changes in generated files
```bash
  $ grunt server
```

#### Step-3
  Create view
```bash
  $ yo angular:view main-toolbar
```


#### Step-4
  Create route
```bash
  $ yo angular:route dashboard
```

#### Step-5
  Create directive
```bash
  $ yo angular:directive awesome-button
```

#### Step-6
  Namespaced modules. p.1 Without nesting modules into directories
  The key is komponent name, it can directive, controller or any other komponent
```bash
  $ yo angular:controller Parent.ChildCtrl
```

#### Step-7
  Namespaced modules. p.2 Create module with namespace directory
  like above but use slash(es) instead of dots
```bash
  $ yo angular:controller Parent/OthrerChildCtrl
```
Take a look at the controller name

#### Step-8
  Build/deploy
  Prepare dev/dest files:
```bash
    $ grunt build
```

  compile ready for production:
```bash
  $ grunt build:dist
```

#### Add-on
{Web|Php}Storm and Idea configuration tip for using yo/grunt/bower and others as external tools:
open IDE settings (Ctrl+Alt+S), then locate external tools (should be in global scope) and click add ("+")
Provide next values in the `Tool settings` section of the configuration dialog (other params are not important),
note that your cann be different:
```ini
;Your path to node executable
Program: C:\Program Files\nodejs\node.exe

; Here specify node binary to run (in our case its yo), in exaple uses globaly installed package
; then specify parameters for binary (in example its angular subgenerator for route), next value is $Prompt$
; $Prompt$ is not limited to one parameter, you can pass any you want separated by spaces
; Case: after controller/service/etc you can provide list of dependency injection
; this is standard makro for Idea-based IDE, you need to specify route name to start task
; tasks like `grunt server` will be assigned static
Parameters: C:\Users\{current user}\AppData\Roaming\npm\node_modules\yo\bin\yo angular:route $Prompt$

; This macro will return current project root directory path
Working directory: $ProjectFileDir$
```

***

<a href="http://www.wtfpl.net/" title="Project licence WTPFL" style="float:right"><img
       src="http://www.wtfpl.net/wp-content/uploads/2012/12/wtfpl-badge-4.png"
       width="80" height="15" alt="WTFPL" /></a>

