# make_help_menu

This is a single R function in a file named make_help_menu.R that you can copy and include into any R package you are contributing to.  
The function was an idea by Theodor Stenevang Klemming in 2017 who also wrote version published here on github.com/stenevang/make_help_menu/


### Result
When the package project is open, you can invoke the function make_help_menu and it will:
* List all .Rd files in the /man/ folder
* Build an R file named like your package that contains roxygen notation with links to the documentation (help) of each of the columns in the package.
* When a user types `?<packagename>` there will be a menu page showing up, with links to the documentation of each function in <packagename>.


### Benefit
In packages with many functions, make_help_menu provides a quick and easy way to create overview of the functions included in the package. It also allows users who are unfamiliar with the package to browse the function names available as a guidance when looking for the right function.


### How to add make_help_menu
1. Warning! make_help_menu.R will write a file in the /R/ folder named exactly like your package. If you already have an R file with source code in the /R/ folder named like the package, you must rename that file first.
2. Copy / Download make_help_menu.R
3. Place make_help_menu.R in the /R/ folder of your package project. There is no need for modifying the R code in make_help_menu.R to make it work with your project. However, you can customize the text strings as you prefer.
4. Open your package project
5. Build/install the package to include make_help_menu.R in the installed version of the package


### How to use make_help_menu
1. Open your package project
2. Invoke the function by typing `<packagename>:::make_help_menu()` Note the tripple-colon - this is because make_help_menu is not an exported function, since users of the installed package are not going to use it.
3. Build/install the package again to include the new <packagename>.R file in the installation.



