##### Return to [About Me](https://pacman715.github.io/pcabano-portfolio/)

When I grew up, phones were connected to a phone jack with a phone cord, the phone jack was connected to wires in the walls and those wires were connected to a junction box which had a cable that went to a telephone pole.  Television was limited to a handful of channels, but needed an antenna to be positioned correctly and within a certain range of the television station.  Radio was also wireless, but dependent upon the proximity of the radio stations.  These were the most common methods of connectivity and electronic information dissemination.

The introduction of the internet and the growth that has occurred since has changed the world.  Today, people are more connected than ever.  Almost everyone has a cellular phone and a computer or laptop of some sort that is connected to the internet.  Many people have other items such as tablets, gaming consoles, and smart televisions that keep us connected to each other and the world.  The internet of things portion of this class concentrated on how we are connected and utilized a device called a microbit to demonstrate how we can write programs to control a device that can receive or transmit data and then can perform a task with this data.


```java
// Step Counter

// micro:bit template code increases step by 1 each shake
input.onGesture(Gesture.Shake, function () {
    steps += 1
    miles += steps / 2000
    if (steps == 10000) {  // plays a tone when user reaches 10,000 steps
        music.playTone(262, music.beat(BeatFraction.Whole))
    }
})

// if B pressed, miles travelled is displayed
input.onButtonPressed(Button.B, function () {
    basic.showString(" MI:")
    basic.showNumber(miles)
})

let miles = 0
let steps = 0
steps = 0

// prompts user to press B to display miles
basic.showString("Press B for Miles")

// always shows step count
basic.forever(function () {
    basic.showNumber(steps)
})
```
