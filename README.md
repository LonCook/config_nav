# Configurable Navigation

![](./screens/DEMO_config_nav.gif)
Proof of concept for slide out drawer interfaces in FileMaker Pro, with the option for a modal drawer.

[DEMO_config_nav.fmp12](DEMO_config_nav.fmp12)

## Navigation Components


### Popover

### Button Bar

### Layout Admin Layout


## Layout Object Visibility
Objects, like sliding drawers and popovers, can get lost on an interface, when not visible. We can do ourselves a favor and make these objects visible in Layout Mode. Underlying objects are not obscured, while remaining readily apparent themselves. The formatting applied here is a transparent cyan.


### Visibility Calculation
For objects you dont want to render at all, but still be able to find in Layout Mode, we turn to the visibilty calculation; also known as "Hide object when".

In this file, the navigation menu is driven by a popover object, which are ordinarily called by a button. Here we are opening the popover object via script. We want the popover, but dont need the button it's attached to. We still need to find the button, when in Layout Mode, so formatting is applied to the object to help it standout in Layout Mode (example: semi-transparent cyan).

<img src="./screens/visibility_calculation.png" width="150">

The visibility calculation is as follows:

    Get ( WindowMode ) ≠ 4

This also works well for leaving developer notes, only visible in Layout Mode.

<img src="./screens/layout_notes.png" width="200">


## Future Development
