try the calculator: https://yusufbolden.github.io/calc-ya-later/ 

## Introduction

This HTML calculator project is going to contain functions for all of the following basic math operators and buttons typically found on simple calculators:

    Numbers (0-9)
    Addition (+)
    Subtraction (-)
    Multiplication (*)
    Division (/)
    Decimal (.)
    Percentage (%)
    Equals (=)
    Clear (AC)
    Plus/Minus (+/-)
    Display window

## Layout

The goal is to design this calculator found on Google images. The colors were matched using [RedKetchup Color Picker](https://redketchup.io/color-picker).

<img width="415" alt="Screen Shot 2022-10-03 at 1 00 07 PM" src="https://user-images.githubusercontent.com/61169982/193636711-5ed0e16f-3f43-46ae-85da-84155d913a57.png">

## Functionality

To make the calculator work, the calculator will need to store the first number that is input into the calculator when a user presses an operator, and also save which operation has been chosen and then operate() on them when the user presses the “=” key. The code will populate the display, so once operate() has been called, the display will update with the ‘solution’ to the operation.

## The Logic

Figuring out how to store all the values and call the operate function with them was the hardest part of the project.

### Some trouble spots:

1. Users should be able to string together several operations and get the
   right answer, with each pair of numbers being evaluated at a time. For example,
   12 + 7 - 5 \* 3 = should yield 42.

2. The calculator should not evaluate more than a single pair of numbers
   at a time. Example: you press a number button (12), followed by an operator
   button (+), a second number button (7), a second operator button (-), a third
   number button (5), a third operator button (\*), a fourth number button (3) and
   finally the equals operator button (=) .

The calculator should then do the following: first, evaluate the first pair of
numbers (12 + 7), second, display the result of that calculation (19), and then,
use that result (19) as the first number in your new calculation, along with the
next operator (19 - 5) and then calculate (14 \* 3) and then produce the result (42)
after the user presses the equals (=) button.

3. The calculator should round answers with long decimals so that they don’t overflow
   the screen.

4. Pressing = before entering all of the numbers or an operator could cause problems!

5. Pressing “clear” should wipe out any existing data.. Make sure the user is really
   starting fresh after pressing “clear”.

6. Users should be unable to type more than one decimal per input. (Ex. 12.3.56.5).
   It is hard to do math on these numbers. Therefore, the decimal button is disabled if
   there’s already one in the display.

## Additional Resources

The [Document](https://developer.mozilla.org/en-US/docs/Web/API/Document) method [querySelector](https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelector) returns the first [Element](https://developer.mozilla.org/en-US/docs/Web/API/Element) within the document that matches the specified selector, or group of selectors. If no matches are found, null is returned.

The [addEventListener](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener) method of the EventTarget interface sets up a function that will be called whenever the specified event is delivered to the target.

The [KeyboardEvent.code](https://developer.mozilla.org/en-US/docs/Web/API/KeyboardEvent/code) property represents a physical key on the keyboard (as opposed to the character generated
by pressing the key). In other words, this property returns a value that isn't altered by
keyboard layout or the state of the modifier keys.

The Document method [getElementById()](https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementById) returns an Element object representing the element whose id property matches the specified string. Since element IDs are required to be unique if specified, they're
a useful way to get access to a specific element quickly.

The [Element.classList()](https://developer.mozilla.org/en-US/docs/Web/API/Element/classList) is a read-only property that returns a live [DOMTokenList()](https://developer.mozilla.org/en-US/docs/Web/API/DOMTokenList) collection of the class attributes of the element. This can then be used to manipulate the class list.

Have fun and CALC-YA-LATER!
