# smooth-scroll-js
Smooth Scroll with mouse JS
The code you provided is a JavaScript implementation of smooth scrolling functionality. It allows for smooth scrolling when the user scrolls using the mouse wheel or trackpad.

Here's a breakdown of how the code works:

1. The `init()` function is called when the window's DOM content is loaded. It initializes the smooth scrolling by creating a new instance of the `SmoothScroll` class.

2. The `SmoothScroll` constructor function takes three parameters: `target`, `speed`, and `smooth`. The `target` parameter represents the element to which the smooth scrolling should be applied. The `speed` parameter determines the scrolling speed, and the `smooth` parameter controls the smoothness of the scrolling.

3. Inside the `SmoothScroll` constructor, the `target` element is determined. If the `target` is set to `document`, it is replaced with a cross-browser compatible scrolling element.

4. Event listeners are added to the `target` element for both the 'mousewheel' and 'DOMMouseScroll' events. The `scrolled` function is called when these events occur.

5. The `scrolled` function is responsible for handling the scroll events. It first prevents the default scrolling behavior. Then, it normalizes the scrolling delta value based on the browser type.

6. The `pos` variable keeps track of the current scroll position of the `target` element.

7. The scroll position is updated based on the scrolling delta and the scrolling speed. The new scroll position is limited to stay within the scrollable range of the `target` element.

8. The `update` function is called to animate the scrolling. It calculates the distance to scroll (`delta`) and gradually updates the `target` element's scrollTop property to move towards the desired scroll position.

9. The `requestFrame` function is a cross-browser compatibility fix for the `requestAnimationFrame` method. It ensures that the `update` function is called at the optimal time for smooth animation.

10. Finally, an event listener is added to the `window` object for the 'DOMContentLoaded' event. When the DOM content is loaded, the `init` function is called to initialize the smooth scrolling functionality.

Overall, this code provides a smooth scrolling experience when the user interacts with the mouse wheel or trackpad.
