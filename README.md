# study_guide_notes

## JavaScript Trivia Questions:

1. Why do you need doctype?
Doctype is an instruction to the browser to inform about the version of the html document and how browser should render it.

2. What is the use of the data-* attribute?
It allows you to store extra information/data in the DOM. 
You can write valid html with embedded private data. 
You can easily access the data attribute by using javascript and hence a lot of libraries like knockout use it.

3. What is createDocumentFragment?
createDocumentFragment is like a mini DOM you can append elements to in order to avoid costly insertions. 
Once you've appended elements to the fragment, you can append the fragment to a node element and the fragment itself will disappear.

4. What does float do?
Float removes the element from the normal flow of the document and pushes the element to the sides of the page with text wrapping around it.

5. Are CSS properties case sensitive?
No

6. What is position static?
The default position value for an html element. Not relative, absolute, fixed, or sticky.

7. Implicit return in JavaScript?
No

8. How can you apply css rules specific to media/screen-size?
Use @media to set rules based on media width, orientation, etc. 
Example:
@media (max-width: 700px) and (orientation: landscape){}

9. What are the 7 falsey values in javascript?
Null, undefined, false, "", -0, +0, NaN.

10. What is a primitive datatype in Javascript?
A primitive datatype is not an object, is immutable, and has no attributes/methods defined directly on it.

11. JavaScript: What's the difference between HTML attribute and DOM property?
*  Attributes are defined by HTML, all definitions inside HTML tag are attributes.
  <div id="test" class="button" custom-attr="1"></div>
  document.getElementById('test').attributes;
  // return: [custom-attr="1", class="button", id="test"]
  
*  The type of attributes is always string. For the DIV above, document.getElementById('test').getAttribute('custom-attr') or $('#test').attr('custom-attr') returns string: "1".

*  Properties belong to DOM, the nature of DOM is an object in JavaScript. We can get and set properties as we do to a normal object in JavaScript and properties can be any types.

*  Non-custom attributes have 1:1 mapping onto properties, like: id, class, title, etc.

*  Non-custom propertiy (attribute) changes when corresponding attribute (property) changes in most cases.

*  Attribute which has a default value doesn't change when corresponding property changes.

*  Best Practice: It is recommended to use property in JavaScript as it's much easier and faster. Especially for boolean type attributes like: "checked", "disabled" and "selected", browser automatically converts them into boolean type properties.
