#Xpand 
Xpand is a tool that let you create with the same HTML different layouts each one of them by a different resolution.

To each resolution you have a different grid. The first grid has 3 columns layout. The second increase the amount of columns to 6, and the next is 12 column grid. 
When more space more columns. So you can distribute your design differently. 

It has modules. One module is the less expression in the grid. This module can expand to place one or more modules. To more expansion more important is the content in that specific grid. 


##How to create a layout? 
You have to set some class name `xpand-[1-3]` to the class attribute in the element that you want to expand, or be used like a grid. When you want to set a row, you have to set the `xpand-row` class to it. 

When you want to set the followings layouts you have to use the followings attributes `data-xpand-m` for the middle size, and the `data-xpand-l` for the large size. Inside that attributes, as a value, you have to set `xpand-[1-6]` and `xpand-[1-12]`.

Example:

```html
<div class="xpand-row xpand-3" data-xpand-m="xpand-row xpand-4" data-xpand-l="xpand-row xpand-7">Some content</div>
```

It means that element is a start row element with full size in the default resolution, a 66% in the middle resolution and a 58% of size in the large resolution.

The following graphics explains how you can set this grids. The r is equivalent to xpand-row and the number is equivalent to the size of expansions. 


###Small Screen
```
 ________
|________| » max module expand
|__|__|__| » min module expand
|__|_____| » module convintations

```

####Snippet

```html
<!-- max module expansion -->
<div class="xpand-row xpand-3"></div>

<!-- min module expansion -->
<div class="xpand-row xpand-1"></div>
<div class="xpand-1"></div>
<div class="xpand-1"></div>

<!-- module convinations -->
<div class="xpand-row xpand-1"></div>
<div class="xpand-2"></div>
```

###Medium Screen
```
 _________________
|_________________| » max module expand
|__|__|__|__|__|__| » min module expand
|__|______________| » module convintations
|_____|___________|
|________|________|

```
####Snippet

```html
<!-- max module expansion -->
<div data-xpand-m="xpand-row xpand-6"></div>

<!-- min module expansion -->
<div data-xpand-m="xpand-row xpand-1"></div>
<div data-xpand-m="xpand-1"></div>
<div data-xpand-m="xpand-1"></div>
<div data-xpand-m="xpand-1"></div>
<div data-xpand-m="xpand-1"></div>
<div data-xpand-m="xpand-1"></div>

<!-- module convinations -->
<div data-xpand-m="xpand-row xpand-1"></div>
<div data-xpand-m="xpand-5"></div>

<div data-xpand-m="xpand-row xpand-2"></div>
<div data-xpand-m="xpand-4"></div>

<div data-xpand-m="xpand-row xpand-3"></div>
<div data-xpand-m="xpand-3"></div>
```

###Large Screen
```
 ___________________________________
|___________________________________| » max module expand
|__|__|__|__|__|__|__|__|__|__|__|__| » min module expand
|_____|_____________________________| » module convintations
|________|__________________________|
|___________|_______________________|
|______________|____________________|
|_________________|_________________|

```

####Snippet

```html
<!-- max module expansion -->
<div data-xpand-l="xpand-row xpand-12"></div>

<!-- min module expansion -->
<div data-xpand-l="xpand-row xpand-1"></div>
<div data-xpand-l="xpand-1"></div>
<div data-xpand-l="xpand-1"></div>
<div data-xpand-l="xpand-1"></div>
<div data-xpand-l="xpand-1"></div>
<div data-xpand-l="xpand-1"></div>
<div data-xpand-l="xpand-1"></div>
<div data-xpand-l="xpand-1"></div>
<div data-xpand-l="xpand-1"></div>
<div data-xpand-l="xpand-1"></div>
<div data-xpand-l="xpand-1"></div>
<div data-xpand-l="xpand-1"></div>

<!-- module convinations -->
<div data-xpand-l="xpand-row xpand-1"></div>
<div data-xpand-l="xpand-11"></div>

<div data-xpand-l="xpand-row xpand-2"></div>
<div data-xpand-l="xpand-10"></div>

<div data-xpand-l="xpand-row xpand-3"></div>
<div data-xpand-l="xpand-9"></div>

<div data-xpand-l="xpand-row xpand-4"></div>
<div data-xpand-l="xpand-8"></div>

<div data-xpand-l="xpand-row xpand-5"></div>
<div data-xpand-l="xpand-7"></div>

<div data-xpand-l="xpand-row xpand-6"></div>
<div data-xpand-l="xpand-6"></div>
```

