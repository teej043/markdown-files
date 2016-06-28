# SIDEL ECOBOOSTER FRONTEND PLAN OUTLINE

This documentation describes the initial plans ahead of actual development to foresee the potential processes needed in order to complete the Sidel EcoBooster project. Most of the subjects and references that will be introduced here are based from the requirements on the specifications provided on this PDF: http://myprojectworld.com/Files/7191-ECO-booster-animation.pdf

## Pre-conditions:

* Add animation framework or javascript plugin to Sidel Assets because currently there are no animation workflow in the Sidel frontend build system to facilitate some of the animations seen in the PDF document.
* There is a chance that degradation on IE9 might occur especially when it comes to some animation as this browser does not support certain CSS features such as keyfranes, transitions and transforms which used to control CSS based animations.
* Based on the pdf, the file size of entire EcoBooster may become large judging from the images and backgrounds used, including the new file assets for animation libraries we will use.
* The EcoBooster is like an interactive presentation, in that sense we may model it to be a simple presentation framework so that it may become reusable in the future.
* A brief study on the chosen new javascript frameworks may be needed.
* We would like to define the terms to designate each entities in the EcoBooster module and make them more flexible than being specific to EcoBooster so we could extend functionality and reuse them with other subject matters other than EcoBooster in the future, see terminologies section below 

## Prerequisites:

* The Herobanner ribbon will be extended to support holding this EcoBooster module.
* The Proof of concepts upon what animation framework we will use that is most efficient for this project.
* The Proof of concepts of the simple presentation framework we will use that is most efficient for this project.
* Learn the API of the frameworks mentioned above.

## Proposed Solutions:

#### Proof of Concepts

POC will be required on our part for us to determine which of the libraries or frameworks will be the best to use in our EcoBooster case, considering the specifications set forth by the PDF documentation. Basically, this ultimately concerns which animation development approach to use. 

#### Potential SVG or GIF Animation libraries
* http://greensock.com/svg-tips
* https://jonobr1.github.io/two.js/
* http://snapsvg.io/
* https://maxwellito.github.io/vivus/
* https://github.com/krasimir/gifffer
* https://jnordberg.github.io/gif.js/
* http://slbkbs.org/jsgif/
* http://rubentd.com/gifplayer/
* https://uncorkedstudios.com/blog/jquery-replacement-for-animated-gif-spritely

#### HTML

Document Object Model markups should conform to Sidel's existing code practices so it will be easier for both frontend and backend developer when implementation phase is reached.

#### Images

Every image assets that will be used in this will be dynamically come from media (user uploaded images), except the animation elements as we will still determine as to what graphic format it needs to be. Whether we will use GIF format which is by far the easiest to implement and can become uploadable media as well, for SVG's case it is quite clean and perform well but it will not be a media asset, it will become static and can be used by adding a certain class name in html element.

#### Terminologies

* Hero Pamphlet : Acts like a presentation, this what the entire module will be called, it pretty much sums up its use case definition.
* Cover : The slide or overlay that opens or closes the presentation. It usually has a CTA button for activating the inner content slides. Also bears some animation to transition between inner content. See http://screencast.com/t/VUoTC2gNSti
* Pages : The top level slides, usually presents the inner content sub slides as clickable content. See   http://screencast.com/t/dfOyRqb0I
* Sub Pages : Top Level slides may lead user to Sub Pages, these can hold detailed information and more elements. http://screencast.com/t/L0KKlYTUsu
* Action Button Element : Pages may have some buttons for navigating the presentation, e.g "Overview", "Back" or "Close" buttons. See http://screencast.com/t/GAWQST9g1h8
* Chart Element : An element that may serve two purpose, show a percentage of appropriate value and to be a clickable element to toggle something inside the Page. See http://screencast.com/t/sXpv5gVmyD
* Animated Element : An element used to perform animation when it becomes visible. We will still determine which graphic format to use the much simple GIF or the more technical and flexible SVG. See http://screencast.com/t/lYgI5QpF