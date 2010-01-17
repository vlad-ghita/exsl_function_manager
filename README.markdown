#EXSL Function Manager

##Status
This is currently pre-alpha. I've put it on Github for my own use, not distribution.

##Synopsis

This extension provides a delegate that allows other extensions to register php functions with Symphony's XSLTProcessor object. It also provides a stream to an XSL document that declares these functions using EXSL:function.

##Background

Symphony 2.0.7 added the capability to register PHP functions for use within XSLT transformations, allowing developers to implement their own functions in a similar fashion as the built-in functions (such as substring(), etc). There are both benefits and pitfalls to this capabilty. One general concern is the increased coupling of XSLT that uses these functions to PHP's XSL implementation. Another related concern is the lack of version control; calling any registered php function uses the php: namespace.

Fortunately EXSL allows for the creation of functions in a client coder-defined namespace. This allows for the use of for version control. The EXSL Function Manager allows function authors to define a namespace, and wraps the php function call in an EXSL function that uses that namespace.

## Usage


## Examples


## Caveats