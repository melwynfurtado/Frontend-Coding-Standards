#Frontend-Coding-Standards

##Code Standards
* Variables, ID & Class
  * All JavaScript variables shall be written in either completely lowercase letter or camelCase. The one exception to this are Constructor functions, which are capitalized by tradition. All id and class declarations in CSS shall be written in only lowercase. Neither dashes nor underscores shall be used.
* Layered semantic markup
  * Semantic class/id names and appropriate HTML tags for content
  * No inline CSS & JS unless absolutely necessary
  * Progressive enhancement
* HTML:
  * HTML5 doctype. Safe to use for all browsers.
  * All markup should be delivered as UTF-8, as its the most friendly for internationalization.
  * Use of HTML5 form field validation.
  * Pages should validate. Not a strict requirement. Some layouts can't be achieved without a few errors. 
  * Use most meaningful tags for content
  * Images/bg images with text in them must have alternate textual representation (alt text or text positioned offscreen for screenreaders).
  * Do not use the size attribute on your input fields. The size attribute is relative to the font-size of the text inside the input. Instead use css width.
  * Items in list form should always be housed in a UL, OL, or DL, never a set of DIVs or Ps.
* CSS:
  * Add CSS through external files, minimizing the # of files, if possible. It should always be in the HEAD of the document.
  * Use the LINK tag to include, never the @import.
  * Don't include styles inline in the document, either in a style tag or on the elements. It's harder to track down style rules.
  * Elements that occur only once inside a document should use IDs, otherwise, use classes.
  * Understand [http://www.stuffandnonsense.co.uk/archives/css_specificity_wars.html cascading and selector specificity] so you can write very terse and effective code.
  * Write selectors that are optimized for speed. Where possible, avoid expensive CSS selectors. For example, avoid the * wildcard selector and don't qualify ID selectors (e.g. ''div#myid'') or class selectors (e.g. ''table.results.'') This is especially important with web applications where speed is paramount and there can be thousands or even tens of thousands of DOM elements. More on [https://developer.mozilla.org/en-US/docs/CSS/Writing_Efficient_CSS?redirectlocale=en-US&redirectslug=Writing_Efficient_CSS writing efficient CSS on the MDC].
  * In general, CSS shorthand is preferred because of its terseness, and the ability to later go back and add in values that are already present, such as the case with margin and padding.
  * For new sites, look into YUI Fonts & Reset, this will reduce browser layout differences
  * It is always preferable to name something, be it an ID or a class, by the nature of what it is rather than by what it looks like. For instance, a class name of bigBlueText for a special note on a page is quite meaningless if it has been changed to have a small red text color. Using a more intelligent convention such as noteText is better because when the visual style changes it still makes sense.
  * Use least amount of selectors possible to allow for overriding
  * Specify font sizes in pixels
  * Hide content for screen readers with position:absolute and position offscreen. Display:none hides content from screen readers.
  * Design layouts to stretch according to their contents (good for localization and good for font-resizing)
  * Avoid selectors that are native element names (i.e. don't style on "div" or "p") except when resetting.
  * Specify in comments the scope of generic sounding class names (what does .block mean and where is it applied? one page or multiple pages?)
* JS
  * We primarily develop new features in jQuery, leveraging core JavaScript features for better organization of code and maintenance
  * Name variables and functions logically: For example: ''popUpWindowForAd'' rather than ''myWindow''.
  * var your variables
  * Minimize global variables - the less globals you create, the better. Generally one, for your application namespace, is a good number
    * I would prefer to use global namespace IN and ES. If you have to write standalone module javascript, wrap it within anonymous function. Example: [http://blogs.independent.co.uk/other/fb/swire_latest.js]
  * Organize your code as an [http://kaijaeger.com/articles/the-singleton-design-pattern-in-javascript.html Object Literal/Singleton], in the [http://www.yuiblog.com/blog/2007/06/12/module-pattern/ Module Pattern], or as an [http://mckoss.com/jscript/object.htm Object with constructors].
  * 99% of code should be housed in external javascript files. They should be included at the END of the BODY tag for maximum page performance
  * Don't use document.write()
  * Make JS reusable as best as possible
  * Use JSlint : http://www.jslint.com/
* Patterns for better JavaScript
  * Writing Maintainable Code
  * Single var Pattern
  * Hoisting: A Problem with Scattered vars
  * (Not) Augmenting Built-in Prototypes
  * Avoiding Implied Typecasting
  * Avoiding eval()
  * Number Conversions with parseInt()
  * Opening Brace Location
  * Capitalizing Constructors
  * Writing Comments
  * Avoid void
  * Avoid with Statement
  * Avoid continue Statement
  * Avoid Bitwise Operators if possible

##Performance Standards

* Recommendations
 * Follow Yahoo!'s 34 rules http://developer.yahoo.com/performance/rules.html
 * Follow these best practices: http://developer.yahoo.net/blog/archives/2008/01/the_7_habits_fo.html
 * Sprite images
 * Concat and minify JS & CSS with 
  * YUI Compressor (http://www.julienlecomte.net/blog/2007/08/13/)
  * or Minify (http://code.google.com/p/minify/)
 * Max 3s load time for all pages
 * Use ySlow to see where pages can be improved
