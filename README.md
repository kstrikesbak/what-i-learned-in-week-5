# **WHAT I LEARNED IN  WEEK 5** 
___

## `This Might Be A DOMb Idea`
This activity allowed us to get some air time with querySelectors and createElements. I found the activity difficult but I am now much more comfortable using these. 
```javascript
const paragraph = document.querySelector('p');
paragraph.style.color = 'lightBlue'

// document.querySelector('p').style.color = 'lightBlue'

const heading = document.querySelector('h1');
heading.style.fontSize = '10px';

paragraph.innerText = 'Lorem ipsum dolor amet viral meh selfies drinking vinegar, intelligentsia poke flannel twee paleo enamel pin cray. Banjo celiac crucifix, kickstarter la croix air plant jianbing hashtag vinyl hell of man bun selvage schlitz banh mi. Tacos hella raclette quinoa blog, williamsburg adaptogen tbh. Hexagon af stumptown lumbersexual synth gentrify quinoa enamel pin celiac master cleanse. Truffaut typewriter shoreditch, semiotics iceland mixtape taxidermy umami distillery austin hashtag. Food truck synth wayfarers, street art banh mi actually authentic. Bitters tousled tattooed vegan neutra pug hell of fixie chia unicorn letterpress.'

const item13 = document.querySelector('#item-13');

item13.style.opacity = '0.5';

const item3 = document.querySelector('#item-3');

item3.innerText = 'I say, "Hi!';

const image = document.querySelector('img');

image.src = "http://www.tioxic.com/wp-content/uploads/trex_4.jpg"

image.style.height = '300px';

const image2 = document.createElement('img');
image2.src = "https://cdn1.cyclist.co.uk/sites/cyclist/files/styles/article_main_wide_image/public/6/44/climbing_steep_hills_0.jpg?itok=yLwzoV6F";

const div = document.querySelector('div');
div.appendChild(image2);
image2.style.height = '300px';

const newDiv = document.createElement('div');
newDiv.appendChild(image2);
div.appendChild(newDiv);

// const newLi = document.createElement('.item');

const newItem = document.createElement('li');
newItem.class = 'item';
newItem.id = 'item-16';
newItem.innerText = "I won't be fooled again.";
const list = document.querySelector('ul');
list.appendChild(newItem);
```
___

## `Domb and Domber`

This was an activity that frustrated me. I went over this activity again and the concepts made more sense to me. I would like to do more similar activities to build more confidence. 


```javascript
function appendToUl (element) {
    const newLiInUl = document.querySelector('ul');
    newLiInUl.appendChild(element);
}

// const heading = document.createElement('h1');
// heading.innerText('TEST');
// appendToUl(heading);

function appendToDiv (element) {
    const newElementInDiv = document.querySelector('#lorem');
    newElementInDiv.appendChild(element);
}

// const thing = document.createElement('li');
// thing.innerText("TEST");
// appendToDiv(thing);

function takesInTextAndReturnsANewLi (text) {
    const newLi = document.createElement('li');
    newLi.innerText = text;
    return item;
}

// const item = takesInTextAndReturnsANewLi('TESTY');
// appendToDiv(item);

function addUrlToImage (url,image) {
    image.src = url;
}

// const newImage = document.createElement('img');
// const monkeyUrl = "https://previews.123rf.com/images/photoloader/photoloader1806/photoloader180600012/103436449-young-cute-monkey-eating-watermelon-in-forest-.jpg"
// addUrlToImage(monkeyUrl,newImage);

function cloneClass (element1, element2) {
    element2.className = element1.className;
}

// const thing1 = document.querySelector('#thing-1')
// const thing2 = document.querySelector('#thing-2')
// const thingC = document.querySelector('#thing-c')

// cloneClass(thing1,thing2);
// cloneClass(thing1,thingC); 

function makeElementWithId(tagName,id){
    const newElement = document.createElement(tagName);
    newElement.id = id;

    return newElement;
}

function giveColorToElement (color, id) {
    const newElement = document.createElement(id);
    newElement.style.color = color;
}

// giveColorToElement('green', '#heading')

```

