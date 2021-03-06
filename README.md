#CSS3 selectors 
***
##Description and syntax

### Attribute Selectors

CSS3 attribute selectors contains a list of new attribute selectors. These allow greater control when selecting elements in a document based on an attribute’s value or even a small portion of that value.
*

```css 

/* 
	Selects any element that contains the attribute that begins with the value of mugshot 
*/
	img[alt^="mugshot"] { width: 100px; }
/* 
	Selects any element that contains the attribute whose value exactly matches photo 
*/
	img[alt$="photo"] { border: 10px solid red; }
/*
	Selects any element that contains the substring executive 
*/
	img[alt*="executive"] { }

/*
	Selects any element that contains an attribute value that’s a list of hyphen-separated values 
*/
	img[alt|="non"] { opacity: .5;}
```

### CSS3 Structural pseudo-classes

[reference]: http://oreil.ly/r1xb1I

```css
/* 
	C:last-child 
	Matches element C that is the last child in another element
..........................................................................*/
	div p:last-child {
	color: white; 
	background-color: black; 
}
/* 
	C:target
	Matches the C element when activating a fragment link (e.g., #section)
..........................................................................*/
	#section:target {
	background-color: yellow;
}
/* 
	C:enabled 
	Matches the C element when the C element is in an enabled state
..........................................................................*/
 	input[type="age"]: enabled {
 	background-color: green;
 } 
/* 
	C:disabled
	Matches the C element when the C element is in a disabled state
..........................................................................*/
	input[type="password"]:disabled {
	background-color: #999;
}
/* 
	:root
	Matches the root of the document; in HTML4 documents, this is the HTML element
...........................................................................*/
	:root {
	display: block;
}
/* 
	C:nth-child(an+b)
	Matches elements in a document tree that have a certain number of siblings before it; where n is an integer, :nth-child(an+b) would match the element that has an+b-1 siblings before it
...........................................................................*/
	tr:nth-child(2n) {
	background-color: #99ff99;
}
/* 
	C:nth-last-child(an+b)
	Matches elements in a document tree that have a certain number of siblings after it; where n is an integer, :nth-last-child(an+b) would match the element that has an+b-1 siblings before it
............................................................................*/
	tr:nth-last-child(-2n) {
	background-color: #99ff99;
}
/* 
	C:nth-of-type(an+b)
	Matches elements in a document tree that have a certain number of siblings before it; where n is an integer :nth-of-type(an+b) would match the element that has an+b-1 siblings before it
.............................................................................*/
	tr:nth-of-type(2n) {
	float:right;
}
/* 
	C:nth-last-of-type(an+b)
	Matches elements in a document tree that have a certain number of siblings after it; where n is an integer :nth-of-type(an+b) would match the element that has an+b-1 siblings before it
..............................................................................*/
tr:nth-last-of-type(2n) {
	float:right;
}
/* 
	C:first-of-type
	Matches the first child element of the specified element type
...............................................................................*/
	p:first-of-type {
	font-weight: bold;
}
/* 
	C:last-of-type
	Matches the last child element of the specified element type
................................................................................*/
	p:last-of-type {
	background-color: black;
}
/* 
	C:only-child 
	Matches the child element if it is the only child element of its parent
................................................................................*/
	li:only-child {
	font-size: 2em;
}
/* 
	C:only-of-type
	Matches the child element if it is the only child element of its parent
................................................................................*/
	li:only-of-type {
	font-size: 2em;
}
/* 
	C:empty
	Matches any element that has no children
.................................................................................*/
	*:empty {
	background: red; 
	height: 100px;
}
/* 
	C:not(R)
	Matches all elements within the C element, except the R elements
................................................................................*/
 *:not(:hover) {
 opacity: .7;
} 


```

