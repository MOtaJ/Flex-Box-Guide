# Flex-Box-Guide

## Solution Guide

## First-Example

**Adjust the input field so that it fills up 100% of the space**

#### Solution

***Add display: flex to .form-row***
- This allows the parent container to be adjusted by flex-box
- Allows new ways of sizing elements in the child

***Add flex: 1 to .form-row input***
- Among the children elements, **flex 1** is the baseline for if we want all children elements to be the same width
- flex 1 is also the default value
- we DIDNT give the Name and FavColor elements a flex value, so that's why they are default size
- Because this is the only child playing the flex game, it takes up all of the available space

## Second Example

**Create a three-column layout with the three div's**

#### Solution

***Add display: flex to .column-layout***
- The children elements inside can now be adjusted using flexbox
- The three main div's have now been set up evenly next to eachother now

***Add flex: 1 to .main-column, sidebar-one, and sidebar-two***
- All three main elements are now lined up together evenly
- If we made main-column flex: 2, it would now be twice as big, etc. etc.

**STOP!!** Explain now that sidebar one is going to be in our far left and we don't want to touch our html because with flexbox, now we don't have to.  

***Add order: 1 to .sidebar-one***
- Will now take first priority in far left

***Add order: 2 to main-column***
- Second Priority

***Add order: 3 to sidebar-two***
- Third Priority

## Third Example

**Create a Three-column layout with margins in between**

#### Solution

***Add display: flex to .call-outs container***
- Notice how all three are now lined up properly this is due to a property called align-items, which is set to default stretch;

***Add align-items to .call-outs container***
- Begin with Flex-Start
  - Notice how teh items are now lined up from the top
- Then add Flex-End
  - Notice how items are now lined up from the bottom
- Then add center
  - Notice how items are now lined up from the center
- Then add stretch
  - Notice how items are now stretch to fill the same amount of space
  - this is the default
  
***Add a width of 30% to the .call-outs***
- Each div will have a width of 30%
  - 30 * 3 is 90 so it will use about 90% of space.  You can then distribute the remaining 10% in between each box for margins.
  
***Add justify-content***
- Start with flex-start
  - It will align the content to the left - this is default
- Then use flex-end
  - This will align content to the right
- Then use flex-center
  - This will align content in the center, with no margin
- Then use space-around
  - This aligns content with space on each side
- Then use space-between
  - This will align content on each end with space between each child
  
***Remove width and use flex-basis***
- This is the flexbox way of calling size

## Fourth Example

**Adjust flex-wrap so that the pictures are wrapping and creating new columns**

#### Solution

***Add flex-wrap to container elements***
- Now decrease the size and show them how it's creating new columns 

***Now add flex-nowrap to show default***

## Fifth Example

**Center the text inside of the gray box**

#### Solution

***Add display: flex to parent container***
- This will allow the child element to be allowed to flex

***Add margin: auto to the child element***
- Flex box now can help align margin's inside of the parent container automatically

## Sixth Example

**Align the box using rows AND columns**

#### Solution

***Add display: flex to .equal-heights-container***
- This allows the parent container to flex it's children

***Add flex: 1 to our .first class***
- Remember, 1 is our base value for when we want to evenly distribute space

***Add flex: 1 to our .second class***
- Now we want our A and B to share the rest of the remaining space.
  - To do this we're going to put a flexbox nest inside of a nest
  
***Now, add display: flex to the .second container***
- This is because our class container is now a parent element to our A and B elements

***Add flex: 1 to both A and B elements***
- This will allow them to share the remaining width

***Add flex-direction: column to .second column***
- Flexbox is naturally sharing the horizonal space, this is already by default
  - By changing the flex-direction, we can now adjust vertical space as well
