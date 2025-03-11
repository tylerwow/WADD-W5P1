# Week 5 Practical 1: CSS Animation
You will create some simple animated scenes using only CSS and some Font Awesome icons. You will also have the opportunity to add animation to your portfolio site.

## Stage 1: Creating Animated Scenes
In the materials for this practical, you will find some starter code and some videos of the expected output. Run index.html using the Live Preview extension. You will see four simple scenes, which have been created using free Font Awesome icons. Your task is to add animations to each scene.


Do the following before getting started with the exercises:
- Take a look at the HTML in index.html. Each scene is created in a `div` with class `window`. Review the CSS for the window class in styles.css. Notice that the `overflow` property is set to `hidden`. This hides HTML elements positioned outside the containing `window`.
- Inside each `window` div, there is a div with class `background`, which contains Font Awesome icons of trees and clouds. Review the CSS for the `background` class in styles.css. The `width` property is 200%, which means that each `background` div is twice as wide as the `window` that contains it. If you inspect a `background` div in the Chrome Dev Tools, you will see that it extends past the right of the `window` and off the edge of the page.
- (Optional) Review the classes related to the trees and clouds to see how the layout is created. You will not need to make any changes to these elements.


### Exercise 1.1: Make the plane fly
Watch the video of expected output for this exercise. The plane appears to fly because the background is sliding to the left. The plane itself is not moving. If you already have experience with CSS animation, go ahead and create the flying effect. Otherwise, follow the guidance below:
1.	The animation will be attached to the `background` div below the exercise 1.1 heading. Although you could set the `animation` property on the existing `background` class, only two of the four `background` divs on index.html will use the sliding animation. Therefore, we need a new class that will be applied only to those divs that need to be animated. Come up with a new class name for a sliding background and add it to the class list of the appropriate `background` div in index.html. I named my class "slide-left". Your div should now look something like this:
`<div class=”background slide-left”>…`

2.	In styles.css, create a new declaration for your new class but don’t put anything in it just yet.
3.	Next, create a new keyframe animation that will be attached to your new class. Here is an outline:

```
@keyframes your-animation-name {
    from {
            
    }
    to {
      
    }
}
```

The animation only needs a start and an end frame—the browser will fill in the rest.

4.	You haven’t animated anything yet but now is a good time to attach the keyframes animation to your class for easy testing. To do this, set the animation property in the CSS declaration you created in step 2. You will need to use the animation name and a duration. The animation should loop forever. You will probably also want to set the timing of the animation to something other than the default (ease). Refer to the slides for the syntax and options.

5.	Finally, fill in the keyframes `from` and `to` blocks to make the background move. You only need to animate one property—a property that has been set in the `background` class.

### Exercise 1.2: Add some turbulence to the plane animation
Watch the video of expected output for this exercise. As you can probably tell, the final scene is almost the same as exercise 1.1 but now the plane shakes up and down.

1.	Reuse the sliding background animation you created for exercise 1.1 by adding the appropriate class name to the class list of the `background` div under the heading for exercise 1.2.

2.	Come up with a new class name that will be used for the turbulence animation and add this to the list of classes on the plane icon. You’re looking for an `<i>` element with a plane class in its class list.

3.	In styles.css, create a new keyframes block for the turbulence animation. For the best results, you will need more than two frames. I used four frames at irregular intervals.

4.	Attach the new keyframes animation to the new class you created in step 2. Give it a short duration (< 1 second). The animation should loop.

5.	Finally, consider what property you will need to change in each keyframe. The [translate transform](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/translate) is recommended.

### Exercise 1.3: Make the helicopter take off, fly, and land

Watch the video of expected output for this exercise. Less guidance is provided below as you’re hopefully getting the hang of keyframe animations. 

Here are some tips:

- You do not need to create a new class for this animation—you can attach a keyframe animation to the existing `helicopter` class because there is only one helicopter on the page.

- You will need quite a few keyframes for this exercise. I recommend tackling one stage of the animation at a time e.g. add keyframes to move the helicopter from the bottom left of the window to the top left of the window then, once that is working, add another keyframe to move the helicopter to the top right.

- In terms of the properties to animate, look for clues in the existing CSS declaration for the `helicopter` class—there are two properties that will need to be changed each keyframe.

### Exercise 1.4: Create a sunrise to sunset animation

This exercise is challenging! Lots of things are animated using separate keyframe declarations. Watch the video closely and see if you can spot them all. Here is a rough guide to implementing this scene. I suggest you tackle each step in order.

1.	In the video, you will see that the sun and moon are rotating around the centre bottom of the window container. To create this effect, you need to animate the div that *contains* the sun and moon, not the sun and moon themselves.

2.	The background colour of the `background` div changes as the sun and moon rotate. You haven’t seen an example of animating colour yet, but it works the same way as animating other properties—pick a start and end colour and the browser will fill in the rest.

3.	The moon has its own rotation animation to keep it upright as the night progresses. This is where it gets tricky…

4.	The sun has a very subtle colour change as it travels across the sky.

## Stage 2: Animate Your Portfolio

The exercises in the previous stage were intended to help you get familiar with keyframes and animating CSS properties. However, you’re not likely to need to create animated scenes in your real websites. Open your portfolio site and consider how you can add animation. For example, you could:
- create a carousel of images to showcase your projects;
- add more complex animations to navigation links on hover;
- create an animated logo for your site.

Note that the final suggestion is an example of animation for the sake of visual flair rather than to communicate change or provide feedback for the user. Although this type of animation is generally to be avoided, a portfolio site is one category of web site that can actually benefit from a little extra flair to show off your CSS skills.
