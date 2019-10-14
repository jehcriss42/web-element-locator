# Web Element Locator
Best practices and examples of web element locators.

Examples created for study purpose using the available test site:

https://demo.cs-cart.com

 *1) Location Strategies:*
   
    Locators are used to find and match elements on a web page. 
    Find elements by the ID and name locator are indicated because these strategies do not relies on 
    the structure of the page.
    If there is not an ID or name present in the application, XPath or CSS locators can be used. 
    Xpath is used to locate elements by the nodes in an XML document. It can be used to locate an element 
    in absolute terms, or relative to a element, or attributes other than id and name. 
    CSS is used to locate elements by CSS selector syntax based in their id, class or other attributes.  
    
    Some of locators types:
    Element's ID
    Element's Name Attribute 
    XPath statement
    CSS Selector
    Link text
    ...    
    
 *2) Examples*
 
    # Getting all menu elements (returns a list):
    class name: 
    "ty-menu__item-link"
    
    # Getting one specific(electronics) menu item 
    a) CSS Selector:
        ".ty-menu__item-active.ty-menu-item__electronics" 
        or
        "#tygh_main_container .ty-menu-item__electronics"
    
    b) XPath:
        "//li[contains(@class, 'ty-menu-item__electronics')]"
    
    (Following are examples of two fragile XPath locator as the language can change 
    and and also the position)
    
    Based on the the text:
        "//a[@class="ty-menu__item-link"][contains(.,"Electronics")]"
    Based on the position:
        "(//a[@class="ty-menu__item-link"])[3]"    
    
*3) References:

    Location Strategies: www.seleniumhq.org
    Locating Elements: selenium-python.readthedocs.io/locating-elements.html
    Web Element Locator Strategies: testautomationu.applitools.com
    CSS selector: www.w3schools.com/cssref/css_selectors.asp
    XPath: www.w3schools.com/xml/xpath_syntax.asp