## `DOMINATION`

These concepts were difficult to grasp. I had a hard time working on this independently over the weekend. Experimenting with different things allowed me to build more of an understanding but still need to work on this! Sometimes I'd make changes that I wasn't planning on and commented those out so I could refer back to them at a later date.

```javascript
function setsImageWithIdToHaveUrl(id,url) {
    const newImage = document.querySelector(id)
    newImage.src = url; 
}

const newUrl = "https://images.pexels.com/photos/1108099/pexels-photo-1108099.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500"
setsImageWithIdToHaveUrl("#image-1",newUrl);
setsImageWithIdToHaveUrl("#image-2",newUrl);
setsImageWithIdToHaveUrl("#image-3",newUrl);

function putsALineThroughText() {
    const newElement = document.querySelector('#arguments li:first-child');
    newElement.style.textDecoration = 'line-through';
}

putsALineThroughText()

function removeTheLastLi() {
    const newElement = document.querySelector('li:last-child');
    newElement.remove();
    
}

removeTheLastLi()

// works for text only...
// function takesInNodeElementAndAppendsIt(element) {
//     const newUl = document.querySelector('#arguments');
//     const newLi = document.createElement('li');
//     newLi.appendChild(document.createTextNode(element));
//     newUl.appendChild(newLi);
// }

// takesInNodeElementAndAppendsIt('TEST');

// did not work at all
// function takesInNodeElementAndAppendsIt(myImage) {
//     const newUl = document.querySelector('#arguments');
//     const newLi = document.createElement('img');
//     newLi.appendChild(document.createElement(myImage))
//     newUl.appendChild(newLi);
// }
// myImage.setAttribute("src", "https://ak9.picdn.net/shutterstock/videos/32738299/thumb/1.jpg");
// takesInNodeElementAndAppendsIt(myImage);

function takesInNodeElementAndAppendsIt(element){
    const toBeAppended = document.querySelector('ul');
    toBeAppended.appendChild(element);
}


const monkeyImage = document.createElement('img');
monkeyImage.src = 'https://wallpaperplay.com/walls/full/3/4/3/306905.jpg'
takesInNodeElementAndAppendsIt(monkeyImage);




// function takeInImageAndMakesIt30Pixels(img) {
//     const changeHeight = document.createElement(img);
//     changeHeight.style.height = '30px';
// }
// const monkeyURL = "http://cdn01.cdn.justjaredjr.com/wp-content/uploads/headlines/2015/04/monkey-king-clip.jpg"
// takeInImageAndMakesIt30Pixels(monkeyURL);

function takeInImageAndMakesIt30Pixels(image){
    image.style.height = '30px'
}

const resizedImage = document.querySelector('img')
takeInImageAndMakesIt30Pixels(resizedImage);




// function makesElementDisappear (element) {
//     const cloak = document.querySelector(element);
//     cloak.style.visibility = 'invisible';
// }

// makesElementDisappear(h1);

function makesElementDisappear(element){
    const disappearingAct = document.querySelector(element);
    disappearingAct.className = 'invisible'

}
makesElementDisappear('h1');


// function setsTheThingWithThatIdToHaveThatSizeForText (size,id) {
//     const AdjustId = document.querySelector(id);
//     // no idea

// }

function setsTheThingWithThatIdToHaveThatSizeForText(fontSize, id){
    const element = document.querySelector(id)
    element.style.fontSize = fontSize;
}


setsTheThingWithThatIdToHaveThatSizeForText('50px', '#heading')

function addingNewLi(str){
    const addLi = document.createElement('li');
    addLi.innerText = str
    return addLi;
}

const addLi = addingNewLi('TEST');
takesInNodeElementAndAppendsIt(addLi);

function creatingNewHeader(headerSize,someText){
    const newHeader = document.createElement('h' + headerSize);
    newHeader.innerHTML = someText;
    return newHeader;
}
const appendingNewHeader= creatingNewHeader('1', 'I love cheese');
takesInNodeElementAndAppendsIt(appendingNewHeader);
```

## `Ugly Query`

