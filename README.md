# startup HTML and CSS
I'm pair programming on the startup project. Here's the repository: https://github.com/dannflor/startup

### Tailwind and leaf:
We are using tailwind combined with Leaf by Vapor. This project has taught me a lot about HTML, but it has also been a lot about learning tailwind. I much prefer tailwind over bootstrap and regular CSS. We're also using the DaisuUI plugin for many of the UI components. Before this project, I didn't realize how helpful plugins on top of regular HTML and CSS could be. I like not having to touch a single .css file while writing a webpage. It makes it easier when you can see everything in one place which is why I love tailwind. I also consider flex and media components to be much easier in tailwind than regular CSS. Templating with leaf is also super nice. Though I do worry that it will become a challenge later when we need to use react. Vapor doesn't work with react, so later we'll have to start using JavaScript for templating.

### Backend:
Overall this project wasn't too hard, I think the challenge will be when we start writing the backend. We did a bit of backend to use dummy data and set up some of the models we'll need.

### Overall:
This is an ambitious project, but we're making it work. There have been some unique challenges with responsiveness and scaling, but most of it has been manageable. The biggest challenge we had was making a grid that maintained a square aspect ratio. That was probably the single hardest piece to program. This is going to be a big project. We split the work pretty evenly, but it was still a lot of work for each of us.


# startup JavaScript
Most of our JavaScript in this project has been DOM stuff. Aside from that, we had to code the logic that checks whether or not a cell has a building, calling endpoints when a building is built/destroyed, and templating arrays of data into HTML components. One challenge has been working around the order at which you append children to a component. There are ways to prepend children, but they're not all that straightforward, so we've just had to change a couple UI things to work easily.

### Things to remember:
Best way to create an onclick: `element.onclick = () => { //functionality }`.

Use `textContent` instead of `innerText`.

General syntax for creating and appending a child:
```
let div1 = document.getElementById('myDiv');
let div2 = document.createElement('div');
div2.setAttribute('class', 'justify-end justify-items-end flex'); //set some class attributes
div2.textContent = 'Some text to go in the div';
div1.appendChild(div2);
```


## CSS practice:
I'm trying to learn how to do all my styling in CSS and treat HTML as more of a skeleton. It's hard when doing stuff from the ground up, but it makes more sense with practice.

### Flex:
Flex components are pretty straightforward, but in my experience, they're easy to mess up. The basic thing to remember is the `@media screen and (max-width: 600px)` and `flex: 1 20%;` or whatever numbers you need to use for it.

### Things to remember:
@import to pull fonts from other sources.

## JavaScript:
Promises are asynchronous, and the content of the promise (including .then and .finally) will not run until after it resolves. The order after it resolves is content of promise function -> then (-> catch if error) (-> finally if no error).

`filter` maps a value to a function. IE `a.filter(v => v.match(/A|f/i);` matches all strings in an array "a" containing a or i (case insensitive) and places them in a new array.

# Simon CSS:
This assignment was more enjoyable than the HTML project because I felt like I could make it a bit more my own. Where HTML is mostly the structure, it was hard to make the first assignment submission unique, but I made this one a bit more unique to me with CSS and various bootstrap components and custom colors.

# Simon JS:
This ended up being much more complex than I originally anticipated. I had some different ideas to accomplish the game functionality, but I prefer the way the code works that we were provided.

## Important things to remember:
Constructors: prepend attribute declaration with `this.`. If you intend to always use the constructor, there's no need to declare the variables elsewhere. 

`??` to check whether left value is not null, else return right value.

`Audio` class to play audio files.

```
setTimeout(() => {
  resolve(true);
}, milliseconds);
```
simple way to add delay.

`document.querySelectorAll('.id').forEach((el, i) => {...}` syntax to query all elements matching `id`. querySelector() only returns a single element.

# Simon service
Setting up an express service script isn't too hard to set up. But it is difficult to set up in a dev environment because it struggles to use the correct port. I eventually tested some curl commands and realized I had it working even though it wasn't working in the web UI because the web UI was running on port 5500, but the express APIs were only available on port 3000. I just deployed the web page and it worked. So I've still gotta figure out how to make it work with the VS code live server extension.
