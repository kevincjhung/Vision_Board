# Vision Board / Mood Board

<b>This was completed as an assignment for the course Web Development II. </b>


* Header
    * There must be a header.  The header must contain a name, and an "Add Image" button.  Mine also contains a settings icon, that's optional.
    
    * The Add Image icon must open a form, with an input available to put in a URL, and buttons to Confirm (or Add) and Cancel
        * This dialog must not be hidden behind other UI elements
        * This dialog must do nothing if the input is empty and the Add button is pressed
        * When an image is added, create a new card and add it to the end of the list of cards
            <!-- https://www.youtube.com/watch?v=P-jKHhr6YxI -->
            add event handler to text area, add event handler to post button

* Main view
    * The main part of the page must contain zero or more cards.
        * It may start empty, but ideally you would random-seed with a few sample images.
        * If you do random-seed, it should be clear in your code how I would comment out that section.
     * Each card is the host for an image, and in normal view the card displays only the image, with no other UI elements
    
    * Cards are displayed in a particular order, and initially they are displayed in the order they are added

* Cards
    * When not in editing mode, a card shows only its image
    * Clicking on a card will toggle it to or from editing mode
        * Also toggling one card to editing mode takes all other cards out of editing mode.
    * When in editing mode, a card shows the image at a smaller size, plus some editing buttons
        * there's a delete button
            * I really should have designed and implemented some system for confirming deletion, maybe you'd like to do a better job than me on this
        * there are two buttons to move the card earlier or later in the order
        * there are two buttons to increase or decrease the size of the card
    * cards must have some type of "size" property, which can be varied (as mentioned above)
        * in my implementation, this size property is in multiples of 30px
            * if varying this slightly allows you to make a nice-looking app, that's fine, but don't stray too far
        * there should be lower and upper bounds on how small or large a card can get (in my case, 60px to 270px)
    
    * all card-edit button functionality must be implemented with delegates (or one delegate), so that there are not hundreds of active event listeners
        * my solution has less than ten event listeners at the PASS level, but the exact number isn't important
        * but if I add ten more pictures, and that adds 50 more listeners, that's not okay

* CSS
    * Your CSS must be at least as nice as mine.  This isn't really a class on CSS, but I know you all passed a class on CSS, and I know that you will be required to do CSS in the future, so...  
        * When making the demo version of this, I spent more time on CSS than on everything else put together.  You may find yourself doing the same.  That's normal.  Some people say CSS isn't as "hard" as JS, and there's some truth to that, but it's not easy either, and it can be a fair bit of work.
    * I have included about 50% of the CSS I used in my solution.  You may use it, or replace it, or whatever you wish.


So, in short, you must be able to

* add images 
* resize images 
* move images 
* delete images 

That will require you to

* select DOM nodes
* create DOM nodes
* modify DOM nodes
* delete DOM nodes