This was a great activity and a chance for play around with DOM manipulation. I like these activities as its like a playground to experiment with changes you make and then seeing the changes directly on the live server. 

```javascript
const newTitle = document.querySelector('h1');
newTitle.style.fontSize = '400px';
newTitle.style.color = 'red';
newTitle.style.background = 'url("https://fsmedia.imgix.net/90/c6/de/0a/9038/4001/893f/16b6aeed38e9/2jpg.jpeg?auto=format%2Ccompress&dpr=2&w=650")'
newTitle.style.backgroundSize = 'cover'

const orderedList = document.querySelector('ol');
orderedList.style.color = 'black';
orderedList.style.fontSize = '500px';
orderedList.style.background = 'url("https://comps.gograph.com/cartoon-tired-ugly-chipmunk_gg75521345.jpg")'

const allBackground = document.querySelector('body')
allBackground.style.background = 'url("https://assets.rebelmouse.io/eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpbWFnZSI6Imh0dHBzOi8vYXNzZXRzLnJibC5tcy8xNDA3NjYwMS85ODB4LnBuZyIsImV4cGlyZXNfYXQiOjE1NzEwNjI2MTB9.IZDj6P4suOXVoF771oEf5SvOSpdr87zBR1YxX7cf5gs/img.png")'
allBackground.style.opacity = 0.8;

const unorderedList = document.querySelector('ul');
unorderedList.style.color = 'white';
unorderedList.style.fontSize = '800px';
unorderedList.style.background = 'url("https://media2.giphy.com/media/KWzzTbkhDvmQU/giphy.gif")';

const newText = document.querySelector('textarea');
newText.style.color = 'green';
newText.style.background= 'url("https://pm1.narvii.com/6207/97ed0e3551fa54a808d697c7522df07e2adffbc3_hq.jpg")'

const firstParagraph = document.querySelector('p');
firstParagraph.style.color = 'blue';
firstParagraph.style.fontSize = '30px';

const secondParagraph = document.querySelector("p:last-child");
secondParagraph.style.color = 'green';
secondParagraph.style.fontSize = '30px';

const thirdParagraph = document.querySelector("p:first-child");
thirdParagraph.style.color = 'red';
thirdParagraph.style.fontSize = '30px';

const list1 = document.querySelector("#list1");
list1.style.color = 'yellow';

const list2 = document.querySelector("#list2");
list2.style.color = 'rebeccapurple';

const list2contents1 = document.querySelector("#list2 #contents:nth-child(1)");
list2contents1.style.fontSize = '50px';
list2contents1.style.fontWeight = '400';
const list2contents2 = document.querySelector("#list2 #contents:nth-child(2)");
list2contents2.style.fontSize = '100px';
const list2contents3 = document.querySelector("#list2 #contents:nth-child(3)");
list2contents3.style.fontSize = '50px';
const list2contents4 = document.querySelector("#list2 #contents:nth-child(4)");
list2contents4.style.fontSize = '100px';
const list2contents5 = document.querySelector("#list2 #contents:nth-child(5)");
list2contents5.style.fontSize = '50px';

const smallHeading1 = document.querySelector("#smallheading1")
smallHeading1.style.fontSize ='50px';
smallHeading1.style.textDecoration = "underline overline";
smallHeading1.style.background= 'red';


const smallHeading2 = document.querySelector("#smallheading2")
smallHeading2.style.fontSize ='50px';
smallHeading2.style.textDecoration = "underline overline";
smallHeading2.style.background= 'red';

const smallHeading3 = document.querySelector("#smallheading3")
smallHeading3.style.fontSize ='50px';
smallHeading3.style.textDecoration = "underline overline";
smallHeading3.style.background= 'red';

const newTextArea = document.querySelector('textarea');
newTextArea.style.background = 'red';
newTextArea.style.height = '500px';

const newButton = document.querySelector('button')
newButton.style.width = '500px';
newButton.style.height = '500px';
newButton.style.background= 'url("https://statics.sportskeeda.com/wp-content/uploads/2015/03/bowden-1426675278.jpg")'



```